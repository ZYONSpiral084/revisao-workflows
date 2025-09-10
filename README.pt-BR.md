# 🔄 Revisão Workflows - Fatec Ourinhos
**2025-09-09**

**Idiomas:** [English](README.md) • [Português (pt-BR)](README.pt-BR.md) • [中文（简体）](README.zh-CN.md)

---

## 📌 Objetivo do Repositório

Este repositório foi criado como parte de uma tarefa acadêmica da Fatec Ourinhos. O objetivo é demonstrar a utilização de Workflows Reutilizáveis no GitHub Actions. Inclui um `ci.yml` reutilizável que outros repositórios podem chamar.

---

## 📌 Estrutura

- **ci.yml** → Workflow reutilizável que recebe uma mensagem como parâmetro e exibe nos logs.  
- **teste.yml** (no repositório [Nycolas-Salvego](https://github.com/Nycolas-Salvego)) → Workflow que chama o `ci.yml` deste repositório e envia a mensagem *"Teste Realizado com sucesso"*.

---

## 🚀 Funcionamento

- Em push ou pull request, o workflow `teste.yml` é disparado.  
- Ele chama `ci.yml` usando `uses: owner/repo/.github/workflows/ci.yml@ref` e passa o input `message`.  
- A mensagem é exibida nos logs do job.

---

## 👤 Autor

Workflow reutilizado por **Nycolas-Salvego** (ZYONSpiral084). Projeto acadêmico da **Fatec Ourinhos**.

---

## 🧭 Exemplo de uso

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

Substitua o `owner/repo` e `@main` conforme necessário.

---

## 📜 Licença

Uso acadêmico / educacional. Cite o autor ao reutilizar.
