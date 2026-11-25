# 出图提示词 · 英文模板（国际平台）

> 读这一份的时机：要在 Midjourney / DALL·E / SD 等英文平台上出图，需要七段骨架与中英关键词对照时读这一份。
>
> 不在这里的内容：中文场景模板在 `prompt-scenes.md`；参数与负面词原则在 `prompt-core.md`。

## 本篇目录

- 七段骨架（按顺序写）
- 关键词对照表
- 三条模板

---

## 英文提示词（国际平台）

> 边界：本节是把中文模板的**结构**翻成英文，方便 Midjourney / 国际版即梦这类平台使用。**没有在国际平台实测过**——结构可靠，措辞可能要按平台微调。国内平台仍用上面的中文模板，不要混用。
> 一条实用提醒：英文提示词里**不要夹中文关键词**，模型可能把汉字当"要渲染的文字"画出来。

### 七段骨架（按顺序写）

1. **主体**：`seamless textile pattern` / `single motif` / `fabric close-up`
2. **母题与单元**：`lotus and scrolling vine, one bloom + two leaves + one bud per unit`
3. **骨格与重复**：`half-drop repeat, offset by half a unit` / `brick repeat` / `radial rosette`
4. **线**：`even-width contour line (iron-wire), closed contours, no gaps`
5. **配色**：`Dunhuang mineral palette: terracotta red, azurite blue, malachite green, warm gold on pale cream`
6. **成色方式**：`flat color fill, no shading, no gradient`
7. **投影与负面**：`flat orthographic view, no perspective, no shadow` + negative list

### 关键词对照表

| 中文 | 英文 |
|---|---|
| 四方连续 | seamless repeating pattern / tileable / half-drop repeat / brick repeat |
| 二方连续 | horizontal repeating border / band pattern |
| 单独纹样 | single motif / standalone motif |
| 适合纹样 | motif fitted in a shape（roundel / square / diamond） |
| 骨格 | structural skeleton / repeat structure |
| 错位半个 | offset by half a unit (half-drop) |
| 单位 / 单元 | repeating unit / tile |
| 密度（疏 / 中 / 密） | low / medium / high density |
| 铁线描 | even-width contour line (iron-wire line) |
| 游丝描 | fine hairline contour |
| 兰叶描 | tapered, variable-width line |
| 闭合完整 | closed contours, no gaps, no open outlines |
| 平涂设色 | flat color fill, no shading |
| 平面正投影 | flat orthographic view, no perspective |
| 无灰阶 | no grayscale, pure black and white |
| 织纹 / 提花 | visible weave / jacquard woven-in pattern |
| 刺绣 | embroidery, visible stitch texture |
| 扎染 | resist-dyed, irregular dye edges |
| 肌理特写 | fabric close-up, macro shot |

### 三条模板

**① 线稿（四方连续）**

```
seamless repeating textile pattern, line art only, black and white;
motif: lotus with scrolling vine skeleton, one bloom + two leaves + one bud per repeating unit;
skeleton: S-curve vine, motifs offset by half a unit (half-drop repeat);
line: even-width contour line (iron-wire), three line weights — main motif thicker, secondary medium, ground pattern finest;
closed contours, no gaps, no open outlines, every stroke joined end to end;
all four edges continuous and tileable, no half motifs at the edges;
full coverage, no large blank areas;
flat orthographic view, no perspective, no shadow;
pure white background.
```

Negative: `grayscale, halftone dots, gradient, broken lines, open contours, single uniform line weight, 3D shading, perspective distortion, random arrangement, inconsistent repeat, half motif at seams, text, watermark`

**② 上色（结构锁定）**

```
colorize the provided line art, keep the exact same composition, unit positions and line structure;
do not add, remove or move any element; do not change any line weight or line position;
Dunhuang mineral palette: terracotta red, azurite blue, malachite green, warm gold, pale cream ground;
flat color fill with light layering, no shading, no highlights, no volume;
dominant colors in solid areas, not scattered;
edges remain seamless and tileable;
flat orthographic view, no fabric texture.
```

Negative: `added elements, missing elements, shifted structure, shading, highlights, volume, fabric texture, gradient`

**③ 肌理特写**

```
fabric close-up, macro shot; jacquard woven pattern, visible weave structure;
motif edges stepped along warp and weft, not smooth curves;
silk satin sheen, soft specular highlight following the folds;
neutral lighting, flat lay, no perspective.
```

Negative: `printed look, flat graphic, plastic sheen, oversaturated, logo, text`

> 用法：把上面的母题、骨格、配色三处替换成自己的参数即可，其余结构不动。中文模板里的"骨格点 / 错位量 / 环绕方式"三格在英文里分别对应 `repeat structure`、`offset ratio`、`radial rings`。
