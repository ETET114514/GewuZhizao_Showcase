# Screenshot index

**English** | [中文](README.zh-CN.md)

## 2026-11-20 · P24 joint collision search for boards and tools

[Source commit 8bc8569](https://github.com/ETET114514/GewuZhizaoNew/commit/8bc8569d42d706ee2fd10a44722f3d4349c3e28f) · [Source PR #3, awaiting merge](https://github.com/ETET114514/GewuZhizaoNew/pull/3) · [Scope and evidence](../docs/updates-2026-11-20-p24.md)

![Verified tool withdrawal detour and turn](p24-joint-stage-turn.png)

[Screenshot source](https://github.com/ETET114514/GewuZhizaoNew/blob/8bc8569d42d706ee2fd10a44722f3d4349c3e28f/wall-recognition/output/p24-joint-stage-turn/preview.png)

![Joint retained-tool collision search](p24-tool-transfer-joint.png)

[Screenshot source](https://github.com/ETET114514/GewuZhizaoNew/blob/f062223e28f1a39eab12dd69706d91b9abfc398c/wall-recognition/output/p24-tool-transfer-joint/preview.png)

![Focused view of the original collision](p24-tool-transfer-timing.png)

[Screenshot source](https://github.com/ETET114514/GewuZhizaoNew/blob/601db4d1e0f2023d0b64d39fac83f5e09edf4a04/wall-recognition/output/p24-tool-transfer-timing/witness.png)

![Retained-tool transfer turn](p24-tool-transfer-turn.png)

[Screenshot source](https://github.com/ETET114514/GewuZhizaoNew/blob/27a9f2228e26bf08a6fdfeb6060f9deaab0dee9d/wall-recognition/output/p24-tool-transfer-turn/preview.png)

![Multi-segment approach and withdrawal turns](p24-tool-multi-turn.png)

[Screenshot source](https://github.com/ETET114514/GewuZhizaoNew/blob/b82b13b86c1e3e23fd15b07ccec774baf04322d3/wall-recognition/output/p24-tool-multi-turn/preview.png)

![Independent approach turn](p24-tool-entry-turn.png)

[Screenshot source](https://github.com/ETET114514/GewuZhizaoNew/blob/0558870f17e7183c7769c00e6432fb3b5b6a3ae7/wall-recognition/output/p24-tool-entry-turn/preview.png)

![Synchronized withdrawal turn](p24-tool-sync-turn.png)

[Screenshot source](https://github.com/ETET114514/GewuZhizaoNew/blob/245b3d21f13ccd6a72919dac7357325099052d83/wall-recognition/output/p24-tool-sync-turn/preview.png)

![In-place withdrawal turn](p24-tool-withdraw-yaw.png)

[Screenshot source](https://github.com/ETET114514/GewuZhizaoNew/blob/bc71e6716c54061b871dfe3aea8494355e4cf784/wall-recognition/output/p24-tool-withdraw-yaw/preview.png)

## 2026-11-18 · Wall reference ranges and kitchen drawing/contact workflows

[Source 9b48db1](https://github.com/ETET114514/GewuZhizaoNew/commit/9b48db190e64f437662d0ac37662332151c6fe97) · [Scope and evidence](../docs/updates-2026-11-18-p12-p24.md)

![Arc-wall horizontal slice at a selected level](p12-wall-slice.png)

Arc-wall horizontal slice at a selected level · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/9b48db190e64f437662d0ac37662332151c6fe97/wall-recognition/output/p12-wall-drawings/arc-elevation.png)

![Explicitly selected upper/lower kitchen elevations](p24-kitchen-combined.png)

Explicitly selected upper/lower kitchen elevations · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/9b48db190e64f437662d0ac37662332151c6fe97/wall-recognition/output/p24-kitchen-combined/aligned-dialog.png)

![Physical-board exploded reference projection](p24-cabinet-exploded.png)

Physical-board exploded reference projection · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/9b48db190e64f437662d0ac37662332151c6fe97/wall-recognition/output/p24-cabinet-assembly/single-assembly-exploded.png)

![Board, countertop and equipment contact checks](p24-component-contacts.png)

Board, countertop and equipment contact checks · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/9b48db190e64f437662d0ac37662332151c6fe97/wall-recognition/output/p24-kitchen-components/overlap-checks.png)

Full P12 and P24 remain unfinished. These are bounded reference drawings and geometric checks. Unknown reference semantics, arbitrary wall topology, complete construction details, professional hidden-line removal, hardware/connection strength, installation constraints, assembly order/motion and manufacturer CNC remain open. Equipment is the existing schematic geometry; an overlap may be intended embedding and requires review.

Development evidence: 809 full Node tests, 57 related Python tests, 15 new Edge workflow groups, and the existing 14 cross-cabinet/11 single-cabinet browser groups passed. Independent GEOS checks cover 24 normal/low-upper-cabinet cases; actual ZIP/CSV/HTML/JSON and native-dimension CAD downloads were read back. Publication preparation additionally passed 22 P12 reference-range/wall-drawing Python tests on 2026-11-18. Counts overlap and are not added; no full Python rerun or fresh rerun of every earlier browser suite is claimed. Showcase publication checks bilingual pages, links and screenshot provenance.

## 2026-11-16 · Continuous wall sections, curved junctions and typed references

[Source 00dd9d8](https://github.com/ETET114514/GewuZhizaoNew/commit/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0) · [Scope and evidence](../docs/updates-2026-11-16-p12-sections.md)

This delivery adds real piecewise-linear thickness/height on finite straight and arc walls, sloping roofs and actual openings; continuous tangent-fillet transitions and host following; multi-wall line/circle endpoint reconstruction; explicit thickness/height/material sources for variable overlap sections; declared external reference migration; and arbitrary-angle room net dimensions with endpoint elevation/band checks. The new data participates in 2D/3D, split/trim/merge, room finishes, P27, quantities, persistence and drawing exports.

Full P12 remains unfinished. Profiles have 2–64 controls, 50–600 mm thickness and 100–20000 mm height; all heights may inherit globally, without mixing inherited and numeric controls. Junctions select 3–12 wall ends with 0–1000 mm movement: retain supports, explicitly rotate straight supports, or reconstruct a circle while retaining its far endpoint/tangent and curvature direction. No valid finite solution or unsupported references rejects the edit. Typed JSON Pointer bindings cover fraction, station and host semantics, including one-to-many rebinding; undeclared business/program semantics stay protected. Elevation checks qualify the measurement-line endpoints, without inferring a new room partition/area at that height. Arc geometry uses the existing bounded sampling; collision stays conservative and quantities retain nominal axis-based face-area conventions. Arbitrary surface/topology transition bodies, undefined reference semantics, complete construction sections/details and unlimited report-external inference/global-optimum guarantees remain open.

Source validation on 2026-11-16: **1363 full Python tests** across all 183 modules, **760 full Node tests**, **78 final related Python checks**, and **14 new real Edge workflow groups** passed. Six existing browser suites were rerun: path finishes, closeout, engineering, whole-room/node, original path walls and P27 drawing export. Final related checks also verify the last calibration/projection binding branches. Coverage includes independent mesh-volume and spiral-length checks, real 3D viewing, holes, split conservation, inheritance, transition following, curve-support reconstruction, explicit overlap sources, external bindings, undo/redo, save/reopen and 390px. Independent downloaded DXF/PDF extraction confirms 5317 mm angled and 3760 mm height-band net dimensions. Counts overlap and are not added. Showcase publication verifies bilingual pages, local links and screenshot provenance without rerunning application suites.

![Real tapered wall in 3D](p12-variable-wall-3d.png)

Real tapered wall in 3D · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/sections-3d.png)

![Continuous fillet transition](p12-continuous-fillet.png)

Continuous fillet transition · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/fillet.png)

![Explicit variable-section sources](p12-variable-merge.png)

Explicit variable-section sources · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/merge.png)

![Declared references and junction reconstruction](p12-reference-bindings.png)

Declared references and junction reconstruction · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/bindings.png)

![Angle and endpoint-band net dimensions](p12-angle-elevation.png)

Angle and endpoint-band net dimensions · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/00dd9d883d67ce5c9be5de6e7b9fae626efedbc0/wall-recognition/output/p12-sections/net.png)

## 2026-11-16 · P12 room finishes, live net dimensions and straight-wall junctions

[Source 65ad14a](https://github.com/ETET114514/GewuZhizaoNew/commit/65ad14a203f1e00fc7e36aebf07fda4530b349a2) · [Scope and evidence](../docs/updates-2026-11-16-p12-room.md)

This batch connects whole-room planar finish boundaries for existing orthogonal, angled and arc walls, including holes and finish-thickness step connectors; P27 live horizontal/vertical interior net dimensions; and explicit common-support endpoint consolidation for 3–12 straight walls. JSON/SVG report the finish contour, while existing DXF/PDF/PNG drawing exports include the current linked P27 values. Finishes remain measurement policies rather than new finish solids.

Full P12 remains unfinished. Arc finish contours use at most 0.5 mm sagitta sampling; their perimeter is a sampled polygon length, distinct from the existing analytic single-wall along-path report. Whole-room contours are planar gross boundaries without opening or height-band deductions. P27 stores room identity, relative measurement-line position and interval intent; ambiguous room changes or interval-count changes become unresolved. Junction consolidation preserves original straight supports and allows 0–1000 mm endpoint movement, with at least 100 mm wall remaining; unsupported references, opening truncation and new overlap reject the complete edit. Curved/moving-support nodes, continuous variable thickness/height, unknown-reference reconstruction, arbitrary topology, full construction sections/details and unlimited report-external inference/global-optimum guarantees remain open.

Source validation on 2026-11-16: **1349 full Python tests** passed across all 181 modules in four independent processes; **753 full Node tests**, **66 final related Python tests**, **12 new Edge workflow groups** and **24 existing P12 browser groups** passed. Final related/browser checks also cover the last source-snapshot guard. Real save/reopen, live wall-edit identity migration, undo/redo, stale-source refusal and 390px were checked. Downloaded DXF/PDF were independently read back with the updated 3720 mm value; PNG is 1754 × 1240. Counts overlap and are not added. Showcase publication checks bilingual content, local links and image provenance without rerunning application tests.

![Whole-room finish contour](p12-room-finishes.png)

Whole-room finish contour · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/65ad14a203f1e00fc7e36aebf07fda4530b349a2/wall-recognition/output/p12-room-finishes/desktop.png)

![390px layout](p12-room-finishes-narrow.png)

390px layout · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/65ad14a203f1e00fc7e36aebf07fda4530b349a2/wall-recognition/output/p12-room-finishes/narrow.png)

![Applied straight-wall junction](p12-wall-junction.png)

Applied straight-wall junction · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/65ad14a203f1e00fc7e36aebf07fda4530b349a2/wall-recognition/output/p12-room-finishes/junction.png)

