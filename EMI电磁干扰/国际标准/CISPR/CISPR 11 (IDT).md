---
# ========== 基础识别信息 ==========
# 文件编码：UTF-8 (无BOM)
# 创建日期：2024-01-01 (标准发布日期)
# 语言环境：英文(English) en-US, 中文翻译 zh-CN
title: "CISPR 11:2024 - 工业、科学和医疗设备 射频骚扰特性 限值和测量方法"
last_modified: 2025-06-16T12:00
aliases:
  - "CISPR 11"
  - "CISPR_11"
  - "CISPR11"
  - "工业科学医疗设备电磁骚扰"
  - "ISM设备EMC"
  - "Industrial Scientific Medical EMC"

# ========== 三维正交标签体系 ==========
tags:
  # 物理现象层(What) - 描述电磁现象的物理本质
  - "射频骚扰EMI/9kHz-400GHz/传导辐射"
  - "ISM频段应用/2.4GHz-24GHz/有意射频能量"
  - "传导发射EMI/150kHz-30MHz/电源线信号线"
  - "辐射发射EMI/30MHz-18GHz/近场远场"
  - "电磁耦合/容性感性/辐射耦合"
  
  # 技术方法层(How) - 描述测试和解决方法
  - "EMI发射标准"
  - "LISN人工电源网络法/50μH-50Ω/标准化阻抗"
  - "电流探头法/转移阻抗/共模电流"
  - "电波暗室法/半消声室/反射衰减>20dB"
  - "开阔场地法/OATS/归一化场地"
  - "准峰值检波/QP/主观听觉效应"
  - "平均值检波/AV/热效应"
  - "等级/ClassA工业商业/ClassB住宅"
  - "等级/Group1内部功能/Group2有意射频"
  - "校准要求/12个月/计量溯源"
  
  # 应用领域层(Where) - 描述应用场景和产品
  - "工业设备/制造业/感应加热焊接"
  - "科学设备/实验室/半导体制造"
  - "医疗设备/透热治疗/医疗扫描仪"
  - "ISM应用/微波炉/射频加热"
  - "工业机器人/自动化/智能制造"
  - "等离子设备/表面处理/清洗改性"
  
  # 关联标准层 - 直接引用相关标准编号用于知识图谱链接
  - "CISPR16-1-1/测量设备/EMI接收机要求"
  - "CISPR16-2-1/测量方法/传导辐射测试"
  - "IEC61000-3-2/谐波电流/电源质量"
  - "EN55011/欧洲标准/区域实施"
  - "FCC-Part18/美国标准/ISM设备"
  - "GB4824/中国标准/等效采用"
  
  # 标准类型判断 - 必填项目
  - "EMI"        # EMI发射标准：限值ClassA/ClassB
  - "A类"        # ClassA工业商业环境
  - "B类"        # ClassB住宅环境

# ========== 标准技术参数 ==========
standard_number: "CISPR 11"
standard_year: 2024
organization: "国际电工委员会(IEC)/国际无线电干扰特别委员会(CISPR)"
standard_type: "国际标准"
status: "现行有效"
effective_date: "2024-01-01"

# ========== 技术范围与限值 ==========
frequency_range:
  lower_limit: "9 kHz"
  upper_limit: "400 GHz"
  characteristic_frequencies: ["150kHz", "30MHz", "1GHz", "18GHz"]

test_levels:
  - level: "Class A Group 1"
    description: "工业商业环境内部功能设备"
    parameters: "传导79-73dBμV, 辐射40-76dBμV/m"
    application: "实验室设备、半导体变频器、工业机器人"
  - level: "Class A Group 2" 
    description: "工业商业环境有意射频设备"
    parameters: "传导66-60dBμV, 辐射47-76dBμV/m"
    application: "感应加热、射频焊接、等离子设备"
  - level: "Class B Group 1"
    description: "住宅环境内部功能设备"
    parameters: "传导66-60dBμV, 辐射30-74dBμV/m"
    application: "家用实验设备、小型工业设备"
  - level: "Class B Group 2"
    description: "住宅环境有意射频设备"
    parameters: "传导66-60dBμV, 辐射30-74dBμV/m"
    application: "微波炉、医疗透热设备"

