# Prompt blueprint and parameters

Use this reference to convert source analysis and user choices into one executable
image-edit prompt. Replace variables; do not paste the schema into a generation tool.

## Parameter schema

```yaml
skill: niu-lai-translator
preset: crude_bootleg_cgi | clean_bootleg_cgi | primitive_folk_cgi | sunlit_game_map | community_cgi_stage | rough_night_render
reconstruction_strength: medium | high | extreme
anchor_lock: minimal_semantic | broad
composition_lock: loose_restage_allowed | broad
identity_lock: low_to_medium | medium | high
detail_budget: low | very_low
skill_level_reference: one_year_animation_student | inexperienced_generalist
simplification_policy: simplify_everything_nonessential | selective
geometry: coarse_continuous_character_mesh | smooth_primitive_assembly | primitive_low_poly
mesh_detail_budget: low_to_medium | low
animal_mesh_detail: moderately_reduced_not_extreme | low
animal_muscle_definition: suppressed_flattened | crude
animal_body_forms: simple_barrel_torso_uniform_limbs | loosely_source_based
surface_smoothing: uneven_manual_smoothing | careless_mixed | visibly_faceted
primitive_abstraction: simple_forms_blended_into_continuous_body | mixed_primitive_parts
joint_construction: continuous_anatomical_mass_no_puppet_seams | crude_integrated
clothing_geometry: simplified_continuous_garments | fused_single_piece_shells
wardrobe_fidelity: category_and_color_hint_only | broad_category
styling_fidelity: deliberately_broken | loose
manual_modeling_artifacts: heavy | strong
aesthetic_failure: severe_unattractive_amateur_character_design | awkward_generic
face_construction: pasted_primitive_features | crude_integrated_features
eye_style: humanlike_half_lidded_unfocused | source_specific_round
background_geometry: visibly_faceted_low_poly | primitive_low_poly
face_geometry: clumsy_asymmetric | lumpy_rounded | angular_readable
gaze_quality: vacant_badly_aimed | stiff_misaligned | crude_readable
proportion_fidelity: deliberately_broken | loosely_source_based
pose_lock: semantic_action_only | broad_pose
pose_quality: symbolic_gesture_failed_rig | crude_rigid | source_faithful
rig_failure_strength: obvious | strong | moderate
bone_weight_errors: 2_to_4_major_joints | sparse | none
collision_quality: visible_clipping | imperfect_contact | clean
clipping_count: 2_to_4 | sparse | none
texture_resolution: low | very_low
material_model: flat_diffuse_with_fur_bump | crude_lambert | diffuse_only_mismatched
surface_relief_scope: fur_and_hair_only | none
bump_scale: short_irregular_baked_fur_strokes_only | none
fur_bump_depth: shallow_visible_controlled | very_shallow
fur_bump_density: medium_uneven | sparse
fur_bump_shape: short_tapered_grooves_and_soft_ridges | irregular
fur_surface_target: cheap_lowres_baked_fur_normal | plain
fur_uv_behavior: locally_directional_with_bad_stretch | random
fur_representation: bump_normal_only_fake_no_hair_geometry | none
fur_diffuse: flat_solid_color_without_drawn_hairs | simple
fur_silhouette: unchanged_solid_mesh | source_based
material_reference_scope: texture_pattern_only_never_content | none
texture_repetition: noticeable | moderate | strong
asset_reuse: heavy | strong | moderate
background_detail: sparse | reduced
background_texture: lowres_repeated_diffuse | crude_tiled_diffuse
background_uv_mapping: nonadaptive_local_xyz | inconsistent_object_uv
background_texture_scale: enlarged_tiles | medium_tiles
background_texture_variation: limited_hue_value_offsets | minimal
background_uv_distortion: occasional_z_stretch | mixed_axis_stretch
tree_construction: crossed_vertical_ellipse_cards | primitive_solid_canopy
rain_style: source_only_white_line_streaks | none
lighting: flat_unskilled_single_light | unrelated_neutral_key | hard_awkward_daylight | crude_point_lights
environment_lighting_link: disconnected | weak | coherent
sky_behavior: pasted_backdrop_no_gi | weak_color_spill | integrated
palette: source_anchored_clean | source_anchored_saturated
color_cleanliness: clean_not_muddy | lightly_washed | source_exact
post_effects: none | subtle_capture_noise | mild_color_fringe
text_mode: none | preserve_exact | user_text
ratio: source_ratio | 1:1 | 3:4 | 4:3 | 9:16 | 16:9
```