## 2026-11-16 · P12 wall engineering and path-side finish measurement

[Source 9189120](https://github.com/ETET114514/GewuZhizaoNew/commit/918912079639253fb9ad7cfcb07d010239d822ed) · [Scope and evidence](../docs/updates-2026-11-16-p12.md)

P12 now connects resumable exhaustive enumeration of the current diagnostic report; explicit straight, bent and circular gap routes between supported wall ends; tolerance-based overlap projection and known-reference migration; adjacent orthogonal/collinear/cocircular wall sections with independent height, real materials and inheritance; and analytic two-host line/arc fillets with explicit unequal-thickness steps, radius edits and continued following. Cross-section wall panels and skirting preserve live host chains and existing piece data. Angled/arc wall sides also gain piecewise construction-finish policies, global inheritance, along-path axis/structure/finish lengths, opening projection/section/full-height-band deductions, and revision-bearing CSV/JSON.

Full P12 remains unfinished. Enumeration certifies only the current finite report after completion (at most 100 reported candidates, 20 selected gaps and 500 resulting wall segments), without report-external semantic or unlimited global-optimum guarantees. Projection requires an explicit supporting line/circle and a tolerance of at most 10px; unknown references and unsupported conflicts reject the complete edit. Fillets require a valid finite analytic solution and preserve explicit thickness steps. Path-side finishes are measurement policies, without new finish solids, whole-room nonorthogonal finished-face reconstruction, step-connector lengths, multi-wall node reconstruction, continuous variable sections or P27-linked construction sheets.

Final source-stage rerun on 2026-11-16: **1342 full Python tests and 744 full Node tests passed**. Real Edge acceptance passed 5 new path-finish groups plus the existing 9 closeout and 10 engineering groups, with no unexpected page/HTTP errors. Coverage includes independent arc formulas, real CSV/JSON read-back, preview/cancel/history, actual panel pieces/volume, door poses, project save/reopen, and 390px layouts; Python also checks restore/ZIP. The 8 new Python tests are included in the full-suite count. Earlier dated counts overlap and are not added. Showcase publication checks bilingual documentation, relative links and screenshot provenance; it does not repeat application tests.

![Explicit circular gap route preview](p12-routes.png)

Explicit circular gap route preview · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/918912079639253fb9ad7cfcb07d010239d822ed/wall-recognition/output/p12-closeout/desktop.png)

