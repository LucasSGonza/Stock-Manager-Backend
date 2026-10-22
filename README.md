# 📦 Stock Manager Backend

Servidor Backend do projeto [Stock Manager](https://github.com/LucasSGonza/Stock-Manager);

---

## 🎯 Funcionalidades

- **Gestão de estoque** — criação, edição e exclusão de itens
- **Fluxo de caixa** — controle de contas a pagar e a receber

---

## 🛠️ Stack

| Tecnologia | Versão |
|---|---|
| Java | 21 |
| Maven | 3.9.16 |
| Spring Boot | 4.0.8 |

| Dependências Instaladas
|---|
| Spring Web MVC |
| Spring Data JPA |
| Spring RestClient |
| Spring Boot Actuator |
| Spring Boot DevTools | — |

---

## 🚀 Como rodar o projeto

### Pré-requisitos

- Java `21`
- Maven `3.9.16` (opcional, pois o projeto inclui o Maven Wrapper `mvnw`)
- Banco de dados configurado e acessível (ex.: PostgreSQL)

### Instalação

```bash
# Clone o repositório
git clone https://github.com/LucasSGonza/Stock-Manager-Backend

# Baixe as dependências e compile
./mvnw clean install
```

> No Windows, use `mvnw.cmd` no lugar de `./mvnw`.

### Configuração de ambiente

Defina as variáveis de ambiente de conexão com o banco, que são lidas pelo `src/main/resources/application-dev.properties`:

```properties
spring.datasource.url=${DB_URL}
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
```

Exemplo de valores:

```env
DB_URL=jdbc:postgresql://localhost:5432/stock_manager
DB_USERNAME=seu_usuario
DB_PASSWORD=sua_senha
```

> ⚠️ Nunca comite credenciais reais. Versione apenas arquivos de exemplo, sem dados sensíveis.

### Execução

```bash
# Ambiente de desenvolvimento
./mvnw spring-boot:run

# Build de produção
./mvnw clean package

# Executar o JAR gerado
java -jar target/*.jar
```

A aplicação sobe por padrão em `http://localhost:8080`.

---

## 📁 Estrutura do Projeto

```
└── 📁Stock-Manager-Backend
    └── 📁.mvn
    └── 📁.tasks
    └── 📁docs
        └── 📁adrs
        └── 📁guides
            ├── java-development-guide.md
        └── 📁rules
            ├── engineering.md
            ├── rules.md
        ├── AGENTS.md
    └── 📁src
        └── 📁main
            └── 📁java
                └── 📁com
                    └── 📁lucas
                        └── 📁goncalves
                            └── 📁dev
                                └── 📁stock_manager_backend
                                    └── 📁config
                                    └── 📁controller
                                    └── 📁dto
                                    └── 📁exception
                                    └── 📁model
                                    └── 📁repository
                                    └── 📁service
                                        └── 📁impl
                                    ├── StockManagerBackendApplication.java
            └── 📁resources
                └── 📁static
                └── 📁templates
                ├── application-dev.properties
                ├── application.properties
        └── 📁test
    └── 📁target
    ├── .gitattributes
    ├── .gitignore
    ├── HELP.md
    ├── mvnw
    ├── mvnw.cmd
    ├── pom.xml
    └── README.md
```

---

## 📄 Documentação

| Arquivo | Descrição |
|---|---|
| `docs/adrs` | Decisões de arquitetura e lógica de negócio |
| `docs/guides/java-development-guide.md` | Padrões de desenvolvimento Java do projeto |
| `docs/rules/engineering.md` | Regras de qualidade de código e commits |
| `docs/rules/rules.md` | Diretrizes de segurança |
| `docs/AGENTS.md` | Instruções para agentes de IA |

---

> Desenvolvido por **Lucas Silva Gonçalves**