# ========== 测试设备技术要求 ==========
test_equipment:
  primary_instrument:
    name: "EMI接收机"
    technical_specs:
      frequency_range: "9kHz-18GHz"
      dynamic_range: ">100dB"
      accuracy: "±1.5dB"
      impedance: "50Ω"
    calibration_cycle: "12个月"
    reference_standard: "CISPR 16-1-1"
  
  auxiliary_equipment:
    - name: "LISN人工电源网络"
      specifications: "50μH/50Ω，插损<1dB，隔离>20dB"
    - name: "电流探头"
      specifications: "转移阻抗校准，10kHz-30MHz"
    - name: "半消声室"
      specifications: "反射衰减>20dB，1-18GHz"
    - name: "天线系统"
      specifications: "双锥+对数周期+喇叭天线"

# ========== 测试条件与环境 ==========
test_conditions:
  environmental:
    temperature: "15-35°C (稳定性±2°C)"
    humidity: "45-75%RH (稳定性±5%)"
    atmospheric_pressure: "86-106kPa"
  
  electromagnetic:
    background_field: "< 限值-6dB (9kHz-18GHz)"
    power_supply: 
      voltage_stability: "±2%"
      frequency_stability: "±0.1Hz"
      harmonic_distortion: "< 3%"
  
  mechanical:
    vibration_isolation: "测试台隔振<0.1g"
    grounding_impedance: "< 1Ω射频接地"

# ========== 性能判据与等级划分 ==========
performance_criteria:
  A级:
    description: "合格，所有频点QP和AV≤限值"
    technical_requirement: "传导辐射发射符合对应Class限值"
    acceptance_criteria: "建议保留3dB设计余量"
  
  B级:
    description: "临界合格，个别频点接近限值±1dB"
    technical_requirement: "需要批量一致性验证"
    acceptance_criteria: "改进设计余量"
    
  C级:
    description: "不合格，超限值需要整改"
    technical_requirement: "确定干扰源和传播路径"
    acceptance_criteria: "滤波屏蔽整改后重测"

# ========== 测量不确定度评估 ==========
measurement_uncertainty:
  type_A_uncertainty: "±2dB (95%置信区间)"
  type_B_uncertainty: "±1.5dB (均匀分布)"
  combined_uncertainty: "±2.5dB (k=2)"
  major_sources:
    - source: "EMI接收机校准不确定度"
      contribution: "±1.0dB"
    - source: "天线系数不确定度"
      contribution: "±1.2dB"
    - source: "LISN特性不确定度"
      contribution: "±0.8dB"
    - source: "环境条件影响不确定度"
      contribution: "±0.5dB"

# ========== 标准关系映射 ==========
Referenced_Standards:
  normative_references:
    - standard: "CISPR 16-1-1:2019"
      application: "无线电干扰测量仪器要求"
    - standard: "CISPR 16-2-1:2014"
      application: "传导辐射发射测量方法"
    - standard: "IEC 61000-3-2:2018"
      application: "谐波电流发射限值"
    - standard: "ITU Radio Regulations"
      application: "ISM频段分配规定"
  
  informative_references:
    - standard: "IEC 60335系列"
      relationship: "家用电器安全标准"
    - standard: "IEC 62233:2005"
      relationship: "人体RF暴露测量方法"

equivalent_standards:
  international:
    primary: "CISPR 11:2024 Edition 6.0"
    adoption_method: "原版国际标准"
    technical_differences: "全球统一技术要求"
  
  regional:
    europe: "EN 55011:2024"
    usa: "FCC Part 18"
    china: "GB 4824"
    japan: "VCCI-CISPR11"

superseded_standards: "CISPR 11:2015"
superseding_standards: "暂无"

