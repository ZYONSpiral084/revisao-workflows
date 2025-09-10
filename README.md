# 🔄 Workflows Review - Fatec Ourinhos / Revisão Workflows - Fatec Ourinhos
**2025-09-09**

**Languages:** [English](README.md) • [Português (pt-BR)](README.pt-BR.md) • [中文（简体）](README.zh-CN.md)

---

## 📌 Repository Purpose / Objetivo do Repositório / 仓库目的

| 🇺🇸 English | 🇧🇷 Português | 🇨🇳 中文（简体） |
|---|---|---|
| This repository was created as part of an **academic assignment at Fatec Ourinhos**. The goal is to demonstrate the use of **Reusable Workflows in GitHub Actions**. It contains a reusable `ci.yml` that other repositories can call. | Este repositório foi criado como parte de uma **tarefa acadêmica da Fatec Ourinhos**. O objetivo é demonstrar a utilização de **Workflows Reutilizáveis no GitHub Actions**. Inclui um `ci.yml` reutilizável que outros repositórios podem chamar. | 本仓库为 Fatec Ourinhos 的学术作业而创建。目标是演示在 GitHub Actions 中使用**可重用工作流（Reusable Workflows）**。仓库包含可被其他项目调用的 `ci.yml`。 |

---

## 📌 Structure / Estrutura / 结构

| 🇺🇸 English | 🇧🇷 Português | 🇨🇳 中文（简体） |
|---|---|---|
| - **ci.yml** → Reusable workflow that receives a message as a parameter and displays it in the logs.<br>- **teste.yml** (in repository [Nycolas-Salvego](https://github.com/Nycolas-Salvego)) → Workflow that calls `ci.yml` from this repo and sends the message *"Teste Realizado com sucesso"*. | - **ci.yml** → Workflow reutilizável que recebe uma mensagem como parâmetro e a exibe nos logs.<br>- **teste.yml** (no repositório [Nycolas-Salvego](https://github.com/Nycolas-Salvego)) → Workflow que chama o `ci.yml` deste repositório e envia a mensagem *"Teste Realizado com sucesso"*. | - **ci.yml** → 可重用工作流，接收一个消息参数并在日志中显示。<br>- **teste.yml**（位于仓库 [Nycolas-Salvego](https://github.com/Nycolas-Salvego)）→ 调用本仓库的 `ci.yml` 并发送消息 *"Teste Realizado com sucesso"*。 |

---

## 🚀 How it Works / Funcionamento / 工作原理

| 🇺🇸 English | 🇧🇷 Português | 🇨🇳 中文（简体） |
|---|---|---|
| - On **push** or **pull request**, the `teste.yml` workflow is triggered.<br>- It calls the workflow defined in `ci.yml` from this repository using `uses: owner/repo/.github/workflows/ci.yml@ref` and passes the message input.<br>- The configured message is displayed as a log in the job. | - Ao realizar um **push** ou **pull request**, o workflow `teste.yml` é disparado.<br>- Ele chama o workflow definido em `ci.yml` deste repositório usando `uses: owner/repo/.github/workflows/ci.yml@ref` e passa o input `message`.<br>- A mensagem configurada é exibida como log no job. | - 在 **push** 或 **pull request** 时触发 `teste.yml` 工作流。<br>- 使用 `uses: owner/repo/.github/workflows/ci.yml@ref` 调用本仓库中的 `ci.yml` 并传递 `message` 输入。<br>- 配置的消息会在作业日志中显示。 |

---

## 👤 Author / Autor / 作者

| 🇺🇸 English | 🇧🇷 Português | 🇨🇳 中文（简体） |
|---|---|---|
| Workflow reused by **Nycolas-Salvego** (ZYONSpiral084). Academic project from **Fatec Ourinhos**. | Workflow reutilizado por **Nycolas-Salvego** (ZYONSpiral084). Projeto acadêmico da **Fatec Ourinhos**. | 工作流由 **Nycolas-Salvego**（ZYONSpiral084）复用。学术项目：**Fatec Ourinhos**。 |

---

## 🧭 Usage example / Exemplo de uso / 使用示例

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

Replace `Nycolas-Salvego/WorkflowsReview` and `@main` with the actual owner/repo and ref if different.

---

## 📜 License / Licença / 许可证

| 🇺🇸 English | 🇧🇷 Português | 🇨🇳 中文（简体） |
|---|---|---|
| Academic / educational use. Please cite the author when reusing. | Uso acadêmico / educacional. Cite o autor ao reutilizar. | 学术 / 教育用途。重复使用请注明作者。 |
