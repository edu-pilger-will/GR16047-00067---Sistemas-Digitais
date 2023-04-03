# Aula 4

## Solução de tabela verdade por KARNAUGH

Para esta tabela verdade:

| A | B | S |
| --- | --- | --- |
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

Temos:

| B\A | 0 | 1 |
| --- | --- | --- |
| 0 | 1 | 1 |
| 1 | 0 | 0 |

Associa-se, então, as posições em nível alto (1) a cada 2, 4 ou 8 que estejam alinhados na vertical ou horizontal.

Depois, olha-se pra esses grupos criados. Se o valor da saída foi interferido pela variável de entrada, ela faz parte da saída.

No exemplo acima, a resposta é `Bn`.


### Exemplo 2:

Dada a tabela verdade:
| A | B | S |
| --- | --- | --- |
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

Temos:

| B\A | 0 | 1 |
| --- | --- | --- |
| 0 | `1` | `1` |
| 1 | `1` | 0 |

Agora, formam-se dois grupos , e a resposta é `An+Bn`.

### Exemplo 3: Três variáveis

Dada a tabela verdade:

<table>
    <tr>
        <th style="color:green">A</th>
        <th style="color:red">B</th>
        <th style="color:blue">C</th>
        <th>S</th>
    </tr>
    <tr>
        <th>0</th>
        <th>0</th>
        <th>0</th>
        <th>0</th>
    </tr>
    <tr>
        <th>0</th>
        <th>0</th>
        <th>1</th>
        <th>0</th>
    </tr>
    <tr>
        <th>0</th>
        <th>1</th>
        <th>0</th>
        <th>1</th>
    </tr>
    <tr>
        <th>0</th>
        <th>1</th>
        <th>1</th>
        <th>1</th>
    </tr>
    <tr>
        <th>1</th>
        <th>0</th>
        <th>0</th>
        <th>0</th>
    </tr>
    <tr>
        <th>1</th>
        <th>0</th>
        <th>1</th>
        <th>1</th>
    </tr>
    <tr>
        <th>1</th>
        <th>1</th>
        <th>0</th>
        <th>0</th>
    </tr>
    <tr>
        <th>1</th>
        <th>1</th>
        <th>1</th>
        <th>1</th>
    </tr> 
</table>

Teremos:

<table>
    <tr>
        <th><span style="color:green">A</span><span style="color:red">B</span><span style="color:blue">C</span></th>
        <th><span style="color:green">0</span><span style="color:red">0</span></th>
        <th><span style="color:green">0</span><span style="color:red">1</span></th>
        <th><span style="color:green">1</span><span style="color:red">1</span></th>
        <th><span style="color:green">1</span><span style="color:red">0</span></th>
    </tr>
    <tr>
        <th style="color:blue">0</th>
        <th>0</th>
        <th style="background-color:orange">1</th>
        <th>0</th>
        <th>0</th>
    </tr>
    <tr>
        <th style="color:blue">1</th>
        <th>0</th>
        <th style="background-color:orange">1</th>
        <th style="background-color:tomato">1</th>
        <th style="background-color:tomato">1</th>
    </tr>
</table>

Onde a resposta fica <span style="background-color:orange;padding:5px;">**An.B**</span>+<span style="background-color:tomato;padding:5px;">**A.C**</span>

> S = `An`.`B` + `A`.`C`

### Exemplo 4

Para o mapa abaixo:

<table>
    <tr>
        <th><span style="color:green">A</span><span style="color:red">B</span><span style="color:blue">C</span></th>
        <th><span style="color:green">0</span><span style="color:red">0</span></th>
        <th><span style="color:green">0</span><span style="color:red">1</span></th>
        <th><span style="color:green">1</span><span style="color:red">1</span></th>
        <th><span style="color:green">1</span><span style="color:red">0</span></th>
    </tr>
    <tr>
        <th style="color:blue">0</th>
        <th style="background-color:orange">1</th>
        <th style="background-color:orange">1</th>
        <th>0</th>
        <th>X</th>
    </tr>
    <tr>
        <th style="color:blue">1</th>
        <th style="background-color:orange">1</th>
        <th style="background-color:orange">1</th>
        <th>0</th>
        <th>X</th>
    </tr>
</table>

Temos a resposta <span style="background-color:orange;padding:5px;">**An**</span>

### Exemplo 5

Para o mapa abaixo:

<table>
    <tr>
        <th><span style="color:green">A</span><span style="color:red">B</span><span style="color:blue">C</span><span style="color:yellow">D</span></th>
        <th><span style="color:green">0</span><span style="color:red">0</span></th>
        <th><span style="color:green">0</span><span style="color:red">1</span></th>
        <th><span style="color:green">1</span><span style="color:red">1</span></th>
        <th><span style="color:green">1</span><span style="color:red">0</span></th>
    </tr>
    <tr>
        <th><span style="color:blue">0</span> <span style="color:yellow">0</span></th>
        <th>0</th>
        <th style="background-color:#FF7E00">1</th>
        <th style="background-color:orange">1</th>
        <th>0</th>
    </tr>
    <tr>
        <th><span style="color:blue">0</span> <span style="color:yellow">1</span></th>
        <th>0</th>
        <th style="background-color:orange">1</th>
        <th style="background-color:orange">1</th>
        <th>0</th>
    </tr>
    <tr>
        <th><span style="color:blue">1</span> <span style="color:yellow">0</span></th>
        <th style="background-color:#999">1</th>
        <th>0</th>
        <th>0</th>
        <th>0</th>
    </tr>
    <tr>
        <th><span style="color:blue">1</span> <span style="color:yellow">1</span></th>
        <th>0</th>
        <th style="background-color:tomato">1</th>
        <th>0</th>
        <th>0</th>
    </tr>
    
</table>

Temos a resposta <span style="background-color:orange;padding:5px;">**B**.**Cn**</span> + <span style="background-color:tomato;padding:5px;">**An**.**B**.**Dn**</span> + <span style="background-color:#999;padding:5px;">**An**.**Bn**.**C**.**D**</span>

> S = `An`.`Bn`.`C`.`D` + `An`.`B`.`Dn` + `B`.`Cn`

> S = `An`.(`Bn`.`C`.`D` + `B`.`Dn`) + `B`.`Cn`