# ========== 知识图谱属性 ==========
graph_attributes:
  node_type: "产品标准"
  cluster_family: "CISPR标准族"
  importance_weight: 10
  connectivity_index: 15
  
graph_relationships:
  references: ["CISPR16-1-1", "CISPR16-2-1", "IEC61000-3-2", "ITU-RR"]
  referenced_by: ["EN55011", "GB4824", "FCC-Part18", "VCCI"]
  complements: ["CISPR12", "CISPR25", "IEC60335"]
  conflicts: ["无"]

# ========== 工程实施信息 ==========
implementation_guidance:
  typical_test_duration: "传导发射4-6小时，辐射发射6-10小时"
  cost_estimate_range: "30000-80000元 (完整ISM设备测试)"
  required_expertise_level: "EMC工程师高级"
  common_failure_modes: 
    - failure: "传导发射超标(150kHz-30MHz)"
      solution: "LISN滤波器，X/Y电容优化"
    - failure: "辐射发射超标(30MHz-1GHz)"
      solution: "屏蔽设计，电缆管理，接地优化"
    - failure: "ISM频段外发射"
      solution: "带外抑制滤波器，谐波滤波"

compliance_information:
  mandatory_regions: ["全球通用", "欧盟", "北美", "亚太"]
  certification_bodies: ["TUV", "SGS", "Intertek", "UL", "CSA"]
  mutual_recognition: ["IECEE-CB", "ILAC-MRA", "APLAC-MRA"]

# ========== 文档管理信息 ==========
document_management:
  creation_date: 2024-01-01
  last_review_date: 2025-06-16
  next_review_date: 2026-01-01
  revision_history:
    - version: "Ed.6.0"
      date: 2024-01-01
      changes: "增加工业机器人特殊要求，按照EMI标准模板重构"
      impact_assessment: "扩展ISM设备覆盖范围，提升技术完整性"

quality_assurance:
  technical_reviewer: "CISPR技术专家委员会"
  validation_method: "国际标准制定程序验证"
  peer_review_status: "已完成国际同行评议"
---

# CISPR 11:2024 - 工业、科学和医疗设备射频骚扰特性

## 标准概要

CISPR 11:2024 是国际电工委员会无线电干扰特别委员会（CISPR）发布的第六版工业、科学和医疗(ISM)设备射频骚扰特性标准，适用于**在9 kHz到400 GHz频率范围内工作的ISM设备的电磁发射限值与测量方法**。标准自2024年1月发布，替代2015版本，重要更新包括**增加工业机器人的特殊要求**，涵盖**传导发射**（150 kHz–30 MHz）及**辐射发射**（30 MHz–18 GHz），按照设备用途分为Group 1和Group 2两组，按照使用环境分为Class A和Class B两类，对各类ISM设备的骚扰电平做出明确限值规定。

## 2024版主要技术变化

### 设备范围扩展
- **工业机器人**：新增工业机器人的特殊EMC要求
- **新兴ISM技术**：覆盖新型感应加热、等离子处理等设备
- **测量方法优化**：针对新设备配置调整测试方法

### 限值调整
- **部分限值更新**：针对新设备配置调整相应限值
- **测量不确定度**：更新测量不确定度要求
- **现场测试**：完善Class A设备现场测试要求

### 标准协调
- **国际协调**：与ITU无线电规则更好协调
- **区域标准**：与EN 55011、FCC Part 18等区域标准同步

## 引用标准

- **CISPR 16-1-1:2019** 无线电干扰测量仪器和测量方法 — 第1-1部分：测量仪器要求
- **CISPR 16-2-1:2014** 无线电干扰测量仪器和测量方法 — 第2-1部分：测量方法
- **IEC 61000-3-2:2018** 电磁兼容性 — 限值 — 谐波电流发射限值
- **IEC 61000-3-3:2013** 电磁兼容性 — 限值 — 电压变化、电压波动和闪烁的限值
- **ITU Radio Regulations** 国际电信联盟无线电规则
- **IEC 60335系列** 家用电器安全标准
- **IEC 62233:2005** 人体暴露于RF场的测量方法

