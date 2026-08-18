---
name: niu-lai-translator
description: >-
  Reconstructs any supplied image as exaggeratedly cheap, badly produced bootleg CGI:
  coarse continuous low-detail character meshes with visually smooth simplified surfaces, visibly
  faceted low-poly backgrounds, distorted proportions, vacant misdirected eyes,
  simplified continuous anatomy, obvious bone-weight failures, local clipping,
  crude low-resolution baked short-fur bump strokes,
  moderately repeated background textures with occasional axis stretching, reused assets,
  flat cheap lighting, and clean source-led color while
  preserving only minimal semantic anchors while freely simplifying composition and styling.
  Use when users invoke 牛来粗制 CGI 转译, 牛来低模转译,
  niu-lai-translator, 反向出圈画质, 低画质重制, 粗制 CGI, 粗糙人物低模, 早期 3D 游戏截图,
  crude CGI, bootleg CGI, or ask to make an image look intentionally
  cheap, awkward, poorly modeled, poorly lit, and less faithfully reproduced.
---

# Niu Lai Translator / 牛来粗制 CGI 转译器

> Core principle: **保留大关系，主动放弃精致还原；让低质量来自各生产环节彼此失调，而不是后期滤镜或低模风格。**

Rebuild the source as a scene made by a sincere but technically limited early-3D
team. Keep the image readable and structurally related to the source while making
modeling, proportions, rigging, collision, materials, assets, lighting, and rendering
visibly fail. Character meshes remain far below refined animation quality, but their
character surfaces must read as continuous simplified anatomy rather than separated
primitive segments. Low quality comes from crude proportions, stiff silhouette, poor
fitting, bad deformation and rigging—not puppet joints. The background may remain plainly faceted low-poly.

## Workflow

Track this sequence:

```text
- [ ] 1. Confirm that an input image exists; request one if absent
- [ ] 2. Read explicit parameters and infer the rest from the bootleg-CGI defaults
- [ ] 3. Extract minimal anchors: subject count/type, relationship, action verb, one or two color cues
- [ ] 4. Release exact anatomy, proportions, joint angles, surface quality, and collision fidelity
- [ ] 5. Build one source-based image-edit prompt in the required order
- [ ] 6. Generate/edit unless the user asked for prompts or options only
- [ ] 7. Inspect against the inverted quality gate; retry polished results
- [ ] 8. Return the image plus one compact treatment note
```

## Interaction

- Require an input image unless the user explicitly asks for a new scene.
- Execute directly when an image is supplied without parameters or the user says
  “默认”, “你来判断”, or equivalent.
- If the user says “先别生成”, “给方案”, or “让我选”, do not generate. Offer at
  most three distinct directions.
- Ask at most one question only when a missing decision materially changes output.
- Use an image-edit tool that receives the source image. Include every target image
  through the tool's supported reference input.
- Treat this as reconstruction, not compression, pixelation, faceting, or a low-poly overlay.
- Treat explicit follow-up scope as a hard edit mask. If the user says to change only
  eyes, trees, fur, lighting, pose, or another named dimension, use the latest approved
  image as the master and lock every unmentioned subject, pose, proportion, material,
  composition, asset, color, and lighting decision. Do not use a local correction as
  permission to rebuild or beautify the rest of the image.

## Analyze minimal anchors internally

Identify without reporting every item unless asked:

- **Subjects:** count, broad type, relationship, role, action verb, and indispensable prop.
- **Broad blocking:** retain left/right or depth order, standing/sitting roles, the main
  acting limb, and indispensable contacts. Crop, camera height, exact spacing, relative
  scale, exact joint angles, and attractive silhouette may change.
- **Scene:** only the major terrain, architecture, or stage masses required for
  the image to remain recognizable.
- **Color cues:** retain one or two dominant source colors; exact costume distribution may change.
- **Deliberately mutable structure:** limb length, head/body ratio, torso width,
  animal proportions, exact joint angles, balance, silhouette accuracy, garment fit,
  and clean separation between intersecting meshes.
- **Discardable detail:** fine facial likeness, subtle expression, hair strands,
  embroidery, microtexture, unique background assets, small signage, and decoration.

## Use bootleg-CGI defaults

Use `crude_bootleg_cgi` unless the user requests a gentler translation. Read
[references/style-system.md](references/style-system.md) when selecting another preset.

