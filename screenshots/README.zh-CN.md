# 截图索引

[English](README.md) | **中文**

## 2026-11-20 · P24 厨房装拆校核与工具退出前转向

[源码提交 bc71e67](https://github.com/ETET114514/GewuZhizaoNew/commit/bc71e6716c54061b871dfe3aea8494355e4cf784) · [源码 PR #3，待合并](https://github.com/ETET114514/GewuZhizaoNew/pull/3) · [范围与验收](../docs/updates-2026-11-20-p24.zh-CN.md)

![装拆预览中的工具独立转向](p24-tool-withdraw-yaw.png)

[截图来源](https://github.com/ETET114514/GewuZhizaoNew/blob/bc71e6716c54061b871dfe3aea8494355e4cf784/wall-recognition/output/p24-tool-withdraw-yaw/preview.png)

## 2026-11-18 · 墙体区间引用与厨房图纸/接触检查

[源码 9b48db1](https://github.com/ETET114514/GewuZhizaoNew/commit/9b48db190e64f437662d0ac37662332151c6fe97) · [范围与验收](../docs/updates-2026-11-18-p12-p24.zh-CN.md)

![指定标高的弧墙水平截面](p12-wall-slice.png)

指定标高的弧墙水平截面 · [来源](https://github.com/ETET114514/GewuZhizaoNew/blob/9b48db190e64f437662d0ac37662332151c6fe97/wall-recognition/output/p12-wall-drawings/arc-elevation.png)

![明确选择的上下柜联合立面](p24-kitchen-combined.png)

明确选择的上下柜联合立面 · [来源](https://github.com/ETET114514/GewuZhizaoNew/blob/9b48db190e64f437662d0ac37662332151c6fe97/wall-recognition/output/p24-kitchen-combined/aligned-dialog.png)

![实体板件爆炸参考投影](p24-cabinet-exploded.png)

实体板件爆炸参考投影 · [来源](https://github.com/ETET114514/GewuZhizaoNew/blob/9b48db190e64f437662d0ac37662332151c6fe97/wall-recognition/output/p24-cabinet-assembly/single-assembly-exploded.png)

![板件、台面和设备实体接触检查](p24-component-contacts.png)

板件、台面和设备实体接触检查 · [来源](https://github.com/ETET114514/GewuZhizaoNew/blob/9b48db190e64f437662d0ac37662332151c6fe97/wall-recognition/output/p24-kitchen-components/overlap-checks.png)

P12和P24整项仍未完成。当前为有限参考图与几何检查；未知引用语义、任意墙体拓扑、完整施工节点、专业隐藏线、五金/连接强度、安装约束、拆装顺序/运动及厂家CNC继续保留。设备采用现有示意几何，材料重叠可能属于预期嵌入，需要人工核对。

开发验收：809项全量Node、57项相关Python、新15组Edge及原跨柜14组/单柜11组浏览器通过；24套正常/低吊柜工程经GEOS独立核验，实际ZIP/CSV/HTML/JSON和原生尺寸CAD下载经独立读回。2026-11-18发布准备另补验22项P12区间引用/单墙图Python并通过。计数交叠不累加，不声称本轮跑全量Python或重新跑全部历史浏览器。Showcase发布核对双语、链接与截图来源。

## 2026-11-16 · 连续截面、曲线节点与声明式引用迁移

[源码 00dd9d8](https://github.com/ETET114514/GewuZhizaoNew/commit/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0) · [范围与验收](../docs/updates-2026-11-16-p12-sections.zh-CN.md)

本次交付真实直/弧墙分段线性变厚/变高、斜顶与实际洞口，连续切向圆角过渡及宿主跟随，多墙直线/圆弧端点支撑重构，渐变重叠的厚度/高度/材质独立选源，声明式外部引用迁移，以及任意角度与端点标高带净距。新数据共用二维/三维、拆分/修剪/合并、房间完成面、P27、参考工程量、保存及图纸导出。

P12原清单整项仍未完成。截面有2～64个控制点，厚度50～600mm、高度100～20000mm；所有墙高可共同继承全局，不与明确高度节点混填。节点选择3～12个墙端，每端移动0～1000mm：可保留原支撑，明确调整直墙支撑，或重构支撑圆并保持远端位置/切向及曲率方向；无有限解或引用语义不支持时整笔拒绝。JSON Pointer规则支持fraction、station、host及一对多改绑，未声明的业务/程序语义继续保护。标高选项校核测线端点，不在该高度重新推断房间分区/面积。圆弧使用既有有界采样，碰撞仍为保守包络，墙面量保留按轴线的参考面积口径。任意曲面/拓扑过渡实体、未定义引用语义、完整立剖面/施工节点及报告外无限制推断/全局最优保证继续保留。

2026-11-16源码验收：全部183个模块的**1363项全量Python、760项全量Node、78项最终相关Python和14组新Edge浏览器流程**通过。六套既有浏览器流程重新通过：饰面、closeout、engineering、整房/节点、原斜弧墙及P27图纸导出。最终相关复验亦确认最后补充的重标定/近似投影绑定分支。覆盖独立网格体积/螺线长度、真实三维、洞口、拆分守恒、继承、过渡跟随、支撑圆重构、重叠选源、外部绑定、撤销重做、保存重开及390px。独立读回下载的DXF/PDF确认5317mm斜向和3760mm标高带净距。计数重叠，不累加。Showcase发布仅核对双语、站内链接和截图来源，不重复运行应用测试。

![真实三维渐变墙](p12-variable-wall-3d.png)

真实三维渐变墙 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/sections-3d.png)

![连续圆角过渡](p12-continuous-fillet.png)

连续圆角过渡 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/fillet.png)

![明确选择渐变截面来源](p12-variable-merge.png)

明确选择渐变截面来源 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/merge.png)

![声明式引用与节点重构](p12-reference-bindings.png)

声明式引用与节点重构 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/bindings.png)

![角度及端点标高带净距](p12-angle-elevation.png)

角度及端点标高带净距 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/net.png)

## 2026-11-16 · P12 整房完成面、活关联净距与多直墙节点

[源码 65ad14a](https://github.com/ETET114514/GewuZhizaoNew/commit/65ad14a203f1e00fc7e36aebf07fda4530b349a2) · [范围与验收](../docs/updates-2026-11-16-p12-room.zh-CN.md)

本批接通已有正交/斜直/圆弧房间的平面完成面闭合轮廓，含孔洞与饰面厚度阶差连接边；新增 P27 横纵内部净距活关联，以及3～12面直墙端点沿原支撑线整理到明确共同节点。JSON/SVG提供完成面轮廓，现有DXF/PDF/PNG图纸共用当前P27关联净距。饰面仍为测量规则，不新增饰面实体。

原P12整项仍未完成。圆弧完成面采用最大0.5mm弦高采样，周长为采样多边形边长，与已有单墙解析沿程报表分开。整房结果是平面毛轮廓，不扣门窗或标高带。P27保存房间身份、相对测线位置与区间意图；房间归属不明确或区间数量变化时待校核。节点整理保持原直线支撑，每端点可移动0～1000mm，至少保留100mm墙长；不支持的引用、门窗截断和新增共线重叠拒绝整笔操作。含圆弧/须移动支撑线的节点、连续变厚/变高、未知引用重构、任意拓扑、完整立剖面/施工节点及报告外无限制推断/全局最优保证继续保留。

2026-11-16源码验收：四个独立进程覆盖全部181个模块，**1349项全量Python**通过；另有**753项全量Node、66项最终相关Python、12组新Edge流程及24组既有P12浏览器回归**通过。最终相关/浏览器亦确认最后的源快照防过期分支。覆盖实际保存重开、改墙后房间身份迁移与净距重算、撤销重做、旧快照拒绝及390px。独立读回下载的DXF/PDF确认更新后的3720mm净距，PNG为1754×1240。计数重叠，不累加。Showcase发布仅核对双语、站内链接和截图来源，不重复运行应用测试。

![整房完成面轮廓](p12-room-finishes.png)

整房完成面轮廓 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/65ad14a203f1e00fc7e36aebf07fda4530b349a2/wall-recognition/output/p12-room-finishes/desktop.png)

![390px布局](p12-room-finishes-narrow.png)

390px布局 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/65ad14a203f1e00fc7e36aebf07fda4530b349a2/wall-recognition/output/p12-room-finishes/narrow.png)

![已应用多直墙节点](p12-wall-junction.png)

已应用多直墙节点 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/65ad14a203f1e00fc7e36aebf07fda4530b349a2/wall-recognition/output/p12-room-finishes/junction.png)

## 2026-11-16 · P12墙体工程与斜弧饰面测量

[源码 9189120](https://github.com/ETET114514/GewuZhizaoNew/commit/918912079639253fb9ad7cfcb07d010239d822ed) · [范围与证据](../docs/updates-2026-11-16-p12.zh-CN.md)

P12本批接通当前诊断报告完整枚举与接续；直/斜/弧墙端的明确直线、折点与圆弧补墙；近似重叠投影并集与已知引用迁移；正交/共线/同圆弧相接实体逐段墙高、真实材质及继承；两宿主直线/圆弧切向圆角、异厚明确阶差、改半径及持续跟随。跨段墙板和踢脚线保留活宿主链与原逐块数据。斜直墙/弧墙另有左右侧分段施工饰面/全局继承，轴线/结构/完成面沿程净长、洞口投影/截线/完整标高带扣减和带修订CSV/JSON。

完整P12仍未完成。完整枚举仅在结束后认证当前有限报告（最多100候选、确认20处、补后500段墙），不保证报告外建筑语义或无限规模全局最优。投影须明确支撑线/圆弧且容差≤10px，未知引用/不支持冲突整笔拒绝。圆角须有可用有限解析解，异厚保留明确阶差。斜弧饰面是施工计量规则，不新增饰面实体，也未生成整房非正交完成面、厚度阶差连接边、多墙节点重构、连续变截面或P27关联施工图。

2026-11-16源码发布前最终复验：**1342项全量Python、744项全量Node通过**。实际Edge通过5组新增饰面、原9组closeout和10组engineering验收，无意外页面/HTTP错误；包含独立圆弧公式、实际CSV/JSON读回、预览/取消/历史、墙板逐块数据/体积、门扇姿态、保存重开和390px布局，Python另覆盖恢复/ZIP。8项新增Python专项已计入全量数。历史各轮覆盖重叠，不累计。Showcase发布检查双语文档、相对链接和截图来源，不重复应用测试。

![明确圆弧补墙预览](p12-routes.png)

明确圆弧补墙预览 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/918912079639253fb9ad7cfcb07d010239d822ed/wall-recognition/output/p12-closeout/desktop.png)

![相接墙段与属性选源](p12-sections.png)

相接墙段与属性选源 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/918912079639253fb9ad7cfcb07d010239d822ed/wall-recognition/output/p12-engineering/sections-desktop.png)