## 适用范围与限制

### 适用范围
- **工业设备**：焊接设备、感应加热设备、电弧炉、等离子设备、工业机器人
- **科学设备**：实验室设备、测试仪器、研究设备、半导体制造设备
- **医疗设备**：透热设备、电外科设备、医疗扫描仪、康复设备
- **ISM频段设备**：在指定ISM频段工作的射频设备
- **频率范围**：9 kHz 至 400 GHz

### 限制条件
- 本标准**不涵盖抗扰度（EMS）要求**；不适用于家用电器（由其他CISPR标准覆盖）
- 不涉及人体安全暴露限值（由IEC 62233等标准规定）
- **不适用于电信设备**（由其他CISPR标准覆盖）
- 不涉及功能安全要求

## 技术要求详解

### 设备分组分类系统

#### Group 1设备 - 内部功能型
- **定义**：为内部功能产生和使用射频能量的设备
- **典型设备**：
  - 实验室设备和测试仪器
  - 半导体变频器和开关电源
  - 医疗电子设备（非射频治疗）
  - 工业测量和控制设备
  - 工业机器人和自动化设备

#### Group 2设备 - 有意射频型
- **定义**：有意产生和使用9 kHz-400 GHz射频能量的设备
- **典型设备**：
  - 微波炉和射频加热设备
  - 医疗透热和电外科设备
  - 射频焊接和切割设备
  - 等离子设备和感应加热设备
  - 紫外线照射设备

### 环境分类系统

#### Class A - 工业商业环境
- **定义**：适用于除住宅环境以外的所有场所的设备
- **典型环境**：工业厂房、实验室、医院、商业建筑
- **限值特点**：相对宽松的发射限值
- **测试要求**：可现场测试或实验室测试

#### Class B - 住宅环境
- **定义**：适用于住宅环境和直接连接到住宅供电网络的设备
- **典型环境**：家庭、小型办公室、轻商业环境
- **限值特点**：严格的发射限值
- **测试要求**：必须在实验室测试

### 传导发射测试（Conducted Emission）

#### 频率范围与测量参数
- **频率范围**：150 kHz – 30 MHz（主要测试范围）
- **测量带宽**：9 kHz（RBW）
- **检波器类型**：准峰值（Quasi-Peak, QP）与平均值（Average, AV）
- **测试电源**：50 µH/50 Ω LISN，50 Ω负载

#### 典型限值示例（dBµV）
| 频率范围 | Class A Group 1 | Class A Group 2 | Class B Group 1 | Class B Group 2 |
|----------|-----------------|-----------------|-----------------|-----------------|
| 150-500 kHz | 79 | 66-56 | 66-56 | 66-56 |
| 0.5-5 MHz | 73 | 56 | 56 | 56 |
| 5-30 MHz | 73 | 60 | 60 | 60 |

*注：Group 2设备限值可能因具体设备类型和功率而异*

### 辐射发射测试（Radiated Emission）

#### 频率范围与测量参数
- **频率范围**：30 MHz – 18 GHz
- **测量带宽**：
  - 30 MHz – 1 GHz：120 kHz
  - 1 GHz – 18 GHz：1 MHz
- **检波器类型**：准峰值（QP）& 平均值（AV）
- **测试距离**：3m（Class B），10m（Class A Group 1），30m（Class A Group 2）

#### 天线系统
- **30 MHz – 300 MHz**：双锥形天线
- **300 MHz – 1 GHz**：对数周期天线
- **1 GHz – 18 GHz**：喇叭天线

#### 典型限值示例（dBµV/m）
| 频率范围 | Class A Group 1 (10m) | Class A Group 2 (30m) | Class B (3m) |
|----------|------------------------|------------------------|--------------|
| 30-230 MHz | 40 | 47 | 30 |
| 230MHz-1GHz | 47 | 47 | 37 |
| 1-18 GHz | 76 | 76 | 74 |

