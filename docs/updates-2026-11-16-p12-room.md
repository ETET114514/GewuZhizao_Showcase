# 2026-11-16 · P12 room finishes, live net dimensions and straight-wall junctions

**English** | [中文](updates-2026-11-16-p12-room.zh-CN.md)

[Source 65ad14a](https://github.com/ETET114514/GewuZhizaoNew/commit/65ad14a203f1e00fc7e36aebf07fda4530b349a2)

This batch connects whole-room planar finish boundaries for existing orthogonal, angled and arc walls, including holes and finish-thickness step connectors; P27 live horizontal/vertical interior net dimensions; and explicit common-support endpoint consolidation for 3–12 straight walls. JSON/SVG report the finish contour, while existing DXF/PDF/PNG drawing exports include the current linked P27 values. Finishes remain measurement policies rather than new finish solids.

Full P12 remains unfinished. Arc finish contours use at most 0.5 mm sagitta sampling; their perimeter is a sampled polygon length, distinct from the existing analytic single-wall along-path report. Whole-room contours are planar gross boundaries without opening or height-band deductions. P27 stores room identity, relative measurement-line position and interval intent; ambiguous room changes or interval-count changes become unresolved. Junction consolidation preserves original straight supports and allows 0–1000 mm endpoint movement, with at least 100 mm wall remaining; unsupported references, opening truncation and new overlap reject the complete edit. Curved/moving-support nodes, continuous variable thickness/height, unknown-reference reconstruction, arbitrary topology, full construction sections/details and unlimited report-external inference/global-optimum guarantees remain open.

Source validation on 2026-11-16: **1349 full Python tests** passed across all 181 modules in four independent processes; **753 full Node tests**, **66 final related Python tests**, **12 new Edge workflow groups** and **24 existing P12 browser groups** passed. Final related/browser checks also cover the last source-snapshot guard. Real save/reopen, live wall-edit identity migration, undo/redo, stale-source refusal and 390px were checked. Downloaded DXF/PDF were independently read back with the updated 3720 mm value; PNG is 1754 × 1240. Counts overlap and are not added. Showcase publication checks bilingual content, local links and image provenance without rerunning application tests.

[Source delivery details](https://github.com/ETET114514/GewuZhizaoNew/blob/65ad14a203f1e00fc7e36aebf07fda4530b349a2/P12_ROOM_FINISHES.md)
