# Niu Lai Translator / 牛来粗制 CGI 转译器

将用户提供的图像重建为一种“制作能力明显不足”的廉价 CGI 场景：不是精致的低模艺术，也不是模糊、像素化或滤镜处理，而是让低质量真正来自建模、比例、绑定、碰撞、材质参数、资产、灯光和渲染能力的全面不足。

## 本次升级说明（2026-08）

这一版不是简单增加几个提示词，而是重新确定了 Skill 的默认审美、角色建模、服装、绑定、毛发材质、背景资产和灯光逻辑。升级时建议直接用本压缩包覆盖旧目录，不要只替换 `SKILL.md`。

### 1. 默认目标从“明显低模”改为“制作能力不足”

- 不再把人物直接做成极低面数、方块、体素或满身可见三角面的角色。
- 人物表面保持圆滑着色，几何量低于成熟动画模型，但粗糙感主要来自比例、造型、动作、绑定、穿模和材质失调。
- 明确禁止 Minecraft、方块体素、古早游戏大三角、设计感低模、黏土、橡皮泥和精致玩具风。
- 背景仍允许明显 low-poly，与人物形成不同的建模层级。

### 2. 更早打破原图审美、构图与妆造

- 默认只锁定主体数量与类型、人物关系、动作动词、必要道具和一两个识别色。
- 构图、裁切、间距、遮挡、准确姿态、漂亮轮廓、妆造、发型细节和服装版型均可重新简化。
- 新增“学习动画制作约一年的学生”能力基准：所有非必要内容都优先采用最快、最省事的处理方式。
- 漂亮、英俊、可爱、优雅或英雄化的角色设计不再被视为必须保留的身份信息。

### 3. 服装由“还原版型”改为“正常大形下的极简处理”

- 删除刺绣、装饰、复杂领口、叠穿、门襟、腰封、精细裁剪、自然褶皱和成熟布料模拟。
- 服装只保留一级类别与颜色提示，例如普通短袖、简单长衣、套头衫或连续裤装。
- 保留最基本的肩线、腋下、袖筒、腰胯与下摆关系，避免把角色套进硬质桶、管套或机器人外壳。
- 服装默认使用平滑、无凹凸、低分辨率漫反射材质。

### 4. 关节恢复连续人体，但绑定必须明显失败

- 肩、肘、腕、髋、膝和踝保持连续身体体积，禁止分段圆柱、插销、球关节、连接环、悬浮肢体和木偶式接缝。
- 动作只保留“抬腿、递物、站立、拥抱、摆荡”等语义，不保留原图准确的关节解决方案。
- 默认加入 2–4 个明显骨骼/权重错误以及 2–4 处局部穿模。
- 错误通过肩部拉扯胸口、肘部夹点、前臂错误扭转、骨盆不随髋部运动、腿部无重心补偿、袖口或手掌陷入身体等方式表现。

### 5. 眼睛改为更接近人的“半闭失焦眼”

- 默认不再使用两个外挂的大白球眼睛。
- 眼球大部分藏在浅眼窝和厚重眼皮后，上眼皮下垂且左右开合不一致。
- 瞳孔较小，偏低或偏侧，双眼不汇聚，眉眼反应迟钝。
- 目标是困倦、无神、反应慢、傻乎乎，而不是惊讶、可爱或精致动画表演。
- 对面罩、机械眼或原图明确的大圆眼角色，可按源图类别使用专门处理，不强制套用人眼结构。

### 6. 动物建模降低肌肉感，但不极端减面

- 动物面数只做适度降低，继续保持圆滑、连续和可辨识的大形。
- 删除明显肩胛、胸肌、腹部、臀腿肌群、肌腱和运动型肢体收分。
- 躯干更接近均匀桶状或椭圆体，四肢粗细变化减少，肩髋过渡宽而平。
- 禁止把动物做成强壮、健美、英雄化或低模解剖展示模型。

### 7. 毛发改为“纯凹凸/法线贴图伪造”

- 不生成真实毛发、毛丝、毛束、绒边、毛发系统、Hair Cards、Shell Fur 或改变轮廓的置换效果。
- 毛发主体仍是实心几何块，漫反射保持纯色，不能直接画出毛丝。
- 毛感仅由低分辨率凹凸/法线贴图产生：短小、不规则、略带尖端的浅凹短划与低矮软凸脊，强度清晰可见但仍保持浅表。
- 纹理密度中等但不均匀，允许错误旋转、镜像、接缝和局部拉伸，形成低劣的 UV 与贴图实现。
- 禁止圆孔、陨石坑、鳞片闭环、虫纹、皮革压花、岩石裂纹和高质量真实毛发。
- 材质参考图只允许提供微观凹凸形态，不得影响角色身份、造型、动作、服装、构图、环境、色彩和灯光。

