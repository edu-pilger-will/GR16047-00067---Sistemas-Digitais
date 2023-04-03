# Revisão aula 02 

## Solução de tabela verdade por MINTERMOS

| A | B | S | Mintermos |
| --- | --- | --- | --- |
| 0 | 0 | 1 | `An * Bn` |
| 0 | 1 | 1 | An * B` |
| 1 | 0 | 0 | A * Bn |
| 1 | 1 | 0 | A * B |

Soma-se então os produtos das situações em que `S` é `1`:
> `An` * `Bn`  +  `An` * `B`



## Solução de tabela verdade por MAXTERMOS

| A | B | S | Maxtermos |
| --- | --- | --- | --- |
| 0 | 0 | 1 | A + B |
| 0 | 1 | 1 | A + Bn |
| 1 | 0 | 0 | `An + B` |
| 1 | 1 | 0 | `An + Bn` |

Multiplica-se então as somas das situações em que `S` é `0`:
> (`An`+`B`) * (`An`+`Bn`)




# Aula 03: Simplificando as equações

## Propriedades algébricas

- Adição lógica:
    - **A** + **0** = **0**
    - **A** + **1** = **1**
    - **A** + **A** = **A**
    - **A** + **An** = **1**
- Multiplicação lógica:
    - **A** * **0** = **0**
    - **A** * **1** = **A**
    - **A** * **A** = **A**
    - **A** * **An** = **0**
- Complementação:
    - **Ann** = **A**
    - **Annn** = **An**
    - ...
- Comutatividade:
    - **A** + **B** = **B** + **A**
    - **A** * **B** = **B** * **A**
- Associatividade:
    - **A** + **B** + **C** = (**A** + **B**) + **C** = (**A** + **C**) + **B**
    - **A** * **B** * **C** = (**A** * **B**) * **C** = (**A** * **C**) * **B**
- Distributiva:
    - **A** * (**B** + **C**) = **A** * **B** + **A** * **C**

## Simplificando os exercícios anteriores (aula anterior):

>`S` = `An` * `Bn`  +  `An` * `B`

>`S` = `An` * (`Bn` + `B`)

>`S` = `An` * `1`

>`S` = `An`

 
 e

>`S` = (`An`+`B`) * (`An`+`Bn`)

>`S` = (`An` + `B`) * `An` + (`An` + `B`) * `Bn`

>`S` = `An` * `An` + `An` * `B` + `Bn` * `An` + `Bn` * `B`

>`S` = `An` + `An` * `B` + `An` * `Bn`

>`S` = `An` + `An` * `B` + `An` * `Bn`

>`S` = `An` * (`1` + `B` + `B`)

>`S` = `An`


## Teorema de Morgan

(`A` * `B` * `C` * ...)n = `An` + `Bn` + `Cn` + `...`

(`A` + `B` + `C` + ...)n = `An` * `Bn` * `Cn` * `...`


## Propriedade Especial - *Decoreba*

Quando existem DUAS (e somente se) variáveis, o correspondente do item que **não está na multiplicação** somado ao **item que multiplica** é a solução. Veja: 

> `A` + `An` * `B` = `B` + `A`

> `Bn` + `An` * `B` = `An` + `Bn`

---

## Exercícios

Simplifique as equações:

**X** = `A` * `B` * `C` + `An` * `C`

*solução*
```txt
X = A.B.C + An.C
X = C.(A.B+An)
X = C.(An+B)
```


**X** = `A` * `B` * `C` + `An` * `B` * `C` + `An`

*solução*
```txt
X = A.B.C + An.B.C + An
X = B.C.(A+An) + An
X = B.C + An
```

*solução 2*
```txt
X = A.B.C + An.B.C + An
X = A.B.C + An.(B.C + 1)
X = A.B.C + An           <-- Imagina B.C como X, e aplica a propriedade especial
X = B.C + An
```


**Q** = (`R` * `S` * `T`)n * (`R` + `S` + `T`)n

*solução*
```txt
Q = (R.S.T)n * (R+S+T)n
Q = (Rn+Sn+Tn) * Rn.Sn.Tn
Q = Rn.Sn.Tn.Rn + Rn.Sn.Tn.Sn + Rn.Sn.Tn.Tn
Q = (Rn.Rn).Sn.Tn + Rn.(Sn.Sn).Tn + Rn.Sn.(Tn.Tn)
Q = Rn.Sn.Tn + Rn.Sn.Tn + Rn.Sn.Tn
Q = Rn.Sn.Tn
```