## Production prompt template

```text
Rebuild the supplied image as badly produced, low-budget bootleg CGI. This is not
a blur filter, compression pass, polygon overlay, or fashionable low-poly illustration.

MINIMAL ANCHOR LOCK — Preserve only [subject count/types], [relationship/action verb],
[indispensable prop], and [one or two color cues]. Release source composition, crop,
spacing, overlap, camera refinement, costume construction, makeup, styling, exact pose,
silhouette, anatomy, and mesh separation. Recognition should come from roles and action,
not faithful visual design.

DETAIL BUDGET — Use [preset], [reconstruction_strength], and [detail_budget].
Apply [skill_level_reference] and [simplification_policy]. Handle every nonessential
decision with the fastest shortcut a first-year animation student would choose. Remove
subtle facial acting, hair strands, fingers, embroidery, microtexture, costume layers,
decorative architecture, small signs, and incidental set dressing.

MODELING — Rebuild characters with [geometry], [mesh_detail_budget],
[surface_smoothing], [primitive_abstraction], and [joint_construction]. Use simple
forms only as an internal blockout, then blend them into a coarse continuous body.
Shoulders flow into arms; elbows, wrists, hips, knees and ankles remain connected
organic volumes without rings, sockets, gaps, detached cylinders, ball joints, hinges,
or wooden-puppet seams. Keep anatomy generic, stiff, asymmetrical, badly proportioned,
and poorly deformed, but not mechanical. Do not make characters faceted, clay-like,
or assembled from visibly separate toy parts. Build the background with
[background_geometry]: obvious facets, primitive silhouettes, and repeated low-poly assets.

ANIMAL ANATOMY — Use [animal_mesh_detail], [animal_muscle_definition], and
[animal_body_forms]. Reduce animal geometry only moderately, but remove readable
shoulder blades, pectoral/abdominal divisions, haunch muscles, tendons, and athletic
limb taper. Use a uniform barrel/ellipsoid torso, simpler limbs with fewer thickness
changes, and broad flat shoulder/hip transitions. Avoid muscular, powerful, athletic,
heroic, or low-poly anatomy-study silhouettes.

FORM SIMPLIFICATION — Use [primitive_abstraction] as a blockout method, not a visible
construction style. Hair buns and similar regular accessories may remain primitives;
body and garment primitives must merge into continuous readable volumes. Preserve
wrong proportions, awkward axes, pinched weight deformation and local penetrations,
but remove exposed insertion seams, detached pieces and mannequin articulation.

CLOTHING — Use [clothing_geometry] with [wardrobe_fidelity] and [styling_fidelity]. Do
not reconstruct the source garment. Preserve only a broad category and one color cue.
Merge decorative and tailored details into one normal simplified garment mass or a
few integrated pieces. Retain basic shoulder line, armhole/underarm, sleeve continuity,
waist/hip volume and garment opening/hem. Delete fine tailoring, embroidery, trim,
closures, layered hems, and natural folds. Use crude T-shirt, simple continuous trousers,
or plain long-garment shapes—not barrels, buckets, tube suits or detached sleeves.
Keep it stiff, bump-free, badly fitted, with only local body intersections.

AESTHETIC AND FACE FAILURE — Use [aesthetic_failure], [face_construction], and
[eye_style]. Actively
discard the source's beauty, cuteness, elegance, heroic bearing, clean silhouette, and
appealing facial anatomy. Preserve only broad identity anchors. Build a clumsy generic
amateur face from shallow human-like sockets, flattened eye openings, thick drooping
half-closed upper lids, unequal opening heights, weak lower lids, small pupils placed
too low or sideways, unrelated gaze targets, a wedge/button nose, crooked mouth slit,
and almost no cheek or lip shaping. Keep eyeballs mostly recessed and show only moderate
sclera; do not default to exposed round cartoon balls or surprised wide-open whites. The face
must read as blank, foolish, confused, delayed, and unintentionally comic—not handsome,
pretty, cute, elegant, charismatic, fashionably stylized, or professionally animated.

PROPORTION FAILURE — Use [proportion_fidelity]. Deliberately depart from source
proportions while preserving category and identity anchors: mismatch limb lengths,
head/body ratio, neck length, torso width, joint size, muzzle size, paw/hoof scale,
and animal body mass. Prefer awkward assembled parts over elegant caricature.

POSE AND RIGGING FAILURE — Use [pose_lock], [pose_quality], [rig_failure_strength],
and [bone_weight_errors]. Preserve only the action verb, not the source pose solution.
Restage it as a crude symbol made from independently aimed limbs. Remove force chain,
contact pressure, counter-pose, balance, and weight transfer, then add two to four
readable failures: shoulder rotation drags chest/collar; elbow bend collapses or
balloons; wrist rotation twists the whole forearm; hip motion fails to tilt pelvis;
knee motion pulls thigh/garment; hand follows wrong axis; sleeve lags/intersects;
raised leg has no support compensation; kneeling body floats without weight.

COLLISION FAILURE — Use [collision_quality] with [clipping_count] readable local
intersections chosen from contact and moving-joint zones in this source: [source-tailored
clipping locations]. Allow sleeve/elbow, upper-arm/shoulder, arm/garment, hand/sleeve,
hand/held-prop, fur/harness, or adjacent-body penetration. Do not hide faces, erase
whole limbs, expose bodies, imply injury, or clip every contact.

FACES AND GAZE — This is a primary degradation cue. Use [face_geometry], [eye_style],
and [gaze_quality]. Default to simple eyeballs mostly hidden behind shallow human-like
sockets and thick flat lids: drooping half-closed upper lids, unequal opening heights,
weak lower lids, small pupils placed too low or sideways, failed convergence, moderate
sclera, crude brows, and delayed-looking reactions. Avoid exposed googly balls,
surprised wide whites, cute or alert eyes, intelligent focus, and professional acting.

MATERIALS, RELIEF, AND REUSE — Use [material_model], [surface_relief_scope],
[bump_scale], [fur_bump_depth], [fur_bump_density], [fur_bump_shape], [fur_surface_target],
and [fur_uv_behavior]. Hair/fur
are plain polygonal masses and the only surfaces allowed to receive bump/normal relief.
Use a low-resolution baked fur bump made from many short irregular tapered marks:
clearly visible but still shallow recessed dashes mixed with low soft ridges at medium uneven density.
Give marks loose local flow around face, neck, torso and limbs, while retaining amateur
UV rotation, mirroring, seams and stretching. Strokes remain short, blurry and low-profile,
affect shading only and never the silhouette. Avoid holes, pores, craters, long scratches,
dense noise, raised worms/swirls, leather embossing, rock, coral or clumps.
The illusion comes exclusively from bump/normal shading on flat solid-color diffuse.
Never paint hair into albedo, displace geometry, or generate fibers/fuzz. When given a
material-only reference, borrow only micro-relief pattern and lock all content/style dimensions.
Do not generate strands, shells, groom,
plush fibers, or volumetric fur. Clothing, skin, scales, wood, stone, and props use
flat low-resolution diffuse maps with little or no bump, simple uniform roughness,
weak specular, and crude painted shadows. Garments must be smooth and flat without
fabric weave. Use [texture_resolution] maps with [texture_repetition] and [asset_reuse]: visibly reuse
a tiny library of skin, eye, hair, cloth, fur, scale, plank, bark, grass, stone,
wall, and ground assets as relevant.

BACKGROUND — Set [background_detail], [background_texture], [background_texture_scale],
and [background_texture_variation]. Keep only essential
setting masses and reuse two or three primitive models. Do not use clean solid-color
background surfaces. Apply a tiny library of blurry low-resolution diffuse maps to
trees, grass, terrain, mountains, soil, wood, rocks, and buildings. Use
[background_uv_mapping] with [background_uv_distortion]: map in local object XYZ
space without global/world-scale normalization, automatic fitting, or adaptive texel
density. Use enlarged tiles so repetition remains noticeable without becoming a
high-frequency wallpaper. Let only some scaled objects visibly distort the texture:
occasional vertical Z-axis elongation on tall trees, posts, towers, or mountains and
occasional inconsistent X/Y scale on broad surfaces. Apply small hue/value offsets
between repeated assets. Preserve a few seams, mirrored regions, abrupt scale changes,
and mismatched texel density. Background textures remain diffuse-only and bump-free.

TREES — When trees are present use [tree_construction]: one crude trunk prism plus
three to six thin vertical ellipse-shaped foliage cards intersecting around it at
different rotations. Reuse one or two enlarged low-resolution leaf diffuse textures.
Keep repeated silhouettes, visible card intersections, hard or jagged alpha edges,
inconsistent opacity, and weak fake depth. No solid detailed canopy, individual
leaves, procedural foliage, or technically correct billboard behavior.

RAIN — Use [rain_style] only when rain exists in the source or the user explicitly
requests it. Draw sparse ugly white or pale-gray thin straight screen-facing line
segments with nearly uniform length, direction, width, and opacity. Do not invent rain.
No droplets, splashes, ripples, wet reflections, mist, refraction, volumetric rain,
or cinematic motion blur.

COLOR — Use [palette] with [color_cleanliness]. Keep source colors clean, readable,
and moderately saturated. Do not use gray-brown grime, dirty overlays, global
desaturation, crushed blacks, or uniformly flat color as shortcuts.

LIGHT, SKY, AND RENDER — Use [lighting], [environment_lighting_link], and [sky_behavior].
Treat the sky or scenic background as a pasted image that contributes little or no
global illumination, bounce, reflection, or color spill. Light subjects with an
unrelated neutral/white or weakly colored direct source. Allow backdrop, foreground,
and nearby objects to disagree in direction, exposure, shadow softness, and color
temperature. Use one broad unshaped light, little facial/body modeling, crude nearly
uniform brightness, and basic shadows. No delicate gradients or attractive highlights.
Use weak antialiasing, limited filtering, basic shadow maps,
[post_effects] kept secondary, and no professional scene integration.

OUTPUT — [ratio]. [text instruction].

DO NOT — [source-tailored prohibitions], exact premium reproduction, correct
source-faithful proportions, natural weight transfer, clean collision everywhere,
attractive aligned eyes, refined facial acting, polished subdivision, voxel/block
construction, Minecraft-like geometry, early Virtua Fighter/Tomb Raider-style exposed
character triangles, origami garments, clean designer geometry, smooth premium hair/fur, strand or plush fur
effects, bump or fabric weave on clothing, unique high-resolution materials, muddy
grading, dirty overlays, rich detailed background, sky-matched global illumination,
rim light, beauty light, three-point lighting, volumetric beams, cinematic depth,
coherent premium PBR, glossy toys,
photorealism, modern game polish, darkness as a shortcut, VHS/CRT/glitch/mosaic,
random text, UI, characters, props, logos, or cow traits absent from the source.
```

