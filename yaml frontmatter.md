```yaml
---
# ========== 基础识别信息 ==========
# 文件编码：UTF-8 (无BOM)
# 创建日期：按实际标准发布日期填写
# 语言环境：中文(简体) zh-CN
title: "GB 5226.1-2019 - 机械电气安全 机械电气设备 第1部分：通用技术条件"
last_modified: 2024-01-20T15:30
aliases:
  - "{标准号}"
  - "{标准号简写}"
  - "{标准号无符号版本}"
  - "{国际标准等效标识}"
  - "{技术领域别名}"

# ========== 三维正交标签体系 ==========
tags:
  # 物理现象层(What) - 描述电磁现象的物理本质 - 严格包含关系
  - "电磁现象|静电放电|接触放电|2-8kV"
  - "电磁现象|射频辐射|电磁场抗扰度|3V-m"
  - "电磁现象|电快速瞬变|群脉冲|1kV"
  - "电磁现象|浪涌|电源端口|1kV"
  - "电磁现象|传导抗扰度|射频耦合|3V"
  - "传播机制|传导耦合|电源线路"
  - "传播机制|辐射耦合|近场耦合"
  - "频谱特征|脉冲干扰|ns级上升时间"
  - "频谱特征|连续波|射频载波"
  
  # 技术方法层(How) - 描述测试和解决方法 - 严格包含关系  
  - "测试方法|IEC61000-4-2|静电放电发生器|接触放电法"
  - "测试方法|IEC61000-4-3|射频发生器|电磁场辐射法"
  - "测试方法|IEC61000-4-4|脉冲发生器|电快速瞬变法"
  - "测试方法|IEC61000-4-5|浪涌发生器|组合波测试"
  - "测试方法|IEC61000-4-6|信号发生器|传导注入法"
  - "测试设备|EMC测试系统|发生器类|IEC61000规范"
  - "测试环境|电磁兼容实验室|屏蔽室环境"
  - "性能判据|A级判据|试验期间正常工作"
  - "性能判据|B级判据|功能降低但可恢复"
  - "性能判据|C级判据|需人工干预恢复"
  
  # 应用领域层(Where) - 描述应用场景和产品 - 严格包含关系
  - "工业应用|机械设备|电气控制系统|可编程控制器"
  - "工业应用|机械设备|电气控制系统|变频驱动器" 
  - "工业应用|机械设备|电气控制系统|伺服系统"
  - "工业应用|机械设备|安全系统|急停回路"
  - "工业应用|机械设备|安全系统|安全继电器"
  - "电压范围|低压系统|交流1000V以下"
  - "电压范围|低压系统|直流1500V以下"
  - "频率范围|工频系统|200Hz以下"
  - "环境分类|工业环境|有防护结构内部"
  - "安装环境|固定安装|非手持便携"
  
  # 关联标准层 - 直接引用相关标准编号用于知识图谱链接 - 倒装结构标准名放在最后
  - "机械电气安全|IEC60204-1"
  - "静电放电抗扰度|IEC61000-4-2"
  - "射频电磁场抗扰度|IEC61000-4-3"
  - "电快速瞬变抗扰度|IEC61000-4-4"
  - "浪涌抗扰度|IEC61000-4-5"
  - "传导抗扰度|IEC61000-4-6"
  - "等同采用IEC60204-1|GB5226-1"
  - "欧盟版本|EN60204-1"
  - "IDT关系|等同采用"
  - "现行有效|2019版"
  
  # 标准类型判断 - 必填项目 - 严格包含关系
  - "标准分类|安全标准|机械电气安全|EMC集成要求"
  - "标准分类|综合标准|安全与EMC并重"
  - "EMC要求|EMS抗扰度要求|工业环境等级"
  - "EMC要求|EMI发射限值|工业设备B类"
  - "安全要求|电气安全|低压电气系统"
  - "安全要求|功能安全|安全相关控制系统"
  
  # 测试等级标注 - GB 5226.1-2019具体等级 - 严格包含关系
  - "抗扰度等级|工业环境|标准测试等级"
  - "性能判据|A级|试验期间正常功能"
  - "性能判据|B级|暂时功能降低"  
  - "性能判据|C级|需要人工干预"
  - "发射等级|B类设备|工业环境适用"
  - "安全等级|电气安全|基本安全要求"
  - "安全等级|功能安全|安全相关系统"

# ========== 标签优化说明 ==========
# 严格包含关系标签体系说明：
# 插件增强格式（需要Tag Wrangler或Nested Tags插件）
# 采用竖线分隔实现严格的层级包含关系：
# 
# GB 5226.1-2019 标签实例：
# - 电磁现象|静电放电|接触放电|2-8kV
# - 测试方法|IEC61000-4-2|静电放电发生器|接触放电法  
# - 工业应用|机械设备|电气控制系统|可编程控制器
# - 国际标准|IEC60204-1|机械电气安全|2016版本
# - 标准分类|安全标准|机械电气安全|EMC集成要求
#
# 严格包含关系原则：
# 1. 语义包含：每一级必须是上一级的真子集
# 2. 层级清晰：最多4层，每层含义明确且不重复
# 3. 路径唯一：每个概念只有一条标准的层级路径
# 4. 知识图谱：标准文档连接到最具体的叶子节点
# 5. 搜索精确：支持从任何层级开始的精确匹配
# 6. 聚类自然：同一父节点下的子节点自动聚类显示
#
# 知识图谱连接策略：
# - 标准文档连接到所有相关的叶子节点（4级标签）
# - 中间节点作为聚类中心，不直接连接标准文档  
# - 支持从任何层级开始的向上或向下导航
# - 相关标准通过共享的中间节点路径自动关联

# ========== 标准技术参数 ==========
standard_number: "{完整标准编号}"
standard_year: {发布年份}
organization: "{标准化组织全称}"
standard_type: "{强制性/推荐性}国家标准"
status: "现行有效"
effective_date: "{生效日期YYYY-MM-DD}"

# ========== 技术范围与限值 ==========
frequency_range:
  lower_limit: "{下限频率} {单位}"
  upper_limit: "{上限频率} {单位}"
  characteristic_frequencies: ["{关键频点1}", "{关键频点2}"]

test_levels:
  - level: 1
    description: "保护良好的环境"
    parameters: "{具体数值和单位}"
    application: "{典型应用场景}"
  - level: 2
    description: "一般电磁环境"
    parameters: "{具体数值和单位}"
    application: "{典型应用场景}"
  - level: 3
    description: "严酷工业环境"
    parameters: "{具体数值和单位}"
    application: "{典型应用场景}"
  - level: X
    description: "开放等级"
    parameters: "用户自定义"
    application: "特殊应用需求"

# ========== 测试设备技术要求 ==========
test_equipment:
  primary_instrument:
    name: "{主测试设备名称}"
    technical_specs:
      frequency_range: "{频率范围}"
      dynamic_range: "{动态范围dB}"
      accuracy: "±{准确度值}dB"
      impedance: "{阻抗值}Ω"
    calibration_cycle: "{校准周期}个月"
    reference_standard: "{计量标准}"
  
  auxiliary_equipment:
    - name: "{辅助设备1}"
      specifications: "{关键技术指标}"
    - name: "{辅助设备2}"
      specifications: "{关键技术指标}"

# ========== 测试条件与环境 ==========
test_conditions:
  environmental:
    temperature: "{温度范围}°C (稳定性±{变化量}°C)"
    humidity: "{湿度范围}%RH (稳定性±{变化量}%)"
    atmospheric_pressure: "{压力范围}kPa"
  
  electromagnetic:
    background_field: "< {场强值} V/m ({频率范围})"
    power_supply: 
      voltage_stability: "±{百分比}%"
      frequency_stability: "±{Hz}Hz"
      harmonic_distortion: "< {百分比}%"
  
  mechanical:
    vibration_isolation: "{隔振要求}"
    grounding_impedance: "< {阻抗值}Ω"

# ========== 性能判据与等级划分 ==========
performance_criteria:
  A级:
    description: "试验期间性能正常"
    technical_requirement: "{具体技术要求}"
    acceptance_criteria: "{合格判据}"
  
  B级:
    description: "试验期间性能暂时降低，试验后自动恢复"
    technical_requirement: "{具体技术要求}"
    acceptance_criteria: "{合格判据}"
    
  C级:
    description: "试验期间性能降低，需要操作者干预恢复"
    technical_requirement: "{具体技术要求}"
    acceptance_criteria: "{合格判据}"
    
  D级:
    description: "设备损坏或数据丢失"
    technical_requirement: "不可接受"
    acceptance_criteria: "不合格"

# ========== 测量不确定度评估 ==========
measurement_uncertainty:
  type_A_uncertainty: "±{数值}dB ({置信度}%置信区间)"
  type_B_uncertainty: "±{数值}dB (均匀分布)"
  combined_uncertainty: "±{数值}dB (k=2)"
  major_sources:
    - source: "{不确定度来源1}"
      contribution: "±{贡献值}dB"
    - source: "{不确定度来源2}"
      contribution: "±{贡献值}dB"

# ========== 标准关系映射 ==========
Referenced_Standards:
  normative_references:
    - standard: "{规范性引用标准1}"
      application: "{引用目的和应用}"
    - standard: "{规范性引用标准2}"
      application: "{引用目的和应用}"
  
  informative_references:
    - standard: "{资料性引用标准1}"
      relationship: "{关系说明}"

equivalent_standards:
  international:
    primary: "{主要国际对等标准}"
    adoption_method: "等同采用/修改采用/等效采用"
    technical_differences: "{技术差异描述}"
  
  regional:
    europe: "{欧盟EN标准}"
    usa: "{美国ANSI/FCC标准}"
    japan: "{日本JIS标准}"

superseded_standards: "{被替代的旧标准}"
superseding_standards: "{替代本标准的新标准}"

# ========== 知识图谱属性 ==========
graph_attributes:
  node_type: "{基础标准/产品标准/测试方法标准}"
  cluster_family: "{标准族群标识}"
  importance_weight: {1-10权重值}
  connectivity_index: {连接度指数}
  
graph_relationships:
  references: ["{引用关系标准列表}"]
  referenced_by: ["{被引用关系标准列表}"]
  complements: ["{互补关系标准列表}"]
  conflicts: ["{冲突关系标准列表}"]

# ========== 工程实施信息 ==========
implementation_guidance:
  typical_test_duration: "{典型测试时间}"
  cost_estimate_range: "{成本估算范围}"
  required_expertise_level: "{所需专业技能等级}"
  common_failure_modes: 
    - failure: "{常见失效模式1}"
      solution: "{解决方案}"
    - failure: "{常见失效模式2}"
      solution: "{解决方案}"

compliance_information:
  mandatory_regions: ["{强制执行地区1}", "{强制执行地区2}"]
  certification_bodies: ["{认证机构1}", "{认证机构2}"]
  mutual_recognition: ["{互认协议1}", "{互认协议2}"]

# ========== 文档管理信息 ==========
document_management:
  creation_date: {创建日期YYYY-MM-DD}
  last_review_date: {最后审查日期YYYY-MM-DD}
  next_review_date: {下次审查日期YYYY-MM-DD}
  revision_history:
    - version: "v{版本号}"
      date: {修订日期YYYY-MM-DD}
      changes: "{主要变更内容}"
      impact_assessment: "{影响评估}"

quality_assurance:
  technical_reviewer: "{技术审查者}"
  validation_method: "{验证方法}"
  peer_review_status: "{同行评议状态}"
---
```