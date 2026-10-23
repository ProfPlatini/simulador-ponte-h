# Simulador de Ponte H

Bancada virtual para aprender a **montar uma ponte H com transistores TIP122**, passo a passo, no celular ou no computador. Feita para apoiar os alunos de eletroeletrônica na atividade prática da revisadeira (componente SELAN 2).

**Acesse:** https://profplatini.github.io/simulador-ponte-h/

## Para que serve

Na atividade, o motor de uma revisadeira precisa girar nos dois sentidos: um botão para FRENTE e outro para RÉ. O circuito usa 4 transistores TIP122 em ponte H e 2 transistores BC337 que impedem o curto-circuito (intertravamento).

Este programa permite montar o circuito antes ou depois da aula, sem material físico, e entender por que cada ligação existe.

## Como usar

1. Abra o link no navegador. Não precisa instalar nada nem criar conta.
2. Siga os 11 passos. Em cada um o programa diz qual peça colocar e quais terminais ligar.
3. **Peças:** toque na peça na gaveta e depois no lugar marcado na bancada. Se a peça for a errada, o programa explica o motivo.
4. **Fios:** toque em um terminal e depois em outro, ou arraste de um ao outro. Ligações erradas mostram uma mensagem explicando por que não se ligam.
5. No último passo, aperte FRENTE, RÉ e os dois juntos para ver o motor, os LEDs e os transistores que conduzem.

Botões da bancada: **Dica** (destaca a próxima ligação), **+ / −** (zoom), **Tudo** (vê a bancada inteira) e **Desfazer** (volta a última ação; com um fio selecionado, vira **Remover fio**).

## O circuito

| Parte | Função |
|---|---|
| Q1 a Q4 (TIP122) | Chaves da ponte H. Q1 e Q4 conduzem em FRENTE; Q2 e Q3 em RÉ |
| Q5 e Q6 (BC337) | Intertravamento: impedem que dois transistores do mesmo lado conduzam juntos |
| R1 a R4 | Limitam a corrente de base dos TIP122 (1 kΩ em cima, 4,7 kΩ embaixo) |
| R5 e R6 (10 kΩ) | Comando dos BC337 |
| R7 (470 Ω) + LEDs | LED verde indica FRENTE e LED vermelho indica RÉ |
| Motor DC 3 a 6 V | Mini motor que representa o da revisadeira |
| Fonte | 7,5 V (nunca passar de 8 V na bancada real) |

## Observações

- Os valores medidos no teste (tensão no motor, VCE dos transistores) são **valores típicos da simulação**. Na bancada real eles variam um pouco.
- O programa é uma ferramenta de estudo. Na bancada, confira sempre os terminais dos TIP122 e desligue a fonte se algum transistor esquentar muito.
- O progresso fica salvo apenas no navegador do aluno. Em outro aparelho ou navegador, a montagem recomeça do passo 1.

## Estrutura do repositório

```
index.html   o programa completo (HTML, CSS e JavaScript em um único arquivo)
README.md    este arquivo
```

Não há dependências nem etapa de build. As fontes vêm do Google Fonts quando há internet.

## Publicação

O site é publicado com o GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / `(root)`**.

## Autor

Prof. Platini, instrutor de eletroeletrônica. Atividade prática de Sistemas Eletroeletrônicos Analógicos 2 (SELAN 2).
