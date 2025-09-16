# AI DCL Prompts

Uma coleção estruturada de prompts para desenvolvimento de software com foco em análise de requisitos, design de arquitetura e planejamento de implementação usando Amazon Q Developer.

## 📋 Índice

- [Visão Geral](#-visão-geral)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Prompts Disponíveis](#-prompts-disponíveis)
  - [Planejamento de Projetos](#planejamento-de-projetos)
    - [1. Análise de Requisitos](#1-análise-de-requisitos)
    - [2. Design de Arquitetura](#2-design-de-arquitetura)
    - [3. Plano de Implementação](#3-plano-de-implementação)
  - [Documentação de Projetos](#documentação-de-projetos)
    - [1. Análise de Projeto](#1-análise-de-projeto)
    - [2. Documentação de Arquitetura](#2-documentação-de-arquitetura)
    - [3. Stack Técnica](#3-stack-técnica)
    - [4. Progresso do Projeto](#4-progresso-do-projeto)
    - [5. Geração de Documentação](#5-geração-de-documentação)
- [Configuração do Projeto](#-configuração-do-projeto)
- [Regras e Padrões](#-regras-e-padrões)
- [Amazon Q CLI Agent](#-amazon-q-cli-agent)
- [Como Usar](#-como-usar)
- [Tecnologias](#-tecnologias)
- [Contribuição](#-contribuição)

## 🎯 Visão Geral

Este projeto fornece uma metodologia estruturada para desenvolvimento de software através de prompts especializados que guiam desde a análise inicial de requisitos até o plano detalhado de implementação. Os prompts são otimizados para trabalhar com Amazon Q Developer e seguem as melhores práticas de engenharia de software.

### Objetivos

- **Padronização**: Estabelecer um processo consistente para análise e planejamento de projetos
- **Qualidade**: Garantir documentação técnica completa e rastreável
- **Eficiência**: Acelerar o processo de planejamento através de templates estruturados
- **Integração**: Facilitar o uso com Amazon Q Developer e ferramentas AWS

## 📁 Estrutura do Projeto

```
ai-dcl-prompts/
├── project-rules/              # Regras e contexto do projeto
│   ├── contexto-de-projeto.md  # Contexto e arquitetura base
│   └── regras-de-projeto.md    # Padrões de código e segurança
├── prompts/                    # Coleção de prompts especializados
│   ├── documentacao/          # Prompts para documentação de projetos
│   │   ├── projeto.md         # Análise geral do projeto
│   │   ├── arquitetura.md     # Documentação de arquitetura
│   │   ├── pilha-tecnica.md   # Stack técnica e dependências
│   │   ├── progresso-projeto.md # Status e progresso
│   │   └── documentacao-de-projeto-e-regras.md # Geração de docs
│   └── planejamento/          # Prompts para planejamento de projetos
│       ├── 1-requisitos.md    # Análise de requisitos
│       ├── 2-design-arquitetura-projeto.md  # Design de arquitetura
│       └── 3-plano-de-implementacao-task-list.md  # Plano de implementação
├── q-cli/                     # Configuração Amazon Q CLI
│   └── q-cli-agent-schema-example.json  # Schema de exemplo para agentes
└── README.md                  # Este arquivo
```

## 🚀 Prompts Disponíveis

### Planejamento de Projetos

#### 1. Análise de Requisitos

**Arquivo**: `prompts/planejamento/1-requisitos.md`

Prompt especializado para análise completa de requisitos de software, incluindo:

- **Requisitos Funcionais**: Identificação, descrição e critérios de aceite
- **Requisitos Não Funcionais**: Performance, segurança, usabilidade, confiabilidade
- **Documentação Estruturada**: Matriz de requisitos, casos de uso, fluxogramas
- **Análise de Riscos**: Identificação de dependências e estimativas

**Entregáveis**:
- Matriz de requisitos completa
- Diagramas de casos de uso
- Fluxogramas principais
- Análise de riscos e dependências

#### 2. Design de Arquitetura

**Arquivo**: `prompts/planejamento/2-design-arquitetura-projeto.md`

Prompt para criação de arquiteturas cloud escaláveis e seguras:

- **Pilares Arquiteturais**: Segurança, performance, resiliência, custos, excelência operacional
- **Diagramas Técnicos**: Visão geral, fluxo de dados, componentes, rede
- **Especificações AWS**: Componentes cloud, configurações, integrações
- **Estratégias de Deployment**: CI/CD, ambientes, monitoramento

**Entregáveis**:
- Documentação arquitetural completa
- Diagramas padronizados
- Especificações técnicas detalhadas
- Estratégias de implementação

#### 3. Plano de Implementação

**Arquivo**: `prompts/planejamento/3-plano-de-implementacao-task-list.md`

Prompt para criação de planos detalhados de implementação:

- **Rastreabilidade**: Mapeamento entre requisitos e componentes arquiteturais
- **Validações Cruzadas**: Conformidade com documentos anteriores
- **Planejamento Detalhado**: Tasks, dependências, cronograma
- **Controle de Qualidade**: Critérios de aceite e métricas

**Entregáveis**:
- Plano de implementação estruturado
- Cronograma detalhado
- Matriz de rastreabilidade
- Plano de testes e validação

### Documentação de Projetos

#### 1. Análise de Projeto

**Arquivo**: `prompts/documentacao/projeto.md`

Prompt para análise completa de repositórios e documentação de aspectos fundamentais:

- **Visão Geral**: Análise de README, estrutura e padrões
- **Objetivos**: Review de issues, milestones e planejamento
- **Escopo**: Análise de branches, módulos e integrações
- **Stakeholders**: Identificação de contribuidores e responsabilidades

#### 2. Documentação de Arquitetura

**Arquivo**: `prompts/documentacao/arquitetura.md`

Prompt especializado para documentação técnica de arquitetura:

- **Design do Sistema**: Padrões arquiteturais e modularização
- **Componentes**: Mapeamento de serviços e dependências
- **Integrações**: APIs, protocolos e fluxos de dados
- **Diagramas**: Geração automática com sintaxe Mermaid

#### 3. Stack Técnica

**Arquivo**: `prompts/documentacao/pilha-tecnica.md`

Prompt para documentação completa da stack tecnológica:

- **Tecnologias**: Linguagens, frameworks e bibliotecas
- **Configurações**: Ambientes, builds e deployments
- **Dependências**: Análise automática de package managers
- **Restrições**: Compatibilidade e requisitos de sistema

#### 4. Progresso do Projeto

**Arquivo**: `prompts/documentacao/progresso-projeto.md`

Prompt para acompanhamento de status e progresso:

- **Status Atual**: Branches, releases e métricas de qualidade
- **Roadmap**: Milestones, backlog e timeline
- **Problemas**: Issues, bugs e débitos técnicos
- **Métricas**: KPIs, cobertura de testes e performance

#### 5. Geração de Documentação

**Arquivo**: `prompts/documentacao/documentacao-de-projeto-e-regras.md`

Prompt coordenador para geração estruturada de documentação:

- **Processo Automatizado**: Geração de múltiplos documentos
- **Validações**: Conformidade e completude
- **Manutenção**: Atualizações incrementais e revisões
- **Metadados**: Índices, rastreabilidade e referências

## ⚙️ Configuração do Projeto

### Contexto Base

O projeto está configurado para uma aplicação web de e-commerce com:

- **Backend**: Django REST Framework
- **Frontend**: React.js com TypeScript
- **Banco de Dados**: PostgreSQL
- **Cloud**: AWS (S3, Lambda, RDS)
- **Containerização**: Docker
- **IaC**: AWS CDK

### Padrões de Nomenclatura

- **Classes**: PascalCase (`ProductManager`)
- **Funções/Variáveis**: snake_case (`get_user_orders`)
- **Constantes**: UPPER_SNAKE_CASE (`MAX_RETRY_ATTEMPTS`)
- **Arquivos**: kebab-case (`user-profile.component.js`)

## 📋 Regras e Padrões

### Segurança AWS

- Criptografia obrigatória em todos os serviços (S3, DynamoDB, SNS)
- SSL obrigatório para comunicações
- Acesso público bloqueado por padrão
- Políticas de IAM com menor privilégio

### Padrões de Código

**Python**:
- Type hints obrigatórios
- Docstrings padrão Google
- Máximo 80 caracteres por linha
- F-strings para formatação
- Tratamento adequado de exceções

**JavaScript/React**:
- TypeScript obrigatório
- Componentes funcionais com hooks
- Props tipadas com interfaces
- Async/await para promises

### Testes

- Cobertura mínima de 80%
- Testes unitários para funções públicas
- Testes de integração para APIs
- Mocks para dependências externas

## 🤖 Amazon Q CLI Agent

O projeto inclui um exemplo de configuração para Amazon Q CLI Agent (`q-cli/q-cli-agent-schema-example.json`) com:

- **Servidores MCP**: CDK, GitHub, AWS Documentation, Frontend
- **Recursos**: Acesso a arquivos de regras e documentação
- **Ferramentas**: Configuração de tools permitidas
- **Prompts**: Especializações técnicas para projetos específicos

### Exemplo de Uso

```json
{
  "name": "projeto-torre-hanoi",
  "description": "Agente específico para projeto Java/Spring Boot",
  "mcpServers": {
    "awslabs.cdk-mcp-server": { ... },
    "github": { ... }
  }
}
```

## 📖 Como Usar

### 1. Configuração Inicial

1. Clone o repositório
2. Adapte os arquivos em `project-rules/` para seu contexto
3. Configure o Amazon Q CLI Agent se necessário

### 2. Processo de Desenvolvimento

**Para Planejamento de Projetos:**
1. **Análise de Requisitos**: Use o prompt `1-requisitos.md`
2. **Design de Arquitetura**: Aplique o prompt `2-design-arquitetura-projeto.md`
3. **Plano de Implementação**: Execute o prompt `3-plano-de-implementacao-task-list.md`

**Para Documentação de Projetos:**
1. **Análise Geral**: Use o prompt `projeto.md`
2. **Documentação Técnica**: Aplique os prompts `arquitetura.md` e `pilha-tecnica.md`
3. **Acompanhamento**: Execute o prompt `progresso-projeto.md`
4. **Geração Automatizada**: Use o prompt `documentacao-de-projeto-e-regras.md`

### 3. Personalização

- Edite `contexto-de-projeto.md` com suas especificações
- Ajuste `regras-de-projeto.md` conforme seus padrões
- Customize os prompts para suas necessidades específicas

## 🛠️ Tecnologias

- **Amazon Q Developer**: IA para desenvolvimento
- **AWS Services**: Cloud computing e infraestrutura
- **MCP (Model Context Protocol)**: Integração com ferramentas
- **Markdown**: Documentação estruturada
- **JSON Schema**: Configuração de agentes

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

### Diretrizes

- Mantenha a estrutura de prompts consistente
- Documente mudanças significativas
- Teste os prompts antes de submeter
- Siga os padrões de nomenclatura estabelecidos

---

**Nota**: Este projeto é um template/framework para desenvolvimento estruturado. Adapte os contextos e regras conforme suas necessidades específicas.
