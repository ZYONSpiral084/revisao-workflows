# Revisão Workflows - Fatec Ourinhos

Este repositório foi criado como parte de uma **tarefa acadêmica da Fatec Ourinhos**.  
O objetivo é demonstrar a utilização de **Workflows Reutilizáveis no GitHub Actions**.

## 📌 Estrutura

- **ci.yml** → Workflow reutilizável que recebe uma mensagem como parâmetro e a exibe nos logs.  
- **teste.yml** (no repositório [Nycolas-Salvego](https://github.com/Nycolas-Salvego)) → Workflow que chama o `ci.yml` deste repositório e envia a mensagem *"Teste Realizado com sucesso"*.

## 🚀 Funcionamento
- Ao realizar um **push** ou **pull request**, o workflow `teste.yml` é disparado.  
- Ele chama o workflow definido em `ci.yml` deste repositório.  
- A mensagem configurada é exibida como log no job.

## 👤 Autor
Workflow reutilizado por **Nycolas-Salvego** (ZYONSpiral084).  
Projeto acadêmico da **Fatec Ourinhos**.
