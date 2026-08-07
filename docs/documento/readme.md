1. Sobre o Projeto
O EduConnect é um sistema desenvolvido para automatizar as operações de uma farmácia (estudo de caso), substituindo processos manuais por uma plataforma integrada que gerencia vendas, estoque, caixa, preços e usuários.
Este repositório contém exclusivamente os documentos técnicos do projeto, incluindo:

Visão geral do sistema

Estudo de viabilidade

Requisitos funcionais e não funcionais

Regras de negócio

Histórico de revisões

2. Estrutura dos Documentos
Todos os documentos técnicos seguem o modelo base presente no arquivo DocumentacaoTecnicaXXXXX.docx (onde XXXXX é o código de versão, ex.: X-0001).
Cada documento contém:

Cabeçalho com título, código do documento, nomes dos autores e data da última atualização.

Histórico de revisões (tabela com data, versão, descrição da alteração e autor).

Identificação dos envolvidos (papel, nome e e-mail).

Corpo do documento (visão geral, requisitos, regras, etc.).

3. Como Atualizar um Documento
Sempre que houver uma alteração no conteúdo (adição, correção, melhoria ou reorganização), você deve atualizar o documento seguindo o procedimento abaixo. Isso garante que o histórico reflita fielmente a evolução do projeto.

3.1. Fluxo Geral
Identifique a necessidade de mudança

Correção de erros

Inclusão de novos requisitos

Ajuste de regras de negócio

Revisão de viabilidade

Organização ou formatação

Faça as alterações no conteúdo do arquivo .docx (ou no formato que a equipe utiliza).

Atualize o cabeçalho:

Versão: incremente o número (ex.: de X-0001 para X-0002 – ver padrão abaixo).

Data: coloque a data atual no formato DD/MM/AAAA.

Preencha o histórico de revisões com uma nova linha:

Data: mesma data do cabeçalho.

Versão: nova versão (ex.: X-0002).

Descrição da alteração: resumo claro e objetivo do que foi mudado.

Autor: nome de quem realizou a alteração.

Atualize a lista de envolvidos se houver mudança de papéis ou contatos.

Salve o documento com o novo código de versão no nome do arquivo (ex.: DocumentacaoTecnicaX-0002.docx).

Commite e push no repositório, com uma mensagem descritiva (ex.: docs: atualiza documentação para versão X-0002 – adiciona RN012).

3.2. Padrão de Versionamento (Código do Documento)
Utilizamos o padrão X-XXXX, onde:

X indica a família do documento (para este projeto, usamos X).

XXXX é um número sequencial de 4 dígitos, começando em 0001.

Exemplos:

X-0001 → primeira versão

X-0002 → segunda versão

X-0003 → terceira versão (e assim por diante)

Importante: Nunca reutilize um número de versão. Cada alteração significativa (mesmo que pequena) gera um novo número.

3.3. Exemplo Prático de Atualização
Suponha que você precise adicionar uma nova regra de negócio (RN012) e corrigir um requisito funcional (RF003).

Passo 1: Edite o conteúdo – insira a nova RN e corrija RF003.

Passo 2: Altere o cabeçalho:

Versão: X-0002 (se antes era X-0001)

Data: 07/08/2026

Passo 3: Adicione ao histórico de revisões:

Data	Versão	Descrição da Alteração	Autor
07/08/2026	X-0002	Adicionada RN012; corrigido RF003 (pesquisa por categoria)	Seu Nome
Passo 4: Renomeie o arquivo para DocumentacaoTecnicaX-0002.docx.

Passo 5: Commit com mensagem: docs: atualiza doc para X-0002 – nova RN e correção RF003.

4. Boas Práticas para a Documentação
Seja descritivo no histórico: use frases curtas, mas que permitam entender o que foi alterado sem precisar abrir o documento.

Mantenha a coerência: se alterar um requisito, verifique se as regras de negócio e os testes (se houver) ainda estão alinhados.

Revise antes de commitar: peça a um colega para revisar as alterações, especialmente se forem grandes.

Nunca sobrescreva versões anteriores: mantenha todos os arquivos no repositório (ou use o histórico do Git para acessar versões antigas).

Use o mesmo padrão de datas: sempre no formato DD/MM/AAAA para evitar ambiguidades.

5. Responsabilidades
Cada membro da equipe pode propor alterações, mas as atualizações que impactam o escopo ou a arquitetura do sistema devem ser validadas em reunião de equipe.

Líder de Documentação: Gabriel Henrique Lopes Garcia (responsável por aprovar versões principais e garantir a consistência geral).

Demais membros: podem atualizar partes específicas (ex.: Arthur cuida da visão geral, Rafael dos requisitos, etc.), sempre seguindo o fluxo descrito.

6. Ferramentas e Ambiente
Editor de texto recomendado: Microsoft Word / LibreOffice Writer (compatível com .docx).

Controle de versão: Git + GitHub/GitLab (repositório privado da equipe).

Convenção de commits: utilize prefixos como docs:, fix:, feat: para facilitar a rastreabilidade.

7. Perguntas Frequentes
Posso alterar mais de uma coisa na mesma versão?
Sim, desde que todas as alterações sejam descritas no histórico de revisões de forma resumida.

E se eu esquecer de atualizar a versão?
O revisor ou o líder de documentação deve apontar o erro antes do merge. Se já tiver sido commitado, faça um novo commit corrigindo a versão e o histórico.

Preciso atualizar o README quando mudar o documento?
Não, a menos que as instruções deste README mudem. O README serve como guia fixo.

8. Contato
Em caso de dúvidas sobre o processo de documentação, entre em contato com o líder de documentação ou com qualquer um dos autores listados no cabeçalho do documento.

Última atualização deste README: 06/08/2026
