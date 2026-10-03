# Complementary "Vibrant" settings

Settings presets for Complementary Reimagined and Unbound r5.9.3, each with and without Euphoria Patches 1.10.5. They aim for a vibrant, trailer-style look: saturated colors, pixelated shadows, a little fog, strong god rays, reflections, colored lighting and glowing ores. They're tuned for a high-end PC.

| File | Shader pack |
|---|---|
| `ComplementaryReimagined_r5.9.3.zip.txt` | Reimagined |
| `ComplementaryUnbound_r5.9.3.zip.txt` | Unbound |
| `ComplementaryReimagined_r5.9.3 + EuphoriaPatches_1.10.5.txt` | Reimagined + Euphoria Patches |
| `ComplementaryUnbound_r5.9.3 + EuphoriaPatches_1.10.5.txt` | Unbound + Euphoria Patches |

Every option name and value was checked against the real r5.9.3 and Euphoria 1.10.5 shader code.

## Install

1. Close Minecraft, or at least leave the shader menu.
2. Copy the files into `.minecraft/shaderpacks/`. Each one replaces the `.txt` already there with the same name.
3. Each file's name must be the shader pack's name plus `.txt`. If your pack file or folder is named differently, rename the settings file to match.
4. Open the game and select the shader. Iris will rewrite the file in its own format, which is expected.

## What it changes

- **Pixelated shadows, block light and AO** at 1x scale (one shadow pixel per texture pixel), with a 4096 shadow map and 256-block shadow distance.
- **Colors:** higher saturation, vibrance and contrast, with less washed-out darks.
- **Fog and sky:** light atmospheric fog, stronger sunrise/noon god rays, cloud shadows, more stars, night nebulae and a sun lens flare. Reimagined also gets the second cloud layer.
- **Reflections:** world-space reflections with Advanced Color Tracing (512), full-resolution reflections, high block reflections and rain puddles.
- **Glowing:** all ores (1.2x), amethyst, glow lichen, redstone/lapis blocks and armor trims. Ores also cast colored light.
- **Materials:** Integrated PBR+ with generated normals and coated textures. Reimagined uses its "Reimagined + Waves" water.
- **Euphoria only:** screen-space colored light, normal-mapped block light, raw-ore and emerald blocks, enchanting table and nether wart glow, faint glowing flowers at night or in rain, better lava, double/high-quality clouds, shooting and twinkling stars, interactive foliage, and Nether and End effects.

## If it runs slowly

Change these first, one at a time:

1. `COLORED_LIGHTING` 512 → 256, or 0 to turn it off (this also turns off world-space reflections and lava edges).
2. `DOUBLE_UNBOUND_CLOUDS` / `HIGH_QUALITY_CLOUDS` → false (Euphoria only).
3. `MCBL_MAIN_DEFINE` 2 → 0 (Euphoria only).
4. `LIGHTSHAFT_QUALI_DEFINE` 4 → 3, `DETAIL_QUALITY` 4 → 3, `REFLECTION_RES` 1.0 → 0.5.
5. `shadowDistance` 256.0 → 192.0.

## Taste tweaks

- **More or less fog:** `ATM_FOG_MULT` (0.50 / 0.65 / 0.80 / 0.95).
- **Even more color:** raise `T_SATURATION` / `T_VIBRANCE` in 0.05 steps.
- **Chunkier pixel shadows:** `PIXEL_SCALE=-1` (0.5x). **Finer:** `PIXEL_SCALE=2`.
- **No glowing flowers:** `EMISSIVE_FLOWERS=0`.
- **Ores glow only in caves and at night:** add `SITUATIONAL_ORES=true` (Euphoria).
- **Pixel-art water (Euphoria):** `PIXEL_WATER=1` and `PIXELATED_WATER_REFLECTIONS=true`.
