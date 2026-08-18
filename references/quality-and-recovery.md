# Inverted quality gate and recovery

Inspect the generated image itself. Success means controlled low production value,
not conventional visual polish.

## Hard pass criteria

- **Minimal anchor fidelity:** subject count/type, relationship, action verb,
  indispensable prop, and one or two color cues remain recognizable. Composition,
  crop, spacing, styling, makeup, costume construction, and exact pose may drift.
- **Fidelity ceiling:** fine faces, eyes, hair, hands, garments, and background are
  visibly simplified; a near-exact polished reproduction fails.
- **Coarse continuous characters:** characters use simple low-detail meshes with
  continuous shoulder, elbow, wrist, hip, knee and ankle volumes. Separated cylinders,
  insertion rings, sockets, hinges, ball joints, gaps, floating limbs, mannequin
  articulation and wooden-puppet seams fail. Under-refinement appears in proportions,
  silhouettes, pinched/stretched skin weights, intersections and rigging.
- **Internal primitive blockout:** simple primitives may guide construction, but body
  and garment parts merge into continuous readable volumes. Only regular accessories
  such as buns remain visibly primitive. Clay blobs and puppet assembly both fail.
- **Normal simplified clothing:** each garment preserves only a category/color hint and
  becomes one normal continuous garment mass or a few integrated pieces.
  Tailoring, lapels, plackets, sashes, trims, closures, layered hems, accurate sleeve
  shapes, natural folds, and source-specific costume silhouettes fail. Basic shoulder,
  underarm, sleeve, waist/hip and hem logic must remain. Barrel suits, tube costumes,
  detached sleeves and wooden-puppet shells fail. Stiff bad fit and local intersections remain.
- **First-year simplification:** every nonessential modeling, styling, composition,
  costume, background, and animation decision uses the fastest plausible beginner
  shortcut. Evidence of mature design judgment or selective polish fails.
- **Aesthetic failure:** source beauty, elegance, heroic bearing, cute facial design,
  and clean silhouette design do not survive. Faces use shallow human-like sockets,
  unequal drooping half-closed lids, small low/side pupils with unrelated targets,
  a wedge/button nose, a crooked mouth slit,
  and little cheek/lip shaping. Pretty, handsome, cute, alert, charismatic, or merely
  simplified-but-still-appealing characters fail.
- **Faceted textured environment:** background terrain, foliage, buildings, props,
  and surfaces remain visibly low-poly, primitive, sparse, and repeatedly reused.
  They use blurry repeated diffuse maps rather than clean solid colors.
- **Broken proportions:** human or animal head/body, limb, neck, torso, joint,
  muzzle, and paw/hoof ratios visibly depart from the source without changing the
  subject category or becoming horrific.
- **Suppressed animal musculature:** animals keep moderately low continuous geometry,
  but shoulder blades, chest/abdomen groups, haunch muscles, tendons and athletic limb
  taper are not readable. Barrel/ellipsoid torsos, uniform limbs and broad flat
  shoulder/hip transitions replace powerful or anatomy-study silhouettes.
- **Failed pose and rigging:** broad pose topology survives: who stands/sits, broad
  facing, the main acting limb, and prop ownership remain readable. Exact joint flow,
  balance, weight transfer, torso compensation, and contact become stiff, simplified,
  or wrong. The result corrupts the source blockout instead of inventing a newly
  choreographed expressive gesture.
  Two to four obvious bone/weight failures are readable at shoulders, elbows, wrists,
  pelvis, hips, knees, hands, sleeves, raised legs, or kneeling support.
- **No invented choreography:** degradation does not add waves, crouches, shy leans,
  heroic reaches, dance-like curves, flourishes, or theatrical reactions absent from
  the source. Such additions are polished character acting even when the pose is odd.
- **Visible collision failure:** when plausible contact or moving-joint zones exist, two to four
  local mesh intersections are visible around sleeves, elbows, shoulders, garments,
  hands, held props, fur, or adjacent bodies. Perfectly clean collision fails; facial
  occlusion, missing limbs, exposure, injury-like deformation, or universal clipping also fail.
