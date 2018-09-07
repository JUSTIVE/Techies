# Real-Time Ray Tracing techiques for integration into existing renderers

## TAKHIRO HARADA, AMD - GDC2018

### Radeon's agenda

- Radeon Prorender
- Radeon Rays

### Radeon Prorender

- Heterogeneous device support
- No limit for the texture usage
- MacOS Metal API support
- Neseted Dielectrics
- More AOVs(angle of view)
  - Per BRDF AOVs(diffuse, reflect, refract, volume)
- Color LUTs
  - color correction using .cube file
- procedural UVs

#### Motivation

offline renderers | PRORENDER REAL-TIME RAY TRACING | GAME ENGINE Renderers
---|---|---
photo real | better quality | good quality  
long render time | adjustable computational cost | real time  
physically accurate | lerp(accurate, fake, on your flavor) | relaxed physically based  
 - | we take care the complexity in the api | fakes  
 - | add physically based effect on your raster renderer | -