```yaml
preset: crude_bootleg_cgi
reconstruction_strength: extreme
anchor_lock: minimal_semantic
composition_lock: broad_blocking
identity_lock: low_to_medium
detail_budget: low
skill_level_reference: one_year_animation_student
simplification_policy: simplify_everything_nonessential
geometry: coarse_continuous_character_mesh
mesh_detail_budget: low_to_medium
animal_mesh_detail: moderately_reduced_not_extreme
animal_muscle_definition: suppressed_flattened
animal_body_forms: simple_barrel_torso_uniform_limbs
surface_smoothing: continuous_shading_without_visible_character_facets
primitive_abstraction: simple_forms_blended_into_continuous_body
joint_construction: continuous_anatomical_mass_no_puppet_seams
clothing_geometry: simplified_continuous_garments
wardrobe_fidelity: category_and_color_hint_only
styling_fidelity: deliberately_broken
manual_modeling_artifacts: heavy
aesthetic_failure: severe_unattractive_amateur_character_design
face_construction: pasted_primitive_features
eye_style: humanlike_half_lidded_unfocused
background_geometry: visibly_faceted_low_poly
face_geometry: clumsy_asymmetric
gaze_quality: vacant_badly_aimed
proportion_fidelity: deliberately_broken
pose_lock: broad_pose_topology
pose_quality: source_blockout_failed_rig
rig_failure_strength: obvious
bone_weight_errors: 2_to_4_major_joints
collision_quality: visible_clipping
clipping_count: 2_to_4
texture_resolution: low
material_model: flat_diffuse_with_fur_bump
surface_relief_scope: fur_and_hair_only
bump_scale: short_irregular_baked_fur_strokes_only
fur_bump_depth: shallow_visible_controlled
fur_bump_density: medium_uneven
fur_bump_shape: short_tapered_grooves_and_soft_ridges
fur_surface_target: cheap_lowres_baked_fur_normal
fur_uv_behavior: locally_directional_with_bad_stretch
fur_representation: bump_normal_only_fake_no_hair_geometry
fur_diffuse: flat_solid_color_without_drawn_hairs
fur_silhouette: unchanged_solid_mesh
material_reference_scope: texture_pattern_only_never_content
texture_repetition: noticeable
asset_reuse: heavy
background_detail: sparse
background_texture: lowres_repeated_diffuse
background_uv_mapping: nonadaptive_local_xyz
background_texture_scale: enlarged_tiles
background_texture_variation: limited_hue_value_offsets
background_uv_distortion: occasional_z_stretch
tree_construction: crossed_vertical_ellipse_cards
rain_style: source_only_white_line_streaks
palette: source_anchored_clean
color_cleanliness: clean_not_muddy
lighting: flat_unskilled_single_light
environment_lighting_link: disconnected
sky_behavior: pasted_backdrop_no_gi
post_effects: subtle_capture_noise
text_mode: none
ratio: source_ratio
```

These are intentional defaults. Correct anatomy, natural poses, perfectly clean
collision in contact-rich scenes, coherent PBR materials, high facial fidelity,
rich backgrounds, unique textures, attractive eyes, muddy color grading, or lighting
that correctly inherits the sky are failures unless requested.

## Preserve only minimal meaning

- Strictly preserve subject count/type, relationship, action verb, indispensable prop,
  one or two color cues, broad left/right or depth order, and broad pose topology: who
  stands or sits, which limb performs the main action, and which subject contacts a prop
  or another subject. Crop, camera refinement, exact spacing, exact joint angles,
  costume design, makeup, styling, and attractive silhouette may be simplified.
- Preserve the source pose only as a crude blockout, then make its execution fail. A
  wave remains the same arm's wave and a held prop remains in the same subject's hand,
  but elbows, shoulders, wrists, knees, weight, balance, contact and torso compensation
  become stiff, simplified, and wrong. Do not invent a new wave, crouch, lean, flourish,
  or expressive reaction merely to prove that the pose changed.
- Preserve only broad identity anchors such as species/age category, one hair cue,
  one outfit color, and subject role. Garment construction, makeup, ornaments, exact
  hair design, source silhouette, and body proportions are disposable.
