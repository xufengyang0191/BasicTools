# Git 简记
本部分是结合 [计算机缺失一课——git](https://missing-semester-cn.github.io/2020/version-control/) 和  [上交 IPADS 新人培训——git](https://www.bilibili.com/video/BV1YR4y1E7LX/?spm_id_from=333.999.0.0) 这两个优秀教程记录的便笺

## Git data model

Git 拥有一个经过精心设计的模型，这使其能够支持版本控制所需的所有特性，例如维护历史记录、支持分支和促进协作。

### Snapshots

`Git` 将顶级目录中的文件和文件夹作为集合，并通过一系列 `Snapshots` 来管理其历史记录。

`Snapshots` 是被追踪的最顶层是的树。文件是一组二进制字节的集合，被称为 `Blob` 对象。目录被称为 `tree` 对象。

```
// 文件就是一组字节
type blob = array<byte>

// 一个包含文件和目录的目录
type tree = map<string, tree | blob>
```

### Modeling history: relating snapshots

- Linear modeling history：一组按照时间顺序线性排列的 Snapshots
- Directed acyclic graph：git 中所使用的模型。

下面是一个 `ASCII` 码构成的简图，其中的 `o` 表示一次 `commit`（`Snapshots`）

```

o <-- o <-- o <-- o <---- o
            ^            /
             \          v
              --- o <-- o

// 每个提交都包含一个父辈，元数据和顶层树
type commit = struct {
    parent: array<commit>
    author: string
    message: string
    snapshot: tree
}
```

### Objects, references and content-addressing

Git 中的 object 可以是 `blob`、`tree` 或 `commit`：

```
type object = blob | tree | commit
```

`Git` 在储存数据时，所有的对象都会基于它们的 SHA-1 哈希进行寻址。

```
objects = map<string, object>

def store(object):
    id = sha1(object)
    objects[id] = object

def load(id):
    return objects[id]
```

`Blobs`、`tree` 和 `commit` 都一样，它们都是 `object`。当它们引用其他对象时，它们并没有真正的在硬盘上保存这些对象，而是仅仅保存了它们的哈希值作为引用。针对哈希，`Git` 的解决方法是给这些哈希值赋予人类可读的名字，也就是引用（references）。

```
references = map<string, string>

def update_reference(name, id):
    references[name] = id

def read_reference(name):
    return references[name]

def load_reference(name_or_id):
    if name_or_id in references:
        return load(references[name_or_id])
    else:
        return load(name_or_id)
```

### Repositories

Git 仓库的定义：`object` 和 `reference`

## Staging area

## Debugging

在 [上交 IPADS 新人培训——git](https://www.bilibili.com/video/BV1YR4y1E7LX/?spm_id_from=333.999.0.0) 中多种 rebase 的情况。当前分支 rebase 到另外一个 分支上。