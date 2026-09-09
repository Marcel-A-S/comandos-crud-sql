# Comando CRUD para o banco de dados Fly By Night

##  Insert na tabela fornecedores

```sql
-- INSERT de defornecedores
INSERT INTO fornecedores (nome) VALUES('Eletrônicos Tabajara');
INSERT INTO fornecedores (nome) VALUES
('Games ABCD'),
('Supermercado Tem de Tudo'),
('Livraria Demais da Conta');

```


##  Insert na tabela Produtos

```sql
   INSERT INTO produtos(nome,descricao,preco,quantidade,fornecedor_id)
   VALUES('Smartphone Galaxy s23',
   'Equipamento com sistema Androind e câmera Full HD e etc etal',
   1599.45,20,1 -- id do fornecedor Eletrônico Tabajara
   );
   
INSERT INTO produtos(nome,descricao,preco,quantidade,fornecedor_id)
   VALUES
   ('Senhor dos Aneis: As duas Torres',
   'Volume 2 de série de livros criados pelo autor J.R.R. Tolkien',
   80.99,100,4 --id do fornecedor Livraria
   
   );
   

INSERT INTO produtos(nome,descricao,preco,quantidade,fornecedor_id)
   VALUES
   ('Tv Led',
   'Tela de 50 polegadas 4K, 4 entradas HDMI e etc e tal',
    3420,12,1 --id fornecedor Eletrônico Tabajara
   );

```

##  Insert na tabela lojas

```sql
INSERT INTO lojas(nome) VALUES('Casas Bahia');
INSERT INTO lojas(nome) VALUES('Shopping Zona Leste');
INSERT INTO lojas(nome) VALUES('Bazar das Coisas');
INSERT INTO lojas(nome) VALUES('Americanas');

```


##  Insert na tabela lojas-produtos

Esta e um tabela intermediária ( também conhecida como **tabela pivot**),
ou seja ela se relaciona com outras duas tabelas: **produto**
através de chaves estrangeiras.

```sql
   INSERT INTO lojas_produtos(loja_id, produto_id, estoque) VALUES 
   (2, 1, 20);

   INSERT INTO lojas_produtos(loja_id, produto_id, estoque) VALUES
   (4, 2, 3);

   INSERT INTO lojas_produtos(loja_id, produto_id, estoque) VALUES
   (2, 3, 5);

   INSERT INFO lojas_produtos(lojas_id, produto_id, estoque)VALUES
   (1, 1,2);
```

---

## UPDATA na tabela fornecedores

```sql
   UPDATE fornecedores SET nome= 'Mundo dos Games'
   WHERE id = 2; 
```

## UPDATA na tabela produto
```sql
        UPDATE produto SET preco = ,2999, quantidade = 5 WHERE id = 3
```



## UPDATA na tabela lojas_produto

```sql
   UPDATE lojas_produtos SET estoque = 4 WHERE lojas_id = 2 AND produtos_id = 1;
```

-- SQL aceita operadores lógicos: AND (E), OR (OU), NOT (NÃO)


## DELETE na tabela fornecedores

```sql
DELETE FROM fornecedores WHERE id = 5;

```