- Deliberately change human and animal proportions. Use mismatched limb lengths,
  oversized or undersized heads, short rigid necks, broad or pinched torsos, chunky
  joints, crude paws/hooves, or uneven body masses. Keep subjects recognizable and
  non-horrific; do not change a real person's apparent age, ethnicity, or body category.
- Introduce two to four readable collision failures when people, animals, clothing,
  or props make contact: sleeves may sink into elbows, upper arms may cut through
  shoulders or loose clothing, hands may intersect sleeves or held objects, and fur
  or garments may penetrate nearby meshes. Do not hide faces, erase whole limbs,
  imply injury, expose the body, or turn every contact into clipping.
- Raise `identity_lock` to `high` only when the user requests likeness or the task
  is identity-sensitive; reduce reconstruction strength if necessary.
- Do not change a real person's apparent age, ethnicity, body category, or
  relationship to others merely to create the style.
- Add no people, animals, horns, cow traits, weapons, props, logos, subtitles,
  interface, meme text, landmarks, or weather not evidenced by the source.

## Rebuild all production layers

Apply all layers together:

1. **Modeling:** build each character as a coarse but continuous low-detail mesh, using
   enough geometry and smooth shading that faces, limbs, clothes, and joint transitions
   do not show polygon fields or separate toy parts. Simple forms may guide construction,
   but blend them into one readable body volume. Shoulders flow into upper arms; elbows
   and knees remain continuous narrowed bends; wrists and ankles connect without rings,
   sockets, gaps, detached cylinders, or visible insertion seams. Keep anatomy generic,
   stiff, asymmetrical, and poorly proportioned, but not mechanical or mannequin-like.
   Hair buns may remain spheres and eyeballs may use hidden spheres behind crude lids.
   Put failures in silhouette, proportions, bad skin weights, pinching, stretching,
   intersections, and pose—not in all-over faceting, puppet assembly, clay lumps, or
   disconnected parts.
   For animals, reduce geometry only slightly but suppress anatomical muscle design:
   remove readable shoulder blades, pectoral divisions, rib/abdomen planes, haunch
   muscles, tendons, and athletic limb taper. Use a more uniform barrel/ellipsoid torso
   and simpler limbs with fewer thickness changes. Shoulders and hips remain continuous
   but broad, flat, and poorly resolved. The animal must not look muscular, powerful,
   athletic, or like a low-poly anatomy study.
   Background terrain, foliage, buildings, props, and architecture remain visibly faceted low-poly.
2. **Normal continuous clothing simplification:** do not reconstruct source tailoring,
   but preserve a believable basic garment relationship to the body.
   Preserve at most a broad category and one color cue, such as “red short outfit” or
   “white long garment.” Merge top, collar, placket, belt, sash, skirt, sleeves, trousers,
   cuffs, and decorative layers into one simplified garment or a few continuous pieces.
   Retain a basic shoulder line, armhole/underarm transition, sleeve-to-arm continuity,
   waist/hip volume, and a plausible opening or hem where the garment category needs it.
   Delete embroidery, trim, elaborate lapels, fine folds, closures, layered
   hems, accurate sleeve shapes, tailoring, and costume-specific silhouette. A shirt may
   become one crude T-shirt-like mass; trousers become a simple continuous pelvis with
   two legs; a robe becomes one plain long garment mass with integrated sleeves. Prefer
   the fastest beginner shortcut over faithful reconstruction, but never turn clothing
   into a rigid barrel, bucket, tube suit, detached sleeve system, or wooden-puppet shell.
   Keep it bump-free, stiff, poorly fitted, with only local body intersections.
3. **Immediate design reset:** before modeling details, break the source composition,
   styling, makeup, costume design, attractive silhouette, and pose solution. Restage
   spacing and overlap loosely if that makes the scene simpler. Actively remove attractiveness, elegance, heroic
   bearing, clean silhouette design, and appealing facial anatomy. Build the face as
   poorly resolved parts: flattened human-like eye openings, heavy half-closed upper
   lids, unequal eyelid heights, small pupils aimed at unrelated targets, a wedge or
   button nose, a crooked mouth slit,
   and nearly absent cheek/lip shaping. Do not merely simplify a beautiful source face;
   replace its aesthetic logic with a clumsy generic amateur face while preserving
   only broad identity anchors such as age category, one hair cue, one outfit color,
   and subject role. Makeup, hair ornaments, garment construction, and styling details
   are disposable. The result should look blank, foolish, confused, and
   unintentionally comic rather than cute, handsome, elegant, or fashionably stylized.