- **Vacant failed gaze:** simple eyeballs sit mostly behind shallow sockets and thick
  eyelids. Upper lids droop half-closed at unequal heights; lower lids are weak; small
  pupils sit too low or sideways, convergence fails, and expressions look sleepy,
  delayed, and foolish. Exposed round cartoon balls, surprised wide whites, alert,
  cute, intelligent, or appealing eyes fail.
- **Texture poverty:** maps are visibly small, stretched, mirrored, tiled, and
  inconsistent in scale; surfaces are not clean premium PBR.
- **Material separation:** only polygonal hair/fur receives a cheap low-resolution
  baked fur bump made of clearly visible but still shallow short irregular tapered grooves and low soft
  ridges at medium uneven density. Marks follow loose body-region direction while bad
  UV rotation, mirroring, seams and stretching remain visible. They affect shading only,
  never silhouette. Holes, craters, long scratches, worms, leather, rock or real fibers fail.
  Flat solid-color diffuse must remain free of painted hair. Displacement, fiber
  roughness, fur geometry and silhouette fuzz fail. Material references must not alter content.
  Strands, shells, plush fibers, or groom effects fail. Clothing and non-fur surfaces
  remain visibly flat, smooth, low-resolution, and nearly bump-free; fabric relief fails.
- **Broken background mapping:** background diffuse maps use non-adaptive local XYZ
  coordinates. Tiling, seams, mirrored copies, inconsistent texel density, and scale
  distortion remain discoverable, with occasional Z-direction stretching on selected
  tall trees, posts, towers, or mountains. Enlarged tiles and limited hue/value offsets
  prevent a full-scene wallpaper effect. Correct world-scale mapping fails, but so
  does identical high-frequency repetition across every object.
- **Cheap tree construction:** where trees exist, foliage is built from three to six
  intersecting vertical ellipse cards around a crude trunk, with repeated low-resolution
  textures, visible intersections, jagged alpha edges, and weak fake depth. Solid
  detailed crowns, individual leaves, or refined foliage fail.
- **Conditional crude rain:** rain is absent unless source-evidenced or explicitly
  requested. When present, it consists of ugly white/pale-gray thin straight lines
  with little variation. Droplets, splashes, wet reflections, mist, or cinematic rain fail.
- **Clean color:** source-led hues remain clean, readable, and moderately saturated.
  Gray-brown grime, dirty overlays, global desaturation, crushed blacks, and uniformly
  flat color fail.
- **Asset poverty:** background and repeated objects visibly come from a very small
  reused library; detailed unique set dressing fails.
- **Flat failed lighting:** the sky/background behaves like a pasted image and does
  not provide coherent global illumination. One broad unshaped light gives subjects
  crude, nearly uniform brightness with basic shadows and little tonal modeling.
  Delicate gradients, attractive highlights, bounce, rim, or cinematic depth fail.
- **True reconstruction:** low quality comes from geometry, materials, repetition,
  lighting, and rendering—not only blur, noise, pixelation, or grading.
- **No invention:** add no unrequested subjects, props, horns, cow traits, captions,
  logos, interface, landmarks, or weather changes.

## Scored checks

Score each dimension 0–2. Accept at 22/28 or above only when all hard checks pass.

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| Broad anchors | lost | partly retained | clearly retained |
| Fidelity ceiling | too exact | mixed | detail clearly reduced |
| Character topology | refined or voxel/retro | mixed | uneven hand-built low-to-mid-poly errors |
| Proportions | source-faithful | mildly altered | visibly broken but readable |
| Pose/rigging | coordinated | partly stiff | 2–4 obvious bone/weight failures |
| Collision | perfectly clean or destructive | subtle/inconsistent | local readable clipping |
| Faces/gaze | alert/appealing | partly stiff | vacant, badly aimed, foolish |
| Textures | clean/unique | some roughness | small and repeated |
| Material split | bump everywhere, holes, or real fur | mixed | short uneven baked-fur strokes, flat clothing/background |
| Color | muddy/flat | mixed | clean source-led separation |
| Asset reuse | rich variety | some reuse | visibly limited library |
| Background | solid-color or wallpaper-heavy | partly textured | faceted, enlarged tiles, limited variation, occasional stretch |
| Lighting integration | coherent with sky | partly mismatched | clearly backdrop-disconnected |
| Capture restraint | gimmicky | some excess | secondary and subtle |

## Failure recovery

### Too faithful, attractive, or polished

