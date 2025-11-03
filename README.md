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

* cite_start**Veterinários:** CRUD completo para cadastro, listagem, edição e exclusão de veterinários[cite: 13].
* [cite_start]**Donos:** CRUD completo para gerenciamento de clientes/donos de animais[cite: 55]. [cite_start]A página de detalhes do dono exibe todos os animais sob sua tutela[cite: 56].
* [cite_start]**Animais:** CRUD completo para registro de animais[cite: 58]. [cite_start]Permite a seleção do Dono e do Veterinário responsável no cadastro[cite: 61, 73].

## 🔒 Regras de Segurança e Autorização

* [cite_start]**Autenticação:** O acesso a qualquer página/servlet (exceto login.jsp) é bloqueado se o usuário (Veterinário) não estiver logado (Filtro de Autenticação)[cite: 18, 19, 41, 125].
* [cite_start]**Autorização:** Apenas veterinários logados podem criar, editar e excluir veterinários, donos e animais[cite: 42].
* [cite_start]**Restrição de Edição/Exclusão de Animal:** Apenas o **veterinário responsável** pode editar ou excluir um animal específico[cite: 60, 105, 126].

* ## 📐 Estrutura Técnica e Arquitetura

O projeto segue um padrão MVC (Model-View-Controller) simplificado:

| Componente | Responsável | Descrição |
| :--- | :--- | :--- |
| **Model** | Hugo e Luan | [cite_start]Contém as classes de modelo (`Veterinario.java`, `Dono.java`, `Animal.java`) e as classes DAO para acesso ao banco de dados (`VeterinarioDAO.java`, `DonoDAO.java`, `AnimalDAO.java`)[cite: 3, 4, 5, 44, 45, 46, 47, 48]. |
| **Controller** | Hugo e Luan | [cite_start]Implementado via **Servlets** (`LoginServlet`, `VeterinarioServlet`, `DonoServlet`, `AnimalServlet`) para processar requisições e gerenciar a lógica de negócio[cite: 6, 7, 12, 53, 54, 57]. [cite_start]Inclui o `AuthFilter` para controle de acesso[cite: 18]. |
| **View** | Hugo e Luan | [cite_start]Páginas **JSP** para interface com o usuário (`login.jsp`, `dashboard.jsp`, `veterinarios.jsp`, etc.) e formulários de cadastro/edição[cite: 20, 65, 114]. |

## ⚙️ Banco de Dados (SQL)

O sistema utiliza um banco de dados relacional com as seguintes tabelas e relacionamentos:

* [cite_start]**Tabelas Criadas:** `veterinarios`, `donos`, `animais`[cite: 29, 77, 85, 127].
* [cite_start]**Relacionamentos Chave:** O relacionamento entre as tabelas `animais` e `donos` e `animais` e `veterinarios` é feito por **chaves estrangeiras** (`FOREIGN KEY`)[cite: 92, 93, 94, 95].
    * [cite_start]Um animal só pode ter um dono e um veterinário[cite: 103].
    * [cite_start]Um dono pode ter vários animais[cite: 104].
* [cite_start]**Dados de Teste:** O projeto inclui scripts SQL para criar e preencher as tabelas com dados iniciais de teste[cite: 28, 37, 96, 99, 127].

* ## 💻 Configuração e Execução do Projeto

### Pré-requisitos
* JDK 8+
* Servidor de Aplicação (Ex: Apache Tomcat)
* Sistema de Banco de Dados (Ex: MySQL ou H2)

### Passos:
1.  **Configuração do Banco de Dados:**
    * Crie o banco de dados.
    * [cite_start]Execute os scripts SQL contidos no arquivo ZIP (Criação de tabelas e inserção de dados de teste de `veterinarios`, `donos` e `animais`)[cite: 28, 76, 127].
    * [cite_start]*Credenciais de teste:* Hugo (`usuario: hugo`, `senha: 1234`), Ana (`usuario: ana`, `senha: abcd`)[cite: 38, 39].
2.  **Configuração da Aplicação:**
    * [cite_start]Ajuste as configurações de conexão JDBC no projeto (se necessário)[cite: 108].
    * Implante o projeto no Servidor de Aplicação (Tomcat).
3.  **Acesso:**
    * Acesse a URL principal. [cite_start]Você será redirecionado para `login.jsp`[cite: 19, 21].
    * Faça o login com as credenciais de teste fornecidas acima.
