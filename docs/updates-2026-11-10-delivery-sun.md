# 2026-11-10 · Delivery and geographic sunlight

**English** | [中文](updates-2026-11-10-delivery-sun.zh-CN.md)

Source: [0de6906](https://github.com/ETET114514/GewuZhizaoNew/commit/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458)

Project delivery now combines four recomputed schedules (room areas, furniture sizes/room assignment, openings and structural elements), searchable review lists, filtered CSV and offline HTML/JSON with a same-snapshot drawing/schedule ZIP. Drawing sets add optional project covers/directories; straight DXF dimensions can be native DIMENSION entities, retaining unit-aware numeric placeholders and graphic blocks. Geographic sunlight uses latitude/longitude, local date/time, an explicit UTC offset and drawing north, with 24 hourly samples, CSV/JSON records and preview/apply/cancel/history. Below-horizon direct sun is disabled.

Source updates since the previous showcase also include arbitrary-angle structural/member transforms, visible-dimension reference sheets/drawing sets, labor/custom-fee/tax quote sheets and a persistent local render gallery. See dated source records; these earlier subscope tests are not claimed as rerun by this showcase update.

Services snapshot the document under the state lock, then produce read-only reports/archives bound to a shared revision and SHA-256 manifests. Native CAD conversion applies only to valid linear measurements; PDF/PNG retain their existing static layout. Solar calculations run locally in Python; application recomputes angles server-side and persists validated solar inputs separately from rendered sunlight settings.

Restart the local service and refresh. Calibrate/open a synthetic project; File → drawing set enables cover/native DXF dimensions; File → project schedules filters/reviews/exports lists or the combined package. In 3D, Design tools → lighting → sunlight opens location/date calculation; choose an hour, preview, then apply or cancel. Use your actual north direction and explicit UTC offset; examples are not automatic geolocation.

These remain reference deliverables: exported CAD dimensions are not constrained to walls; arc/net conventions that differ from endpoint distance stay static. Schedules are not manufacturing/procurement BOMs or formal approvals. NOAA fractional-year solar positions are approximate geometric directions, without refraction/weather/timezone lookup or regulatory sunlight-duration/illuminance analysis. Ambient/HDRI/interior lighting remains separately controlled. No cloud collaboration or DWG completion is claimed.

Source-stage final evidence: **692 full Node tests and 75 related Python tests**, plus real Edge workflows, 390px checks and independent read-back of native DXF entities, ZIP hashes/shared revisions and downloaded solar CSV/JSON. Earlier stage counts overlap and are not added; no full Python rerun. Showcase publication checks documentation, relative links, bilingual navigation and image provenance, without rerunning application suites.

Four added PNGs are actual captures of isolated synthetic acceptance projects, shared by both languages. Source paths: wall-recognition/output/project-schedules/desktop.png, p27-drawing-cover/render-1.png, native-dimensions/desktop.png and solar-position/desktop.png. No customer drawings, full source, project/exchange packages, textures or model assets are copied. Existing asset licenses remain unchanged. Solar formula attribution: https://gml.noaa.gov/grad/solcalc/solareqns.PDF .

- [P19_GEOGRAPHIC_SUNLIGHT.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P19_GEOGRAPHIC_SUNLIGHT.md)
- [P27_NATIVE_DIMENSIONS.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P27_NATIVE_DIMENSIONS.md)
- [PROJECT_SCHEDULES.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/PROJECT_SCHEDULES.md)
- [P27_DRAWING_SETS.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P27_DRAWING_SETS.md)
- [P28_COMMERCIAL.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P28_COMMERCIAL.md)
- [P22_MIXED_ROTATION.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/P22_MIXED_ROTATION.md)
- [RENDER_STUDIO.md](https://github.com/ETET114514/GewuZhizaoNew/blob/0de69064f7a98e5cab7dd4db0e9707ab3a6ce458/RENDER_STUDIO.md)
