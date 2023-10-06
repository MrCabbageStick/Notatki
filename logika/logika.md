# LOGIKA

### Symbole:
<!-- $$\neg \land \lor \to \leftrightarrow$$ -->
$\neg$ negacja (zaprzeczenie)\
$\land$ koniunkcja\
$\lor$ alternatywa\
$\to$ implikacja\
$\leftrightarrow$ równoważnik

### Logika zdaniowa:
*Każde zdanie ma wartość logiczną: prawdę (1) lub fałsz (0).*

#### Jeden podział
1. Zdania przygodne: wartość zdania zależy od sytuacji i okoliczności
2. Zdanie konieczne: wartość nie zależy od sytuacji lub okoliczności

#### Przykład:
Zdanie przygodne: "Janek jest wysoki." ->  wartość zależy od wyborażenia lub osoby Janka.

Zdanie konieczne: "Pada deszcz albo nie pada deszcz" -> niezależnie od kontekstu zdanie jest prawdziwe lub nie.

---
#### Drugi podział
1.  Zdanie proste (elementarne): Zdanie nie można podzielić na mniejsze zdania zachowując przy tym sens logiczny.
2.  Złożone: złożone ze zdań prostych i przez to można je podzielić na mniejsze.

#### Przykład:

Zdanie proste (elementarne): "Dzisiaj pada deszcz"\
Zdanie złożone: "Wezmę parasol, jeśli będzie padał deszcz"

---
### Sposoby składania zdań:
| Nazwa | Spójnik w zdaniu | Symbol logiczny | Opis |
|-|-|-|-|
| Koniunkcja | "i" | $\land$ | Koniunkcja jest prawdziwa wtedy i tylko wtedy, gdy wszystkie zdania tworzące koniunkcję są prawdziwe. |
| Alternatywa | "lub" | $\lor$ | Alternatywa jest prawdziwa wtedy i tylko wtedy, gdy chociaż jedno zdanie ja tworzące jest prawdziwe. |
| Implikacja | "jeśli... to..." | $\to$ | Fałszywa wtedy i tylko wtedy, gdy poprzednik jest prawdziwy, a następnik fałszywy. Poprzednik występuje po "jeżeli", a następnik po "to". |
| Równoważnik | "...wtedy i tylko wtedy, gdy..." | $\leftrightarrow$ | Prawdziwa wtedy i tylko wtedy, gdy obie składowe są równocześnie prawdziwe lub jednocześnie fłaszywe |
| Negacja | "Nieprawda, że..." | $\neg$ | Prawdziwa, gdy zdanie początkowe jest fałszywe |

---
### Język logiki formalnej:

Zdania proste oznacza się jako: P<sub>0</sub>, P<sub>1</sub>, P<sub>2</sub>, P<sub>3</sub>, ...\
Jeżeli zdań jest mniej niż 6 można użyc: P, Q, R, S, T


#### Przykład zdania:

"Jan jest wysoki i nie prawda, że Jan jest piłkarzem"

Rozbicie: 
- P = "Jan jest wysoki"
- Q = "Jan jest piłkarzem"

Zapis logiczny: \
(P $\land \neg$ Q)\
Zdania należy zamykać w nawiasach okrągłych

---
### Definicja poprawnie zbudowanej formuły logiki zdaniowej

P.Z.F. (Poprawnie zbudowana formuła) jest pojedynczą zmienną (symbolem) zdaniową lub jest w postaci:
- $(\alpha \land \beta)$
- $(\alpha \lor \beta)$
- $(\alpha \to \beta)$
- $(\alpha \leftrightarrow \beta)$

, gdzie $\alpha, \beta$ są p.z.f.

#### Przykłady:
| Zdanie | Jego poprawność | Wytłumaczenie |
|-|-|-|
| P | ✅ | - |
| P<sub>3</sub> | ✅ | - |
| P $\land$ Q | ❌ | Zdanie nie zamknięte w nawiasach |
| (P $\land$ Q) | ✅ | - |
| $\neg$ P | ✅ | - |
| ($\neg$ P) | ❌ | Negacja nie może znajdować sie w nawiasie tak sama z siebie |
| $\neg \neg$ P | ✅ | Dwie negacje mogą występować zaraz po sobie |
| <span style="white-space: nowrap">(((P $\land$ Q) $\to\neg$ P) $\lor$ (R $\leftrightarrow\neg$ Q))</span> | ✅ | - |

**Podformułą** nazywamy napis, który jest częścią pewnej formuły i jest p.z.f.\
Zdanie: (((P $\land$ Q) $\to\neg$ P) $\lor$ (R $\leftrightarrow\neg$ Q))\
❌ **Niepoprawne** podzdanie: P) $\lor$ (R\
✅ Poprawne podzdanie: (P $\land$ Q)\
✅ Inne poprawne podzanie: Q


### Tabele prawdy dla symboli:
(*Nie było na wykładzie ale ja je lubię*)

<div class="truth-tables">
<div class="truth-table__wrapper">

Koniunkcja (AND):
| P | Q | AND |
|-|-|-|
|0|0|0|
|0|1|0|
|1|0|0|
|1|1|1|
</div>

<div class="truth-table__wrapper">

Alternatywa (OR)
| P | Q | OR |
|-|-|-|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

</div>
<div class="truth-table__wrapper">

Implikacja (¯\\_(ツ)_/¯)
| P | Q | $\to$ |
|-|-|-|
|0|0|1|
|0|1|1|
|1|0|0|
|1|1|1|

</div>
<div class="truth-table__wrapper">

Równoważnik (XNOR)
| P | Q | XNOR |
|-|-|-|
|0|0|1|
|0|1|0|
|1|0|0|
|1|1|1|

</div>
<div class="truth-table__wrapper">

Negacja (NOT)
| P | NOT |
|-|-|
|0|1|
|1|0|

</div>
</div>

**Legenda**:\
P, Q - Wartość zdania wejściowego\
AND, OR, $\to$, XNOR, NOT - Wartość zdania wyjściowego

<style>
    .truth-tables{
        display: flex;
        gap: 1rem;
        flex-wrap: wrap;
    }

    .truth-table__wrapper{
        border-left: 1px solid currentcolor;
        padding-left: .5rem;
    }
</style>