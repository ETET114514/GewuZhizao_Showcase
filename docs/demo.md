# Demo guide

**English** | [中文](demo.zh-CN.md)

Explore the project in the following order. All images come from the running interface or scene rendering; some 3D detail scenes demonstrate one specific feature.

2026-10-23: the top 2D/3D switch uses one workbench with five shared tool groups/property positions. 2D zoom/scroll and 3D camera state are retained separately. Preview changes, then use the bottom **Apply changes** (`应用修改`) or **Cancel preview** (`取消预览`). Esc cancels ordinary form drafts. Resolve unapplied changes before switching objects/tools. Expand auxiliary views for a small 3D preview or 2D camera map. UI labels below are translated for reference; screenshots retain the captured application interface.

![Unified workbench and canvas handles](../screenshots/unified-workbench.png)

## 1. Turn a floor plan into editable objects

Import an image and inspect numbered wall, opening and furniture candidates. Select objects on the plan and edit category, dimensions or orientation on the right. Add missing objects manually.

![2D recognition and review workbench](../screenshots/workbench.png)

Alternatively, start with a blank canvas or calibrate an image and trace continuous orthogonal walls. Edit physical length/thickness; connected walls update together when endpoints move. Diagonal/curved walls are not implemented.

## 2. Confirm scale, room boundaries and area

Calibrate with a known length, inspect/repair boundaries and generate or draw room regions. Areas derive from valid contours and scale; users still need to review automatic regions.

![Room regions and reference areas](../screenshots/floorplan-regions.png)

Under **Measure → Show wall lengths** (`测量 → 显示墙长`), switch between original centerlines, room-side net lengths and solid-wall net lengths, optionally filtering by room. Solid-wall measurements exclude horizontal projections of openings; unconfirmed openings withhold values. Enabling floor deductions on elements shows gross/deducted/paveable room area and restores paving after deletion or movement.

![Room-side net lengths](../screenshots/p13-room-net-lengths.png)

## 3. Adjust space and materials in 3D

Walls, openings, furniture and floors derive from editable data. Change views, move furniture and select a wall-side material, then preview/cancel/apply.

**Detailing → Finishes and structure → Batch materials · Room wall sides · GLB parts** (`做深化 → 硬装与结构 → 批量材质 · 房间墙侧 · GLB 部位`) lets you select locations and assign, replace by source material or restore. GLB parts support original UVs/physical projection and original-material restoration. Interior room sides clip to actual adjacency intervals; laid floors retain orientation/per-piece records. Multi-map PBR requires color; normal/roughness/metalness/AO are optional. Apply the project after import.

![Batch materials and room wall sides](../screenshots/p18-material-batch.png)

![3D wall material editing](../screenshots/material-editor.png)

Open **Detailing → Floor laying · Origin and pattern** (`做深化 → 地面铺贴 · 起点与铺法`), select a room floor and enable piece-based layout. Set straight/half-offset/third-offset or physical herringbone, piece width/length, origin, joint width/color and direction. Use the room bounds' upper-left or center as origin. Mini/2D/3D views clip to room boundaries and holes. Coverage dimensions continue to control texture scale; layout piece counts are not procurement quantities.

![Floor laying and layout mini view](../screenshots/floor-layout.png)

Ordinary material panels and **Individual floor pieces · Materials and hiding** (`地面逐块 · 换材质与隐藏`) accept PNG/JPG/WebP uploads, carried with the project after application. Select pieces in the main 2D canvas, mini view or 3D to change materials, hide or restore them. Herringbone offers a 15 × 60 cm / 45° example with textures following boards. Changing the grid clears old overrides; cancel/undo can restore them.

![Physical herringbone and individual-board editing](../screenshots/herringbone.png)

**Furniture groups · Group operations** (`家具成组 · 整组操作`) groups 2–40 objects for movement/rotation/copying. Drag the selected dashed bounds in 2D or use 3D handles. Ungrouping preserves furniture. **Multi-select · Mixed groups · Transport paths** (`多选 · 混合成组 · 搬运路径`) supports direct batch actions, mixed/nested groups, scaling and multi-segment path checks. Custom clearances are not a code-compliance review.

![Furniture group bounds in 2D](../screenshots/furniture-groups-plan.png)

## 4. Edit door and window operation

Hinged openings, double/unequal doors and dual-track sliding share editing/persistence. Here, a moving sliding leaf passes behind the fixed leaf to free roughly half the opening.

![Open dual-track sliding door](../screenshots/sliding-door.png)

Original horizontal 2–6-leaf windows and per-leaf operation remain available. A dedicated detailing entry now adds vertical subdivisions, mullions/transoms and screens.

Opening properties include **Subdivisions · Frame profiles · Screens · Bay windows** (`分格 · 框型 · 纱窗 · 飘窗`): per-cell operation, door transoms/sidelights, actual profiles and independent screens. Rectangular three-sided bays and explicit different-height shared frames have their own constraints.

![Opening detailing](../screenshots/p25-opening-details.png)

## 5. Detail walls and ceilings

Edit flat feature panels, vertical slats and room skirting: position, dimensions, thickness and materials. Finishes preserve actual door/window openings. Ceilings, dropped ceilings and coves also accept actual materials.

![Feature wall preserving a window opening](../screenshots/background-wall.png)

![Vertical timber slats](../screenshots/slats-wall.png)

Flat panels support regular seams. Both flat/slatted finishes accept perimeter rectangular trim and independent materials while preserving openings.

