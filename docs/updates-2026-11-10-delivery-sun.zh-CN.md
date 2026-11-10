# 2026-11-10 · 资料交付与地理日光

[English](updates-2026-11-10-delivery-sun.md) | **中文**

源码: [0de6906](https://github.com/ETET114514/GewuZhizaoNew/commit/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458)

本批交付四类重算清单（房间面积、家具尺寸/房间归属、门窗洞口及柱梁构件）、搜索/待校核筛选、筛选CSV及离线HTML/JSON，并与图纸组成同快照ZIP。图纸集新增可选项目封面/目录，直线DXF尺寸可选原生DIMENSION、单位数值占位符及图形块。地理日光按经纬度、当地日期时间、明确UTC时差和图上北向计算，支持24整点、CSV/JSON及预览/应用/取消/历史，地平线下关闭直射。

距前次Showcase同步，源码还新增构件及混合组任意角度变换、可见尺寸参考图/图纸集、人工/手工费用/优惠税费报价，以及本机持久成图库。范围与当时验证见源码带日期记录，不宣称本次展示同步重新验收了这些早期子项。

服务端在状态锁内取工程快照，再生成只读资料/归档，共同修订与SHA-256清单绑定。原生CAD转换仅作用于合适的直线尺寸，PDF/PNG继续使用静态排版。日光在本机Python计算；应用时服务端重算角度，校验后的地理输入与实际渲染日光设置分开保存。

重启本机服务并刷新。打开并标定合成演示工程；文件→图纸集开启封面/原生DXF尺寸；文件→项目资料筛选、校核和导出清单/组合包。三维做深化→顶面与灯光→日光与阴影中打开地点日期计算，选时刻、预览后应用或取消。填写实际北向与UTC时差，示例不是自动定位。

当前仍为参考交付：导出CAD尺寸不与墙体约束关联，弧长/端点不等的净长口径保留静态；清单不是制造采购BOM或正式签审。NOAA分数年公式计算近似几何方向，不含折射/天气/时区检索或规范日照时数/照度分析；环境光/HDRI/室内灯另行控制。不据此宣布云协作或DWG等完整目标完成。

源码阶段最终证据：**692项全量Node、75项相关Python**，以及实际Edge流程、390px与原生DXF/ZIP校验及共同修订/太阳位置CSV和JSON独立读回。更早各阶段数字有重叠，不相加；未跑全量Python。Showcase发布只检查文档、相对链接、双语导航与素材来源，不重新运行应用测试集。

新增四张PNG为隔离合成工程的实际验收截图，两种语言共用。源码路径：wall-recognition/output/project-schedules/desktop.png、p27-drawing-cover/render-1.png、native-dimensions/desktop.png及solar-position/desktop.png。没有复制客户图纸、完整源码、项目/交换包、贴图或模型素材，原有许可保持。太阳位置公式来源：https://gml.noaa.gov/grad/solcalc/solareqns.PDF 。

- [P19_GEOGRAPHIC_SUNLIGHT.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P19_GEOGRAPHIC_SUNLIGHT.md)
- [P27_NATIVE_DIMENSIONS.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P27_NATIVE_DIMENSIONS.md)
- [PROJECT_SCHEDULES.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/PROJECT_SCHEDULES.md)
- [P27_DRAWING_SETS.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P27_DRAWING_SETS.md)
- [P28_COMMERCIAL.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P28_COMMERCIAL.md)
- [P22_MIXED_ROTATION.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P22_MIXED_ROTATION.md)
- [RENDER_STUDIO.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/RENDER_STUDIO.md)
