# SQL SELECT - Exemplos de consultas ao banco FLY BY Night

O comando 'SELECT' é para **consultar dados armazenados nas tabelas do
banco de dados**

## SELECT básico

Consultar todos os dados de uma tabela:

```sql
SELECT * FROM produtos;
```
## SELECT para apenas determinadas colunas

```sql
SELECT nome, preco FROM produto;    

```

## Alterando o nome de exibição das colunas

Usamos o comando 'AS' paracriar um **apelido (alias)**

```sql
SELECT
nome AS produto,
preco AS "Preço em R$"
FROM produtos;
```

## Filtrar registros com WHERE

O 'WHERE' permite determinar **quais registros devem aparecer** no resultado. Na prática, são condições para execução do 'SELECT'.

### Comparação de igualdade

```sql
SELECT * FROM produtos WHERE quantidade = 0;
```

### Comparação de maior/menor

```sql
SELECT nome, preco FROM produtos WHERE preco > 1000;
```

### Comparação de menor igual

```sql
SELECT nome, preco FROM produtos WHERE preco <= 100;
```

### Comparação de diferença

Normalmente se usa o operador '<>' em vez de '!'.
** esteristicos representa todas as colunas**

```sql
SELECT * FROM produtos WHERE fornecedor_id <> 1;

```