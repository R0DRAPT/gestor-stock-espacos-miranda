# Gestor de Stock Web — Espaços Miranda (PAP)

Aplicação web de gestão de stock de mobiliário, desenvolvida em **Vue.js** como **Prova de Aptidão Profissional** do Curso Profissional de Técnico de Gestão e Programação de Sistemas Informáticos — Agrupamento de Escolas Alcaides de Faria, Barcelos (2023/2024).

O projeto foi feito para a empresa **Espaços Miranda** e foi o ponto de partida para o [Gestor Orçamentos](https://github.com/R0DRAPT/gestor-orcamentos-releases), a aplicação que hoje está em produção na empresa.

> Os dados incluídos no repositório são fictícios.

## Funcionalidades

- **Autenticação:** registo e login de utilizadores, com validações e mensagens de sucesso/erro
- **Dois perfis:** utilizador normal e administrador (com chave de acesso adicional)
- **Produtos organizados por categoria:** Sofás, Cadeirões, Consolas, Peças de Decoração, Cadeiras, Banquetas, Mesas de Cabeceira, Camas e Mesas
- **Tabelas de produtos com filtros**, em páginas próprias para cada categoria
- **Componentes de cada produto** e cálculo automático do preço final (soma dos componentes + IVA a 23%)
- **Área de administração:** gestão de todos os utilizadores (editar e eliminar) e funcionalidades adicionais nas páginas de produto
- **Definições de conta:** cada utilizador pode editar ou eliminar a sua conta
- Componentes reutilizáveis (Navbar, Banner, Footer) e página de contactos

## Tecnologias

| Camada | Tecnologia |
|---|---|
| Interface | Vue.js 3, Vue Router, Bootstrap, Font Awesome |
| Dados | json-server a partir de `db/db.json` (API REST local), Axios |
| Testes de API | Postman |

## Como executar

### Pré-requisitos
- [Node.js](https://nodejs.org/) e npm

### Passos

```bash
# Instalar dependências
npm install

# Iniciar o servidor de dados (API local em http://localhost:3000)
npm run backend

# Noutro terminal, iniciar a aplicação (http://localhost:8080)
npm run serve
```

**Contas de teste:**
| Perfil | Utilizador | Password |
|---|---|---|
| Administrador | admin | admin123 (chave de acesso: `demo`) |
| Utilizador | utilizador | teste123 |

## Limitações e próximos passos

Este foi o meu primeiro projeto completo em Vue.js. Algumas decisões refletem esse contexto:
- Os dados são guardados num ficheiro JSON servido por um servidor simulado, em vez de uma base de dados real.
- As passwords não são encriptadas.

A evolução prevista era migrar os dados para **MySQL** e criar uma API própria. Essas ideias acabaram por ser aplicadas no [Gestor Orçamentos](https://github.com/R0DRAPT/gestor-orcamentos-releases), com servidor Node.js e base de dados SQLite.

## Autor

**Rodrigo Miranda** — [GitHub](https://github.com/R0DRAPT) · [LinkedIn](https://www.linkedin.com/in/rodrigo-miranda-dev)
