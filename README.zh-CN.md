# 🔄 Workflows 复审 - Fatec Ourinhos
**2025-09-09**

**语言：** [English](README.md) • [Português (pt-BR)](README.pt-BR.md) • [中文（简体）](README.zh-CN.md)

---

## 📌 仓库目的

本仓库为 Fatec Ourinhos 的学术作业而创建，旨在演示在 GitHub Actions 中使用可重用工作流（Reusable Workflows）。仓库包含可被其他项目调用的 `ci.yml`。

---

## 📌 结构

- **ci.yml** → 可重用工作流，接收消息参数并在日志中显示。  
- **teste.yml**（位于仓库 [Nycolas-Salvego](https://github.com/Nycolas-Salvego)）→ 调用本仓库的 `ci.yml` 并发送消息 *"Teste Realizado com sucesso"*。

---

## 🚀 工作原理

- 在 push 或 pull request 时触发 `teste.yml`。  
- 使用 `uses: owner/repo/.github/workflows/ci.yml@ref` 调用 `ci.yml` 并传递 `message`。  
- 消息将显示在作业日志中。

---

## 👤 作者

工作流由 **Nycolas-Salvego**（ZYONSpiral084）复用。学术项目：**Fatec Ourinhos**。

---

## 🧭 使用示例

```yaml
# .github/workflows/consume-ci.yml
name: Test Reusable CI
on: [push]
jobs:
  call-ci:
    uses: Nycolas-Salvego/WorkflowsReview/.github/workflows/ci.yml@main
    with:
      message: "Teste Realizado com sucesso"
```

---

## 📜 许可证

学术 / 教育用途。重复使用请注明作者。
