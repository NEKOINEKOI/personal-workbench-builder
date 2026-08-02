# 关键任务闭环

# 关键任务闭环模板

每套工作台至少定义一条完整闭环。

```yaml
core_workflow:
  id:
  name:
  user_goal:
  trigger:
  actors:
    - user
    - system
    - ai
    - external_service

  steps:
    - step:
      actor:
      input:
      action:
      output:
      next_step:

  completion_result:
  saved_record:
  success_signal:
  failure_points: []
  failure_recovery: []
  related_features: []
```

## 判断标准

一条闭环必须回答：

- 用户最终想完成什么？
- 什么情况下开始？
- 第一步是什么？
- 中间每一步由谁完成？
- 结果是什么？
- 结果保存在哪里？
- 如何判断完成？
- 失败后如何继续？

如果多个模块无法连成一条完整任务路径，说明当前方案只是功能拼盘，需要重新调整。

## 验收要求

验收时必须让用户完成一次真实闭环：

- 使用真实输入
- 经过完整步骤
- 生成真实结果
- 保存真实记录
- 刷新后仍可找到
- 失败时可以恢复

---
