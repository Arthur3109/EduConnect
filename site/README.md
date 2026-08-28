EduConnect

Repositório oficial do projeto EduConnect.

Este documento apresenta as orientações que devem ser seguidas pelos programadores da empresa para desenvolvimento, atualização, organização e entrega do projeto no GitHub.

📌 Objetivo

O GitHub é o local oficial para armazenamento e acompanhamento do código-fonte do EduConnect.

Todo código desenvolvido ou atualizado deve ser enviado para este repositório, respeitando a estrutura de pastas e o fluxo de trabalho definido neste documento.

📂 Estrutura do projeto

Atualmente, o projeto está organizado da seguinte forma:

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
│   │   └── Código da API e regras de negócio
│   │
│   ├── frontend/
│   │   └── Interface e aplicação do usuário
│   │
│   └── README.md
│
├── Descrição.md
├── LICENSE
└── README.md

Onde colocar cada tipo de código?
Tipo de desenvolvimento	Local
Front-end / interface	site/frontend/
Back-end / API	site/backend/
Servidor	site/Server/
Documentação	docs/
Informações gerais do projeto	README.md
Descrição detalhada do projeto	Descrição.md

Importante: não crie novas pastas ou altere a estrutura principal do projeto sem alinhar previamente com o responsável pelo projeto.

🚀 Fluxo de trabalho

Todo programador deve seguir o fluxo abaixo ao realizar uma atualização.

Atualizar projeto
       ↓
Criar branch
       ↓
Desenvolver
       ↓
Testar
       ↓
Commit
       ↓
Push para o GitHub
       ↓
Abrir Pull Request
       ↓
Revisão
       ↓
Aprovação
       ↓
Merge na main

1. 🔄 Atualizar o projeto local

Antes de começar qualquer desenvolvimento, certifique-se de que sua versão local está atualizada.

git checkout main
git pull origin main


Isso evita trabalhar com uma versão antiga do projeto.

Verifique se existem alterações locais

Antes de atualizar, também é recomendado executar:

git status


Caso existam alterações importantes que ainda não foram salvas ou enviadas, resolva-as antes de atualizar a main.

2. 🌿 Criar uma branch

Não faça alterações diretamente na main.

Cada tarefa deve possuir sua própria branch.

Crie uma branch específica para a tarefa:

git checkout -b nome-da-tarefa


Exemplos:

git checkout -b desenvolvimento-login

git checkout -b correcao-cadastro-aluno

git checkout -b melhoria-dashboard

Padrão recomendado

Utilize os seguintes padrões:

feature/nome-da-funcionalidade
fix/nome-do-problema
docs/nome-da-documentacao
refactor/nome-da-alteracao

Exemplos
git checkout -b feature/login-usuario

git checkout -b feature/cadastro-professor

git checkout -b fix/erro-autenticacao

git checkout -b docs/documentacao-api

git checkout -b refactor/organizacao-backend

Regras para nomes de branches

Os nomes devem:

ser objetivos;
descrever a tarefa;
evitar espaços;
evitar caracteres especiais;
utilizar - para separar palavras.

Evite:

minha branch nova


Prefira:

feature/nova-funcionalidade

3. 💻 Realizar o desenvolvimento

Após criar a branch, realize o desenvolvimento solicitado.

Faça as alterações somente nos arquivos relacionados à tarefa.

Durante o desenvolvimento:

mantenha o código organizado;
siga o padrão utilizado no projeto;
evite arquivos desnecessários;
não altere funcionalidades que não fazem parte da tarefa;
não remova código sem necessidade;
mantenha comentários somente quando forem realmente úteis;
atualize a documentação quando necessário;
mantenha o projeto funcionando.
4. 🧪 Testar as alterações

Antes de enviar qualquer atualização para o GitHub, o programador deve testar as alterações realizadas.

Verifique, no mínimo:

se o projeto inicia corretamente;
se a funcionalidade desenvolvida funciona;
se não existem erros no console;
se não existem erros de compilação;
se as funcionalidades existentes continuam funcionando;
se as integrações entre front-end, back-end e servidor continuam funcionando;
se os dados estão sendo tratados corretamente.

