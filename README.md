![208833-dbaas-banco-de-dados-hibridos-por-que-ter-na-minha-empresa](https://github.com/Ilan-dev0/projeto-bdbanco/assets/79155978/f9107483-a529-4efd-b5b6-d926a4dfad85)

# Banco de dados Estruturado no Excel
Um projeto de banco de dados para uma universidade fictícia, feito no SENAI.



## Tabela Cliente (Não aplicadas as normalizações)

| COD | NOME DO CLIENTE       | CPF | TELEFONES2 | CIDADE     | UF | BANCO                   | AGENCIA         | CONTA    | SALDO |
|-----|-----------------------|-----|------------|------------|----|-------------------------|-----------------|----------|-------|
| 1   | JOSE DA SILVA         | 111 | 89387483   | BELO HTE   | MG | 001 - Banco do Brasil  | 0219 - Praça    | 9384-1   | 10,00 |
|     |                       |     | 89748950   |            |    | 033 - Santander         | 0343 - Shopping | 9873-7   | 40,00 |
|     |                       |     |            |            |    | 104 - Caixa             | 0034 - Matriz   | 0349-8   | 100,00|
| 2   | JOAO GAVIAO           | 222 | 89865869   | CONTAGEM   | MG | 001 - Banco do Brasil  | 0219 - Praça    | 9344-2   | 32,00 |
| 3   | MARIA DAS TRANCAS     | 343 | 89487494   | BELO HTE   | MG | 001 - Banco do Brasil  | 0001 - Matriz  | 9098-0   | 13,00 |
|     |                       |     |            |            |    | 104 - Caixa             | 0394 - Engenho | 0837-5   | 34,00 |
| 4   | PEDRO LUIZ            | 948 | 99809495   | SÃO PAULO  | SP | 104 - Caixa             | 0394 - Engenho | 9489-8   | 99,00 |

### Tabela Clientes

| COD | NOME DO CLIENTE    | CPF |
|-----|--------------------|-----|
| 1   | JOSE DA SILVA      | 111 |
| 2   | JOAO GAVIÃO        | 222 |
| 3   | MARIA DAS TRANCAS  | 343 |
| 4   | PEDRO LUIZ         | 948 |

### Tabela Telefone 

| COD | COD_CLIENTE | TELEFONE  |
|-----|------------|-----------|
| 1   | 1          | 89387483  |
| 2   | 1          | 89748950  |
| 3   | 2          | 89865869  |
| 4   | 3          | 89487494  |
| 5   | 4          | 99809495  |
| 6   | 4          | 99849593  |

### Tabela Cidade

| COD | CIDADE     | COD_UF |
|-----|------------|--------|
| 1   | BELO HTE   | 2      |
| 2   | CONTAGEM   | 2      |
| 3   | SÃO PAULO  | 1      |

### Tabela UF

| Nome         | COD |
|--------------|-----|
| SÃO PAULO    | 1   |
| MINAS GERAIS | 2   |

### Tabela Banco

| COD | BANCO                 |
|-----|-----------------------|
| 001 | Banco do Brasil      |
| 033 | Santander            |
| 104 | Caixa                |

### Tabela Agência

| COD_AGENCIA | AGENCIA           |
|------------|-------------------|
| 219        | Praça             |
| 343        | Shopping          |
| 394        | Engenho           |
| 1          | Matriz            |

### Tabela Agencia_Banco

| COD_AGENCIA | COD_AGENCIA_NOME | COD_BANCO |
|------------|-------------------|-----------|
| 219        | 1               | 1         |
| 343        | 2               | 33        |
| 34         | 3               | 104       |
| 1          | 3               | 1         |
| 394        | 4               | 104       |

### Tabela Agencia_Nome

| COD_AGENCIA | COD_AGENCIA_NOME | COD_BANCO |
|------------|-------------------|-----------|
| 219        | 1               | 1         |
| 343        | 2               | 33        |
| 34         | 3               | 104       |
| 1          | 3               | 1         |
| 394        | 4               | 104       |

### Tabela Cliente_Banco

| COD_CLI | COD_AGENCIA | CONTA    | SALDO |
|---------|-------------|----------|-------|
| 1       | 219         | 9384-1   | 10    |
| 1       | 343         | 9873-7   | 40    |
| 1       | 343         | 0349-8   | 100   |
| 2       | 219         | 9344-2   | 32    |
| 3       | 1           | 9098-0   | 13    |
| 3       | 394         | 0837-5   | 34    |
| 4       | 394         | 9489-8   | 99    |


