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

Este projeto é um sistema web desenvolvido em Java (Servlets/JSP) para gerenciar algumas informações de uma clínica veterinária. O sistema precisa permitir o cadastro de informações de animais, veterinários e donos de animais e inclui funcionalidades de autenticação, controle de acesso e operações CRUD completas.

## 🚀 Funcionalidades Principais

O sistema é dividido nas seguintes áreas:

* **Veterinários:** Possuem nome, idade, telefone, usuário e senha. O sistema deve possuir CRUD completo para os veterinários.
* **Donos:** Possuem nome, idade, CPF, endereço e telefone. O sistema deve possuir CRUD completo para os donos.
    * Deve existir um mecanismo que permita mostrar todos os animais de um determinado dono.
* **Animais:** Possuem nome, raça, peso e idade. O sistema deve possuir CRUD completo para os animais.
    * Deve existir um mecanismo que permita mostrar todos os animais que um determinado veterinário atende.
    * Um animal só pode ser atendido por um único veterinário, mas um veterinário pode atender vários animais.
* **Páginas de Detalhe:** Para cada animal, dono e veterinário deve existir uma página que mostre todas as suas informações.

---

## 🔒 Regras de Segurança e Autorização

* **Autenticação:** Deve existir um sistema de login para os veterinários.
* **Restrição de Acesso:** Apenas veterinários podem acessar as informações do sistema.
* **Autorização (CRUD):** Apenas veterinários podem se autenticar no sistema para fazer cadastro e edição de donos, animais e outros veterinários.
* **Restrição de Edição/Exclusão de Animal:** Só é permitido excluir ou editar um animal se o veterinário logado for o mesmo que está cuidando daquele animal.

---

## 📐 Estrutura Técnica e Arquitetura

O projeto segue um padrão MVC (Model-View-Controller) simplificado:

| Componente | Classes / Páginas | Relacionamentos e Observações |
| :--- | :--- | :--- |
| **Model** | `Veterinario.java`, `Dono.java`, `Animal.java`, Classes DAO | **Animal-Dono:** Um dono pode ter vários animais, mas cada animal possui apenas um único dono. **Animal-Veterinário:** Um animal só pode ser atendido por um único veterinário. |
| **Controller** | Servlets e `AuthFilter` | Gerencia requisições, lógica de negócio e o filtro de autenticação. |
| **View** | Páginas JSP | Interfaces para o usuário (login, dashboard, listagens, formulários CRUD e páginas de detalhe). |

---

## 💻 Configuração e Execução do Projeto

### Pré-requisitos
* JDK 8+
* Servidor de Aplicação (Ex: Apache Tomcat)
* Sistema de Banco de Dados Relacional.

### Passos:

1.  **Configuração do Banco de Dados:**
    * Execute o SQL para criação do banco de dados com as tabelas de `veterinarios`, `donos` e `animais`.
    * O SQL deve incluir informações prévias para teste .
2.  **Configuração da Aplicação:**
    * Ajuste as configurações de conexão JDBC no projeto.
    * Implante o projeto no Servidor de Aplicação (Tomcat).

---
