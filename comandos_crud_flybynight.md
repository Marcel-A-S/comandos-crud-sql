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
   


```
