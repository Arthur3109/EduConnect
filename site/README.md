# EduConnect

Repositório oficial do projeto **EduConnect**.

Este README define o padrão de desenvolvimento, organização do código e processo oficial de entrega das atualizações no GitHub.

---

## 📋 Índice

- [Objetivo](#-objetivo)
- [Estrutura do projeto](#-estrutura-do-projeto)
- [Fluxo de desenvolvimento](#-fluxo-de-desenvolvimento)
- [Branches](#-branches)
- [Desenvolvimento](#-desenvolvimento)
- [Testes](#-testes)
- [Commits](#-commits)
- [Envio para o GitHub](#-envio-para-o-github)
- [Pull Request](#-pull-request)
- [Revisão](#-revisão)
- [Segurança](#-segurança)
- [Documentação](#-documentação)
- [Checklist de entrega](#-checklist-de-entrega)
- [Comandos principais](#-comandos-principais)
- [Regras obrigatórias](#-regras-obrigatórias)

---

## 🎯 Objetivo

O GitHub é a **fonte oficial do código-fonte do EduConnect**.

Todo desenvolvimento, correção ou atualização deve ser versionado e enviado para este repositório.

A entrega de uma tarefa somente é considerada oficial após:

1. desenvolvimento;
2. testes;
3. `commit`;
4. `push` para o GitHub;
5. criação do Pull Request;
6. revisão;
7. aprovação;
8. merge na `main`.

---

## 📂 Estrutura do projeto

```text
EduConnect/
│
├── docs/
│   └── Documentações do projeto
│
├── site/
│   ├── Server/
│   │   └── Código relacionado ao servidor
│   │
│   ├── backend/
│   │   └── API e regras de negócio
│   │
│   ├── frontend/
│   │   └── Interface da aplicação
│   │
│   └── README.md
│
├── Descrição.md
├── LICENSE
└── README.md

Onde colocar cada código?
Área	Diretório
Front-end	site/frontend/
Back-end / API	site/backend/
Servidor	site/Server/
Documentação	docs/
Informações gerais	README.md
Descrição do projeto	Descrição.md

⚠️ Não altere a estrutura principal do projeto sem autorização do responsável técnico.

🔄 Fluxo de desenvolvimento
Tarefa
  ↓
Atualizar main
  ↓
Criar branch
  ↓
Desenvolver
  ↓
Testar
  ↓
Commit
  ↓
Push
  ↓
Pull Request → main
  ↓
Revisão
  ↓
Aprovação
  ↓
Merge

🌿 Branches
Regra principal

Nunca desenvolva diretamente na main.

Cada tarefa deve possuir sua própria branch.

Padrões
Tipo	Padrão	Exemplo
Nova funcionalidade	feature/nome	feature/login-usuario
Correção	fix/nome	fix/erro-login
Documentação	docs/nome	docs/documentacao-api
Refatoração	refactor/nome	refactor/backend
Criar uma branch
git checkout main
git pull origin main
git checkout -b feature/minha-funcionalidade


Utilize nomes objetivos, sem espaços ou caracteres especiais.

💻 Desenvolvimento

Durante o desenvolvimento:

mantenha o código organizado;
siga os padrões existentes;
altere somente o necessário;
evite código duplicado;
remova códigos de teste antes da entrega;
mantenha a documentação atualizada;
não altere funcionalidades fora do escopo da tarefa.
🧪 Testes

Antes de criar o Pull Request, teste completamente a alteração.

Verifique:

 O projeto inicia corretamente;
 A funcionalidade funciona;
 Não existem erros de compilação;
 Não existem erros no console;
 As funcionalidades existentes continuam funcionando;
 Integrações entre Front-end, Back-end e Server funcionam;
 Cenários de erro foram testados.
Teste também situações inválidas

Exemplos:

Campos vazios
Dados inválidos
Usuário inexistente
Senha incorreta
Falha de conexão
Dados duplicados
Permissão insuficiente


❗ Código não testado não deve ser entregue para revisão.

🔎 Verificar alterações

Antes do commit:

git status


Para visualizar as alterações:

git diff


Confirme se:

somente arquivos necessários foram modificados;
não existem arquivos temporários;
não existem credenciais;
não existem arquivos pessoais;
não existem alterações acidentais.
💾 Commits

As mensagens de commit devem ser claras e objetivas.

✅ Bons exemplos
git commit -m "Adiciona tela de login"

git commit -m "Corrige validação do cadastro"

git commit -m "Implementa autenticação de usuários"

git commit -m "Atualiza documentação da API"

❌ Evite
git commit -m "alterações"

git commit -m "teste"

git commit -m "mudanças"

git commit -m "coisas novas"

☁️ Envio para o GitHub

Depois de testar e realizar o commit:

git add .
git commit -m "Descrição da alteração"
git push -u origin nome-da-branch


Exemplo:

git push -u origin feature/login-usuario


Após o push, a branch estará disponível no GitHub.

📤 Pull Request

Depois de enviar a branch, crie um Pull Request (PR).

Destino obrigatório
main


O Pull Request é a entrega oficial da tarefa.

⚠️ Código funcionando apenas na máquina local não é considerado uma entrega.

📝 Como preencher o Pull Request
Título

Use um título curto e objetivo.

Exemplo:

Implementa sistema de login

Descrição

Informe:

o que foi desenvolvido;
qual problema foi resolvido;
quais áreas foram alteradas;
como testar;
observações importantes.
Modelo
## Alteração

Implementado o sistema de login dos usuários.

## Alterações realizadas

- Criada tela de login
- Implementada autenticação
- Integrada API
- Adicionado tratamento de erros

## Testes realizados

- Login válido
- Senha inválida
- Usuário inexistente
- Campos obrigatórios

## Observações

Informações adicionais sobre a implementação.

👀 Revisão

Todo Pull Request deverá passar por revisão.

O responsável poderá:

✅ aprovar;
🔄 solicitar alterações;
❌ rejeitar a implementação.

A revisão pode verificar:

funcionamento;
qualidade do código;
organização;
segurança;
desempenho;
testes;
documentação;
aderência aos requisitos.
🔧 Alterações solicitadas

Caso sejam solicitadas alterações, continue utilizando a mesma branch.

Após corrigir:

git add .
git commit -m "Corrige ajustes solicitados na revisão"
git push


O Pull Request será atualizado automaticamente.

Não é necessário criar outro Pull Request para a mesma tarefa.

🔀 Merge

Após a aprovação, o Pull Request poderá ser integrado à main.

Depois do merge, atualize sua cópia local:

git checkout main
git pull origin main


A main deve representar uma versão estável do projeto.

🔐 Segurança
Nunca envie para o GitHub:
❌ Senhas
❌ Tokens
❌ API Keys
❌ Credenciais de banco de dados
❌ Arquivos .env
❌ Chaves privadas
❌ Certificados privados
❌ Dados confidenciais de clientes
❌ Credenciais de serviços externos
Variáveis de ambiente

Utilize .env localmente.

Exemplo de .env.example:

DATABASE_URL=
API_KEY=
JWT_SECRET=


⚠️ Os valores reais nunca devem ser enviados para o repositório.

📄 Documentação

Alterações que modificam o funcionamento do sistema devem ser documentadas.

Documentações gerais:

docs/


Documentações específicas podem ficar dentro do respectivo módulo:

site/
├── backend/
│   └── README.md
├── frontend/
│   └── README.md
└── Server/
    └── README.md

📦 Dependências

Ao adicionar uma nova dependência:

confirme se ela é necessária;
utilize uma versão adequada;
atualize o arquivo de dependências;
instale e teste;
informe a alteração no Pull Request.

Evite adicionar bibliotecas desnecessárias.

🧹 Organização

Mantenha o projeto limpo.

Evite:

código duplicado;
arquivos sem utilização;
funções sem utilização;
variáveis sem utilização;
console.log() desnecessários;
código de teste esquecido;
comentários desnecessários;
alterações fora do escopo;
arquivos temporários.
🔀 Conflitos

Caso ocorram conflitos com a main:

identifique os arquivos;
analise as alterações;
mantenha o código correto;
remova os marcadores de conflito;
teste o projeto;
finalize o merge.

Depois:

git add .
git commit -m "Resolve conflitos com a main"
git push


⚠️ Nunca resolva conflitos simplesmente apagando alterações sem verificar o impacto.

📋 Checklist de entrega

Antes de criar o Pull Request:

 Minha branch foi criada corretamente;
 A main estava atualizada antes do desenvolvimento;
 O código foi testado;
 A funcionalidade está funcionando;
 Não existem erros conhecidos;
 Não existem arquivos .env;
 Não existem senhas ou tokens;
 Não existem dados sensíveis;
 O código está organizado;
 A documentação foi atualizada;
 As dependências foram atualizadas, se necessário;
 O commit possui uma mensagem clara;
 O Pull Request está direcionado para main;
 O Pull Request possui uma descrição;
 Os testes realizados foram informados.
🛠️ Comandos principais
Atualizar a main
git checkout main
git pull origin main

Criar branch
git checkout -b feature/minha-tarefa

Ver status
git status

Ver alterações
git diff

Adicionar arquivos
git add .

Criar commit
git commit -m "Descrição da alteração"

Enviar branch
git push -u origin feature/minha-tarefa

Voltar para main
git checkout main

Atualizar main
git pull origin main

🚨 Regras obrigatórias
1. Não trabalhar diretamente na main

Sempre utilize uma branch.

2. Testar antes de entregar

Toda alteração deve ser testada.

3. Entregar através de Pull Request

A entrega oficial é o Pull Request direcionado para main.

4. Não enviar informações sensíveis

Senhas, tokens, chaves e .env não devem ser enviados.

5. Manter o código organizado

Não faça alterações fora do escopo da tarefa.

6. Documentar quando necessário

Alterações relevantes devem atualizar a documentação.

7. Respeitar a revisão

Solicitações de alteração devem ser corrigidas antes do merge.

8. Manter a main estável

A main deve conter somente código revisado e aprovado.

🏢 Responsabilidade do programador

É responsabilidade do programador garantir que sua entrega:

esteja funcionando;
esteja testada;
esteja organizada;
esteja documentada quando necessário;
não contenha informações sensíveis;
esteja na branch correta;
possua commits claros;
tenha um Pull Request devidamente preenchido;
esteja pronta para revisão.
📌 Regra principal

Todo desenvolvimento do EduConnect deve ser realizado em uma branch própria, testado, versionado e entregue através de um Pull Request para a main.

DESENVOLVER
     ↓
TESTAR
     ↓
COMMIT
     ↓
PUSH
     ↓
PULL REQUEST
     ↓
REVISÃO
     ↓
APROVAÇÃO
     ↓
MERGE → MAIN

🚀 EduConnect

Projeto: EduConnect
Branch principal: main
Repositório: GitHub

Código desenvolvido localmente não é considerado entregue. A entrega oficial acontece através do Pull Request no GitHub.
