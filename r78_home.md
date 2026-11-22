# HR科技

![四个单文件工具](https://img.shields.io/badge/工作台-4个-E8792E) ![在线预览](https://img.shields.io/badge/在线预览-GitHub%20Pages-4C8C4A) ![License](https://img.shields.io/badge/license-MIT-8A6A3B) ![离线](https://img.shields.io/badge/数据-只存本机-2B2B2B)

做能离线跑的单文件小工具。不依赖框架、不联网，数据只留在自己的浏览器里。

四个工作台都是原生 HTML / CSS / JavaScript，没有 CDN、没有构建步骤，下载一个文件双击就能用。

## 四个工作台

| 项目 | 解决什么 | 体积 |
|---|---|---|
| [生活投资工作台](https://github.com/253631672/life-invest-workbench) | 资产分配、持仓条件单、账本、待办和打卡放一屏 | 44KB |
| [深度读书工作台](https://github.com/253631672/deep-reading-workbench) | 一本书十章，双角色对话精读加 1/3/7/15 天间隔回顾 | 44KB |
| [饮食配餐工作台](https://github.com/253631672/diet-planner-workbench) | 训练日 2400、休息日 2000 两档热量，641 条食物库 | 112KB |
| [健身工作台](https://github.com/253631672/fitness-workbench) | 三分化推拉腿队列顺延，容量、围度、PR 自动汇总 | 40KB |

### 直接在线打开

- [生活投资工作台](https://253631672.github.io/life-invest-workbench/)
- [深度读书工作台](https://253631672.github.io/deep-reading-workbench/)
- [饮食配餐工作台](https://253631672.github.io/diet-planner-workbench/)
- [健身工作台](https://253631672.github.io/fitness-workbench/)

不用下载，点开就是完整程序，数据存在你自己的浏览器里。想离线用，去对应仓库下载那个 HTML 文件。

## 单文件命令行小工具

工作台是给自己天天用的，下面这五个是给文件干活的。

| 工具 | 做什么 | 依赖 |
|---|---|---|
| [batchrename](https://github.com/253631672/batchrename) | 批量重命名：前缀后缀、序号补零、查找替换、去空格、日期前缀，默认只预览，加 `--apply` 才真改，改完留一封撤销记录 | Python 标准库，零依赖 |
| [imgcomp](https://github.com/253631672/imgcomp) | 图片批量压缩：先按最长边缩放，再在质量区间里二分，找刚好不超目标体积的那一档，300张43秒压到1/5 | 只要 Pillow |
| [csvfix](https://github.com/253631672/csvfix) | CSV乱码修复：批量把 GBK/UTF-8 转成 Excel 友好编码，多份表合并去重，默认只预览，带撤销记录 | Python 标准库，零依赖 |
| [img2pdf](https://github.com/253631672/img2pdf) | 图片批量转 PDF：票据、扫描件、截图按顺序合成一份，JPEG 原样嵌入不压画质，手机竖拍自动转正 | Python 标准库，零依赖 |
| [md2docx](https://github.com/253631672/md2docx) | Markdown 转 Word：笔记、周报、README 一条命令出 .docx，标题带大纲、表格代码块都保留，不装 Office 不上传 | Python 标准库，零依赖 |

都是一条命令跑完，Mac 和 Windows 通用，下载一个 .py 就能用。batchrename、imgcomp、csvfix 的源码打包在 [marco-tools](https://github.com/253631672/marco-tools)。

不想自己装环境的，成品包已经上架：

- [小工具全家桶 ¥9.9](https://mbd.pub/o/bread/YZaWmJxqbQ==)：batchrename + imgcomp 一次拿走，省一半
- [CSV乱码修复 ¥3.9](https://mbd.pub/o/bread/YZaWmJxraA==)：Excel 打开表格不再乱码，多份表合一还带去重
- [图片批量转 PDF ¥3.9](https://mbd.pub/o/bread/YZaWmJxsZA==)：票据照片合成一份，不上传、不重压
- [Markdown 转 Word ¥3.9](https://mbd.pub/o/bread/YZaWmJxtZg==)：笔记周报一键变 .docx，不装 Office

- [面包多 · 办公工具箱](https://mbd.pub/o/marco)：PPT/Excel/Word 模板合集，加这几个工具的单文件打包版
- [爱发电](https://afdian.com/a/Marco666)：后续新工具优先放这里

## 共同的做法

- **单文件**：HTML、CSS、JS、图标全部内联，没有外部资源
- **零依赖**：不用框架、不用 CDN，断网、内网都能打开
- **数据本机**：localStorage 存一份 JSON，导出走 Blob 下载，导入走 FileReader
- **移动优先**：最大宽度 560px，底部标签栏，手机上单手操作
- **图表手绘**：环形图用 conic-gradient，柱状图用 flex 高度，进度环用 SVG

## 怎么用

1. 进对应仓库，点绿色 Code 按钮下载 zip，或者直接下载那个 `.html` 文件
2. 电脑上双击，用浏览器打开；手机上把文件传过去，用浏览器打开
3. 首次打开是随机演示数据，看明白后逐条删掉，换成自己的
4. 数据存在浏览器里，换设备前记得在「我的」页导出 JSON

## 关于

不是产品团队做的，这四个工具是从具体麻烦里长出来的：钱分散在几个账户要算比例，书读完就忘，减脂期每天算热量，训练被加班打断后计划全乱。

与其在每个 App 里重复填一遍，不如把记录收回到自己能控制的地方。

代码不复杂，难的是把「我实际会怎么用」想清楚，比如训练队列必须能顺延，比如早餐不该推荐盖浇饭。

## 技术栈

`HTML5` `CSS3` `JavaScript` `localStorage` `SVG` `conic-gradient`

如果这些工具帮你省了点时间，给任意一个仓库点个 Star 就是最好的支持。

## 支持与订阅

如果这些工具帮你省了点时间，可以在爱发电支持我。后续更新、新工具和模板会优先放在那里：

https://afdian.com/a/Marco666

也可以给任意一个仓库点个 Star，都是实在的支持。

## 许可

MIT。可自由使用、修改和商用，保留版权与许可声明即可。
