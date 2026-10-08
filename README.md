# ⚖️ JurisFlow

Aplicação web de **gestão jurídica** desenvolvida com **Python e Flask**, criada para centralizar o gerenciamento de clientes, processos, prazos e documentos em uma única plataforma.

O projeto foi desenvolvido utilizando uma abordagem de **desenvolvimento assistido por IA (AI-assisted development / Vibe Coding)**, utilizando ferramentas de inteligência artificial como apoio durante o processo de desenvolvimento, implementação, depuração e melhoria da aplicação.

## 🎯 Objetivo

O JurisFlow foi desenvolvido para criar uma solução simples e organizada para gerenciamento de informações jurídicas, permitindo acompanhar clientes, processos, prazos e documentos através de uma interface web.

Durante o desenvolvimento, foram aplicados conceitos de:

- Desenvolvimento web com Flask
- Operações CRUD
- Modelagem de banco de dados
- Relacionamento entre entidades
- Autenticação e gerenciamento de sessões
- Upload e gerenciamento de arquivos
- Desenvolvimento de interfaces web
- Integração entre frontend, backend e banco de dados
- Uso de IA como ferramenta de desenvolvimento

## 🤖 Desenvolvimento assistido por IA

Este projeto foi desenvolvido utilizando **IA como ferramenta de desenvolvimento**, seguindo uma abordagem de **Vibe Coding**.

A IA foi utilizada como apoio para:

- Estruturação inicial da aplicação
- Implementação de funcionalidades
- Geração e refatoração de código
- Identificação e correção de erros
- Desenvolvimento de queries SQL
- Criação de componentes da interface
- Análise e melhoria do código
- Documentação do projeto

A utilização da IA não substituiu a tomada de decisões durante o desenvolvimento. O processo envolveu **definir requisitos, orientar a implementação, testar as funcionalidades, identificar problemas e revisar as soluções geradas**.

> O objetivo do projeto é demonstrar a capacidade de utilizar ferramentas de IA de forma produtiva para transformar requisitos em uma aplicação funcional.

## 🚀 Funcionalidades

### 🔐 Autenticação

- Login com e-mail e senha
- Controle de sessão
- Proteção das páginas internas
- Logout

### 📊 Dashboard

- Total de clientes
- Total de processos
- Total de prazos
- Total de documentos
- Processos recentes
- Prazos próximos
- Prazos atrasados
- Processos por status
- Indicadores gerais do sistema

### 👤 Clientes

- Cadastro
- Visualização
- Edição
- Exclusão
- CPF
- Telefone
- E-mail
- Endereço

### ⚖️ Processos

- Cadastro de processos
- Associação com clientes
- Número do processo
- Tipo
- Status
- Vara / órgão
- Descrição
- Edição e exclusão

### ⏰ Prazos

- Data de vencimento
- Prioridade
- Status
- Observações
- Associação com processos
- Identificação de prazos próximos
- Identificação de prazos atrasados

### 📄 Documentos

- Cadastro
- Visualização
- Edição
- Exclusão
- Upload de arquivos
- Substituição de arquivos
- Acesso aos arquivos
- Associação com processos

## 🛠️ Tecnologias

### Backend

- **Python**
- **Flask**
- **SQLite**
- **Werkzeug**

### Frontend

- **HTML5**
- **CSS3**
- **JavaScript**
- **Jinja2**

### Banco de dados

O projeto utiliza **SQLite** para armazenamento dos dados e `sqlite3` para comunicação com o banco.

## 🗄️ Modelagem de dados

```text
┌──────────────┐
│   Usuários   │
└──────────────┘

┌──────────────┐
│   Clientes   │
└──────┬───────┘
       │
       │ 1:N
       ▼
┌──────────────┐
│  Processos   │
└──────┬───────┘
       │
       ├───────────────┐
       │               │
       │ 1:N           │ 1:N
       ▼               ▼
┌──────────────┐  ┌──────────────┐
│    Prazos    │  │  Documentos  │
└──────────────┘  └──────────────┘
```

Um cliente pode possuir vários processos, enquanto cada processo pode possuir diversos prazos e documentos.

## 📁 Estrutura do projeto

```text
Jurisflow/
│
├── app.py
├── database.py
├── criar_usuario.py
├── jurisflow.db
│
├── Static/
│   └── style.css
│
├── Templates/
│   ├── Index.html
│   ├── login.html
│   ├── dashboard.html
│   ├── clientes.html
│   ├── novo_cliente.html
│   ├── editar_cliente.html
│   ├── visualizar_cliente.html
│   ├── processos.html
│   ├── novo_processo.html
│   ├── editar_processo.html
│   ├── visualizar_processo.html
│   ├── prazos.html
│   ├── novo_prazo.html
│   ├── editar_prazo.html
│   ├── visualizar_prazo.html
│   ├── documentos.html
│   ├── novo_documento.html
│   ├── editar_documento.html
│   └── visualizar_documento.html
│
└── uploads/
    └── documentos/
```

## 💻 Como executar

### Pré-requisitos

- Python 3.x
- pip

### 1. Clone o repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd Jurisflow
```

### 2. Crie um ambiente virtual

```bash
python -m venv .venv
```

No Windows:

```bash
.venv\Scripts\activate
```

No Linux/macOS:

```bash
source .venv/bin/activate
```

### 3. Instale as dependências

```bash
pip install flask werkzeug
```

### 4. Inicialize o banco de dados

```bash
python database.py
```

### 5. Crie o usuário inicial

```bash
python criar_usuario.py
```

### 6. Execute a aplicação

```bash
python app.py
```

A aplicação estará disponível em:

```text
http://127.0.0.1:5000
```

## 🔑 Credenciais de acesso

Para testar a aplicação localmente:

```text
E-mail: admin@jurisflow.com
Senha: 123456
```

## 📌 Competências demonstradas

- **Python**
- **Flask**
- **SQL / SQLite**
- **HTML / CSS / JavaScript**
- **Jinja2**
- **CRUD**
- **Modelagem de dados**
- **Relacionamentos entre tabelas**
- **Autenticação**
- **Gerenciamento de sessões**
- **Upload de arquivos**
- **Debugging**
- **Refatoração**
- **Desenvolvimento assistido por IA**
- **Vibe Coding**
- **Transformação de requisitos em software funcional**

## 🚧 Possíveis melhorias

- [ ] Hash de senhas
- [ ] Cadastro de usuários pela interface
- [ ] Diferentes níveis de acesso
- [ ] Busca e filtros
- [ ] Paginação
- [ ] Calendário de prazos
- [ ] Notificações
- [ ] Geração de relatórios
- [ ] Exportação para PDF
- [ ] Histórico de alterações
- [ ] Testes automatizados
- [ ] API REST
- [ ] Deploy em ambiente de produção

## 👨‍💻 Sobre o projeto

O **JurisFlow** é um projeto de portfólio desenvolvido para demonstrar minha capacidade de utilizar tecnologias modernas de desenvolvimento e ferramentas de inteligência artificial para transformar uma ideia em uma aplicação web funcional.

O projeto foi construído utilizando uma abordagem de **Vibe Coding**, na qual a IA atua como uma ferramenta de apoio durante o desenvolvimento, enquanto as decisões sobre funcionalidades, estrutura, requisitos, testes e evolução da aplicação são conduzidas pelo desenvolvedor.
