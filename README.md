# 🌱 EcoFood - Protótipo Interativo Contra o Desperdício de Alimentos

O **EcoFood** é um protótipo de aplicativo móvel desenvolvido como uma **SPA (Single Page Application)** em um único arquivo HTML. O objetivo central do aplicativo é mitigar o desperdício de comida doméstico utilizando alertas de validade inteligentes, sugestões de receitas personalizadas com base no que está vencendo e integração comunitária para doações.

Este repositório contém a interface de alta fidelidade simulando **8 telas principais** mapeadas a partir dos requisitos do projeto.

---

## 📱 Telas Mapeadas no Protótipo

1. **Tela de Login:** Acesso seguro com e-mail/senha e suporte a login social (Google e Apple).
2. **Dashboard (Início):** Visão geral de métricas (itens salvos, economia em R$) e alertas urgentes de alimentos que estão vencendo hoje ou nos próximos dias.
3. **Minha Dispensa:** Inventário completo de mantimentos com filtros por categorias (Urgente, Geladeira, Secos) e status visual de validade (Verde, Amarelo, Vermelho).
4. **Receitas Inteligentes:** Sugestões culinárias focadas em "Zero Desperdício", priorizando o uso imediato dos ingredientes que estão na data limite de consumo.
5. **Lista de Compras Automatizada:** Sugestões preditivas geradas por Inteligência Artificial para evitar compras redundantes baseadas no histórico do usuário.
6. **Doações Coletivas:** Espaço para compartilhar alimentos excedentes com vizinhos ou instituições próximas geograficamente.
7. **Configurações:** Customização de perfil, gerenciamento de notificações de validade e ajustes de preferências (como Modo Escuro).
8. **Escanear Cupom/Alimento:** Simulação de uso da câmera (com efeito de laser de escaneamento) para cadastrar produtos rapidamente via código de barras.

---

## 🛠️ Tecnologias Utilizadas

Para garantir a máxima portabilidade e facilidade de execução, todo o aplicativo foi construído usando a stack nativa da web:

* **HTML5:** Estrutura semântica dos blocos de conteúdo e das seções de cada tela.
* **CSS3 moderno:** Layout responsivo simulando a moldura e a proporção de um smartphone padrão (375px x 812px), uso de variáveis CSS para paleta de cores (Dark Mode nativo) e animações de transição suaves (`@keyframes slideUp`).
* **JavaScript (Vanilla):** Lógica interna para gerenciar o roteamento dinâmico entre as telas sem recarregar a página, além de simulações interativas (como ativação de botões, seleção de abas e comportamento de checkboxes).

---

## 🚀 Como Executar o Projeto

Como o protótipo foi unificado, você não precisa instalar nenhuma dependência, node_modules ou servidores locais.

1. Baixe ou copie o arquivo `index.html` deste projeto.
2. Dê um duplo clique no arquivo `index.html` ou arraste-o para dentro de qualquer navegador web (Chrome, Edge, Safari, Firefox).
3. Para uma experiência ainda mais fiel de aplicativo, abra as **Ferramentas do Desenvolvedor** no seu navegador (F12 ou Ctrl+Shift+I) e ative a **Visualização Responsiva de Dispositivos Móveis**.

---

## 🔄 Lógica de Navegação Interna

O controle de visualização é feito inteiramente pelo JavaScript através da manipulação do DOM:
* A função `changeScreen(screenId)` esconde os contêineres inativos adicionando/removendo classes CSS e atualiza os estados visuais da barra inferior.
* A barra de navegação inferior (`bottom-nav-bar`) oculta-se automaticamente na tela de login para simular o fluxo de autenticação real de um aplicativo móvel.
