# 🔄 Workflows Review - Fatec Ourinhos / Revisão Workflows - Fatec Ourinhos  

| 🇺🇸 English | 🇧🇷 Português |
|-------------|--------------|
| This repository was created as part of an **academic assignment at Fatec Ourinhos**.<br>The goal is to demonstrate the use of **Reusable Workflows in GitHub Actions**. | Este repositório foi criado como parte de uma **tarefa acadêmica da Fatec Ourinhos**.<br>O objetivo é demonstrar a utilização de **Workflows Reutilizáveis no GitHub Actions**. |

---

## 📌 Structure / Estrutura  

| 🇺🇸 English | 🇧🇷 Português |
|-------------|--------------|
| - **ci.yml** → Reusable workflow that receives a message as a parameter and displays it in the logs.<br>- **teste.yml** (in the repository [Nycolas-Salvego](https://github.com/Nycolas-Salvego)) → Workflow that calls the `ci.yml` from this repository and sends the message *"Teste Realizado com sucesso"*. | - **ci.yml** → Workflow reutilizável que recebe uma mensagem como parâmetro e a exibe nos logs.<br>- **teste.yml** (no repositório [Nycolas-Salvego](https://github.com/Nycolas-Salvego)) → Workflow que chama o `ci.yml` deste repositório e envia a mensagem *"Teste Realizado com sucesso"*. |

---

## 🚀 How it Works / Funcionamento  

| 🇺🇸 English | 🇧🇷 Português |
|-------------|--------------|
| - On **push** or **pull request**, the `teste.yml` workflow is triggered.<br>- It calls the workflow defined in `ci.yml` from this repository.<br>- The configured message is displayed as a log in the job. | - Ao realizar um **push** ou **pull request**, o workflow `teste.yml` é disparado.<br>- Ele chama o workflow definido em `ci.yml` deste repositório.<br>- A mensagem configurada é exibida como log no job. |

---

## 👤 Author / Autor  

| 🇺🇸 English | 🇧🇷 Português |
|-------------|--------------|
| Workflow reused by **Nycolas-Salvego** (ZYONSpiral084).<br>Academic project from **Fatec Ourinhos**. | Workflow reutilizado por **Nycolas-Salvego** (ZYONSpiral084).<br>Projeto acadêmico da **Fatec Ourinhos**. |