## Compact prompt

Use only when the editor follows source images reliably:

```text
Rebuild the supplied image like a one-year animation student's cheap CGI assignment.
Lock only subject count/type, relationship, action verb, indispensable prop, and one
or two color cues. Immediately release and crudely restage composition, crop, spacing,
makeup, styling, costume design, exact pose, silhouette, and anatomy. Simplify every
nonessential element. Use
smooth-shaded coarse continuous character meshes. Blend simple blockout forms into
connected organic limbs and joints; no sockets, rings, hinges, ball joints, gaps,
detached cylinders or wooden-puppet seams. Preserve bad proportions, pinched skin
weights and local penetrations. Simplify each outfit into a normal continuous garment
mass with basic shoulder, underarm, sleeve, waist and hip logic; delete tailoring,
layers, trims, folds and source-specific costume silhouette, but avoid barrels and tube suits. No clay look.
Keep the background visibly faceted low-poly with primitive repeated assets.
Actively discard attractive facial design and elegant silhouettes. Rebuild faces from
recessed human-like eyes behind unequal drooping half-closed lids, small low/side pupils
with failed convergence, a wedge/button nose, a crooked mouth slit, and almost no
cheek/lip shaping; make them sleepy, blank, foolish, confused,
and unintentionally comic rather than cute or handsome. Preserve only the action verb,
then restage the body as an uncoordinated symbolic gesture. Deliberately distort
human/animal proportions. Make the torso rigid, joints
single-axis, shoulders too high, elbows kinked, wrists straight, balance poor, and
contact weak. Add two to four obvious bone-weight failures plus two to four intersections at source-evidenced contact
zones such as sleeve/elbow, arm/shoulder, hand/prop, garment/torso, or fur/harness;
keep faces and whole limbs visible. Use unequal half-lidded human-like eye openings
with small low/side pupils aimed at different targets, moderate eye white, delayed-looking crude faces, wedge hands,
and plain polygonal hair/fur masses. Apply medium-uneven short tapered shallow grooves
and very low soft ridges only to hair/fur, with loose local direction plus bad UV rotation,
mirroring, seams and stretch. Keep the marks short, blurry and shading-only. No holes,
craters, long scratches, raised worms, leather grain, real fibers or rocky/coral clumps.
Clothing and all non-fur materials stay bump-free. Background low-poly assets are
not solid colors: cover them with enlarged blurry diffuse tiles using local XYZ mapping
without adaptive scaling, limited hue/value variations, moderate visible repetition,
and occasional Z-axis stretching on selected tall objects. Keep source colors clean,
readable, and moderately saturated;
no gray-brown grime or dirty overlay. Treat sky/background as a pasted image with no
global illumination, bounce, reflection, or color spill. Light subjects with one
flat unshaped neutral direct light even when the sky is strongly colored. Give
faces little tonal modeling and no delicate gradients or attractive highlights. Weak antialiasing
and filtering only. No correct anatomy, natural rigging, clean collision everywhere,
subdivision, refined character geometry, voxel blocks, Minecraft styling, early-console
exposed triangles, visible character triangle fields, origami garments, clay/plasticine/stop-motion sculpting, kneaded blobs,
natural cloth drape, smooth premium materials, strand/plush fur effects, clothing bump, detailed
sets, coherent PBR, sky-matched lighting, beauty light, horror, VHS, text, UI, new
subjects, props, logos, cows, or horns.
```