![Regular panels and perimeter trim](../screenshots/seamed-wall-trim.png)

Place single-floor columns, beams, flues and pipe enclosures in 2D and edit dimensions, height, elevation and materials. Optional floor-contact deductions affect paving/paveable area while preserving contours/regions and leaving the structural floor uncut. Flues/enclosures still represent external occupancy envelopes.

![Single-floor columns, beams, flues and pipe enclosures](../screenshots/structures.png)

Panel seams use wall-segment/floor positioning or nonuniform horizontal/vertical lines. Perimeter/opening edges have separate rectangular dimensions/materials; a specific opening inherits direction defaults. Enable reveals and set depth/board thickness; doors/full-height windows have no bottom strip. Select a 2D opening and expand **Frame · Depth and reveal fitting** (`门窗框 · 进深与包覆适配`), or use the 3D **Frame depth and reveal fitting** (`框进深与包覆适配`) shortcut to the same form, then preview/apply. The initial version covered ordinary single-leaf openings within one wall segment; special/irregular types and element-geometry integration were pending at that stage. Consult the current feature list for expanded fitting support.

![Opening surrounds and per-opening settings](../screenshots/wall-opening-surround.png)

![Nonuniform rectangular panel seams](../screenshots/wall-panel-lines.png)

![Opening reveal and fitted window frame](../screenshots/opening-frame-fit.png)

![Frame depth, offset and fitting properties](../screenshots/opening-frame-fit-editor.png)

The upload library supports search, renaming and deletion of unused entries, protecting saved/recovery/history references. Wall panels, elements, kitchen worktops and procedural furniture/custom cabinet parts have direct uploads. Five-map PBR, OpenGL/DirectX normals, batch naming/removal and unreferenced-cache checks/cleanup are now supported.

![Uploaded material library management](../screenshots/upload-library.png)

## 6. Design custom cabinetry and straight/L/U kitchens

Wardrobes/storage offer editable boards, compartments, shelves, rails, internal drawers and doors. Each compartment's doors/drawers operate independently and carry materials with them. Internal drawers require doors open to 90°; current poses participate in collision/walking.

![Wardrobe interior and operation](../screenshots/wardrobe-open.png)

Kitchen base/wall presets align same-type cabinets with matching depth/height/elevation in list order. The first cabinet anchors the run and orientation is orthogonal. Base cabinets can share one independent-material worktop with adjustable thickness/overhang. Moving one cabinet out of alignment pauses the worktop and requests realignment. Ungrouping preserves cabinets.

For an existing valid group, choose whole-group move/right-angle rotation or copy under **Operation** (`操作`). Enter the first cabinet center in X/Y centimeters and 0/90/180/270°, preview, then apply. Cabinets/worktops follow together; independent copies retain structure, materials and operation with new IDs. Bounds/budget failures leave no partial moves/copies; realign invalid groups first.

![Kitchen groups and unified editing](../screenshots/workflow-model.png)

![Base/wall cabinets and continuous worktop](../screenshots/straight-kitchen.png)

For an L-shaped kitchen, prepare main-run base cabinets, one left/right blind-corner cabinet and return cabinets. Add them in that order under **Kitchen groups · Straight/L worktops** (`厨房组合 · 直线 / L 形台面`). The corner cannot be first/last; depth/height/elevation must match. Applying creates a continuous L worktop. The blind panel is fixed while the operable zone retains compartments, doors and drawers. Numeric/canvas controls move, right-angle rotate and independently copy the group. One gesture is one undo step; Esc restores the prior state.

![Left/right blind-corner L kitchens and continuous worktops](../screenshots/l-kitchen.png)

Under **Sink/hob and holes** (`水槽 / 灶具与开孔`), add equipment to an ordinary base cabinet and set hole dimensions, lateral/front-back offsets and inset depth. Worktop/top-panel geometry avoids the hole; equipment follows group movement/rotation/copying. Conflicts with structure/drawer envelopes reject application; adjust compartments/shelves before previewing again.

![Kitchen holes and equipment editing](../screenshots/kitchen-cutouts.png)

Red boxes in the historical L-shaped screenshots are current-pose collision aids in an isolated scene. Equipment holes/group scope follow the latest update. Product equipment, further corner mechanisms, board schedules and custom drawings remain pending.

The current round supports L-shaped wall cabinets/U-shaped matching base/wall groups and continuous base worktops, circular/rounded holes, blind corners and equipment holes across two or three adjacent cabinets in a run. Holes around turns, further mechanisms and product equipment remain pending.

## 7. Inspect daylight and interior lighting

Adjust daylight direction, brightness and shadows, or edit fixtures, light groups and coves. Daylight direction is relative to the plan; coves use one diffuse-bounce approximation.

![Daylight and real-time shadows](../screenshots/design-result.png)

![Cove lighting and soft nearby-wall light](../screenshots/cove-lighting.png)

## 8. Save, recover and export images

Name projects and find them through thumbnails/search; undo/redo is supported. Every applied change autosaves locally and can recover after refresh/service restart. Unapplied forms are excluded; undo history restarts between sessions. Manual saves create independent versions.

![Project names, search and thumbnails](../screenshots/projects.png)

Save common camera positions as named views. JPG/PNG image output supports longest edges of 1920, 2560 or 3840 pixels.

The Showcase currently offers static screenshots; no demo video or public online trial has been published. Browsing this repository does not run the private application.

[Back to project home](../README.md)