![弧墙侧继承与显式饰面规则](p12-path-finishes.png)

弧墙侧继承与显式饰面规则 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/918912079639253fb9ad7cfcb07d010239d822ed/wall-recognition/output/p12-path-finishes/settings-desktop.png)

![弧墙沿程净长报表与下载](p12-path-report.png)

弧墙沿程净长报表与下载 · [源码](https://github.com/ETET114514/GewuZhizaoNew/blob/918912079639253fb9ad7cfcb07d010239d822ed/wall-recognition/output/p12-path-finishes/desktop.png)

## 2026-11-14 · 空间工具、整柜视图与采购续作

[源码 2c0bbbb](https://github.com/ETET114514/GewuZhizaoNew/commit/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da) · [范围与验证](../docs/updates-2026-11-14.zh-CN.md)

四项约定改造已串起墙体原图证据、独立功能区与实际灯具、尺寸链诊断，以及限定范围的矢量PDF/HouseSpec结构导入；本次源码还交付P24单柜四视图与板件联查，以及P28多单核对、剩余需求草稿、整批收退货、供应商单据和凭据追溯。

功能区保持物理房间与铺装工程量，色层仅作示意；尺寸建议不改几何。PDF仅提取独立直线/多边形边界，HouseSpec只导入选定单层的支持结构并逐项列未转换内容。P24整组厨房/装配/工艺图，以及P28真实库存、任意制造和身份/ERP/支付/签章/CNC等完整外部目标仍待，不据此宣称通用识别精度。

验证：本开发批次744项全量Node、58项相关Python、22组新浏览器及原P31/DXF轴线/墙体复核回归通过；发布前另复跑27项P24/P28相关Python，通过。计数重叠，不声称全量Python或已完整重跑此前柜体/采购浏览器验收。Showcase发布检查双语文档、链接和截图来源。

以下均为合成验收工程的实际截图。

![只读墙体原图证据叠加](wall-evidence.png)

只读墙体原图证据叠加 · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/wall-image-audit-v1/desktop.png)

![三维功能区与实际灯具](open-zones.png)

三维功能区与实际灯具 · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/learned-design-complete/zone-3d.png)

