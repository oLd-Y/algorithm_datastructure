# algorithm_datastructure
数据结构和算法

dataview 元数据
```
- `file.name`: 该文件标题(字符串)。
- `file.folder`: 该文件所在的文件夹的路径(字符串)。
- `file.path`: 该文件的完整路径(字符串)。
- `file.link`: 该文件的一个链接(链接)。
- `file.size`: 该文件的大小(bytes)(数字)
- `file.ctime`: 该文件的创建日期(日期和时间)。
- `file.cday`: 该文件的创建日期(仅日期)。
- `file.mtime`: 该文件最后编辑日期(日期和时间)。
- `file.mday`: 该文件最后编辑日期(仅日期)。
- `file.tags`: 笔记中所有标签组成的数组。子标签按每个级别进行细分，所以`#Tag/1/A`将会在数组中储存为`[#Tag, #Tag/1, #Tag/1/A]`。
- `file.etags`: 笔记中所有显式标签组成的数组；不同于`file.tags`，不包含子标签。
- `file.outlinks`: 该文件所有外链(outgoing link)组成的数组。
- `file.aliases`: 笔记中所有别名组成的数组。
```
dataview基本用法
```text
TABLE|LIST|TASK <field> [AS "Column Name"], <field>, ..., <field> 
FROM <source> // like `#tag` or `"folder"`)
WHERE <expression> // like 'field = value'
SORT <expression> [ASC/DESC] // like 'field ASC'
... other data commands
```

dataview排除某个文件夹
```text
list 
from -"template" // 或者 where !contains(file.path,“文件夹”) 或者 !"template"

```