# Source-Based Study

[English](README.md) | Português

Uma instrução de projeto do claude.ai que faz o Claude fazer perguntas sobre uma fonte, um conceito por vez, em vez de explicar a fonte para você.

Envie um link, um texto colado, um arquivo ou uma ideia. O Claude lista os conceitos da fonte e testa você em cada um com oito técnicas de aprendizagem.

## Por que usar em vez de "me ensine X"

Quando você pede ao Claude para ensinar um tema, o Claude escreve uma explicação e você lê. Ler dá a sensação de aprender, mas você não testa a sua memória.

Esta instrução muda a ordem:

- Você responde a uma pergunta antes de ler a explicação.
- O Claude explica só o que a sua resposta mostrou que você não sabe.
- O Claude dá a resposta correta e nomeia o seu erro específico depois de cada resposta.
- O Claude não elogia as suas respostas e não dá aula expositiva.

O custo: uma sessão é mais lenta do que ler um resumo. Se você precisa de uma visão rápida, peça um resumo.

## Exemplo

Este exemplo é ilustrativo. O Claude responde em formato de voz: mensagens curtas, uma pergunta cada.

> **Claude:** Li a fonte. Ela tem 3 conceitos: 1. Principal e taxa. 2. Juros compostos. 3. A regra dos 72. Antes de explicar o conceito 1, o que você acha que "principal" significa em um empréstimo?
>
> **Você:** Os juros?
>
> **Claude:** Não exatamente. Fora da fonte, o principal é o valor original do dinheiro, antes de qualquer juro. Os juros são o custo que se soma a esse valor. Com as suas palavras, como a taxa de juros se relaciona com o principal?

## Como usar

1. Abra o claude.ai e crie um novo projeto.
2. Copie o conteúdo de `instructions.md` (no macOS, rode o comando abaixo).
3. Cole nas instruções do projeto.
4. Abra um chat novo no projeto e envie a sua fonte.
5. Responda à primeira pergunta.

```bash
pbcopy < instructions.md
```

> **Dica:** use o modo de voz quando puder. Você responde falando, o que usa o efeito de produção (production effect). Uma revisão encontrou que produzir itens ao dizê-los, escrevê-los ou digitá-los pode melhorar algumas formas de memória de longo prazo em comparação com a leitura silenciosa ([MacLeod e Bodner, 2017](https://uwaterloo.ca/memory-attention-cognition-lab/sites/default/files/uploads/files/macleodbodner_cdps17_0.pdf)).

Fontes aceitas: um link público, texto colado, um PDF ou outro arquivo, ou uma ideia sem fonte. Para uma ideia, o Claude busca uma fonte na web e mostra o link primeiro.

## Como uma sessão funciona

O Claude repete estes passos para cada conceito. O Claude dá a resposta correta e o seu erro específico depois de cada resposta (passo 6).

| Passo | O que você faz | Técnica |
|---|---|---|
| 1 | Responde 1 ou 2 perguntas antes de qualquer explicação. | [Pré-teste (Pretest)](https://pubmed.ncbi.nlm.nih.gov/37640836/) |
| 2 | Lê uma solução completa, passo a passo. O Claude mostra isso só para cálculos e procedimentos sem código. | [Exemplo resolvido (Worked example)](https://link.springer.com/article/10.1007/s10648-023-09745-1) |
| 3 | Explica com suas palavras como o conceito funciona. | [Autoexplicação (Self-explanation)](https://link.springer.com/article/10.1007/s10648-018-9434-x) |
| 4 | Explica por que o conceito é verdadeiro. | [Interrogação elaborativa (Elaborative interrogation)](https://www.uwlax.edu/catl/guides/teaching-improvement-guide/how-can-i-improve/elaborative-interrogation/) |
| 5 | Responde 2 ou 3 perguntas novas, sem a fonte. | [Prática de recuperação (Retrieval practice)](https://eric.ed.gov/?id=EJ1141817) |
| 6 | Recebe a resposta correta e o erro específico depois de cada resposta. | [Feedback](https://www.frontiersin.org/articles/10.3389/fpsyg.2019.03087/full) |
| 7 | Explica o conceito inteiro para um iniciante. | [Ensino (Learning by teaching)](https://onlinelibrary.wiley.com/doi/10.1111/jpr.12221) |
| 8 | No fim, responde perguntas misturadas de todos os conceitos. | [Prática intercalada (Interleaved practice)](https://www.psychologie.uni-wuerzburg.de/fileadmin/06020400/2019/Brunmair_Richter_in_press__2019_META-ANALYSIS_OF_INTERLEAVED_LEARNING.pdf) |

Depois do último conceito, o Claude faz pelo menos uma pergunta aberta por conceito, em ordem misturada (passos 5 e 8), e diz que a sessão está completa. Se você sair e voltar, o Claude continua no próximo conceito que não está completo.

## Limites

- O Claude não lê links privados nem páginas que exigem login. Cole o texto nesses casos.
- A instrução não agenda revisões. Ela não sugere revisão espaçada. Controle as suas revisões fora do projeto.
- O Claude usa só fatos da fonte ou da web. Quando o Claude não tem fonte para um fato, ele diz isso.
- Nenhuma avaliação compara sessões com esta instrução a outras formas de estudar. A pesquisa acima cobre cada técnica, não esta combinação.

## Alterar a instrução

1. Edite `instructions.md`.
2. Teste com uma fonte curta.
3. Confira se cada mensagem da fase de prática termina com exatamente uma pergunta e tem no máximo 4 frases antes dela.