![Adjacent wall sections and property sources](p12-sections.png)

Adjacent wall sections and property sources · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/918912079639253fb9ad7cfcb07d010239d822ed/wall-recognition/output/p12-engineering/sections-desktop.png)

![Arc-side inherited and explicit finish policies](p12-path-finishes.png)

Arc-side inherited and explicit finish policies · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/918912079639253fb9ad7cfcb07d010239d822ed/wall-recognition/output/p12-path-finishes/settings-desktop.png)

![Arc path net-length report and downloads](p12-path-report.png)

Arc path net-length report and downloads · [Source](https://github.com/ETET114514/GewuZhizaoNew/blob/918912079639253fb9ad7cfcb07d010239d822ed/wall-recognition/output/p12-path-finishes/desktop.png)

## 2026-11-14 · Spatial tools, cabinet views and purchasing

[Source 2c0bbbb](https://github.com/ETET114514/GewuZhizaoNew/commit/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da) · [Scope and evidence](../docs/updates-2026-11-14.md)

The four agreed spatial adaptations now connect wall-image evidence, independent functional zones with actual lamps, diagnostic dimension chains, and bounded vector-PDF/HouseSpec structure import. This source push also delivers P24 single-cabinet four-view/board-linked drawings and P28 multi-order purchasing, remaining-demand drafts, batch receipts/returns and supplier documents with reference histories.

Zones preserve physical rooms and flooring quantities; color overlays are illustrations. Dimension suggestions do not move geometry. PDF extraction is limited to independently drawn straight/polygon edges, and HouseSpec imports one floor of supported structure with explicit unsupported-item reports. Full P24 kitchen/assembly/process drawings and full P28 inventory, arbitrary manufacturing and external identities/ERP/payment/signature/CNC integrations remain open. No universal recognition accuracy is claimed.

Evidence: 744 full Node and 58 related Python tests, 22 new browser groups and existing P31/DXF-axis/wall-review regressions passed in this development batch. Immediately before publication, another 27 P24/P28-related Python checks passed. Counts overlap; no full Python-suite or complete rerun of prior cabinet/procurement browser evidence is claimed. Showcase publication checks bilingual documentation, links and image provenance.

All images below are actual synthetic acceptance captures.

![Read-only wall evidence overlay](wall-evidence.png)

Read-only wall evidence overlay · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/wall-image-audit-v1/desktop.png)

![Functional zone and actual lamps in 3D](open-zones.png)

Functional zone and actual lamps in 3D · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/learned-design-complete/zone-3d.png)

