# 第四轮图片生成记录

日期：2026-10-02（Asia/Shanghai）。使用 OpenAI 内置 `image_gen`，未使用外部 CLI。实际图像模型版本未由响应明确提供，文件来源记为 imagegen。

两次调用均为不透明背景。第二次使用第一次 PNG 作为产品身份参考，非沿用旧方案图片。

## 01 / 完整外形

原始文件名：`exec-5b9b93cd-45cd-4f0a-a22e-b4d5c83ab55e.png`。PNG 保留在本次工具默认生成目录，项目不依赖该本机目录。

对应归档：[shelter-v04-exterior-concept-imagegen.webp](shelter-v04-exterior-concept-imagegen.webp)。

实际提示词：

```text
Use case: product-mockup
Asset type: new v04 modular stray-cat shelter exterior concept for a mechanical design project, landscape 3:2 image.
Primary request: show a structurally intelligible small single-cat semi-outdoor shelter built from segmented matte PETG printed hardware, simple warm architectural form, not a toy or injection molded one-piece box.
Subject and proportions: overall roof envelope approximately 600 mm wide x 520 mm deep x 550 mm high. Body approximately 520 x 440 mm. Four low printed feet lift the base 60 mm above ground. A shallow symmetric pitched roof, approximately 16 degrees each slope, ridge along front-to-back direction, no cat ears. Warm ivory rectangular body, subdued sage-gray roof and frame, rounded safe edges, fine believable printed layer texture.
Construction: walls have deliberate 2 columns x 2 rows of small panels per side, smooth inset seams with thin upright corner channels, no exposed puzzle teeth. Roof has FOUR clearly recognizable panels, two on each slope split front/rear, with a narrow printed ridge cap and narrow seam-cover strips over the front/rear joints. These panels fit a roughly 330 x 300 mm print allowance when appropriately oriented. Printed broad support rails carry the panels; small rectangular wedge retainers only prevent withdrawal. NO screws, rivets, metal hinges, twist lock knobs, or decorative hardware. No false claim of manufacturability.
Entry/layout: a modest 160 mm wide x 190 mm high rounded arch opening offset to the LEFT on the FRONT face, raised slightly above the internal floor, with a short discreet canopy. The opening is empty and dark enough to see a short internal wind-turn baffle just to its right without closing off the passage. A large quiet sleeping area lies beyond and to the right; nothing stored outside. No exterior feeding bowls.
Maintenance: entire assembled roof can be lifted off; use discreet finger pockets under the roof overhang instead of hinges. A tiny blank sage identification plate on the front right, NO lettering. NO front drawer: internal liner tiles are removed upward after roof removal.
Composition: one three-quarter front-right perspective showing FRONT opening and RIGHT wall, entire shelter with good margins, approximately 75% image width. Place on neutral pale paving under a plain wall eave, subtle shadow, minimal context, no plants obstructing structure, no cats and no people. Elegant restrained industrial-design visualization with soft natural daylight, crisp modular seams visible, not a diagram collage.
Constraints: no text, no labels, no logos, no watermarks. Exactly one shelter. This is an unverified concept rendering, not an engineering drawing.
```

## 02 / 开顶维护

原始文件名：`exec-a36586d1-baf8-4cec-b563-ebc7e01ab8ec.png`。PNG 保留在本次工具默认生成目录。

对应归档：[shelter-v04-maintenance-concept-imagegen.webp](shelter-v04-maintenance-concept-imagegen.webp)。

引用图片：01 的原始 PNG，以本地路径传入 `referenced_image_paths`。实际提示词：

```text
Use case: precise-object-edit
Asset type: matching v04 modular single-cat shelter top-cleaning concept, landscape 3:2 engineering product visualization.
Input image 1: reference for product identity, exterior shape, panel construction, exact sage gray/ivory material palette; transform the assembly into a maintenance exploded view.
Primary request: show the SAME shelter in a clear studio three-quarter front-right raised viewpoint, with the roof assembly lifted straight upward and internal four shallow liner tiles visible, explaining top-access cleaning.
Keep the body, offset LEFT front arched entrance, four feet, 2 x 2 wall panels, sage frame, four-panel symmetric pitched roof and roof seam cover strips consistent with reference. Remove the exterior background and use clean warm off-white studio floor/backdrop, soft shadows. No metal hardware.
Composition: the house body stays at the bottom center, the COMPLETE assembled roof is hovering above it with a 130 mm air gap, without moving sideways. The camera is high enough to look down into the open interior without changing the object's proportions. No duplicated roofs and no detached walls. The four rectangular shallow ivory/sand liner tiles form a TWO by TWO grid across the interior floor. ONE front-right tile is lifted straight up about 60 mm to show independent tile removal; the other THREE remain supported in their floor positions. Tray tiles roughly 225 x 190 mm each, short rounded lips and two recessed finger grips, not a single large drawer and not free-floating with no bottom support. A removable short vertical sage wind baffle just inside and to the right of the LEFT entrance extends only 130 mm inward, then stops to leave a broad unobstructed route around it into the RIGHT sleeping area. Insulation stays behind smooth inner panels; no exposed foam for cats. Show roof support perimeter rails and simple blank wedge retaining locations. Do not show detailed fabricated joints, screws, rivets or hinges.
Style: clear attractive 3D industrial-design concept rendering, credible matte printed PETG texture, restrained modular seams. The first image's overall form must be preserved; no cat-shaped decorations, no pets, no people, no bowls, no bedding to conceal liner tile grid. Entire roof and all feet inside frame with ample margin.
Constraints: no text, labels, arrows, dimensions, logos or watermark. This is an unverified visual concept, not a proven mechanical assembly.
```

## 图片归档

两张原图均为 1536 × 1024。用 FFmpeg 8.1.1 / libwebp，quality 85、compression_level 6 转换为同分辨率有损 WebP；不覆盖 PNG 原件。两张查看版合计 226,146 字节，约 221 KiB。

| 文件 | 字节数 | SHA-256 |
| --- | --- | --- |
| 原始 exterior PNG | 2,312,289 | `95175cd810138de8674344ad0f8802f1a40671e5bba15fa083a6daedec471460` |
| 原始 maintenance PNG | 1,965,791 | `00f6b42a135a931fc340c7f3ba6c7bb86cb7079d271b520b1794d5e47d5c2a63` |
| exterior WebP | 147,108 | `f0f2d4cf52778c8a013fb23b50306847772cdf3e446a663c409e612178c52b06` |
| maintenance WebP | 79,038 | `2918c0e20ac9a853d8451e1e7b79e79712e071c90c5cd0aab8e0d39c8aaeb320` |
