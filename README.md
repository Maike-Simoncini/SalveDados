# 💾 Salve Dados

O **Salve Dados** é um gerenciador de informações pessoais leve, rápido e totalmente focado em privacidade. O aplicativo roda de forma 100% independente no navegador (front-end estático) e não depende de servidores externos ou bancos de dados pesados, utilizando recursos nativos da web para guardar e exportar suas informações de maneira segura.

---

## ✨ Funcionalidades

*   **Cadastro de Registros:** Formulário completo para salvar Nome, E-mail, CPF, RG, Telefone e Chave Pix.
*   **Persistência Offline:** Os dados permanecem guardados mesmo se você fechar o navegador ou reiniciar o computador, utilizando o `LocalStorage`.
*   **Visualização e Controle:** Tabela dinâmica e responsiva que lista os registros com a opção de excluir itens individualmente.
*   **Backup em .txt:** Um botão dedicado que processa todos os dados salvos e gera um arquivo de texto limpo e organizado direto para a sua pasta de downloads.
*   **Feedback Inteligente (Toast):** Sistema de notificação fluida no canto da tela que confirma visualmente quando o arquivo foi baixado com sucesso.
*   **Design Dark Mode:** Interface escura moderna e confortável aos olhos estruturada com Tailwind CSS.

---

## 🛠️ Tecnologias Utilizadas

O projeto preza pela simplicidade e portabilidade, utilizando apenas a tríade padrão da web moderna sem necessidade de build (`npm install`):

*   **HTML5:** Estruturação semântica da aplicação.
*   **Tailwind CSS:** Estilização responsiva via CDN utilizando o ecossistema utilitário nativo.
*   **JavaScript (ES6+):** Manipulação dinâmica do DOM, consumo da API do `LocalStorage` e geração física de arquivos usando `Blob`.

---

## ⚙️ Como o Backup .txt Funciona

1.  **Leitura do Banco Local:** Ao clicar em "Salvar Arquivo .txt", o JavaScript lê a string JSON armazenada na chave do navegador.
2.  **Formatação Estruturada:** O script varre o array de objetos e reconstrói as linhas usando caracteres especiais de separação (ex: `====================`), gerando um relatório altamente legível.
3.  **Injeção de Download (Blob API):** Um arquivo temporário invisível é injetado no DOM e o navegador dispara o gatilho de download nativo, nomeando o arquivo com a data atual (ex: `Backup_SalveDados_2026-05-19.txt`).
4.  **Feedback:** O elemento de memória é limpo instantaneamente e a notificação flutuante é disparada para o usuário.

---

## 🚀 Como Executar o Projeto

Por ser uma aplicação *serverless* (sem servidor), você não precisa instalar nenhuma dependência!

1.  Faça o clone ou baixe o arquivo ZIP deste repositório:
    ```bash
    git clone [https://github.com/Maike-Simoncini/SalveDados.git](https://github.com/Maike-Simoncini/SalveDados.git)

 2. Navegue até a pasta do projeto e abra o arquivo **index.html** diretamente no seu navegador padrão (dando um duplo clique sobre ele).

 3. Pronto! O sistema funcionará imediatamente.