Sempre que possível, realize testes para os principais cenários:

Cenário esperado
Usuário realiza uma ação válida
↓
Sistema processa corretamente
↓
Resultado esperado é apresentado

Cenários de erro

Também devem ser testados:

Dados inválidos
Campos vazios
Usuário inexistente
Senha incorreta
Falha de conexão
Dados duplicados
Permissões insuficientes


Não envie código para revisão sem realizar os testes necessários.

5. 🔎 Verificar as alterações

Antes de realizar o commit, verifique quais arquivos foram modificados:

git status


Também é recomendado visualizar as alterações:

git diff


Confira se:

somente os arquivos necessários foram alterados;
não existem arquivos temporários;
não existem senhas ou tokens;
não existem arquivos pessoais;
não existem alterações acidentais.
6. 💾 Fazer o commit

Depois de testar e verificar as alterações, adicione os arquivos:

git add .


Em seguida, crie o commit:

git commit -m "Descrição da alteração"

Exemplos
git commit -m "Adiciona tela de login"

git commit -m "Corrige validação do cadastro"

git commit -m "Implementa autenticação de usuários"

git commit -m "Atualiza documentação do backend"

📌 Padrão das mensagens de commit

A mensagem deve explicar de forma objetiva o que foi alterado.

Evite
git commit -m "alterações"

git commit -m "teste"

git commit -m "coisas novas"

git commit -m "mudanças"

Prefira
Adiciona sistema de login

Corrige validação de cadastro

Implementa recuperação de senha

Atualiza documentação da API

7. ☁️ Enviar o código para o GitHub

Depois de criar o commit, envie sua branch para o GitHub:

git push origin nome-da-tarefa


Por exemplo:

git push origin feature/login-usuario


Na primeira vez que enviar a branch, pode ser necessário:

git push -u origin feature/login-usuario


Após o push, a branch estará disponível no GitHub.

8. 📤 Criar o Pull Request

Após enviar a branch para o GitHub, o programador deve abrir um Pull Request (PR).

O Pull Request deve ser direcionado para:

main


O Pull Request é a entrega oficial da tarefa.

Ter o código funcionando apenas na máquina local não significa que a tarefa foi entregue.

📍 Onde o programador deve entregar?

A entrega oficial deve ser feita no repositório GitHub do EduConnect, através de um Pull Request direcionado para a branch:

main


O processo correto é:

Código desenvolvido
        ↓
Testes realizados
        ↓
Commit criado
        ↓
Branch enviada para o GitHub
        ↓
Pull Request criado
        ↓
Responsável revisa
        ↓
Alterações solicitadas (se necessário)
        ↓
Aprovação
        ↓
Merge na main

9. 📝 Preencher o Pull Request

O Pull Request deve conter informações suficientes para que outra pessoa consiga entender o que foi desenvolvido.

Título

O título deve ser curto e objetivo.

Exemplo:

Implementação do sistema de login


Outro exemplo:

Correção do cadastro de alunos

Descrição

A descrição deve informar:

o que foi desenvolvido;
qual problema foi resolvido;
quais partes do sistema foram alteradas;
como testar;
observações importantes.
Exemplo
## Alteração

Implementado o sistema de login dos usuários.

## Alterações realizadas

- Criada tela de login
- Criada validação de usuário
- Integrado login com a API
- Adicionado tratamento de erros
- Implementada autenticação

## Testes realizados

- Login com usuário válido
- Login com senha inválida
- Usuário inexistente
- Campos obrigatórios
- Logout

## Observações

A funcionalidade depende da API de autenticação estar disponível.

👀 10. Revisão do código

Depois que o Pull Request for criado, o responsável técnico ou pessoa designada deverá revisar o código.

Durante a revisão poderão ser analisados:

qualidade do código;
organização;
segurança;
funcionamento;
desempenho;
possíveis bugs;
padrões utilizados;
documentação;
testes.

O Pull Request poderá ser:

✅ Aprovado

O código está adequado e pode ser integrado.

🔄 Alterações solicitadas

O programador deverá corrigir os pontos indicados.

❌ Rejeitado

