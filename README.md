![balta](https://baltaio.blob.core.windows.net/static/images/dark/balta-logo.svg)

## 🎖️ Desafio
**Caça aos Bugs 2024** é a sexta edição dos **Desafios .NET** realizados pelo [balta.io](https://balta.io). Durante esta jornada, fizemos parte da equipe __NOME_DA_BANDA__ onde resolvemos todos os bugs de uma aplicação e aplicamos testes de unidade no projeto.

## 📱 Projeto
Depuração e solução de bugs, pensamento crítico e analítico, segurança e qualidade de software aplicando testes de unidade.

## Participantes
### 🚀 Líder Técnico
[Guilherme Bley](https://github.com/GuilhermeBley)
### 👻 Caçadores de Bugs
* [Jorge Lima](http://github.com/CastionDev)
* [Vitor Galache](https://github.com/vitor-galache)
* [Matheus Sanches](https://github.com/MatheusSanches02)
* [Vitor Galache](https://github.com/vitor-galache)

## ⚙️ Tecnologias
* C# 12
* .NET 8
* ASP.NET
* Minimal APIs
* Blazor Web Assembly
* xUnit

## 🥋 Skills Desenvolvidas
* Comunicação
* Trabalho em Equipe
* Networking
* Muito conhecimento técnico

## 🧪 Como testar o projeto

## Como Executar o Projeto `Dima.Api` e `Dima.Web` Localmente

Essas instruções mostram como configurar e executar os projetos `Dima.Api` e `Dima.Web` no seu computador. Siga o passo a passo com calma, e se tiver dúvidas, confira os links de documentação de cada ferramenta mencionada.

### Pré-requisitos

Para rodar esse projeto, você precisa instalar:

1. **.NET 8**: é a plataforma que usamos para desenvolver a aplicação.
2. **Docker**: necessário para criar e gerenciar o banco de dados.

> 📝 **Dica**: Confira no site oficial do [.NET](https://dotnet.microsoft.com/download/dotnet) e do [Docker](https://docs.docker.com/get-docker/) como instalar essas ferramentas.

---

### 1. Criando o Banco de Dados com Docker

Para o projeto funcionar, ele precisa de um banco de dados, que vamos criar com o Docker. Abra o terminal (ou prompt de comando) e use o comando para criar o banco de dados com o Docker. Verifique se ele está rodando corretamente antes de seguir para o próximo passo.

---

### 2. Configurações de Desenvolvimento

Agora, vamos ajustar as configurações da aplicação. Abra o arquivo `appsettings.Development.json` e insira as informações abaixo para que a aplicação saiba onde está o banco de dados que você criou:

```json
{
  "FrontendUrl": "http://localhost:5028",
  "BackendUrl": "http://localhost:5164",
  "ConnectionStrings": {
    "DefaultConnection": "Server=sqlserver,1433;Database=dima-dev;User Id=sa;Password=Secret123!"
  },
  "StripeApiKey": "",
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}
```

> 🔍 **Observação**: Confirme que o valor de `ConnectionStrings:DefaultConnection` está correto para o seu banco de dados.

---

### 3. Inserindo Dados Iniciais no Banco de Dados

Alguns dados iniciais precisam ser adicionados ao banco para que o projeto funcione corretamente.

1. Instale a ferramenta **Entity Framework** (caso ainda não tenha) com o comando abaixo:
   ```bash
   dotnet tool install --global dotnet-ef
   ```

2. Agora, crie as tabelas no banco de dados usando:
   ```bash
   dotnet ef database update
   ```

3. Para inserir dados iniciais:
   - Abra o banco de dados `dima-dev` com seu programa de gerenciamento de banco de dados.
   - Execute os scripts `seed.sql` e `views.sql` que estão em `desafio-caca-aos-bugs\bugs\Dima.Api\Data\Scripts`.

---

### 4. Executando a API e a Aplicação Web

Por último, vamos executar a aplicação completa com o Docker.

- No terminal, vá até a pasta do projeto: `desafio-caca-aos-bugs\bugs`.
- Digite o seguinte comando para construir e iniciar o projeto:

```bash
docker-compose up --build
```

> 🎉 **Parabéns!** O projeto agora deve estar rodando localmente. Acesse os endereços `http://localhost:5028` e `http://localhost:5164` no navegador para ver o frontend e o backend.

---

# 💜 Participe
Quer participar dos próximos desafios? Junte-se a [maior comunidade .NET do Brasil 🇧🇷 💜](https://balta.io/discord)

