# 📚 EduConnect – Documentação Técnica

> Repositório destinado ao gerenciamento da documentação técnica do projeto **EduConnect**, seguindo um padrão de versionamento e controle de alterações.

---

# 📖 Sobre o Projeto

O **EduConnect** é um sistema desenvolvido para automatizar as operações de uma **farmácia** (estudo de caso), substituindo processos manuais por uma plataforma integrada para gerenciamento de:

* 💰 Vendas
* 📦 Estoque
* 💵 Caixa
* 🏷️ Preços
* 👥 Usuários

Este repositório contém **exclusivamente a documentação técnica** do projeto.

## Documentos disponíveis

* Visão Geral do Sistema
* Estudo de Viabilidade
* Requisitos Funcionais
* Requisitos Não Funcionais
* Regras de Negócio
* Histórico de Revisões

---

# 📂 Estrutura dos Documentos

Todos os documentos seguem como base o modelo:

```text
DocumentacaoTecnicaX-0001.docx
```

Cada documento possui:

* Cabeçalho

  * Título
  * Código do documento
  * Autores
  * Data da última atualização

* Histórico de Revisões

  * Data
  * Versão
  * Descrição
  * Autor

* Identificação dos Envolvidos

  * Papel
  * Nome
  * E-mail

* Corpo do Documento

  * Visão Geral
  * Requisitos
  * Regras de Negócio
  * Demais informações técnicas

---

# ✏️ Como Atualizar um Documento

Sempre que houver qualquer alteração relevante no documento, siga o fluxo abaixo.

## 1️⃣ Identifique a necessidade

A alteração pode ser:

* Correção de erros
* Inclusão de novos requisitos
* Ajuste de regras de negócio
* Revisão de viabilidade
* Melhorias de organização
* Alterações de formatação

---

## 2️⃣ Atualize o conteúdo

Realize as alterações normalmente no arquivo **.docx**.

---

## 3️⃣ Atualize o cabeçalho

Modifique:

| Campo  | Ação                          |
| ------ | ----------------------------- |
| Versão | Incrementar (X-0001 → X-0002) |
| Data   | Data atual (DD/MM/AAAA)       |

---

## 4️⃣ Atualize o Histórico de Revisões

Adicione uma nova linha à tabela.

| Data       | Versão | Descrição                      | Autor |
| ---------- | ------ | ------------------------------ | ----- |
| DD/MM/AAAA | X-0002 | Resumo objetivo das alterações | Nome  |

---

## 5️⃣ Atualize os envolvidos

Caso haja mudança de responsáveis, cargos ou contatos, atualize essa seção.

---

## 6️⃣ Renomeie o arquivo

Utilize sempre a nova versão.

**Exemplo**

```text
DocumentacaoTecnicaX-0002.docx
```

---

## 7️⃣ Commit e Push

Utilize mensagens claras.

**Exemplo**

```bash
docs: atualiza documentação para versão X-0002 - adiciona RN012
```

---

# 🔢 Padrão de Versionamento

Os documentos utilizam o padrão:

```text
X-XXXX
```

Onde:

| Parte | Significado                     |
| ----- | ------------------------------- |
| X     | Família do documento            |
| XXXX  | Número sequencial com 4 dígitos |

## Exemplos

| Versão | Descrição       |
| ------ | --------------- |
| X-0001 | Primeira versão |
| X-0002 | Segunda versão  |
| X-0003 | Terceira versão |

> **Importante:** Nunca reutilize números de versão. Toda alteração significativa gera uma nova versão.

---

# 💡 Exemplo de Atualização

Suponha que seja necessário:

* adicionar a regra **RN012**
* corrigir o requisito **RF003**

## Cabeçalho

| Campo  | Valor      |
| ------ | ---------- |
| Versão | X-0002     |
| Data   | 07/08/2026 |

## Histórico

| Data       | Versão | Descrição                                                  | Autor    |
| ---------- | ------ | ---------------------------------------------------------- | -------- |
| 07/08/2026 | X-0002 | Adicionada RN012; corrigido RF003 (pesquisa por categoria) | Seu Nome |

## Novo nome do arquivo

```text
DocumentacaoTecnicaX-0002.docx
```

## Commit

```bash
docs: atualiza doc para X-0002 - nova RN e correção RF003
```

---

# ✅ Boas Práticas

* Escreva descrições objetivas no histórico de revisões.
* Verifique se requisitos e regras de negócio continuam consistentes.
* Solicite revisão de outro membro antes de grandes alterações.
* Nunca sobrescreva versões anteriores.
* Utilize sempre datas no formato **DD/MM/AAAA**.
* Mantenha o padrão de documentação em todos os arquivos.

---

# 👥 Responsabilidades

Cada integrante pode propor alterações.

Entretanto, mudanças que impactem:

* escopo
* arquitetura
* estrutura geral do sistema

devem ser aprovadas em reunião da equipe.

## Líder de Documentação

**Gabriel Henrique Lopes Garcia**

Responsável por:

* Aprovação das versões principais
* Garantia da consistência da documentação

## Demais membros

Cada integrante pode ser responsável por partes específicas da documentação.

Exemplo:

| Membro | Responsabilidade  |
| ------ | ----------------- |
| Arthur | Visão Geral       |
| Rafael | Requisitos        |
| ...    | Demais documentos |

---

# 🛠 Ferramentas

| Ferramenta         | Utilização            |
| ------------------ | --------------------- |
| Microsoft Word     | Edição dos documentos |
| LibreOffice Writer | Compatível com .docx  |
| Git                | Controle de versão    |
| GitHub/GitLab      | Repositório da equipe |

### Convenção de commits

Utilize os prefixos:

```text
docs:
fix:
feat:
```

Exemplos:

```bash
docs: atualiza documentação

fix: corrige requisito RF008

feat: adiciona RN015
```

---

# ❓ Perguntas Frequentes (FAQ)

### Posso alterar mais de uma coisa na mesma versão?

Sim. Basta descrever todas as alterações de forma resumida no histórico de revisões.

---

### Esqueci de atualizar a versão. O que fazer?

O revisor ou líder de documentação deverá identificar o problema antes do merge.

Caso já tenha sido enviado ao repositório, faça um novo commit corrigindo:

* versão
* histórico de revisões

---

### Preciso atualizar este README quando alterar um documento?

Não.

Atualize o README apenas quando houver mudanças nas instruções ou no processo de documentação.

---

# 📬 Contato

Em caso de dúvidas sobre o processo de documentação, entre em contato com:

* Líder de Documentação
* Qualquer um dos autores listados no cabeçalho dos documentos

---

## 📅 Última atualização

**06/08/2026**