### 8. 背景资产、树木与天气规则更新

- 树木、草地、山体、木材、岩石和建筑使用少量低分辨率重复漫反射贴图，不再只用纯色。
- 放大单块贴图，配合有限色相/明度变化，降低满屏墙纸式重复。
- 保留局部坐标映射错误、纹理密度不一致和部分高瘦物体的 Z 向拉伸。
- 树冠默认由 3–6 个交叉的竖向椭圆薄片组成，保留穿插、锯齿透明边和虚假体积。
- 雨仅在原图存在或用户明确要求时出现，并简化为方向和粗细近似一致的白色细直线。

### 9. 色彩与灯光重新分工

- 保留清晰、适度饱和的大色块，不再用灰脏、压暗和全局去饱和制造廉价感。
- 天空被视为贴上去的背景，不产生正确的全局光照、反弹光、环境反射或色彩溢出。
- 主体默认只接受一盏未经塑形的中性直接光，缺少轮廓光、精细明暗和电影感。

### 10. 新增反向质量门槛与失败恢复

- `references/quality-and-recovery.md` 现在会主动拒绝过于漂亮、准确、协调、精致或还原度过高的结果。
- 对人物木偶化、服装桶装化、眼睛卡通球化、动物肌肉过强、毛发变成真实纤维、背景纯色或重复过度等问题，均增加了专项恢复提示。
- 默认最多重试两次；仍存在明显硬伤时应如实说明，不把结果强行描述为成功。

### 升级时需要替换的文件

```text
README.md
SKILL.md
agents/openai.yaml
references/prompt-blueprint.md
references/quality-and-recovery.md
references/style-system.md
```

## 核心效果

- 粗糙连续人体：人物几何量低、比例笨拙、轮廓僵硬，但肩—上臂—肘—前臂以及髋—大腿—膝—小腿必须保持连续人体关系。禁止分段圆柱、插销、球形关节、连接环、悬浮肢体和木偶式接缝。
- 基础形体内化：基础球体、胶囊和管体只用于内部搭形，最终必须融合成连续身体；只有发髻等明确规律部件可以直接保留球体。眼球藏在眼眶与眼皮后，不以外挂零件呈现。
- 正常化简服装：不还原原服装的复杂版型和装饰，但需要保留基本肩线、腋下、袖筒、腰胯和下摆关系。上衣可以简化成普通短袖大形，裤子是连续腰胯连接两条裤腿，长袍是带整合袖子的简单长衣；禁止桶装、管套、独立袖筒和木偶外壳。
- 一年级学生能力基准：把结果看成学习动画制作约一年的学生作业。能用基础体完成角色和场景，但所有非必要内容都选择最快、最省事、最不讲究的简化方案，不展示成熟建模、服装设计、构图或动画能力。
- 审美主动失败：不保留原图漂亮、英俊、可爱或优雅的脸部设计，只保留少量身份锚点。眼睛采用粗糙的人形眼眶：扁平眼裂、沉重半闭上眼皮、左右开合不一、小瞳孔偏低或偏侧且视线不汇聚；搭配按钮/楔形鼻、歪斜嘴缝和几乎不存在的面部塑形，表情必须蠢懵、空白、困倦且不讨喜。
- 比例失真：主动改变人物与动物的头身比、肢体长度、躯干宽度和关节大小。
- 动物弱肌肉化：动物面数只小幅下调，仍保持连续圆滑大形，但删除肩胛、胸肌、腹部、臀腿肌群、肌腱和运动型肢体收分。躯干更接近均匀桶状/椭圆体，四肢粗细变化更少，肩髋过渡宽而平，禁止强壮、健美或低模解剖展示感。
- 符号化错误动作：只保留“抬腿、递物、抱住、站立”等动作动词，不保留原图准确姿态；肢体只负责做出符号，躯干不配合，完全没有发力链、重心、承重、接触压力或反向平衡。至少出现 2–4 个明显骨骼或权重错误。
- 动作穿模：默认加入 2–4 处清晰但局部的碰撞失败，例如上臂切进肩部、肘部压进躯干、前臂穿过袖口、手掌陷入衣服或相邻身体。身体仍保持连续，不使用断开的木偶关节。
- 失败眼神：默认不是外挂大圆眼，而是更接近人的半睁眼。上眼皮下垂、两眼开合不一致、瞳孔小且偏低/偏侧、视线没有落点、眉眼反应迟钝；眼白适量，不做惊讶式全露。
- 材质分工：仅毛发表面使用低分辨率的廉价毛发凹凸贴图，由大量短小、不规则、略带尖端的浅凹短划与低矮软凸脊组成。密度中等但疏密不均，脸、颈、躯干和四肢有松散方向性，同时保留错误旋转、镜像、接缝和局部拉伸。纹理只影响明暗，不形成真实毛丝或轮廓绒毛。禁止圆孔、陨石坑、长划痕、虫纹、皮革压花和岩石裂纹；服装及非毛发表面保持平滑无凹凸。
- 假毛发通道：所谓“毛发”只能由凹凸/法线贴图伪造。漫反射仍是纯色，不能画出毛丝；禁止置换几何、毛发系统、毛束、纤维、绒边和轮廓变化。若用户另给材质参考图，只借用微观凹凸形态，绝不借用参考图的角色、服装、动作、构图、环境、色彩或灯光。
- 背景错贴图：树木、草地、山体、木材、岩石和建筑不能只用纯色，要复用少量低分辨率漫反射贴图；放大单块纹理以降低重复频率，对副本做有限色相/明度偏移，并仅在部分高瘦物体上保留 Z 向拉伸。
- 椭圆薄片树：树干使用简单柱体，树冠由 3–6 个交叉的竖向椭圆薄片构成，重复使用一两张低分辨率树叶纹理，并保留薄片穿插、锯齿透明边缘与虚假的体积感。
- 条件降雨：只有原图存在雨或用户明确要求时才生成；雨表现为方向、长度、粗细和透明度近似一致的丑陋白色细直线，不做水滴、水花、湿地反射、雨雾或电影化运动模糊。
- 重复资产：明显复用少量树木、木桩、岩石、建筑、贴图和角色部件。
- 干净色彩：保留原图清晰、适度饱和的色块，不用灰脏、压暗或全局去饱和制造廉价感。
- 粗平灯光：天空只是背景贴图；人物只用一盏未经塑形的中性光，亮度近乎均匀，缺少细腻明暗、轮廓光、反弹光和电影感。

