# OBDS

## My intel setup
- Set record dump folder
- if using flatpak
    - open flatseal allow to see *all libraries* and *devices*, allow *gpu acceleration*

### Encoder Selection
- Go to Settings > Output, set Output Mode to *Advanced*, and click the Recording tab. Choose this encoder:
    1. Primary Choice: `QuickSync H.264` (Best compatibility for editing)
    2. Secondary Choice: `QuickSync HEVC` (Better quality, but harder for some editors to play back)

### Recommended Recording Settings

| Setting | Recommended Value |
| -------------- | --------------- |
| Column1 | Column2 |
| Target Usage | Balanced (Safest for FPS) or Quality |
| Rate Control | CQP (Constant Quality) |
| CQ Level | 20 (Lower is higher quality; 20-23 is the sweet spot) |
| Keyframe Interval	 | 2s |
| Latency |	Normal |
| Profile |	high |



