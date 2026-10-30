# 2026-10-30 · Design workflow checkpoint

**English** | [中文](updates-2026-10-30-design.zh-CN.md)

Source [0f28b3e](https://github.com/ETET114514/GewuZhizaoNew/commit/0f28b3e043333f733bcf8c89ca6fc11f0b6eb1cf). This follows the earlier same-day CAD checkpoint; its historical evidence remains unchanged.

## Delivered

- P15 wall heights, physical splits and angled/arc wall authoring with basic hosted openings, opening-aware meshes, rooms/materials and project reuse.
- P26 entry-interior → living → selected rooms through actual door passages, manual waypoints, finite obstacle avoidance, room looks/pauses and temporary open-door restoration. Silent 1280×720 WebM recording/preview/download; 2K/4K equirectangular JPG/PNG. The visible shortcut and re-entry behavior preserve drafts.
- P27 interior region scans and door/window positioning; associated/fixed aligned/horizontal/vertical custom lines, units/offsets/visibility/edit/delete, current geometry/scale updates and split-anchor migration. Missing hosts do not retain numeric measurements.
- P28 current-model reference quantities, alternative cabinet projection/rectangular-board-area/per-item pricing, rate/loss/inclusion settings, incomplete-row status, reference totals and quote/board CSV.

## Verification

Latest: **555 frontend tests**; **79 related Python checks plus 4 final overlapping rechecks**; **18 main and 6 opening-dimension browser checks**, plus original P13 wall-length acceptance. Rechecks cover no-change redo preservation, ZIP migration and the 200-line budget; browser checks cover pointers, preview/cancel, missing/split hosts, scale changes, save/reopen and 390 px.

Earlier dated snapshots: P15 800 Python / 44 targeted rechecks / 523 frontend / 21 new browser groups plus height/split regressions; P26 549 frontend / 30 targeted Python / 19 guided-tour browser groups plus tour/panorama regressions; P28 532 frontend / 22 targeted Python / 15 browser groups. Overlapping groups are not summed; no new full Python suite is claimed at publication.

## Remaining scope

Full CAD constraints and specialized curved-wall detailing; multilevel tours, exterior arrival/opening animations, narration/MP4/hotspots/GPano/shared web; finish-surface/level/elevation/section/full construction delivery; manufacturing/procurement BOM/nesting/hardware/formal labor/tax/contract quotes remain separate. Complex cabinet boards pause board-area pricing. DWG and independent real-data recognition validation remain open.

[Home](../README.md) · [Features](features.md) · [Demo](demo.md) · [Screenshots](../screenshots/README.md)