4. **Proportions:** break source-faithful anatomy while keeping subject category and
   action readable. Prefer visibly mismatched assembled parts over elegant caricature.
5. **Pose and rigging:** preserve broad pose topology and limb responsibility while
   discarding the source's competent joint solution. Use the source stance as a crude
   blockout: keep who stands/sits, the main acting limb, held-prop ownership, and broad
   facing direction, then remove the force chain, counterbalance, weight transfer,
   contact pressure, and coordinated torso response. Pose degradation comes from bad
   deformation and rigging—not from newly choreographing an expressive alternative.
   Do not add waves, crouches, shy leans, heroic reaches, dance-like curves, or other
   gestures absent from the source unless the user explicitly requests free restaging.
   Use locked torsos, kinked elbows, elevated shoulders, straight wrists, planted feet,
   poor balance, floating hands, and no counter-pose. Add two to four obvious skeletal
   or skin-weight failures: shoulder rotation drags the chest or collar; elbow bending
   collapses or balloons the forearm; wrist rotation twists the entire forearm; hip
   motion fails to tilt the pelvis; knee bending pulls the thigh or garment incorrectly;
   a hand follows the wrong arm axis; sleeves lag behind or intersect the limb; a raised
   leg has no supporting-body compensation; a kneeling body floats without weight.
6. **Collision:** show a small number of intentional mesh penetrations at shoulders,
   upper arms, elbows, sleeves, garments, fur, hands, or held props when plausible.
7. **Faces and gaze:** treat eyes as the primary failure signal, but default to a crude
   human-like construction rather than two exposed cartoon balls. Place simple eyeballs
   mostly inside the head behind shallow eye sockets and thick flat eyelids. Use drooping
   half-closed upper lids, unequal opening heights, weak lower lids, small pupils placed
   too low or too far sideways, failed convergence, and an unfixed gaze. Show only a
   moderate amount of sclera; avoid surprised wide-open whites. Brows sit too high or
   respond weakly to the lids. The result should feel sleepy, vacant, slow, foolish,
   and absent-minded rather than startled, cute, alert, or professionally acted. Use
   exposed round ball eyes only when the source species or explicit user request needs them.
8. **Materials and relief:** separate fur from every other material. Hair and fur
   remain plain polygonal masses and may receive a cheap badly scaled bump/normal map
   made from many short irregular tapered fur-stroke marks baked into the surface.
   Combine shallow recessed dashes with very low soft ridges; use medium but uneven
   density, with local sparse and crowded patches. Give the marks a loose directional
   flow around the face, neck, torso and limbs, but allow cheap UV rotation, seams,
   mirroring and stretching between body regions. Individual strokes stay short,
   blurry and low-profile; they never become real fibers or affect the silhouette.
   The fur illusion must come exclusively from a cheap bump/normal channel on an
   otherwise flat solid-color diffuse material. Do not paint hair strokes into albedo,
   add roughness fibers, displace vertices, or create any fur geometry. If a separate
   material reference is supplied, borrow only the micro-relief pattern; never import
   its character design, anatomy, colors, pose, composition, environment, or lighting.
   Match the look of a low-resolution amateur fur bump/normal map—not holes, pores,
   craters, scratches, carved lines, worms, leather embossing, rock or coral. Do not add strand, shell,
   groom, plush, or volumetric-fur effects. Clothing, skin, scales, wood, and props
   should use flat low-resolution diffuse color with little or no bump, simple uniform
   roughness, and weak specular. Garments must look smooth, thin, flat, and cheaply shaded.
9. **Repetition:** visibly tile textures and reuse a very small library of trees,
   posts, rocks, buildings, props, hair cards, cloth maps, or eye assets.
10. **Background textures:** do not leave trees, grass, mountains, soil, wood, rocks,
   or buildings as clean solid-color surfaces. Cover faceted background assets with
   a few low-resolution repeated diffuse textures at a relatively large tile scale,
   so repetition is discoverable but not wallpaper-like. Map them in local object XYZ space
   without global or world-scale normalization, automatic fitting, or adaptive scale.
   Object scaling should occasionally distort the maps: some tall objects stretch the
   pattern vertically along Z, some wide objects stretch it on X/Y, and neighboring
   copies may use inconsistent texel density. Add small hue/value offsets between
   repeated assets. Keep seams, tiling, mirroring, and scale errors noticeable on
   inspection but subordinate to the characters. These are color textures only.