## 目录结构

```text
NiuLai-Skill/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── prompt-blueprint.md
    ├── quality-and-recovery.md
    └── style-system.md
```

## 安装

将整个 `NiuLai-Skill` 文件夹放入支持 Skills 的工具所使用的 Skills 目录中。不要只上传 `SKILL.md`，因为主文件会按需读取 `references/` 中的风格、提示词和质量检查规则。

如果通过 GitHub 使用，可直接克隆或下载仓库，并将仓库目录作为一个完整 Skill 安装。

## 调用方式

```text
/niu-lai-translator
启用牛来粗制 CGI 转译器
把这张图重制成建模、绑定、材质和灯光都很差的廉价 CGI
```

提供原图后，如果没有额外参数，Skill 会默认直接执行 `crude_bootleg_cgi` 预设。也可以要求先给方案、降低劣化强度、提高身份相似度或指定输出比例。旧的 `primitive_folk_cgi` 仅作为明确要求多边形风格时的兼容预设。

## 默认参数

```yaml
skill: niu-lai-translator
preset: crude_bootleg_cgi
reconstruction_strength: extreme
anchor_lock: minimal_semantic
composition_lock: loose_restage_allowed
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
proportion_fidelity: deliberately_broken
pose_lock: semantic_action_only
pose_quality: symbolic_gesture_failed_rig
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
asset_reuse: heavy
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
ratio: source_ratio
```

## 设计原则

Skill 只严格保留主体数量与类型、人物关系、动作动词、必要道具和一两个识别色。构图、镜头裁切、间距、遮挡、具体姿态、轮廓、妆造、发型细节和服装版型都可以在第一步主动打破并重新简化。

低质量应来自完整的生产流程失调。人物既不能精致细分，也不能退化成方块、体素、早期游戏大三角角色或分段木偶。身体和服装保持粗糙但连续的正常大形；低劣感来自比例、权重拉扯、关节塌陷、穿模、眼神和不协调动作，而不是外露插接结构。

## 文件说明

- `SKILL.md`：触发条件、默认工作流、核心约束与输出规则。
- `references/style-system.md`：风格支柱、预设和不同原图类型的处理策略。
- `references/prompt-blueprint.md`：参数体系、完整提示词模板与负面约束。
- `references/quality-and-recovery.md`：反向质量门槛、评分方法与失败恢复提示。
- `agents/openai.yaml`：ChatGPT/Codex 中显示名称、简述和默认调用提示。

## 边界

- 不通过恐怖、血腥、肢体缺失或身体暴露制造“穿模”。
- 不随意增加人物、动物、牛角、字幕、标志、界面或原图不存在的道具。
- 不把 VHS、马赛克、JPEG 损坏、重度噪点或黑暗调色当作主要劣化手段。
- 对真实人物保持年龄、族裔、身体类别及人物关系不变。

---

**人物是“圆滑着色的粗糙连续人体”，不能出现分段木偶关节；服装保持正常连续大形但删除复杂版型。背景才是明显低模，低劣感主要来自眼神、比例、权重变形、穿模和不协调动作。**
