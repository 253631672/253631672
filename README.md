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

## 许可

MIT。可自由使用、修改和商用，保留版权与许可声明即可。