Caso a implementação não esteja de acordo com os requisitos, o responsável poderá solicitar que a tarefa seja refeita.

🔧 11. Quando forem solicitadas alterações

Não é necessário criar uma nova Pull Request.

Continue trabalhando na mesma branch.

Faça as correções:

git add .


Depois:

git commit -m "Corrige ajustes solicitados na revisão"


E envie novamente:

git push


O Pull Request existente será atualizado automaticamente.

✅ 12. Aprovação e Merge

Após a revisão e aprovação, o Pull Request poderá ser integrado à main.

O merge deve ser realizado conforme as permissões e o processo definido pela empresa.

Após o merge, o programador deve atualizar sua cópia local:

git checkout main
git pull origin main

🚫 13. Não trabalhar diretamente na main

A branch main deve representar uma versão estável do projeto.

Portanto:

Não faça commits diretamente na main, salvo quando expressamente autorizado pelo responsável técnico.

O desenvolvimento deve acontecer em branches próprias.

🔐 14. Segurança

É proibido enviar informações sensíveis para o GitHub.

Nunca envie:

senhas;
tokens;
API Keys;
credenciais de banco de dados;
arquivos .env;
certificados privados;
chaves privadas;
informações confidenciais de clientes;
dados pessoais desnecessários;
credenciais de serviços externos.
Arquivo .env

Informações sensíveis devem ficar em variáveis de ambiente.

Exemplo:

DATABASE_URL=
API_KEY=
JWT_SECRET=


Os valores reais não devem ser enviados ao GitHub.

Quando necessário, utilize:

.env.example


Exemplo:

DATABASE_URL=coloque_aqui
API_KEY=coloque_aqui
JWT_SECRET=coloque_aqui

📄 15. Documentação

Sempre que uma alteração modificar o funcionamento do sistema, a documentação também deverá ser atualizada.

Documentações gerais devem ficar em:

docs/


Documentações específicas podem ficar junto ao respectivo módulo quando necessário.

Exemplo:

site/
│
├── backend/
│   └── README.md
│
├── frontend/
│   └── README.md
│
└── Server/
    └── README.md

📦 16. Dependências

Ao adicionar uma nova biblioteca ou dependência ao projeto:

confirme se ela é realmente necessária;
utilize uma versão adequada;
atualize o arquivo de dependências correspondente;
teste o projeto após a instalação;
informe a alteração no Pull Request.

Não adicione bibliotecas desnecessárias.

🧹 17. Organização do código

O código deve ser mantido limpo e organizado.

Evite:

código duplicado;
arquivos sem utilização;
funções sem utilização;
variáveis sem utilização;
comentários desnecessários;
código de teste esquecido;
console.log() desnecessários;
credenciais dentro do código;
alterações fora do escopo da tarefa.
🎯 18. Uma tarefa por branch

Sempre que possível, cada branch deve representar uma tarefa específica.

Exemplo correto
feature/login-usuario


Contendo apenas alterações relacionadas ao login.

Evite

Uma única branch contendo:

Login
Cadastro
Dashboard
Correção de menu
Alteração de banco
Atualização de documentação


Isso dificulta a revisão e aumenta o risco de problemas.

🔄 19. Atualizar a branch antes da entrega

Caso a main tenha recebido novas alterações durante seu desenvolvimento, atualize sua branch antes de finalizar a tarefa.

Primeiro:

git checkout main
git pull origin main


Depois volte para sua branch:

git checkout nome-da-sua-branch


Atualize sua branch conforme o fluxo adotado pela equipe.

Por exemplo, utilizando merge:

git merge main


Resolva eventuais conflitos e teste novamente o projeto antes de atualizar o Pull Request.

⚠️ 20. Conflitos de código

Caso o Git informe que existem conflitos, não simplesmente apague arquivos ou escolha alterações sem entender o que está acontecendo.

O programador deve:

identificar os arquivos em conflito;
analisar as alterações;
manter o código correto;
remover os marcadores de conflito;
testar o projeto;
finalizar o merge.

Depois:

git add .

git commit -m "Resolve conflitos com a main"

git push

🗂️ 21. Organização das entregas

Cada entrega deve permitir identificar facilmente:

