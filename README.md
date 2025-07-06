# MyFinance Web - Sistema de Controle Financeiro Pessoal

![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-6.0-blue)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework-6.0-green)
![SQLite](https://img.shields.io/badge/SQLite-3.0-lightgrey)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.0-purple)

## Descrição do Projeto

O **MyFinance Web** é um sistema de controle financeiro pessoal desenvolvido para ajudar famílias a registrar suas receitas e despesas, possibilitando uma análise detalhada dos gastos e um melhor planejamento financeiro.

### Objetivo

Resolver o problema identificado pela pesquisa que mostra que **52% dos brasileiros não possuem ou não sabem como montar um planejamento financeiro** para os próximos anos, oferecendo uma ferramenta simples e eficaz para organização das finanças pessoais.

## Arquitetura Utilizada

### Padrão MVC (Model-View-Controller)
- **Models**: Entidades de dados (PlanoContas, Transacao)
- **Views**: Interface do usuário com Razor Pages
- **Controllers**: Lógica de negócio e controle de fluxo

### Camadas da Aplicação
```
├── Controllers/           # Controladores MVC
├── Models/               # Modelos de dados
├── Views/                # Interfaces de usuário
├── Data/                 # Contexto do banco de dados
├── wwwroot/              # Arquivos estáticos (CSS, JS, imagens)
└── docs/                 # Documentação e scripts
```

### Banco de Dados
- **ORM**: Entity Framework Core 6.0
- **Banco**: SQLite (desenvolvimento)
- **Migrations**: Controle de versão do schema
- **Relacionamentos**: Transacao → PlanoContas (FK)

## Tecnologias

### Backend
- **ASP.NET Core 6.0 MVC** - Framework web
- **Entity Framework Core 6.0** - ORM para acesso a dados
- **SQLite** - Banco de dados leve e portátil
- **C# 10** - Linguagem de programação

### Frontend
- **HTML5 & CSS3** - Estrutura e estilização
- **Bootstrap 5** - Framework CSS responsivo
- **JavaScript ES6** - Interatividade client-side
- **Chart.js** - Biblioteca para gráficos interativos
- **FontAwesome** - Ícones modernos

### Ferramentas de Desenvolvimento
- **.NET CLI** - Interface de linha de comando
- **Entity Framework CLI** - Gerenciamento de migrations
- **Visual Studio / VS Code** - IDEs recomendadas

## Como Configurar para Startup do Projeto

### Pré-requisitos
- [.NET 6.0 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)
- Editor de código (Visual Studio, VS Code, etc.)

### 1️ - Clonar o Repositório
```bash
git clone <url-do-repositorio>
cd myfinance-web-dotnet-o8/myfinance-web-netcore
```

### 2️ - Restaurar Dependências
```bash
dotnet restore
```

### 3️ - Instalar Ferramenta Entity Framework (se necessário)
```bash
dotnet tool install --global dotnet-ef --version 6.0.25
```

### 4️ - Configurar String de Conexão
O arquivo `appsettings.json` já está configurado para SQLite:
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Data Source=myfinance.db"
  }
}
```

### 5️ - Criar e Aplicar Migrations
```bash
# Criar migration inicial (se não existir)
dotnet ef migrations add InitialCreate

# Aplicar migrations ao banco
dotnet ef database update
```

### 6️ - Executar o Projeto
```bash
dotnet run
```

### 7️ - Acessar a Aplicação
- **URL**: https://localhost:7006
- **HTTP**: http://localhost:5088

## Licença

Este projeto foi desenvolvido como trabalho acadêmico para o curso de **Pós-Graduação em Engenharia de Software** da **PUC Minas**.

## Autor

Fabio Alves dos Santos \
Desenvolvido como projeto final da disciplina **Práticas de Implementação e Evolução de Software**. \
Professor Filipe Tório \
Julho 2025
