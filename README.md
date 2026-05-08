[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/zHqjFsRx)
# Diagnóstico de retomada - Teoria da Computação

Esta atividade serve para mapear o que você já domina sobre linguagens formais, autômatos, gramáticas e computabilidade.

Responda individualmente. Use suas palavras. Se usar IA depois da primeira tentativa, registre o uso na seção 7.

## 1. Mapa do que eu lembro

Marque cada tópico como: lembro bem, lembro parcialmente, não lembro, nunca vi ou não tenho certeza.

- alfabeto: lembro bem
- cadeia: lembro bem
- linguagem: lembro bem
- gramática: lembro parcialmente
- autômato finito: lembro parcialmente
- linguagem regular: lembro bem
- linguagem livre de contexto: lembro parcialmente
- linguagem sensível ao contexto: lembro parcialmente
- linguagem irrestrita: nao lembro
- hierarquia de Chomsky: nao lembro
- computabilidade: nao lembro
- máquina de Turing: lembro parcialmente

## 2. Definições com exemplo

Explique, com suas palavras e com um exemplo simples, usando o alfabeto `Sigma = {a, b}`.

1. O que é um alfabeto? conjunto finito de simbolos ou caracteres ex: {a, b}
2. O que é uma cadeia? sequencia finita de simbolos de um alfabeto especifico ex: aab
3. O que é uma linguagem? semantica, sintaxe e reconhecido por automatos ex: {a^n b | n>=0}
4. O que é uma gramática? conjunto das regras para formar uma cadeia valida ex: S → aS | b

## 3. Linguagens

Considere as linguagens:

```text
L1 = { w em {0,1}* | w termina com 01 }
L2 = { a^n b^n | n >= 0 }
L3 = { a^n b^n c^n | n >= 0 }
```

Para cada linguagem:

1. escreva três palavras que pertencem à linguagem;
L1: `01` `0001` `1101`
L2: ` ` `ab` `aabb`
L3: ` ` `abc` `aabbcc`
2. escreva duas palavras que não pertencem;
L1: ` ` `10` `0000` `1111` `0110`
L2: `ba` `aab` `bbaa`
L3: `acb` `aabbc` `ccbbaa`
3. diga, se souber, em qual classe ela provavelmente se encaixa;
nao sei
4. explique o motivo em linguagem simples.
nao sei

Não há problema em dizer "não sei". Nesse caso, escreva o que te deixou em dúvida.

## 4. Autômato finito

Considere o autômato abaixo, sobre o alfabeto `{0,1}`:

```text
Estados: q0, q1, q2
Estado inicial: q0
Estado final: q2

Transições:
q0 --0--> q1
q0 --1--> q0
q1 --0--> q1
q1 --1--> q2
q2 --0--> q1
q2 --1--> q0
```

Responda:

1. Qual linguagem esse autômato parece reconhecer?
strings com sequencia `01`
2. Execute manualmente as cadeias abaixo e diga se aceita ou rejeita:
   - `01` aceita
   - `101` aceita
   - `100` nao aceita
   - `1101` aceita
   - `111` nao aceita
3. Monte uma tabela curta mostrando o caminho dos estados para pelo menos duas cadeias.
| 01 | q0 → q1 → *q2* | Aceita
| 101 | q0 → q0 → q1 → *q2* | Aceita
| 100 | q0 → q0 → q1 → q1 | Rejeita
| 1101 | q0 → q0 → q0 → q1 → *q2* | Aceita
| 111 | q0 → q0 → q0 → q0 | Rejeita

## 5. Gramática

Considere a gramática:

```text
S -> aS
S -> b
```

Responda:

1. Gere cinco cadeias produzidas por essa gramática.
| S → b | b
| S → aS → ab | ab
| S → aS → aaS → aab | aab
| S → aS → aaS → aaaS → aaab | aaab
| S → aS → ... → aaaaab | aaaaab

2. Descreva a linguagem em palavras.
na notacao formal fica: L = { aⁿb | n ≥ 0 }
exemplos: `b` `ab` `aab` `aaab` `aaaab`
a regra S → aS vai empilhando a`s indefinidamente, e a regra S → b encerra a derivação com um b no final

3. Essa gramática parece regular, livre de contexto ou outra classe? Justifique de forma simples.
Ela é regular
- S → aS → um terminal (a) seguido de um não-terminal (S) à direita
- S → b → apenas um terminal

## 6. Ponto de dificuldade

Escolha um tópico da lista inicial e escreva:

1. o que você entende dele;
topico 3, entendo bem mas nao domino
3. onde você se confunde;
as classes
5. que tipo de explicação ajudaria: desenho, exemplo, exercício guiado, analogia, prova passo a passo ou lista curta.
exemplos, analogia

## 7. Uso de IA, se houver

Se você usou IA depois da primeira tentativa, registre:

```text
Pergunta feita:
Resumo da resposta:
Como eu verifiquei:
O que eu alterei na minha resposta:
O que ainda não entendi:
```

## Submissão no Moodle

Depois de finalizar, copie no Moodle:

```text
Repositório:
Commit final:
Autoavaliação: nível atual, maior dificuldade e tópico que precisa ser retomado.
```