Retry with: “Lock count/type, relationship, action verb, indispensable prop, one or two
color cues, broad scene order, and broad pose topology. Release exact crop, spacing,
joint angles, balance, styling, makeup, costume construction, attractive silhouette,
anatomy, and clean collision.
Discard fine likeness and reduce modeling competence, garment detail,
unique assets, and material coherence. Keep character faces sparsely modeled but
smooth-shaded, and keep the environment visibly faceted low-poly. Replace appealing
faces with recessed half-lidded human-like eyes, unequal openings, low/side pupils,
failed convergence, a wedge nose, crooked mouth slit, and almost no cheek/lip shaping.
Keep existing limb responsibilities and make their rigging fail without adding new acting.”

### Characters become refined, voxel-like, or retro-faceted

Retry with: “Use a smooth-shaded coarse continuous body mesh. Blend shoulders, elbows,
wrists, hips, knees and ankles into connected organic volumes. Remove cylinder ends,
rings, sockets, hinges, ball joints, gaps, floating parts and puppet seams. Keep
cheapness in proportions, pinched skin weights, intersections and rigging.”

### Clothing remains designed, tailored, layered, or professionally simulated

Retry with: “Keep only the garment's broad category and one color cue. Delete the
source tailoring, lapels, placket, sash structure, trims, closures, layers, accurate
sleeves, natural folds, and costume silhouette. Rebuild it as a normal continuous
garment mass with basic shoulder, underarm, sleeve, waist/hip and hem logic. Keep it
stiff, bump-free and badly fitted, but forbid barrels, tube suits and detached sleeves.”

### Result looks like clay or irregular polygon fitting

Retry with: “Use clean primitives only as an internal blockout. Buns and hidden eyeball
bases may remain spheres, but blend limbs, joints and garments into coarse continuous
volumes with no rings, sockets, gaps or puppet seams. Preserve bad proportions, pinched
weights and local intersections. Remove clay softness, fingerprints and kneaded lumps.”

### Proportions remain correct or flattering

Retry with: “Keep subject type, identity anchors, and semantic action, but release
the source silhouette. Deliberately mismatch head/body ratio, limb lengths, neck,
torso width, joint size, muzzle, paws/hooves, and animal body mass. Make assembled
parts awkward rather than elegantly caricatured.”

### Pose still looks natural

Retry with: “Preserve broad pose topology and limb responsibility but remove the
competent joint solution. Keep who stands/sits, broad facing, the main acting limb and
prop ownership. Do not add a new wave, crouch, lean, flourish or reaction. Remove
counter-pose and weight transfer, then add two to four visible failures: shoulder drags chest/collar, elbow
collapses or balloons, wrist twists entire forearm, hip fails to tilt pelvis, knee
pulls thigh/garment, hand follows wrong axis, sleeve lags/intersects, raised leg lacks
support compensation, or kneeling body floats without weight.”

### Pose becomes newly choreographed or expressive

Retry with: “Return to the source's broad pose blockout. Keep the same standing/sitting
roles, broad facing, acting limb, prop ownership and simple group relationship. Remove
all newly invented waves, crouches, shy leans, heroic reaches, dance-like curves,
flourishes and deliberate character acting. Make the existing pose fail through rigid
axes, missing torso compensation, bad weights and local clipping instead.”

### Garments and bodies remain collision-free

Retry with: “Add two to four local visible intersections at source-evidenced contact
or moving-joint zones: sleeve into elbow, upper arm through shoulder or garment, hand into sleeve or
held prop, garment into torso, fur into harness, or adjacent bodies slightly intersecting.
Keep faces and complete limbs visible; do not imply injury or expose the body.”

### Eyes still look intelligent, cute, or professionally animated

Retry with: “Make the eyes the main failure signal without exposed ball eyes. Recess
simple eyeballs behind shallow human-like sockets and thick flat lids. Droop the upper
lids half-closed at unequal heights, weaken the lower lids, place small pupils too low
or sideways, break convergence, keep sclera moderate, and create a sleepy delayed
vacant reaction. Keep it foolish and awkward, not grotesque.”

### Background is too detailed

Retry with: “Delete incidental set dressing. Keep only essential scene masses.
Rebuild them as visibly faceted low-poly primitives. Reuse two or three tree,
building, beam, post, or rock models many times with minimal variation. No smooth
high-detail environment, individually authored clutter, or atmospheric depth.”

