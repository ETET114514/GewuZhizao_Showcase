# Showcase materials and third-party assets

**English** | [中文](NOTICE.zh-CN.md)

## 2026-11-20 · P24 kitchen disassembly and retained-tool transfer turns

[Source commit 27a9f22](https://github.com/ETET114514/GewuZhizaoNew/commit/27a9f2228e26bf08a6fdfeb6060f9deaab0dee9d) · [Source PR #3, awaiting merge](https://github.com/ETET114514/GewuZhizaoNew/pull/3) · [Scope and evidence](docs/updates-2026-11-20-p24.md)

The isometric screenshot comes from the generated cabinet fixture used in Edge acceptance testing.

[Screenshot source](https://github.com/ETET114514/GewuZhizaoNew/blob/27a9f2228e26bf08a6fdfeb6060f9deaab0dee9d/wall-recognition/output/p24-tool-transfer-turn/preview.png)

## 2026-11-18 · Wall reference ranges and kitchen drawing/contact workflows

[Source 9b48db1](https://github.com/ETET114514/GewuZhizaoNew/commit/9b48db190e64f437662d0ac37662332151c6fe97) · [Scope and evidence](docs/updates-2026-11-18-p12-p24.md)

Four shared PNGs are self-produced captures from synthetic acceptance projects, copied byte-for-byte from the source revision. No customer drawings, local project archives, full source, models or textures are copied into this Showcase. The wall screenshot shows a horizontal arc-wall slice despite its original filename; the kitchen combined/exploded captures represent their dated acceptance stages. See the bilingual screenshot index for exact source paths and provenance. Existing third-party notices remain unchanged.

Full P12 and P24 remain unfinished. These are bounded reference drawings and geometric checks. Unknown reference semantics, arbitrary wall topology, complete construction details, professional hidden-line removal, hardware/connection strength, installation constraints, assembly order/motion and manufacturer CNC remain open. Equipment is the existing schematic geometry; an overlap may be intended embedding and requires review.

Development evidence: 809 full Node tests, 57 related Python tests, 15 new Edge workflow groups, and the existing 14 cross-cabinet/11 single-cabinet browser groups passed. Independent GEOS checks cover 24 normal/low-upper-cabinet cases; actual ZIP/CSV/HTML/JSON and native-dimension CAD downloads were read back. Publication preparation additionally passed 22 P12 reference-range/wall-drawing Python tests on 2026-11-18. Counts overlap and are not added; no full Python rerun or fresh rerun of every earlier browser suite is claimed. Showcase publication checks bilingual pages, links and screenshot provenance.

## 2026-11-16 · Continuous wall sections, curved junctions and typed references

[Source 00dd9d8](https://github.com/ETET114514/GewuZhizaoNew/commit/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0) · [Scope and evidence](docs/updates-2026-11-16-p12-sections.md)

Five added PNGs are self-produced actual application captures from isolated synthetic acceptance projects: p12-variable-wall-3d.png, p12-continuous-fillet.png, p12-variable-merge.png, p12-reference-bindings.png and p12-angle-elevation.png. Both language editions share these files. No customer drawings, project archives, full source, models or textures are copied. Existing third-party licenses remain unchanged.

Full P12 remains unfinished. Profiles have 2–64 controls, 50–600 mm thickness and 100–20000 mm height; all heights may inherit globally, without mixing inherited and numeric controls. Junctions select 3–12 wall ends with 0–1000 mm movement: retain supports, explicitly rotate straight supports, or reconstruct a circle while retaining its far endpoint/tangent and curvature direction. No valid finite solution or unsupported references rejects the edit. Typed JSON Pointer bindings cover fraction, station and host semantics, including one-to-many rebinding; undeclared business/program semantics stay protected. Elevation checks qualify the measurement-line endpoints, without inferring a new room partition/area at that height. Arc geometry uses the existing bounded sampling; collision stays conservative and quantities retain nominal axis-based face-area conventions. Arbitrary surface/topology transition bodies, undefined reference semantics, complete construction sections/details and unlimited report-external inference/global-optimum guarantees remain open.

Source validation on 2026-11-16: **1363 full Python tests** across all 183 modules, **760 full Node tests**, **78 final related Python checks**, and **14 new real Edge workflow groups** passed. Six existing browser suites were rerun: path finishes, closeout, engineering, whole-room/node, original path walls and P27 drawing export. Final related checks also verify the last calibration/projection binding branches. Coverage includes independent mesh-volume and spiral-length checks, real 3D viewing, holes, split conservation, inheritance, transition following, curve-support reconstruction, explicit overlap sources, external bindings, undo/redo, save/reopen and 390px. Independent downloaded DXF/PDF extraction confirms 5317 mm angled and 3760 mm height-band net dimensions. Counts overlap and are not added. Showcase publication verifies bilingual pages, local links and screenshot provenance without rerunning application suites.

## 2026-11-16 · P12 room finishes, live net dimensions and straight-wall junctions

[Source 65ad14a](https://github.com/ETET114514/GewuZhizaoNew/commit/65ad14a203f1e00fc7e36aebf07fda4530b349a2) · [Scope and evidence](docs/updates-2026-11-16-p12-room.md)

The three new PNGs are self-produced application captures from isolated synthetic acceptance projects: p12-room-finishes.png, p12-room-finishes-narrow.png and p12-wall-junction.png. English and Chinese editions share these assets. No customer drawings, local project archives, full source, models or textures are copied. Existing third-party licenses remain unchanged.

Full P12 remains unfinished. Arc finish contours use at most 0.5 mm sagitta sampling; their perimeter is a sampled polygon length, distinct from the existing analytic single-wall along-path report. Whole-room contours are planar gross boundaries without opening or height-band deductions. P27 stores room identity, relative measurement-line position and interval intent; ambiguous room changes or interval-count changes become unresolved. Junction consolidation preserves original straight supports and allows 0–1000 mm endpoint movement, with at least 100 mm wall remaining; unsupported references, opening truncation and new overlap reject the complete edit. Curved/moving-support nodes, continuous variable thickness/height, unknown-reference reconstruction, arbitrary topology, full construction sections/details and unlimited report-external inference/global-optimum guarantees remain open.

Source validation on 2026-11-16: **1349 full Python tests** passed across all 181 modules in four independent processes; **753 full Node tests**, **66 final related Python tests**, **12 new Edge workflow groups** and **24 existing P12 browser groups** passed. Final related/browser checks also cover the last source-snapshot guard. Real save/reopen, live wall-edit identity migration, undo/redo, stale-source refusal and 390px were checked. Downloaded DXF/PDF were independently read back with the updated 3720 mm value; PNG is 1754 × 1240. Counts overlap and are not added. Showcase publication checks bilingual content, local links and image provenance without rerunning application tests.

## 2026-11-16 · P12 wall engineering and path-side finish measurement

[Source 9189120](https://github.com/ETET114514/GewuZhizaoNew/commit/918912079639253fb9ad7cfcb07d010239d822ed) · [Scope and evidence](docs/updates-2026-11-16-p12.md)

Four added PNGs are self-produced actual application captures from isolated synthetic acceptance projects: p12-routes.png, p12-sections.png, p12-path-finishes.png and p12-path-report.png. Both language editions share these files. No customer drawings, project archives, models, textures or full source are copied. Existing third-party licenses remain unchanged. Source paths and the exact source revision are recorded in the screenshot index.

Full P12 remains unfinished. Enumeration certifies only the current finite report after completion (at most 100 reported candidates, 20 selected gaps and 500 resulting wall segments), without report-external semantic or unlimited global-optimum guarantees. Projection requires an explicit supporting line/circle and a tolerance of at most 10px; unknown references and unsupported conflicts reject the complete edit. Fillets require a valid finite analytic solution and preserve explicit thickness steps. Path-side finishes are measurement policies, without new finish solids, whole-room nonorthogonal finished-face reconstruction, step-connector lengths, multi-wall node reconstruction, continuous variable sections or P27-linked construction sheets.

Final source-stage rerun on 2026-11-16: **1342 full Python tests and 744 full Node tests passed**. Real Edge acceptance passed 5 new path-finish groups plus the existing 9 closeout and 10 engineering groups, with no unexpected page/HTTP errors. Coverage includes independent arc formulas, real CSV/JSON read-back, preview/cancel/history, actual panel pieces/volume, door poses, project save/reopen, and 390px layouts; Python also checks restore/ZIP. The 8 new Python tests are included in the full-suite count. Earlier dated counts overlap and are not added. Showcase publication checks bilingual documentation, relative links and screenshot provenance; it does not repeat application tests.

[Screenshot provenance](screenshots/README.md)

## 2026-11-14 · Spatial tools, cabinet views and purchasing

[Source 2c0bbbb](https://github.com/ETET114514/GewuZhizaoNew/commit/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da) · [Scope and evidence](docs/updates-2026-11-14.md)

Six added PNGs are self-produced captures of isolated synthetic acceptance projects, shared by both language editions. No customer drawings, project archives, purchase packages, upstream screenshots, models, textures or full source are copied into this showcase. The source-stage study credits the MIT house-plan-designer projects by chencheng666 and ZWD11; existing third-party runtime licenses remain unchanged.

Zones preserve physical rooms and flooring quantities; color overlays are illustrations. Dimension suggestions do not move geometry. PDF extraction is limited to independently drawn straight/polygon edges, and HouseSpec imports one floor of supported structure with explicit unsupported-item reports. Full P24 kitchen/assembly/process drawings and full P28 inventory, arbitrary manufacturing and external identities/ERP/payment/signature/CNC integrations remain open. No universal recognition accuracy is claimed.

Evidence: 744 full Node and 58 related Python tests, 22 new browser groups and existing P31/DXF-axis/wall-review regressions passed in this development batch. Immediately before publication, another 27 P24/P28-related Python checks passed. Counts overlap; no full Python-suite or complete rerun of prior cabinet/procurement browser evidence is claimed. Showcase publication checks bilingual documentation, links and image provenance.

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