## ISM频段特殊要求

### 指定ISM频段
- **6.765-6.795 MHz**：工业加热
- **13.553-13.567 MHz**：工业、科学应用
- **26.957-27.283 MHz**：工业、科学、医疗
- **40.66-40.70 MHz**：工业、科学、医疗
- **2.4-2.5 GHz**：工业、科学、医疗（微波炉）
- **5.725-5.875 GHz**：工业、科学、医疗
- **24-24.25 GHz**：工业、科学、医疗

### ISM频段内的特殊限值
- **带内发射**：允许更宽松的限值
- **带外发射**：严格控制以保护其他服务
- **谐波发射**：特殊谐波发射限值要求

## 测试设备与环境要求

### 主要测试设备

| 测试项目 | 设备名称 | 技术参数 | 标准要求 |
|----------|----------|----------|----------|
| 传导发射 | LISN | 50µH/50Ω | CISPR 16-1-2 |
| | EMI接收机 | 9kHz-30MHz | CISPR 16-1-1 |
| | 电流探头 | 10kHz-30MHz | 转移阻抗校准 |
| 辐射发射 | 半消声室 | 30MHz-18GHz | 反射衰减≥20dB |
| | 天线系统 | 多频段覆盖 | 天线因子校准 |
| | 转台 | 360°旋转 | 方位角精度±1° |
| 环境控制 | 温湿度控制 | ±2°C, ±5%RH | 环境稳定性 |

### 环境条件要求
- **温度**：15–35°C（环境温度稳定性±2°C）
- **湿度**：45–75% RH（相对湿度稳定性±5%）
- **大气压力**：86–106 kPa
- **电磁环境**：背景噪声比限值低6dB以上

## 测试程序与操作要点

### 预试验准备
1. **设备校准**
   - 校准所有测量仪器和天线系统
   - 验证天线因子和电缆损耗
   - 检查LISN性能参数

2. **环境检查**
   - 确认测试环境符合标准要求
   - 测量背景噪声水平
   - 检查屏蔽室或暗室性能

3. **DUT准备**
   - 确认被测设备工作状态正常
   - 检查电源线、接口连接状态
   - 设置DUT典型工作模式

### 传导发射测试程序
1. **测试设置**
   - 将被测线缆通过LISN接入接地网
   - 连接EMI接收机或频谱分析仪
   - 设置适当的测量参数

2. **测量执行**
   - 扫描150 kHz–30 MHz频率范围
   - 记录准峰值（QP）和平均值（AV）
   - 识别超标频点进行精确测量

3. **结果判定**
   - 对照相应分类限值表
   - QP值≤限值，AV值≤限值-6dB

### 辐射发射测试程序
1. **测试设置**
   - 将DUT置于消声室中央转台上
   - 设置天线高度扫描范围（1-4m）
   - 配置水平和垂直极化测试

2. **测量执行**
   - 天线高度扫描寻找最大发射
   - 转台旋转360°寻找最大方位角
   - 记录最大发射值的频率和方位

3. **数据记录**
   - 记录各频点QP和AV值
   - 标注最大发射方位和天线高度
   - 绘制频谱图和极坐标图

## 特殊设备测试要求

### 微波炉测试
- **工作状态**：标准负载（1升水）
- **测试功率**：额定功率
- **特殊要求**：门密封性能检查
- **安全考虑**：RF泄漏测量

### 医疗透热设备
- **患者模拟**：标准假体或等效负载
- **功率设置**：临床典型功率
- **频率稳定性**：载波频率监测
- **安全要求**：人体暴露限值验证

### 感应加热设备
- **负载条件**：标准金属负载
- **功率控制**：各档位功率测试
- **频率监测**：工作频率稳定性
- **谐波分析**：谐波发射特性

### 工业机器人（2024新增）
- **运动状态**：典型工作循环
- **负载条件**：额定负载
- **控制系统**：完整控制链路
- **安全功能**：安全系统正常工作

