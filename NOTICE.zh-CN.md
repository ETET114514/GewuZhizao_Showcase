# 展示材料与第三方素材说明

[English](NOTICE.md) | **中文**

## 2026-11-10 · 资料交付、原生CAD尺寸与地理日光

源码 [0de6906](https://github.com/ETET114514/GewuZhizaoNew/commit/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458) · 范围与验证: [资料交付、原生CAD尺寸与地理日光](docs/updates-2026-11-10-delivery-sun.zh-CN.md)

本批交付四类重算清单（房间面积、家具尺寸/房间归属、门窗洞口及柱梁构件）、搜索/待校核筛选、筛选CSV及离线HTML/JSON，并与图纸组成同快照ZIP。图纸集新增可选项目封面/目录，直线DXF尺寸可选原生DIMENSION、单位数值占位符及图形块。地理日光按经纬度、当地日期时间、明确UTC时差和图上北向计算，支持24整点、CSV/JSON及预览/应用/取消/历史，地平线下关闭直射。

新增四张PNG为隔离合成工程的实际验收截图，两种语言共用。源码路径：wall-recognition/output/project-schedules/desktop.png、p27-drawing-cover/render-1.png、native-dimensions/desktop.png及solar-position/desktop.png。没有复制客户图纸、完整源码、项目/交换包、贴图或模型素材，原有许可保持。太阳位置公式来源：https://gml.noaa.gov/grad/solcalc/solareqns.PDF 。

当前仍为参考交付：导出CAD尺寸不与墙体约束关联，弧长/端点不等的净长口径保留静态；清单不是制造采购BOM或正式签审。NOAA分数年公式计算近似几何方向，不含折射/天气/时区检索或规范日照时数/照度分析；环境光/HDRI/室内灯另行控制。不据此宣布云协作或DWG等完整目标完成。

源码阶段最终证据：**692项全量Node、75项相关Python**，以及实际Edge流程、390px与原生DXF/ZIP校验及共同修订/太阳位置CSV和JSON独立读回。更早各阶段数字有重叠，不相加；未跑全量Python。Showcase发布只检查文档、相对链接、双语导航与素材来源，不重新运行应用测试集。

## 2026-11-07 · 本机渲染与模型/平面交付

源码 [f913696](https://github.com/ETET114514/GewuZhizaoNew/commit/f913696701fd4c8e94aaea153ea14f6d65bb86b1). [素材与验证](docs/updates-2026-11-07-render-exchange.zh-CN.md)

新增三张PNG仅来自独立合成验收工程；两种语言共用。来源为New中的`output/p20-model-export/plan-paper-{desktop,mobile}.png`及`output/render-studio/full-render.png`。不携带用户户型、源码、模型/贴图/HDR或工程/导出包，不改变既有素材许可。

## 2026-10-31 · P26与P13整项收尾

源码 [77736ba](https://github.com/ETET114514/GewuZhizaoNew/commit/77736bac6b0e83db23a9c269ad21c66d09f9c1d9); [范围与证据](docs/updates-2026-10-31-closeout.zh-CN.md). 本轮新增五张PNG为程序生成空房间中的真实验收画面，包含P13厚度/标高与P26成片/只读分享。仅复制概要和截图；测试音调、MP4、项目ZIP、全景包和源码仍仅在New中。

## 2026-10-31 · 全景验收素材

源码 [b9ee167](https://github.com/ETET114514/GewuZhizaoNew/commit/b9ee167b494268e74a54c2e242c904004dbced65); [范围与证据](docs/updates-2026-10-31-panorama.zh-CN.md). 新增四张PNG来自本机生成的空房间验收场景；两种语言共用图片。仅复制截图与概要，没有用户图纸、源码、全景/工程包、贴图或模型素材。

## 2026-10-30 · 设计功能材料

源码[0f28b3e](https://github.com/ETET114514/GewuZhizaoNew/commit/0f28b3e043333f733bcf8c89ca6fc11f0b6eb1cf)；[范围与验证](docs/updates-2026-10-30-design.zh-CN.md)。新增P15/P26/P27/P28图片均为隔离验收场景的实际运行截图，两种语言共用PNG并分别翻译说明。不镜像源码、用户工程、CAD文件、模型/贴图或录像包；源码侧测试录像单独记录，合成场景不证明独立真实识别精度。

## 2026-10-30 本轮材料

对应New [d9338b5](https://github.com/ETET114514/GewuZhizaoNew/commit/d9338b5dd8194e8acb36768fa068e6626959531e)。[范围与验证](docs/updates-2026-10-30.zh-CN.md)。P21 CAD/双线/门窗/住宅骨架、P31 OCR、P17 glTF及P30路线图片为隔离验收场景的实际运行截图；中英文共用图片并分别翻译说明。仅发布PNG和概要，不复制源代码、CAD/工程包、模型/贴图或标注数据。合成场景不能作为真实泛化精度证明。

## 2026-10-28 新增材料

新增 P30/P29/P31 图片均为实际隔离验收场景，两种语言共用。仅发布截图及文档，不携带项目 ZIP、方案 JSON、模型或贴图原文件；对应源码检查点 01e2db7。

本仓库用于展示格物智造（GewuZhizao）的项目功能与开发成果，发布文档和运行截图。源代码保持私有；本仓库未授予私有源码的访问或使用权限。

## 截图说明

截图来自项目真实界面或三维渲染，包含已有户型示例及专用功能演示场景。展示材料不包含源码、模型权重、原始户型项目包、原始材质贴图或原始 GLB 文件。

部分截图拍摄于不同开发阶段，界面文案与样式可能随迭代变化。功能状态以本仓库功能清单的更新日期为准。

## 第三方内容

三维预览使用 [Three.js](https://github.com/mrdoob/three.js)，其软件采用 MIT 许可；本仓库未分发该软件。

真实家具模型预览中出现的 Sofa 03、Gothic Bed 01、Dining Table、Dining Chair 02 和 Gothic Cabinet 01 来自 [Poly Haven](https://polyhaven.com/)，原始素材采用 [CC0 许可](https://polyhaven.com/license)。这些素材不作为项目原创建模成果声明。

材质库包含外部 CC0 素材、项目制作的图案和物理材质预设。材质总览用于说明已接入的选择与预览能力，不声明所有素材均为原创。

P35 在源码仓库增加六款项目原创 CC0 灯具 GLB 示例，与上述五款外部家具素材分开。Showcase 发布其应用截图，不分发原始 GLB。原创示例和验收专用品牌字段不代表真实品牌关联；尚未连接外部厂商在线目录。用户/提供方填写的品牌资料不替代模型原始来源和许可。

原始第三方素材与其他内容的权利归各自权利人所有。此处的私有源码声明不改变第三方素材原有许可。

[返回项目首页](README.zh-CN.md)
