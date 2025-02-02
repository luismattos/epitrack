# 🌿 Epitrack - Estratégia de Branches

Para manter o projeto organizado, seguimos um modelo baseado no **Git Flow** e no **GitHub Flow**.

---

## 📌 Branches Principais
- **`main`** → Branch estável contendo código pronto para produção e documentação revisada.
- **`dev`** → Branch principal de desenvolvimento. Todas as novas funcionalidades e correções são integradas aqui antes de serem movidas para `main`.


---

## 🔀 Branches Temporários
Utilizamos branches temporários para manter o fluxo de desenvolvimento estruturado:

- **`feature/{nome}`** → Para novas funcionalidades. Criado a partir de `dev` e mesclado de volta quando finalizado.
- **`fix/{nome}`** → Para correções de bugs. Criado a partir de `dev` e mesclado de volta após a correção.
- **`hotfix/{nome}`** → Para correções urgentes aplicadas diretamente no `main` (casos raros).

---