![Dimension-chain total conflict](dimension-chains.png)

Dimension-chain total conflict · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/learned-design-complete/chain-conflict.png)

![HouseSpec structure preview before replacement](source-import.png)

HouseSpec structure preview before replacement · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/learned-design-complete/house-preview.png)

![Whole-cabinet views and physical board dimensions](cabinet-views.png)

Whole-cabinet views and physical board dimensions · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/p24-cabinet-drawings/report.png)

![Supplier documents and receipt-reference history](purchase-documents.png)

Supplier documents and receipt-reference history · [New source](https://github.com/ETET114514/GewuZhizaoNew/blob/2c0bbbb7c9481c78dec968c07d40b92ef56eb7da/wall-recognition/output/p28-purchase-documents/documents-desktop.png)

## 2026-11-13 · P28 manufacturing references and local procurement

Source [7714f04](https://github.com/ETET114514/GewuZhizaoNew/commit/7714f0486a557d35aa069b249a37d29947030ed6) · [P28 manufacturing references and local procurement](../docs/updates-2026-11-13-p28.md)

All three are actual captures of synthetic acceptance projects, shared by both languages; no real customer project is included.

![Manual concave board with through hole and overlapping pockets](p28-custom-board.png)

Manual concave board with through hole and overlapping pockets · [New: p28-custom-boards/desktop.png](https://github.com/ETET114514/GewuZhizaoNew/blob/7714f0486a557d35aa069b249a37d29947030ed6/wall-recognition/output/p28-custom-boards/desktop.png)

![Bounded stock comparison and reusable offcut](p28-stock-planning.png)

Bounded stock comparison and reusable offcut · [New: p28-stock-planning/desktop.png](https://github.com/ETET114514/GewuZhizaoNew/blob/7714f0486a557d35aa069b249a37d29947030ed6/wall-recognition/output/p28-stock-planning/desktop.png)

![Closed local purchase with independent prices and receipt balances](p28-procurement.png)

Closed local purchase with independent prices and receipt balances · [New: p28-procurement/desktop.png](https://github.com/ETET114514/GewuZhizaoNew/blob/7714f0486a557d35aa069b249a37d29947030ed6/wall-recognition/output/p28-procurement/desktop.png)

Validation on 2026-11-13: **737 full Node tests and 70 related Python tests passed in the final pre-push rerun**; this is not a full Python-suite run. Earlier acceptance in this development batch passed the new procurement browser workflow and five existing P28 browser flows sequentially, including narrow layouts, plus independent ZIP/SHA-256, DXF, CSV and PDF read-back. These browser/export checks were not rerun for Showcase publication. Earlier counts overlap and must not be added. One earlier parallel browser startup failure was retained; subsequent sequential runs passed.

## 2026-11-10 · Project delivery, native CAD dimensions and geographic sunlight

Source [0de6906](https://github.com/ETET114514/GewuZhizaoNew/commit/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458) · Scope and evidence: [Project delivery, native CAD dimensions and geographic sunlight](../docs/updates-2026-11-10-delivery-sun.md)

Project delivery now combines four recomputed schedules (room areas, furniture sizes/room assignment, openings and structural elements), searchable review lists, filtered CSV and offline HTML/JSON with a same-snapshot drawing/schedule ZIP. Drawing sets add optional project covers/directories; straight DXF dimensions can be native DIMENSION entities, retaining unit-aware numeric placeholders and graphic blocks. Geographic sunlight uses latitude/longitude, local date/time, an explicit UTC offset and drawing north, with 24 hourly samples, CSV/JSON records and preview/apply/cancel/history. Below-horizon direct sun is disabled.

Four actual captures from synthetic acceptance projects: schedule center, cover/directory, native CAD export settings and location/date sunlight. These show UI/reference outputs rather than real customer work or a quantitative illumination benchmark.

These remain reference deliverables: exported CAD dimensions are not constrained to walls; arc/net conventions that differ from endpoint distance stay static. Schedules are not manufacturing/procurement BOMs or formal approvals. NOAA fractional-year solar positions are approximate geometric directions, without refraction/weather/timezone lookup or regulatory sunlight-duration/illuminance analysis. Ambient/HDRI/interior lighting remains separately controlled. No cloud collaboration or DWG completion is claimed.

Source-stage final evidence: **692 full Node tests and 75 related Python tests**, plus real Edge workflows, 390px checks and independent read-back of native DXF entities, ZIP hashes/shared revisions and downloaded solar CSV/JSON. Earlier stage counts overlap and are not added; no full Python rerun. Showcase publication checks documentation, relative links, bilingual navigation and image provenance, without rerunning application suites.

![Project schedule center](project-schedules.png)

![Location/date sunlight](geographic-sun.png)

![Cover and directory](drawing-cover.png)

![Native CAD export settings](native-cad.png)

## 2026-11-07 · Local rendering and model/plan delivery

Source [f913696](https://github.com/ETET114514/GewuZhizaoNew/commit/f913696701fd4c8e94aaea153ea14f6d65bb86b1). [Scope and evidence](../docs/updates-2026-11-07-render-exchange.md)

Three PNGs from isolated synthetic acceptance scenes: desktop/390px plan-export forms and a 320×180/64-sample path-traced image with remaining noise, not a high-resolution quality benchmark. Both languages share these assets.

![Plan export](plan-export.png)

![Narrow export form](plan-export-narrow.png)

![Small sampling acceptance image](render-sample.png)

## 2026-10-31 · P26 and P13 closeout

Source [77736ba](https://github.com/ETET114514/GewuZhizaoNew/commit/77736bac6b0e83db23a9c269ad21c66d09f9c1d9); [scope and evidence](../docs/updates-2026-10-31-closeout.md).

![Video clips, audio and deterministic MP4](p26-production.png)

![Video production at 390 px](p26-production-narrow.png)

![Read-only password panorama sharing and jumps at 390 px](p26-share-narrow.png)

![Finish faces, height conventions and linked wall lengths](p13-wall-measurements.png)

![Wall measurement conventions at 390 px](p13-wall-measurements-narrow.png)

Five PNGs come from synthetic empty-room acceptance scenes and are shared by both languages. No real user plans, project packages, audio/video or model resources are mirrored.

## 2026-10-31 · Panoramas and batch capture

Source [b9ee167](https://github.com/ETET114514/GewuZhizaoNew/commit/b9ee167b494268e74a54c2e242c904004dbced65); [scope and evidence](../docs/updates-2026-10-31-panorama.md).

![Multiple panorama scenes and a jump marker](p26-panorama-tour.png)

![Local text hotspot editing](p26-panorama-hotspots.png)

![Saved-human-view capture and explicit download](p26-panorama-capture.png)

![Panorama batch capture at 390 px](p26-panorama-capture-narrow.png)

Both languages share PNGs from generated acceptance scenes with translated descriptions. No source, user projects, panorama packages or model assets are mirrored.

## 2026-10-30 · Design checkpoint materials

Source [0f28b3e](https://github.com/ETET114514/GewuZhizaoNew/commit/0f28b3e043333f733bcf8c89ca6fc11f0b6eb1cf); [scope and evidence](../docs/updates-2026-10-30-design.md). New P15/P26/P27/P28 images are actual isolated acceptance screenshots. Both languages share PNG assets with translated captions. No source, user projects, CAD files, model/texture assets or video packages are mirrored. Source-side videos remain separately documented; these synthetic scenes do not establish independent recognition accuracy.

![Angled and circular-arc wall modeling](p15-curved-walls.png)

![Entry-to-room guided tour controls](p26-guided-tour.png)

![Live door positioning dimensions](p27-position-dimensions.png)

![Basic quantities and reference quotes](p28-basic-quote.png)

## 2026-10-30 checkpoint materials

Corresponds to New [d9338b5](https://github.com/ETET114514/GewuZhizaoNew/commit/d9338b5dd8194e8acb36768fa068e6626959531e). [Scope and verification](../docs/updates-2026-10-30.md). P21 CAD/boundary/opening/residential scenes, P31 OCR, P17 glTF and P30 route captures come from actual isolated acceptance runs; both languages share images with translated descriptions. Only PNGs and summaries are copied, without source, CAD/project packages, models/textures or annotations. Synthetic scenes do not establish real-world generalization accuracy.

![CAD references, cached dimensions and fills](p21-cad-reference.png)

![Boundary-wall candidates](p21-outline-candidates.png)

![Door/window candidates](p21-opening-candidates.png)

![Seven-template library and two-bathroom skeleton](p21-residential-template.png)

![Local OCR workbench](p31-ocr-workbench.png)

![Separated-resource glTF import](p17-gltf-import.png)

![Fixed-pose furniture route](p30-furniture-route.png)

## 2026-10-28 captures

Complete layout comparison/390 px, current path/opening validation, saved-version comparison and independent dimensions are acceptance-scene captures from New 01e2db7. Only PNG screenshots are copied; no project archives or source assets. See [verification](../docs/updates-2026-10-28.md).

![Complete plans](p30-plans.png)
![Narrow plans](p30-plans-narrow.png)
![Path and opening validation](p30-validation.png)
![Version comparison](p29-comparison.png)
![Independent dimensions](p31-scale-checks.png)

All images are original captures from the running interface or rendering. They do not include AI-generated product mockups.

| File | Content | Scene type |
| --- | --- | --- |
| [design-result.png](design-result.png) | 3D plan, furniture, openings, daylight and shadows | Existing floor-plan example |
| [workbench.png](workbench.png) | 2D recognition, asset sidebar and furniture editing | Existing floor-plan example |
| [floorplan-regions.png](floorplan-regions.png) | Room regions, properties and reference area | Existing floor-plan example |
| [material-editor.png](material-editor.png) | Material/color editing on one wall side | Existing floor-plan example |
| [sliding-door.png](sliding-door.png) | Dual-track sliding door and glass | Feature demo |
| [cove-lighting.png](cove-lighting.png) | Cove illumination on ceilings and soft wall light | Feature demo |
| [material-library.jpg](material-library.jpg) | Eight categories/160 base materials | Material samples |
| [furniture-models.jpg](furniture-models.jpg) | Five built-in CC0 furniture GLBs | Model thumbnails |

## Latest update · 2026-10-27 · P35

Corresponds to New [99882a8](https://github.com/ETET114514/GewuZhizaoNew/commit/99882a803e649666153e617bcf2b132661040c9d). Unmodified captures from the actual isolated acceptance scene; see [current scope and verification](../docs/updates-2026-10-27-p35.md). These demonstrate section inspection and ceiling controls, not construction drawings or an online brand catalog.

| File | Content |
| --- | --- |
| [p35-section-caps.png](p35-section-caps.png) | Rotated/multiple section planes with actual mesh-intersection caps |
| [p35-ceiling-narrow.png](p35-ceiling-narrow.png) | Double-curvature ceiling controls at 390 px |

## Earlier update · 2026-10-27 · P16/P18

Corresponds to New `2164415`. All are original isolated acceptance screenshots; see [update details](../docs/updates-2026-10-27.md) for scope/tests. Red boxes show current collision aids; path clearances use project-defined criteria.

| File | Content |
| --- | --- |
| [p16-mixed-objects.png](p16-mixed-objects.png) | Mixed/nested furniture, structural elements and lights |
| [p16-path-check.png](p16-path-check.png) | Multi-segment translation/rotation and passage-clearance checks |
| [p18-material-batch.png](p18-material-batch.png) | Cross-object materials for room wall sides/furniture parts |

## Previous update · 2026-10-26

Actual UI from isolated acceptance scenes, corresponding to New `35d29cd`. See [scope and verification](../docs/updates-2026-10-26.md).

| File | Content |
| --- | --- |
| [p13-room-net-lengths.png](p13-room-net-lengths.png) | Room-side net lengths alongside original centerline labels |
| [p13-solid-wall-lengths.png](p13-solid-wall-lengths.png) | Solid-wall segments excluding opening projections and areas requiring review |
| [p22-floor-occupancy.png](p22-floor-occupancy.png) | Element occupancy linked to paving/paveable area |
| [p25-opening-details.png](p25-opening-details.png) | Subdivisions, actual profiles and independent screens |
| [p25-bay-window.png](p25-bay-window.png) | Rectangular three-sided bay window |
| [p24-kitchen-cutouts.png](p24-kitchen-cutouts.png) | Blind-corner equipment and actual hole shapes |
| [p23-free-wall-panels.png](p23-free-wall-panels.png) | Free straight seams/simple polygon panels |

## Previous update · 2026-10-25

| File | Content | Scene type |
| --- | --- | --- |
| [opening-frame-fit.png](opening-frame-fit.png) | Reveal, fitted frame and 3D shortcut | Isolated acceptance scene |
| [opening-frame-fit-editor.png](opening-frame-fit-editor.png) | Frame depth/offset and fitted outer dimensions | Isolated acceptance scene |
| [wall-panel-opening-details.png](wall-panel-opening-details.png) | Per-opening edge material/upload and rectangular-dimension overrides | Isolated acceptance scene |
| [wall-panel-lines.png](wall-panel-lines.png) | Nonuniform horizontal/vertical rectangular panel divisions | Isolated acceptance scene |
| [upload-library.png](upload-library.png) | Uploaded-material names and entry management | Isolated acceptance scene |

Corresponds to New `3d812a2d9bc78b7e51271c6ae7f04357ea00ff1a`. Actual captures do not represent product installation details, construction drawings or a final interior design.

## Previous update · 2026-10-24

| File | Content | Scene type |
| --- | --- | --- |
| [herringbone.png](herringbone.png) | Herringbone, uploaded material and hidden board | Isolated acceptance scene |
| [herringbone-4k.jpg](herringbone-4k.jpg) | 3840 × 2160 JPG with selection hidden | Isolated acceptance scene |
| [floor-tiles-upload.png](floor-tiles-upload.png) | Per-piece uploads/textures and selection map | Isolated acceptance scene |
| [furniture-groups.png](furniture-groups.png) | Furniture group and 3D handles | Isolated acceptance scene |
| [furniture-groups-plan.png](furniture-groups-plan.png) | 2D group bounds and drag entry | Isolated acceptance scene |
| [wall-opening-surround.png](wall-opening-surround.png) | Top/right opening strips and per-opening switches | Isolated acceptance scene |

Corresponds to New 544714f145bec6094d7a9b3ed4ac20582f59d265. Blue boards use a project-created striped upload; gaps demonstrate hiding, not structural openings or a complete construction deliverable.

## Historical kitchen holes and floor laying · 2026-10-23

| File | Content | Scene type |
| --- | --- | --- |
| [kitchen-cutouts.png](kitchen-cutouts.png) | Equipment editing, rectangular holes, group binding and 2D settings | Isolated acceptance scene |
| [kitchen-cutouts-4k.jpg](kitchen-cutouts-4k.jpg) | Simplified sink/hob, continuous worktop and through-holes; 3840 × 2160 real-time image | Isolated acceptance scene |
| [floor-layout.png](floor-layout.png) | Floor origin, three patterns, piece size and layout mini view | Isolated acceptance scene |
| [floor-layout-4k.jpg](floor-layout-4k.jpg) | PBR floor clipped to room boundaries; 3840 × 2160 real-time image | Isolated acceptance scene |

Corresponds to New `a1407646daa384e1bc5c7f8650724208c2118d80`. Kitchen red boxes show existing collision aids; exported images hide helpers. These are not construction drawings or a finished interior.

## Historical unified workbench and L kitchens · 2026-10-23

| File | Content | Scene type |
| --- | --- | --- |
| [unified-workbench.png](unified-workbench.png) | Unified 3D workbench, shared tools/properties and furniture handles | Isolated acceptance scene |
| [unified-plan.png](unified-plan.png) | Unified 2D workbench and auxiliary views | Isolated acceptance scene |
| [l-kitchen.png](l-kitchen.png) | Independent left/right blind-corner L kitchens, continuous concave worktops and editor | Isolated acceptance scene |
| [l-kitchen-plan.png](l-kitchen-plan.png) | Six-vertex L-worktop contour in 2D | Isolated acceptance scene |
| [l-kitchen-narrow.png](l-kitchen-narrow.png) | Kitchen editor at 390 px | Isolated acceptance scene |

Corresponds to New `37c066b3becd011e96714efd648b8600e50aedc3` (including workbench commit `66c8761`). L-shaped red boxes show current-pose collision aids. These original acceptance screenshots do not represent a finished interior.

## Historical workflow foundations · 2026-10-23

| File | Content | Scene type |
| --- | --- | --- |
| [workflow-plan.png](workflow-plan.png) | Five detailing tool groups, ceiling properties and unified status | Isolated acceptance scene |
| [workflow-model.png](workflow-model.png) | 3D kitchen position/orientation and unified apply/cancel | Isolated acceptance scene |
| [workflow-model-narrow.png](workflow-model-narrow.png) | Kitchen properties and unified controls at 390 px | Isolated acceptance scene |

Corresponds to New `d89af66dd1e72552ac1a8f874389232fd6db75db`. Not a complete interior; that round still used separate 2D/3D containers, since replaced by the U03 unified workbench.

## Historical interior design · 2026-10-20

| File | Content | Scene type |
| --- | --- | --- |
| [seamed-wall-trim.png](seamed-wall-trim.png) | Regular seams/perimeter rectangular trim preserving windows | Feature demo |
| [structures.png](structures.png) | Single-floor columns, beams, flues and pipe enclosures | Feature demo |
| [wardrobe-open.png](wardrobe-open.png) | Wardrobe boards, compartments, doors and internal drawers | Feature demo |
| [straight-kitchen.png](straight-kitchen.png) | Straight base/wall cabinets and continuous independent-material worktop | Feature demo |

## Interior design and project management · 2026-10-19

| File | Content | Scene type |
| --- | --- | --- |
| [background-wall.png](background-wall.png) | Timber feature wall preserving an actual window opening | Feature demo |
| [slats-wall.png](slats-wall.png) | Vertical timber slat thickness and spacing | Feature demo |
| [projects.png](projects.png) | Project naming/search/thumbnails and autosave entry | Feature demo |

## Material library

![Overview of 160 materials](material-library.jpg)

## Real furniture models

![Five built-in CC0 furniture GLB previews](furniture-models.jpg)

See the [asset notice](../NOTICE.md) for external sources. This is a feature prototype; images do not represent complete construction plans or offline photorealistic rendering.

[Back to project home](../README.md)
