# 功能卡

# 功能卡模板

每个候选功能必须转换成结构化功能卡。

```yaml
feature:
  id:
  name:
  product_type: dashboard | tracker | action_workspace
  user_problem:
  user_quote:
  user_story:
  typical_scenario:
  frequency:
  type: display | record | action
  priority: P0 | P1 | P2

  trigger:
    type: open_page | manual_input | schedule | external_event
    details:

  input:
    fields: []
    source:

  processing:
    steps: []
    ai_required: false
    human_confirmation: false

  output:
    result:
    destination:

  data:
    source_type: manual | local_file | third_party | ai_generated
    source_details:
    update_frequency:
    storage:
    backup:
    export:

  integration:
    external_tool_exists: false
    external_tool:
    recommended_strategy: self_build | embed | sync | keep_external
    auth_required: false
    api_required: false
    estimated_cost:

  privacy:
    sensitive_data: []
    risks: []
    mitigation: []

  states:
    empty_state:
    loading_state:
    error_state:
    offline_state:

  actions: []

  failure_handling:
    user_message:
    retry:
    data_protection:

  acceptance_criteria: []

  score:
    frequency:
    pain:
    time_saved:
    risk_reduction:
    implementation_cost:
    maintenance_cost:
    total:

  release:
    decision: current | future | reject
    reason:
```

## 真实功能四问

每个功能必须回答：

1. 数据从哪里来？
2. 用户如何触发？
3. 系统实际执行什么？
4. 失败时会发生什么？

无法回答任意一项：

- 不进入当前版本
- 不允许用占位内容伪装
- 标记为未来功能或待确认

## 现有工具替代判断

必须判断：

- 是否已有成熟工具？
- 自建是否真的少步骤？
- 是否更适合嵌入？
- 是否更适合同步关键数据？
- 是否继续保留原工具？

策略：

- self_build
- embed
- sync
- keep_external

---