11. **Cheap tree construction:** when trees are present, build each canopy from three
   to six thin vertical ellipse-shaped foliage cards intersecting around one crude
   trunk prism. Rotate the cards around the vertical axis to fake volume. Reuse one
   or two enlarged low-resolution leaf diffuse textures; preserve visible card
   intersections, repeated silhouettes, hard or jagged alpha edges, inconsistent
   opacity, and weak fake depth. Do not create solid detailed crowns, individual
   leaves, procedural foliage, or a technically correct billboard system.
12. **Conditional rain:** never invent rain. Only when rain exists in the source or
   the user explicitly requests it, render sparse ugly white or pale-gray thin straight
   line segments with nearly uniform width, length, direction, and opacity. Use simple
   screen-facing streaks with weak depth ordering. No droplets, splashes, ripples,
   wet-surface reflections, rain mist, refraction, volumetric atmosphere, or cinematic blur.
13. **Color:** retain clean, recognizable source colors with moderate saturation and
   readable separation. Do not use gray-brown grime, global desaturation, dirty
   overlays, or flat color as shortcuts for low production value.
14. **Flat failed lighting:** use one broad, unshaped neutral direct light with basic
   hard or uniformly soft shadows. Faces and bodies should have little modeling,
   no delicate gradients, no attractive highlight control, no bounce, no rim, and
   no cinematic separation. Treat the sky as a pasted image with no global illumination.
15. **Rendering:** use weak antialiasing, limited texture filtering, simple shadow
   maps, fine noise, mild color fringe, and modest screen-capture softness.

Do not use darkness, horror grading, VHS damage, heavy JPEG corruption, or mosaic
as shortcuts. “Bad” must come primarily from limited scene production.

## Build the edit prompt

Read [references/prompt-blueprint.md](references/prompt-blueprint.md) for the full
schema and reusable clauses. Construct prompts in this order:

1. Declare source-based badly produced bootleg-CGI reconstruction.
2. Lock count/type, relationship, action verb, one or two color cues, broad scene order,
   and broad pose topology; release exact crop, spacing, joint angles, balance, attractive
   silhouette, costume construction, makeup, and styling.
3. Set a smooth-shaded coarse continuous character mesh; ban visible character triangle
   fields, voxel/block forms, separated primitive limbs, and puppet/mannequin joints.
4. Apply the one-year-student rule: simplify every nonessential element. Reduce clothing
   to one normal continuous garment mass or a few integrated pieces while keeping basic
   shoulder, sleeve, waist, and hip logic; ban faithful tailoring, rigid barrel suits,
   puppet construction, clay sculpting, and decorative recovery.
5. Specify two to four visible bone-weight/rig hierarchy failures plus local clipping.
6. Make human-like half-lidded, vacant, badly aimed eyes the dominant facial signal;
   avoid default exposed ball eyes and simplify hands, paws, and joints.
7. Apply medium uneven short tapered baked-fur grooves and soft ridges only to
   polygonal fur/hair, with crude local direction and occasional UV stretch; keep
   clothing and other materials bump-free.
8. Strip background detail to repeated faceted primitives, then add low-resolution
   enlarged tiled diffuse maps with limited color variation and occasional Z stretching.
9. If trees exist, build their crowns from intersecting vertical ellipse foliage cards.
10. If source-evidenced or requested rain exists, reduce it to ugly white line streaks.
11. Keep source-led color clean, then disconnect foreground lighting from the sky backdrop.
12. State ratio, text behavior, and source-tailored prohibitions.

Prefer observable flaws over labels such as “ugly” or “bad quality”. Mention a
named game, engine, or film only when the user asks; always translate the name into
construction, material, lighting, and rendering properties.

## Inspect and recover

Read [references/quality-and-recovery.md](references/quality-and-recovery.md) before
judging output. Retry whenever the result is too faithful, attractive, detailed,
varied, or professionally lit. In particular, reject results where:

- character geometry becomes refined or professionally subdivided, or instead collapses
  into voxel/block shapes, Minecraft-like construction, large exposed retro triangles,
  Virtua Fighter/Tomb Raider-era character faceting, or deliberate vintage-game style;
