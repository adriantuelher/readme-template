# Readme Template 📜

Bem-vindo(a) ao **Readme Template**! Aqui você encontrará uma variedade de modelos de readme para usar em seus repositórios e perfil no GitHub. Explore nossa coleção de templates e encontre aquele que melhor se adequa ao seu projeto. Comece agora mesmo e deixe o seu readme brilhar!

## Templates de perfil ☕️

Diga adeus aos perfis sem graça. Com nossos **[templates de perfil](https://github.com/iuricode/readme-template/tree/main/perfil)**, você terá um readme de perfil incrível. Com cores vibrantes, imagens surpreendentes e outros elementos visuais cativantes.

## Templates de repositório 🎉

Documente seus projetos com nossos exemplos de **[templates de repositório](https://github.com/iuricode/readme-template/tree/main/repositorio)** incríveis. Esses templates abrangem diversas seções essenciais, incluindo descrição, instalação, uso, contribuição e licença.

## Status e badges shields 🦄

Aperfeiçoe o seu perfil e os seus repositórios adicionando **[cards de status](https://github.com/iuricode/readme-template/tree/main/cards-status/readme.md)** e **[badges shields](https://github.com/iuricode/readme-template/tree/main/badges-shields/readme.md)** ao seu readme. Esses cards proporcionam uma visão aprimorada e detalhada das informações relevantes, tornando o seu perfil e os seus projetos ainda mais impressionantes.

## Formatações avançadas 🔥

Melhore seus readmes adicionando interações com as **[formatações avançadas.](https://github.com/iuricode/readme-template/tree/main/avancado/readme.md)**

## Contribuição ✨

Ajude a comunidade tornando este projeto ainda mais incrível. Leia como contribuir clicando **[aqui](https://github.com/iuricode/readme-template/blob/main/CONTRIBUTING.md)** e a **[licença](https://github.com/iuricode/readme-template/blob/main/LICENSE.md)**. Estou convencido de que juntos alcançaremos coisas incríveis!

## Aprenda desenvolvimento frontend ❤️

Este repositório é um projeto gratuito para a comunidade de desenvolvedores, mas você pode me ajudar comprando o meu ebook "**[eFront - Estudando frontend do zero](https://iuricode.com/efront)**" se estiver interessado em aprender ou melhorar suas habilidades de desenvolvimento frontend. A sua compra me ajuda a produzir e fornecer mais conteúdo gratuito para a comunidade. Adquira agora e comece sua jornada no desenvolvimento frontend.






# 🐶 Sistema de Gerenciamento de Clínica Veterinária

Este projeto é um sistema web básico desenvolvido em Java (Servlets/JSP) para gerenciar dados de Veterinários, Donos e Animais em uma clínica. Inclui funcionalidades de autenticação, controle de acesso e operações CRUD completas.

## 🚀 Funcionalidades Principais

O sistema é dividido nas seguintes áreas:

* **Veterinários:** CRUD completo para cadastro, listagem, edição e exclusão de veterinários.
* **Donos:** CRUD completo para gerenciamento de clientes/donos de animais. A página de detalhes do dono exibe todos os animais sob sua tutela.
* **Animais:** CRUD completo para registro de animais. Permite a seleção do Dono e do Veterinário responsável no cadastro.

---

## 🔒 Regras de Segurança e Autorização

* **Autenticação:** O acesso a qualquer página/servlet (exceto `login.jsp`) é bloqueado se o usuário (Veterinário) não estiver logado. O controle de acesso é realizado por um Filtro de Autenticação (`AuthFilter`).
* **Autorização:** Apenas veterinários logados podem criar, editar e excluir outros veterinários, donos e animais.
* **Restrição de Edição/Exclusão de Animal:** Apenas o **veterinário responsável** pode editar ou excluir um animal específico.

---

## 📐 Estrutura Técnica e Arquitetura

O projeto segue um padrão MVC (Model-View-Controller) simplificado:

| Componente | Responsável | Descrição |
| :--- | :--- | :--- |
| **Model** | Hugo e Luan | Contém as classes de modelo (`Veterinario.java`, `Dono.java`, `Animal.java`) e as classes DAO para acesso ao banco de dados (`VeterinarioDAO.java`, `DonoDAO.java`, `AnimalDAO.java`) com os métodos CRUD necessários. |
| **Controller** | Hugo e Luan | Implementado via **Servlets** (`LoginServlet`, `VeterinarioServlet`, `DonoServlet`, `AnimalServlet`) para processar requisições e gerenciar a lógica de negócio. Inclui o `AuthFilter` para controle de acesso por sessão. |
| **View** | Hugo e Luan | Páginas **JSP** para interface com o usuário (`login.jsp`, `dashboard.jsp`, `veterinarios.jsp`, `animais.jsp`, etc.) e formulários de cadastro/edição, além do layout geral. |

---

## ⚙️ Banco de Dados (SQL)

O sistema utiliza um banco de dados relacional com as seguintes tabelas e relacionamentos:

* **Tabelas Criadas:** `veterinarios`, `donos`, `animais`.
* **Relacionamentos Chave:** O relacionamento entre as tabelas `animais` e `donos` e `animais` e `veterinarios` é feito por **chaves estrangeiras** (`FOREIGN KEY`).
    * Um animal só pode ter um dono e um veterinário.
    * Um dono pode ter vários animais.
* **Dados de Teste:** O projeto inclui scripts SQL para criar e preencher as tabelas com dados iniciais de teste (incluindo dois registros de veterinários e dois de donos/animais).

---

## 💻 Configuração e Execução do Projeto

### Pré-requisitos
* JDK 8+
* Servidor de Aplicação (Ex: Apache Tomcat)
* Sistema de Banco de Dados Relacional (Ex: MySQL ou H2)

### Passos:

1.  **Configuração do Banco de Dados:**
    * Crie o banco de dados.
    * Execute os scripts SQL para a criação das tabelas (`veterinarios`, `donos`, `animais`) e a inserção dos dados de teste.
    * *Credenciais de teste disponíveis:*
        * **Hugo:** `usuario: hugo`, `senha: 1234`
        * **Ana:** `usuario: ana`, `senha: abcd`
2.  **Configuração da Aplicação:**
    * Ajuste as configurações de conexão JDBC no projeto (se necessário, de acordo com o servidor de banco de dados escolhido).
    * Implante o projeto (`.war`) no Servidor de Aplicação (Tomcat).
3.  **Acesso:**
    * Acesse a URL principal do projeto. Você será redirecionado para `login.jsp`.
    * Faça o login com as credenciais de teste fornecidas acima.