quem desenvolveu;
qual tarefa foi realizada;
quais arquivos foram alterados;
qual problema foi resolvido;
como a alteração foi testada.

Por isso, o histórico do Git deve ser mantido organizado.

📋 22. Checklist antes de criar o Pull Request

Antes de abrir o Pull Request, confirme:

 O código foi testado;
 A funcionalidade está funcionando;
 Não existem erros conhecidos;
 Não existem erros de compilação;
 Não foram enviados arquivos .env;
 Não foram enviados dados sensíveis;
 Não foram enviadas senhas ou tokens;
 O código está organizado;
 A documentação foi atualizada, quando necessário;
 As dependências foram atualizadas, quando necessário;
 O commit possui uma mensagem clara;
 A branch possui um nome adequado;
 O Pull Request foi criado para main;
 A descrição do Pull Request explica o que foi desenvolvido;
 Os testes realizados foram informados.
📋 23. Checklist do responsável pela revisão

O responsável pela revisão deverá verificar:

 A tarefa corresponde ao solicitado;
 O código está funcionando;
 Não existem alterações desnecessárias;
 Não existem informações sensíveis;
 O código segue o padrão do projeto;
 Não existem problemas evidentes de segurança;
 Os testes foram realizados;
 A documentação está adequada;
 O Pull Request está devidamente descrito.

Após a aprovação:

APROVADO → MERGE → MAIN

🏆 24. Regra principal da EduConnect

Todo desenvolvimento deve ser versionado no GitHub e entregue através de um Pull Request para a branch main, seguindo o processo de revisão definido pela EduConnect.

A main deve permanecer estável.

O programador deve desenvolver em sua própria branch, testar, realizar o commit, enviar a branch para o GitHub e criar o Pull Request.

🔁 Resumo rápido

Para uma nova funcionalidade:

# 1. Atualizar a main
git checkout main
git pull origin main

# 2. Criar uma branch
git checkout -b feature/minha-funcionalidade

# 3. Desenvolver e testar

# 4. Verificar alterações
git status
git diff

# 5. Adicionar arquivos
git add .

# 6. Criar commit
git commit -m "Adiciona minha funcionalidade"

# 7. Enviar para o GitHub
git push -u origin feature/minha-funcionalidade


Depois:

GitHub
   ↓
Pull Request
   ↓
main
   ↓
Revisão
   ↓
Aprovação
   ↓
Merge

📌 Regras essenciais
1. Nunca trabalhar diretamente na main

Sempre crie uma branch.

2. Sempre testar antes de entregar

Código não testado não deve ser enviado para aprovação.

3. Sempre criar Pull Request

O Pull Request é a forma oficial de entrega.

4. Nunca enviar informações sensíveis

Senhas, tokens, chaves e .env não devem ir para o GitHub.

5. Manter o código organizado

Evite alterações que não estejam relacionadas à tarefa.

6. Descrever o que foi feito

Todo Pull Request deve explicar claramente as alterações.

7. Respeitar a revisão

Alterações solicitadas devem ser corrigidas antes do merge.

📞 Responsabilidade do programador

É responsabilidade do programador garantir que sua entrega:

esteja funcionando;
esteja testada;
esteja organizada;
esteja documentada quando necessário;
não contenha informações sensíveis;
esteja na branch correta;
tenha commits claros;
possua um Pull Request devidamente preenchido.
🏢 EduConnect

Projeto: EduConnect
Repositório: EduConnect
Branch principal: main

A partir deste documento, este é o fluxo padrão recomendado para desenvolvimento e entrega das atualizações do projeto.

🚀 Fluxo oficial
┌──────────────────────┐
│  Receber a tarefa    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Atualizar a main     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Criar uma branch     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Desenvolver          │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Testar               │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Commit               │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Push para o GitHub   │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Pull Request → main  │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Revisão              │
└──────────┬───────────┘
           ↓
      ┌────┴─────┐
      │          │
   Ajustes    Aprovado
      │          │
      ↓          ↓
    Push       Merge
      │          │
      └────→ main ←────┘


Este fluxo deve ser seguido para manter o projeto EduConnect organizado, seguro e rastreável.