## Negative constraint block

```text
Avoid: fine likeness; source-faithful proportions; natural counter-pose; correct
weight transfer; flexible realistic joints; perfectly separated garments and limbs;
separated cylinder limbs; exposed joint rings; sockets; hinges; ball joints; mannequin
articulation; wooden-puppet seams; rigid barrel clothing; bucket torsos; tube suits;
detached sleeves; clothing that ignores shoulders, underarms, waist, or hips;
source-faithful composition, polished framing, faithful makeup, hairstyle ornaments,
tailored garment construction, layered costumes, lapels, sashes, trims, closures,
natural folds, source-specific outfit silhouettes, decorative recovery;
attractive aligned eyes; exposed oversized cartoon eyeballs; cute googly eyes; surprised
wide-open whites; intelligent or appealing gaze; expressive professional facial animation; polished anatomy;
professional subdivision; voxel/cube construction; Minecraft look; large clean exposed
retro triangles; Virtua Fighter/Tomb Raider-era character faceting; origami clothing;
clay, plasticine, stop-motion clay, fingerprints, kneaded/sculpted blobs; biomechanically
correct rigging; clean designer low-poly; rounded premium toy forms;
coherent premium PBR; smooth realistic hair/fur; strand, shell, plush, or groomed fur;
bump, weave, or tactile relief on clothing or background; absent fur bump; deep chunky
rock-like fur relief; solid-color background assets; globally normalized texture scale;
perfectly hidden tiling; excessive wallpaper repetition; identical high-contrast maps
on every object; solid detailed tree canopies; individual leaves; procedural foliage;
invented rain; realistic droplets, splashes, wet reflections, rain mist, refraction,
volumetric rain, or cinematic rain streaks;
muddy gray-brown grading; dirty overlays; global desaturation; uniformly flat
color; procedural background variety; rich set dressing; sky-matched global
illumination; sunset color spill; coherent reflections; cinematic lighting;
three-point light; rim light; soft bounce; volumetric fog; depth of field; premium game graphics;
photorealism; darkness or horror as a shortcut; heavy blur; large pixelation;
JPEG damage; VHS; CRT; glitch; invented text, UI, logos, characters, or props.
```

