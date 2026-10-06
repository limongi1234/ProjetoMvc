# ProjetoMVC — Agenda de Contatos

Aplicação web **ASP.NET Core MVC** com **Entity Framework Core** e **SQL Server** para cadastrar, listar, editar e excluir contatos. Projeto desenvolvido durante a trilha .NET da DIO.

## Tecnologias

- C# / ASP.NET Core MVC (Razor Views)
- Entity Framework Core (SQL Server) com Migrations
- Bootstrap e jQuery Validation

## Funcionalidades

| Rota | Tela |
|---|---|
| `/Contato` | Lista de contatos |
| `/Contato/Criar` | Cadastro de contato |
| `/Contato/Editar/{id}` | Edição de contato |
| `/Contato/Detalhes/{id}` | Detalhes do contato |
| `/Contato/Deletar/{id}` | Confirmação de exclusão |

## Como executar

Pré-requisitos: [.NET 10 SDK](https://dotnet.microsoft.com/download) e SQL Server (Express ou LocalDB).

1. Ajuste a connection string `ConexaoPadrao` em `appsettings.Development.json` se o seu servidor não for `localhost\sqlExpress`.
2. Crie o banco aplicando as migrations:
   ```bash
   dotnet tool install --global dotnet-ef
   dotnet ef database update
   ```
3. Rode a aplicação:
   ```bash
   dotnet run
   ```
4. Acesse `https://localhost:<porta>/Contato`.

## Estrutura

```
Context/      DbContext (AgendaContext)
Controllers/  ContatoController e HomeController
Migrations/   Migrations do EF Core
Models/       Contato e ErrorViewModel
Views/        Telas Razor (Contato, Home, Shared)
wwwroot/      CSS, JS e bibliotecas front-end
```