![尺寸链总标注冲突](dimension-chains.png)

尺寸链总标注冲突 · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/learned-design-complete/chain-conflict.png)

![替换前的HouseSpec结构预览](source-import.png)

替换前的HouseSpec结构预览 · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/learned-design-complete/house-preview.png)

![整柜视图与实体板尺寸联查](cabinet-views.png)

整柜视图与实体板尺寸联查 · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/p24-cabinet-drawings/report.png)

![供应商单据与收退货凭据追溯](purchase-documents.png)

供应商单据与收退货凭据追溯 · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/p28-purchase-documents/documents-desktop.png)

## 2026-11-13 · P28制造参考交付与本机采购收退货

源码 [7714f04](https://github.com/ETET114514/GewuZhizaoNew/commit/7714f0486a557d35aa069b249a37d29947030ed6) · [P28制造参考交付与本机采购收退货](../docs/updates-2026-11-13-p28.zh-CN.md)

三张均为合成验收工程的实际界面截图，两种语言共用图片；不含真实客户项目。

![手工凹多边形板、通孔与重叠盲槽](p28-custom-board.png)

手工凹多边形板、通孔与重叠盲槽 · [New: p28-custom-boards/desktop.png](https://github.com/ETET114514/GewuZhizaoNew/blob/7714f0486a557d35aa069b249a37d29947030ed6/wall-recognition/output/p28-custom-boards/desktop.png)

![有限直切方案比较与可复用余料](p28-stock-planning.png)

有限直切方案比较与可复用余料 · [New: p28-stock-planning/desktop.png](https://github.com/ETET114514/GewuZhizaoNew/blob/7714f0486a557d35aa069b249a37d29947030ed6/wall-recognition/output/p28-stock-planning/desktop.png)

![独立采购价、收退货余额与本机结单](p28-procurement.png)

独立采购价、收退货余额与本机结单 · [New: p28-procurement/desktop.png](https://github.com/ETET114514/GewuZhizaoNew/blob/7714f0486a557d35aa069b249a37d29947030ed6/wall-recognition/output/p28-procurement/desktop.png)

2026-11-13验证：**推送前重新运行737项全量Node测试、70项相关Python测试，全部通过**；未声称全量Python测试。本开发批次此前已顺序通过新增采购浏览器流程及五项原有P28浏览器流程（含窄屏），并独立回读ZIP/SHA-256、DXF、CSV和PDF；Showcase发布未重跑这些浏览器/导出验收。此前测试数有重叠，不累加。更早并行浏览器启动失败的记录保留，后续顺序复验已通过。

## 2026-11-10 · 资料交付、原生CAD尺寸与地理日光

源码 [0de6906](https://github.com/ETET114514/GewuZhizaoNew/commit/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458) · 范围与验证: [资料交付、原生CAD尺寸与地理日光](../docs/updates-2026-11-10-delivery-sun.zh-CN.md)

本批交付四类重算清单（房间面积、家具尺寸/房间归属、门窗洞口及柱梁构件）、搜索/待校核筛选、筛选CSV及离线HTML/JSON，并与图纸组成同快照ZIP。图纸集新增可选项目封面/目录，直线DXF尺寸可选原生DIMENSION、单位数值占位符及图形块。地理日光按经纬度、当地日期时间、明确UTC时差和图上北向计算，支持24整点、CSV/JSON及预览/应用/取消/历史，地平线下关闭直射。

四张实际合成验收截图：资料中心、封面目录、原生CAD导出设置、地点日期日光。展示界面和参考交付，不是客户成果或定量光照分析。

当前仍为参考交付：导出CAD尺寸不与墙体约束关联，弧长/端点不等的净长口径保留静态；清单不是制造采购BOM或正式签审。NOAA分数年公式计算近似几何方向，不含折射/天气/时区检索或规范日照时数/照度分析；环境光/HDRI/室内灯另行控制。不据此宣布云协作或DWG等完整目标完成。

源码阶段最终证据：**692项全量Node、75项相关Python**，以及实际Edge流程、390px与原生DXF/ZIP校验及共同修订/太阳位置CSV和JSON独立读回。更早各阶段数字有重叠，不相加；未跑全量Python。Showcase发布只检查文档、相对链接、双语导航与素材来源，不重新运行应用测试集。

![项目资料中心](project-schedules.png)

![地点与日期日光](geographic-sun.png)

![封面与目录](drawing-cover.png)

![原生CAD尺寸设置](native-cad.png)

## 2026-11-07 · 本机渲染与模型/平面交付

源码 [f913696](https://github.com/ETET114514/GewuZhizaoNew/commit/f913696701fd4c8e94aaea153ea14f6d65bb86b1). [范围与验证](../docs/updates-2026-11-07-render-exchange.zh-CN.md)

三张图片来自独立合成验收场景：桌面/390px平面导出表单及320×180/64次采样的路径追踪图片（仍有噪点，非高清画质基准）。两种语言共用素材。

![平面导出](plan-export.png)

![窄屏导出](plan-export-narrow.png)

![小图采样验收](render-sample.png)

## 2026-10-31 · P26与P13整项收尾

源码 [77736ba](https://github.com/ETET114514/GewuZhizaoNew/commit/77736bac6b0e83db23a9c269ad21c66d09f9c1d9); [范围与证据](../docs/updates-2026-10-31-closeout.zh-CN.md).

![视频剪辑、音轨和逐帧MP4](p26-production.png)

![390px视频制作](p26-production-narrow.png)

![390px只读密码全景分享与跳转](p26-share-narrow.png)

![完成面、标高与关联墙长尺寸](p13-wall-measurements.png)

![390px墙长施工口径](p13-wall-measurements-narrow.png)

五张截图来自合成空房间验收，两种语言共用PNG；无真实用户图纸、工程包、音视频或模型资源镜像。

## 2026-10-31 · 全景与批量采集

源码 [b9ee167](https://github.com/ETET114514/GewuZhizaoNew/commit/b9ee167b494268e74a54c2e242c904004dbced65); [范围与验证](../docs/updates-2026-10-31-panorama.zh-CN.md).

![多站位全景与跳转编号](p26-panorama-tour.png)

![本机文字热点编辑](p26-panorama-hotspots.png)

![已保存人视批量采集与显式下载](p26-panorama-capture.png)

![390px全景批量采集](p26-panorama-capture-narrow.png)

两种语言共用生成验收场景的PNG，说明分别翻译；不复制源码、用户工程、全景文件包或模型素材。

## 2026-10-30 · 设计功能材料

源码[0f28b3e](https://github.com/ETET114514/GewuZhizaoNew/commit/0f28b3e043333f733bcf8c89ca6fc11f0b6eb1cf)；[范围与验证](../docs/updates-2026-10-30-design.zh-CN.md)。新增P15/P26/P27/P28图片均为隔离验收场景的实际运行截图，两种语言共用PNG并分别翻译说明。不镜像源码、用户工程、CAD文件、模型/贴图或录像包；源码侧测试录像单独记录，合成场景不证明独立真实识别精度。

![斜墙与圆弧墙建模](p15-curved-walls.png)

![入户连续带看操作区](p26-guided-tour.png)

![实时门窗定位尺寸](p27-position-dimensions.png)

![基础工程量与参考报价](p28-basic-quote.png)

## 2026-10-30 本轮材料

对应New [d9338b5](https://github.com/ETET114514/GewuZhizaoNew/commit/d9338b5dd8194e8acb36768fa068e6626959531e)。[范围与验证](../docs/updates-2026-10-30.zh-CN.md)。P21 CAD/双线/门窗/住宅骨架、P31 OCR、P17 glTF及P30路线图片为隔离验收场景的实际运行截图；中英文共用图片并分别翻译说明。仅发布PNG和概要，不复制源代码、CAD/工程包、模型/贴图或标注数据。合成场景不能作为真实泛化精度证明。

![CAD底图、已有标注与填充](p21-cad-reference.png)

![双线墙候选](p21-outline-candidates.png)

![门窗候选](p21-opening-candidates.png)

![7种模板与双卫结构骨架](p21-residential-template.png)

![本机OCR工作台](p31-ocr-workbench.png)

![分离资源glTF导入](p17-gltf-import.png)

![保持姿态家具路线](p30-furniture-route.png)

## 2026-10-28 截图

整套布局比较/390 px、路径/开合验证、保存版本对比及独立尺寸均来自 New 01e2db7 的验收场景。仅复制 PNG 运行截图，不复制项目包或原始资产。见[验证](../docs/updates-2026-10-28.zh-CN.md)。

![整套方案](p30-plans.png)
![窄屏方案](p30-plans-narrow.png)
![路径与开合验证](p30-validation.png)
![版本对比](p29-comparison.png)
![独立尺寸](p31-scale-checks.png)

所有图片来自实际运行界面或渲染，保留原图，不含 AI 生成的产品效果示意。

| 文件 | 展示内容 | 场景类型 |
| --- | --- | --- |
| [design-result.png](design-result.png) | 三维户型、家具、门窗、日光与阴影 | 已有户型示例 |
| [workbench.png](workbench.png) | 二维识别结果、素材栏与家具编辑 | 已有户型示例 |
| [floorplan-regions.png](floorplan-regions.png) | 房间分区、区域属性与参考面积 | 已有户型示例 |
| [material-editor.png](material-editor.png) | 单面墙的材质与色卡编辑 | 已有户型示例 |
| [sliding-door.png](sliding-door.png) | 双轨推拉门及玻璃材质 | 功能演示场景 |
| [cove-lighting.png](cove-lighting.png) | 灯槽照射顶面与墙面柔光 | 功能演示场景 |
| [material-library.jpg](material-library.jpg) | 八类、160 款基础材质总览 | 材质样片 |
| [furniture-models.jpg](furniture-models.jpg) | 五个内置 CC0 家具 GLB 预览 | 模型缩略图 |

## 本轮更新 · 2026-10-27 · P35

对应 New [99882a8](https://github.com/ETET114514/GewuZhizaoNew/commit/99882a803e649666153e617bcf2b132661040c9d)。实际隔离验收场景的未修改截图，详见[当前范围与验证](../docs/updates-2026-10-27-p35.zh-CN.md)。展示剖切查看和顶面控制，不代表施工图或在线品牌商品库。

| 文件 | 内容 |
| --- | --- |
| [p35-section-caps.png](p35-section-caps.png) | 旋转/多切面及真实网格截线封口 |
| [p35-ceiling-narrow.png](p35-ceiling-narrow.png) | 390 px 双曲率顶面控制 |

## 同日早前更新 · 2026-10-27 · P16/P18

对应 New `2164415`，均为隔离验收场景的原始截图，功能边界和测试见[更新概要](../docs/updates-2026-10-27.zh-CN.md)。红框表示当前碰撞辅助显示，路径净距使用项目自定义判据。

| 文件 | 展示内容 |
| --- | --- |
| [p16-mixed-objects.png](p16-mixed-objects.png) | 家具、构件、灯具的混合与嵌套对象编辑 |
| [p16-path-check.png](p16-path-check.png) | 多段搬运/旋转路径与通道净距检查 |
| [p18-material-batch.png](p18-material-batch.png) | 房间墙侧及家具部位的跨对象材质替换工作台 |

## 历史更新 · 2026-10-26

以下为隔离验收场景的实际界面；对应 New `35d29cd`，功能边界与验证见[更新概要](../docs/updates-2026-10-26.zh-CN.md)。

| 文件 | 展示内容 |
| --- | --- |
| [p13-room-net-lengths.png](p13-room-net-lengths.png) | 在原轴线标注上新增按房间墙侧净长 |
| [p13-solid-wall-lengths.png](p13-solid-wall-lengths.png) | 扣门窗水平投影后的实墙分段与待校核范围 |
| [p22-floor-occupancy.png](p22-floor-occupancy.png) | 构件占用与铺装/可铺面积联动 |
| [p25-opening-details.png](p25-opening-details.png) | 分格、真实截面与独立纱窗 |
| [p25-bay-window.png](p25-bay-window.png) | 矩形三面飘窗 |
| [p24-kitchen-cutouts.png](p24-kitchen-cutouts.png) | 盲角柜设备及真实孔型 |
| [p23-free-wall-panels.png](p23-free-wall-panels.png) | 自由直缝、简单多边形墙板 |

## 历史更新 · 2026-10-25

| 文件 | 展示内容 | 场景类型 |
| --- | --- | --- |
| [opening-frame-fit.png](opening-frame-fit.png) | 洞内包覆、适配窗框与三维快捷入口 | 隔离验收场景 |
| [opening-frame-fit-editor.png](opening-frame-fit-editor.png) | 框进深、偏移及适配后框外宽高 | 隔离验收场景 |
| [wall-panel-opening-details.png](wall-panel-opening-details.png) | 单洞口逐边材质/上传和矩形尺寸例外 | 隔离验收场景 |
| [wall-panel-lines.png](wall-panel-lines.png) | 非等距横竖线矩形分板 | 隔离验收场景 |
| [upload-library.png](upload-library.png) | 上传材质库名称与条目管理 | 隔离验收场景 |

对应 New 提交 `3d812a2d9bc78b7e51271c6ae7f04357ea00ff1a`。实际运行截图不代表商品安装节点、施工图或最终装修方案。

## 历史更新 · 2026-10-24

| 文件 | 展示内容 | 场景类型 |
| --- | --- | --- |
| [herringbone.png](herringbone.png) | 人字拼、上传材质与隐藏单板 | 隔离验收场景 |
| [herringbone-4k.jpg](herringbone-4k.jpg) | 3840 × 2160 JPG，隐藏选框 | 隔离验收场景 |
| [floor-tiles-upload.png](floor-tiles-upload.png) | 单块上传材质、纹理及选块图 | 隔离验收场景 |
| [furniture-groups.png](furniture-groups.png) | 家具组与三维操纵器 | 隔离验收场景 |
| [furniture-groups-plan.png](furniture-groups-plan.png) | 二维组范围与拖动入口 | 隔离验收场景 |
| [wall-opening-surround.png](wall-opening-surround.png) | 洞口上/右包口及逐洞开关 | 隔离验收场景 |

对应 New 提交 544714f145bec6094d7a9b3ed4ac20582f59d265。蓝板为自制上传条纹图，空缺为隐藏示例，不表示结构洞或完整装修交付。

## 历史厨房开孔与地面铺贴 · 2026-10-23

| 文件 | 展示内容 | 场景类型 |
| --- | --- | --- |
| [kitchen-cutouts.png](kitchen-cutouts.png) | 厨房设备编辑、矩形开孔、柜组绑定与二维参数 | 隔离验收场景 |
| [kitchen-cutouts-4k.jpg](kitchen-cutouts-4k.jpg) | 简化水槽/灶具、连续台面与通孔，3840 × 2160 实时图片 | 隔离验收场景 |
| [floor-layout.png](floor-layout.png) | 地面起点、三种铺法、单块尺寸与排版小图 | 隔离验收场景 |
| [floor-layout-4k.jpg](floor-layout-4k.jpg) | 按房间边界裁切的 PBR 地面排版，3840 × 2160 实时图片 | 隔离验收场景 |

对应 New 提交 `a1407646daa384e1bc5c7f8650724208c2118d80`。厨房界面红框为现有碰撞提示，图片输出隐藏辅助线；不代表施工图或完成的装修方案。

## 历史统一工作台与 L 形厨房 · 2026-10-23

| 文件 | 展示内容 | 场景类型 |
| --- | --- | --- |
| [unified-workbench.png](unified-workbench.png) | 同一三维工作台、共用工具/属性与家具画布手柄 | 隔离验收场景 |
| [unified-plan.png](unified-plan.png) | 统一二维工作台与辅助视图入口 | 隔离验收场景 |
| [l-kitchen.png](l-kitchen.png) | 两个独立左右盲位 L 形厨房、单块连续凹台面与编辑器 | 隔离验收场景 |
| [l-kitchen-plan.png](l-kitchen-plan.png) | 二维六顶点 L 形台面轮廓 | 隔离验收场景 |
| [l-kitchen-narrow.png](l-kitchen-narrow.png) | 390 px 厨房编辑器 | 隔离验收场景 |

该轮对应 New 提交 `37c066b3becd011e96714efd648b8600e50aedc3`（含工作台提交 `66c8761`）。L 形截图红框为当前姿态碰撞提示；保留原始验收截图，不代表完成的装修方案。

## 历史操作基础 · 2026-10-23

| 文件 | 展示内容 | 场景类型 |
| --- | --- | --- |
| [workflow-plan.png](workflow-plan.png) | 五组深化工具、当前顶面属性和统一状态提示 | 隔离验收场景 |
| [workflow-model.png](workflow-model.png) | 三维厨房组定位、朝向与统一应用/取消 | 隔离验收场景 |
| [workflow-model-narrow.png](workflow-model-narrow.png) | 390 px 下的当前厨房属性与统一操作 | 隔离验收场景 |

截图对应 New 提交 `d89af66dd1e72552ac1a8f874389232fd6db75db`，不代表完整装修方案；当轮二维/三维仍使用原有容器，目前已由 U03 统一工作台替代。

## 历史室内设计 · 2026-10-20

| 文件 | 展示内容 | 场景类型 |
| --- | --- | --- |
| [seamed-wall-trim.png](seamed-wall-trim.png) | 规则网格分缝、四周矩形收边并保留窗洞 | 功能演示场景 |
| [structures.png](structures.png) | 单层柱、梁、烟道与包管 | 功能演示场景 |
| [wardrobe-open.png](wardrobe-open.png) | 衣柜板件、分格、门板与内部抽屉开合 | 功能演示场景 |
| [straight-kitchen.png](straight-kitchen.png) | 地柜/吊柜直线排列、独立材质连续台面 | 功能演示场景 |

## 室内设计与项目管理 · 2026-10-19

| 文件 | 展示内容 | 场景类型 |
| --- | --- | --- |
| [background-wall.png](background-wall.png) | 木饰面背景墙保留实际窗洞 | 功能演示场景 |
| [slats-wall.png](slats-wall.png) | 竖向木格栅的厚度与间隔 | 功能演示场景 |
| [projects.png](projects.png) | 项目命名、搜索、缩略图与自动保存入口 | 功能演示场景 |

## 材质库

![160 款材质总览](material-library.jpg)

## 真实家具模型

![五个内置 CC0 家具 GLB 预览](furniture-models.jpg)

外部素材来源见[素材说明](../NOTICE.zh-CN.md)。当前展示为功能原型，图片不代表完整施工方案或离线写实渲染成果。

[返回项目首页](../README.zh-CN.md)
