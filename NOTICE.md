# Showcase materials and third-party assets

**English** | [中文](NOTICE.zh-CN.md)

## 2026-11-13 · P28 manufacturing references and local procurement

Source [7714f04](https://github.com/ETET114514/GewuZhizaoNew/commit/7714f0486a557d35aa069b249a37d29947030ed6) · [P28 manufacturing references and local procurement](docs/updates-2026-11-13-p28.md)

This update adds only three self-produced synthetic acceptance captures: p28-custom-board.png, p28-stock-planning.png, p28-procurement.png. See the [screenshot index](screenshots/README.md) for source paths and captions. No full source, customer projects, commercial/purchase delivery packages, models or textures are copied; existing third-party asset licenses remain unchanged. Manufacturing-reference and local-procurement validation is scoped in the update record above.

## 2026-11-10 · Project delivery, native CAD dimensions and geographic sunlight

Source [0de6906](https://github.com/ETET114514/GewuZhizaoNew/commit/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458) · Scope and evidence: [Project delivery, native CAD dimensions and geographic sunlight](docs/updates-2026-11-10-delivery-sun.md)

Project delivery now combines four recomputed schedules (room areas, furniture sizes/room assignment, openings and structural elements), searchable review lists, filtered CSV and offline HTML/JSON with a same-snapshot drawing/schedule ZIP. Drawing sets add optional project covers/directories; straight DXF dimensions can be native DIMENSION entities, retaining unit-aware numeric placeholders and graphic blocks. Geographic sunlight uses latitude/longitude, local date/time, an explicit UTC offset and drawing north, with 24 hourly samples, CSV/JSON records and preview/apply/cancel/history. Below-horizon direct sun is disabled.

Four added PNGs are actual captures of isolated synthetic acceptance projects, shared by both languages. Source paths: wall-recognition/output/project-schedules/desktop.png, p27-drawing-cover/render-1.png, native-dimensions/desktop.png and solar-position/desktop.png. No customer drawings, full source, project/exchange packages, textures or model assets are copied. Existing asset licenses remain unchanged. Solar formula attribution: https://gml.noaa.gov/grad/solcalc/solareqns.PDF .

These remain reference deliverables: exported CAD dimensions are not constrained to walls; arc/net conventions that differ from endpoint distance stay static. Schedules are not manufacturing/procurement BOMs or formal approvals. NOAA fractional-year solar positions are approximate geometric directions, without refraction/weather/timezone lookup or regulatory sunlight-duration/illuminance analysis. Ambient/HDRI/interior lighting remains separately controlled. No cloud collaboration or DWG completion is claimed.

Source-stage final evidence: **692 full Node tests and 75 related Python tests**, plus real Edge workflows, 390px checks and independent read-back of native DXF entities, ZIP hashes/shared revisions and downloaded solar CSV/JSON. Earlier stage counts overlap and are not added; no full Python rerun. Showcase publication checks documentation, relative links, bilingual navigation and image provenance, without rerunning application suites.

## 2026-11-07 · Local rendering and model/plan delivery

Source [f913696](https://github.com/ETET114514/GewuZhizaoNew/commit/f913696701fd4c8e94aaea153ea14f6d65bb86b1). [Materials and evidence](docs/updates-2026-11-07-render-exchange.md)

Three added PNGs come only from isolated synthetic acceptance projects and are shared by both languages. Sources in New: `output/p20-model-export/plan-paper-{desktop,mobile}.png` and `output/render-studio/full-render.png`. No user plans, source, models/textures/HDR or project/exchange packages are included; existing material licenses remain unchanged.

## 2026-10-31 · P26 and P13 closeout

Source [77736ba](https://github.com/ETET114514/GewuZhizaoNew/commit/77736bac6b0e83db23a9c269ad21c66d09f9c1d9); [scope and evidence](docs/updates-2026-10-31-closeout.md). Five new PNGs are actual acceptance captures of generated empty rooms, covering P13 finish/height measurements and P26 production/read-only sharing. Only summaries/screenshots are copied; test tones, MP4s, project ZIPs, panorama packages and source remain in New.

## 2026-10-31 · Panorama acceptance materials

Source [b9ee167](https://github.com/ETET114514/GewuZhizaoNew/commit/b9ee167b494268e74a54c2e242c904004dbced65); [scope and evidence](docs/updates-2026-10-31-panorama.md). Four new PNGs come from locally generated empty-room acceptance scenes and are shared by both languages. Only screenshots and summaries are copied, without user plans, source, panorama/project packages, textures or models.

## 2026-10-30 · Design checkpoint materials

Source [0f28b3e](https://github.com/ETET114514/GewuZhizaoNew/commit/0f28b3e043333f733bcf8c89ca6fc11f0b6eb1cf); [scope and evidence](docs/updates-2026-10-30-design.md). New P15/P26/P27/P28 images are actual isolated acceptance screenshots. Both languages share PNG assets with translated captions. No source, user projects, CAD files, model/texture assets or video packages are mirrored. Source-side videos remain separately documented; these synthetic scenes do not establish independent recognition accuracy.

## 2026-10-30 checkpoint materials

Corresponds to New [d9338b5](https://github.com/ETET114514/GewuZhizaoNew/commit/d9338b5dd8194e8acb36768fa068e6626959531e). [Scope and verification](docs/updates-2026-10-30.md). P21 CAD/boundary/opening/residential scenes, P31 OCR, P17 glTF and P30 route captures come from actual isolated acceptance runs; both languages share images with translated descriptions. Only PNGs and summaries are copied, without source, CAD/project packages, models/textures or annotations. Synthetic scenes do not establish real-world generalization accuracy.

## 2026-10-28 additions

The new P30/P29/P31 images are actual isolated acceptance scenes, shared by both language versions. Only screenshots/documentation are published, without project ZIPs, plan JSON, model assets or texture data. Source checkpoint 01e2db7.

This repository presents GewuZhizao's features and development results through documentation and actual application screenshots. Source code remains private; this repository grants no access or usage rights to that private source.

## Screenshots

Screenshots come from the actual interface or 3D rendering, including existing plan examples and dedicated feature demos. Showcase materials do not include source code, model weights, original plan project packages, original material textures or original GLB files.

Some screenshots were captured at different development stages; UI wording and styling may change. Feature status follows the update date of this repository's feature list.

## Third-party content

The 3D preview uses [Three.js](https://github.com/mrdoob/three.js), licensed under MIT. This repository does not distribute that software.

The Sofa 03, Gothic Bed 01, Dining Table, Dining Chair 02 and Gothic Cabinet 01 shown in real furniture-model previews come from [Poly Haven](https://polyhaven.com/). The original assets use the [CC0 license](https://polyhaven.com/license). They are not claimed as original project modeling work.

The material library includes external CC0 assets, project-created patterns and physical material presets. Its overview demonstrates available selection and preview capabilities; it does not claim that all assets are original.

P35 adds six project-original CC0 lamp GLB examples in the source repository, separate from the five external furniture assets above. Showcase publishes their application screenshots rather than the original GLB files. Original examples and acceptance-only brand fields imply no real brand affiliation; no external vendor online catalog is connected. User/provider-entered brand metadata does not replace the model's recorded provenance or license.

Rights to original third-party assets and other content remain with their respective rights holders. The private-source statement does not change those assets' original licenses.

[Back to project home](README.md)