- faces, buns, limbs, or clothes show dense readable polygon facets instead of
  continuously shaded primitive surfaces;
- limbs are separate cylinders joined by rings, sockets, gaps, exposed hinges, ball
  joints, or abrupt wooden-puppet connections;
- garments become rigid barrels, buckets, tube suits, detached sleeves, or puppet shells;
- garments preserve recognizable tailoring, layered construction, lapels, sash structure,
  decorative hems, natural folds, or source-specific costume design instead of collapsing
  into one simplified continuous garment mass or a few integrated pieces;
- characters resemble clay, plasticine, stop-motion clay figures, hand-sculpted blobs,
  kneaded surfaces, fingerprints, or uniformly lumpy organic masses;
- regular parts such as hair buns, hidden eyeball bases, sleeves, trouser legs, or robe masses are
  irregularly polygon-fitted when a simple sphere, tube, strip, cone, or shell would work;
- composition, makeup, hairstyle details, or costume silhouette remain attractively
  source-faithful rather than being simplified and crudely restaged;
- poses remain biomechanically coordinated or lack two to four obvious bone-weight,
  joint-hierarchy, pelvis, shoulder, elbow, wrist, hip, or knee failures;
- poses introduce new expressive gestures, theatrical reactions, waves, crouches,
  leans, flourishes, or elegant curves instead of corrupting the source's broad pose
  blockout and existing limb responsibilities;
- human or animal proportions remain correct, flattering, or source-faithful;
- animals retain readable shoulder blades, chest/abdominal groups, haunch muscles,
  tendons, athletic limb taper, or a powerful anatomical silhouette;
- poses retain natural balance, joint flow, weight transfer, or clean contact;
- a contact-rich image offers plausible intersections but all garments, limbs, fur,
  and held objects remain perfectly collision-free;
- faces retain polished animation acting, intelligent focus, or appealing aligned eyes;
- eyes become exposed oversized cartoon balls, surprised wide-open whites, cute googly
  eyes, or alert expressive anime eyes instead of recessed half-lidded vacant eyes;
- fur bump is absent or too subtle, becomes round holes/craters, long scratches, dense
  continuous noise, raised worms/swirls, embossed leather, or chunky rock/coral; fur gains strand/plush effects,
- a material-only reference changes subject identity, geometry, pose, clothing,
  composition, background, palette, or lighting;
  or clothing/background gains visible bump relief;
- background objects are numerous, detailed, and individually modeled;
- background trees, grass, mountains, soil, wood, rocks, or buildings use clean solid
  colors or perfectly normalized UV scale; repetition also fails when it becomes a
  dominant wallpaper pattern with identical contrast on every object;
- present trees become solid detailed crowns, individual leaves, or refined foliage
  instead of intersecting vertical ellipse cards with visible low-budget construction;
- rain is invented when absent, or source-evidenced rain becomes realistic droplets,
  splashes, wet reflections, mist, refraction, or cinematic streaks;
- colors become muddy, gray-brown, desaturated, or uniformly flat;
- sky/background color correctly produces matching global illumination, bounce, and reflections;
- lighting contains delicate tonal modeling, cinematic separation, rim light, soft bounce, or volumetric depth;
- the effect is only blur, pixelation, noise, or color grading.

On retry, change only the failed dimension and restate all anchor locks. For scoped
follow-up edits, explicitly lock every unmentioned layer and use the latest approved
image as the master. Stop after two retries unless the user asks to continue.

## Output

For a completed edit, return the generated image and one sentence naming the
preset plus the main retained anchors. Include YAML only when requested.

For prompt-only requests, return one production prompt and one negative block.

## Minimal invocation

```text
/niu-lai-translator
启用牛来粗制 CGI 转译器
把这张图重制成建模、绑定、材质和灯光都很差的廉价 CGI
```

```yaml
skill: niu-lai-translator
preset: crude_bootleg_cgi
reconstruction_strength: extreme
identity_lock: low_to_medium
anchor_lock: minimal_semantic
composition_lock: broad_blocking
simplification_policy: simplify_everything_nonessential
clothing_geometry: simplified_continuous_garments
asset_reuse: heavy
lighting: unrelated_neutral_key
ratio: source_ratio
```

**不是做成“低模艺术”，而是像建模、绑定、材质和灯光各自都做得很差，而且彼此没有协调。**