### Background uses solid colors or correct texture scaling

Retry with: “Keep all background geometry and composition fixed. Replace clean solid
colors with a tiny library of enlarged blurry low-resolution diffuse tiles for trees,
grass, terrain, mountains, wood, rocks, and buildings. Use local object XYZ mapping
without world-scale normalization. Keep repetition noticeable but not wallpaper-like:
add small hue/value offsets, vary density between some copies, and apply Z stretching
only to selected tall objects. Do not add bump to the background.”

### Trees are too solid or detailed

Retry with: “Keep tree count and placement fixed. Replace each foliage crown with
three to six thin vertical ellipse cards intersecting around one crude trunk prism.
Reuse one or two enlarged blurry leaf textures; expose card crossings, repeated
silhouettes, jagged alpha edges, inconsistent opacity, and weak fake depth. No solid
canopy, individual leaves, procedural foliage, or refined billboard system.”

### Rain is invented or too realistic

If the source has no rain, remove it completely. If rain is source-evidenced, replace
it with sparse ugly white or pale-gray thin straight screen-facing lines of nearly
uniform length, width, direction, and opacity. Remove splashes, wet reflections,
droplets, mist, refraction, volumetric atmosphere, and cinematic motion blur.

### Textures are too clean or varied

Retry with: “Replace surfaces with tiny blurry diffuse maps. Make tiling, seams,
UV stretch, mirrored details, inconsistent scale, and reuse clearly visible.
Reuse the same map across multiple compatible objects.”

### Fur bump is absent, too strong, sophisticated, or clothing has bump

Retry with: “Remove strands, cards, shells, groom, plush fibers, and volumetric fur.
Use a plain polygonal hair/fur mass with a low-resolution baked bump map of short
irregular tapered shallow grooves and very low soft ridges at medium uneven density.
Give marks loose regional direction with bad UV rotation, mirroring, seams and stretch.
Keep strokes short, blurry, low-profile and shading-only. Remove holes, craters, long
scratches, worms, leather, rock and any real fiber or silhouette fuzz. Remove
all bump, weave, pits, and tactile relief from clothing and non-fur surfaces; make
garments smooth, flat, low-resolution, and cheaply diffuse.”

### Color becomes dirty, gray, or flat

Retry with: “Restore the source's clean large color blocks with moderate saturation
and readable separation. Remove gray-brown grime, dirty overlays, global desaturation,
crushed blacks, and uniformly flat color. Keep production flaws in modeling, rigging,
materials, and lighting rather than in a dirty grade.”

### Sky and foreground lighting integrate too well

Retry with: “Change lighting only. Treat the sky/background as a non-emissive pasted
image. Remove its global illumination, bounce, reflection, and color spill. Use one
broad unshaped neutral direct light with basic shadows and nearly uniform brightness.
Remove delicate gradients, facial modeling, attractive highlights, rim, and depth.”

### Result becomes dark, horrific, or grotesque

Restore source-led color and readable exposure. Keep awkward eyes and crude faces
within ordinary stylization. Remove horror grading, extreme distortion, deep black
voids, dramatic fog, and threatening light.

### Composition becomes unreadable

Restate only subject count/type, relationship, action verb, indispensable prop, and
very loose left/right or depth logic. Do not restore polished framing or source-accurate
spacing; allow a simpler beginner restage.

### Result looks like a filter

Say: “Rebuild every object as actual underbuilt 3D geometry. Make uneven hand-built
character topology, manual dents, lumpy joins, coarse continuous garments, fur-only bump,
faceted background assets, and crude lighting visible before adding capture noise.”

### Unwanted cows, horns, captions, or UI

Say: “The skill name is not a content instruction. Render only source-evidenced
content. Add no cows, horns, animal traits, meme text, subtitles, watermarks, logos,
HUD, or new props.”

## Retry discipline

1. Restate only minimal semantic anchors on every retry.
2. Change only the failed dimension. When the user names a local correction, use the
   latest approved image as the master and explicitly lock every unmentioned layer.
3. Prefer further simplification over restoring source composition or wardrobe fidelity.
4. Stop after two retries unless the user asks to continue.
5. Disclose remaining hard failures rather than calling the result successful.
