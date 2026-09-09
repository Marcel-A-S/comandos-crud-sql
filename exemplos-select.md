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


---



## Combinado condições

Usamos o 'WHERE' e operadores lógicos e relacionais.

### Operador AND (E)

Exibir os produtos que custem menos de 500 e quantidade acima de 20

```sql
SELECT nome, preco, quantidade FROM produtos
WHERE preco < 500 AND quantidade > 20;
```


### Operador OR (OU)

Exibir os produtos que custem mais de 3000 ou com quantidade zerada.

```sql
SELECT nome, preco, quantidade FROM produtos
WHERE preco > 3000 OR quantidade = 0;
```


### Operador NOT (NÃO)

Exibir os produtos que **não possuem preço acima de 1000**.

```sql
SELECT nome, preco, FROM produtos WHERE NOT preco > 1000;
```

**OBS.:** o uso do 'NOT' não é obrigatório, desde que você consiga o mesmo resultado usando uma lógica diferente, como no exemplo:

'SELECT nome, preco FROM Produtos WHERE preco <= 1000;'