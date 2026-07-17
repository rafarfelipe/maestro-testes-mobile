# ShopDemo - Automação Mobile com Maestro

[![Maestro](https://img.shields.io/badge/Maestro-Framework-blue)](https://maestro.mobile.dev/)
[![Android](https://img.shields.io/badge/Platform-Android-green)]()
[![CI/CD](https://img.shields.io/badge/CI-GitHub%20Actions-orange)]()
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Este projeto demonstra a automação de testes *end-to-end* (E2E) para o aplicativo **ShopDemo**, utilizando o **Maestro**, um framework moderno e de alta performance para automação mobile.

## 🚀 Sobre o Projeto

O objetivo deste projeto é validar fluxos críticos de uma aplicação de e-commerce mobile, garantindo que as funcionalidades principais — como login, catálogo, carrinho e checkout — funcionem corretamente. Além da automação funcional, o foco foi **garantir a estabilidade dos testes em ambientes de Integração Contínua (CI)**, resolvendo desafios comuns de carregamento em emuladores e estados de aplicação.

## 🛠 Principais Desafios e Soluções

*   **Estabilidade na CI:** Problemas com emuladores offline e timeout de renderização foram resolvidos otimizando o workflow do GitHub Actions e implementando lógicas de login resilientes.
*   **Testes Condicionais:** O subfluxo de login foi refatorado para ser condicional, permitindo que os testes detectem o estado atual do app e evitem interações desnecessárias ou redundantes.
*   **Boas Práticas de Automação:** Implementação de uma estrutura modular de *flows* e *subflows*, facilitando a manutenção e a reutilização de cenários de teste.

## 📱 Fluxos Automatizados

| Fluxo | Descrição |
| :--- | :--- |
| `CT-001-login` | Valida o fluxo de login com sucesso. |
| `CT-002-catalogo` | Navegação e validação de produtos no catálogo. |
| `CT-003-carrinho` | Adição de produtos e fluxo de checkout. |
| `CT-004-e2e-compra`| Cenário completo de ponta a ponta. |
| `CT-005-logica` | Teste com lógica condicional. |
| `CT-006-scroll` | Validação de elementos via *scroll* e repetição. |

## ⚙️ Tecnologias Utilizadas

*   **Maestro CLI:** Framework principal de testes.
*   **Android SDK:** Emulação e execução de testes.
*   **GitHub Actions:** Pipeline de CI/CD para execução automática dos testes em cada *push*.

## 🚀 Como Executar

### Pré-requisitos
*   [Maestro instalado](https://maestro.mobile.dev/getting-started/installing-maestro)
*   Android SDK configurado

### Executando Localmente
```bash
# Executar toda a suíte
maestro test flows/s3-suite-shopdemo/

# Executar um fluxo específico
maestro test flows/s3-suite-shopdemo/CT-001-login.yaml
```

---
*Desenvolvido para fins de demonstração de competências em Automação Mobile e Qualidade de Software.*