## Text handling

- `none` (default): omit incidental signs, subtitles, watermarks, and interface text.
- `preserve_exact`: quote exact source text and inspect character by character.
- `user_text`: include only exact user-supplied text; invent nothing.

## Source recipes

### Portrait or group

Use `community_cgi_stage` for groups and `crude_bootleg_cgi` for a single figure.
Lock count, relationships, action verbs, one hair cue, and one or two color cues.
Freely simplify spacing, crop, styling, and costume construction. Reuse eyes, skin,
hair, and cloth maps. Build hair as sparse polygonal masses with badly scaled bump
relief. Simplify garments into continuous normal clothing masses, smooth and bump-free,
with basic shoulder/sleeve/waist/hip logic. Distort ratios,
lock the torso, kink limb joints, and add local
sleeve/arm/shoulder clipping when contact exists.

### Animal scene

Use `crude_bootleg_cgi`. Lock species, count, semantic action, markings, and composition.
Change body ratios, leg length, paw/hoof scale, neck and muzzle proportions, and
balance. Use rigid joints and local fur/harness or limb/body clipping where plausible.
Build fur as sparse polygonal masses with cheap short-stroke baked bump relief; keep scales
flat and bump-free. Make the eyes vacant and badly aimed. Reduce facial refinement
and keep the environment visibly faceted low-poly.

### Architecture or landscape

Use `sunlit_game_map`. Lock perspective, horizon, landform, massing, and openings.
Reuse a tiny module library and tile enlarged blurry wall, ground, grass, tree, and
rock diffuse maps. Use non-adaptive local XYZ mapping so selected scaled modules show
mismatched texel density and occasional Z-direction stretching. Add small hue/value
offsets between copies. Build trees from three to six intersecting vertical ellipse
foliage cards around a simple trunk. Keep background maps bump-free and avoid wallpaper density.

### Lighting-only follow-up

Lock all geometry, materials, poses, color, and composition. Replace only lighting
with `unrelated_neutral_key`: treat the sky/background as a non-emissive pasted image,
remove its global illumination, bounce, reflection, and color spill, then light the
foreground with a mismatched neutral direct source and simple cheap shadows.