## 性能评估与判定准则

### 通过准则
- **传导发射**：所有测点QP ≤ 规定限值，AV ≤ 限值-6dB
- **辐射发射**：QP ≤ 限值，AV ≤ 限值-6dB
- **重复性要求**：三次测量结果偏差 ≤ 2dB
- **频率稳定性**：ISM频段内工作频率稳定

### 测量不确定度
- **传导发射**：典型不确定度 ±2dB
- **辐射发射**：典型不确定度 ±3dB
- **环境影响**：温度湿度变化引起的偏差 <1dB

## 与相关标准的关系

### CISPR标准族
- **[[CISPR 16]]**：测量仪器和方法标准，提供测试设备技术要求
- **[[CISPR 12]]**：车辆EMC标准，汽车ISM设备可能需要同时符合
- **[[CISPR 25]]**：车载设备EMC标准，与车载ISM设备相关

### IEC标准系列
- **[[IEC 61000系列]]**：EMC基础标准，提供通用要求
- **IEC 62233**：人体RF暴露测量方法
- **IEC 60335系列**：家用电器安全标准

### 国家标准对应
- **欧盟**：EN 55011 - 欧洲统一标准
- **美国**：FCC Part 18 - 北美ISM设备标准
- **中国**：[[GB 4824]] - 中国ISM设备标准
- **日本**：VCCI-CISPR11 - 日本信息设备标准

## 测试报告要求

### 必要内容
1. **标准引用**：CISPR 11:2024及相关引用标准版本
2. **被测对象**：设备型号、软硬件版本、工作状态描述
3. **测试环境**：温湿度、大气压、电源条件等环境参数记录
4. **设备信息**：测试设备清单、校准证书、设置参数
5. **测试数据**：频率vs电平数据表格、超标频点详细分析
6. **图表资料**：频谱图、极坐标图、测试现场照片
7. **判定结论**：合格/不合格判定、不合格项原因分析
8. **建议措施**：针对超标项目的整改建议

### 质量控制
- **数据完整性**：确保所有测试点数据记录完整
- **可追溯性**：所有测量设备具有有效校准证书
- **重现性**：提供足够详细的测试条件以便重现
- **审核签字**：测试人员、技术审核、授权签字完整

## 新兴技术挑战

### 工业4.0与智能制造
- **工业机器人**：复杂控制系统EMC要求
- **无线工业通信**：工业WiFi、5G应用
- **边缘计算**：工业边缘计算设备EMC

### 新型ISM技术
- **等离子处理**：新型等离子清洗、改性设备
- **激光加工**：激光切割、焊接设备
- **3D打印**：增材制造设备EMC要求

### 医疗设备发展
- **数字化医疗**：数字医疗设备网络化
- **远程医疗**：远程诊断设备通信
- **人工智能**：AI辅助医疗设备

## 实施指导

### 设计阶段考虑
1. **早期EMC设计**：在产品设计初期考虑CISPR 11要求
2. **分类确认**：明确设备的Group和Class分类
3. **频率规划**：合理规划ISM频段使用

### 测试策略
1. **预合规测试**：开发阶段进行预合规测试
2. **分级测试**：先进行传导发射，再进行辐射发射
3. **现场验证**：Class A设备可进行现场验证测试

### 成本优化
1. **设计优化**：通过滤波、屏蔽等设计降低发射
2. **测试计划**：合理安排预测试和正式测试
3. **标准化**：建立企业内部ISM设备测试流程

---

## 相关资源链接

- **官方标准**：[IEC Webstore - CISPR 11:2024](https://webstore.iec.ch/en/publication/103802)
- **技术指导**：[[CISPR测试方法详解]]
- **设备选型**：[[ISM设备EMC设计指南]]
- **案例分析**：[[工业设备EMC典型问题及解决方案]]

---

*最后更新：2025年6月16日*  
*版本：CISPR 11:2024 Ed.6.0解读*  
*编制：工业设备EMC技术委员会*