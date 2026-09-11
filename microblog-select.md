### Utilizando comandos SQL SELECT no  Microblog

##  1 SELECT 
1. Consulte todos os dados de todos os `usuários` cadastrados.
```sql

SELECT * FROM usuarios;
```
2. Consulte apenas algumas informações dos usuários, como `nome `e `e-mail`

```sql
SELECT nome, email FROM usuario;    
```

3. Consulte os dados das `categorias` cadastradas

```sql
SELECT * FROM categoria;    
```

4. Consulte apenas algumas informações das notícias, como `título` e `data de publicação`.

```sql
SELECT data_publicacao FROM noticias;    
```

5. Faça uma consulta utilizando `AS` para alterar o nome de pelo menos duas colunas no resultado

```sql
SELECT 
    titulo AS "titulo da noticia",
    data_publicacao AS "data de publicaao"
FROM noticia;
```

## 2 Utilizando o comando WHERE 

6. Consulte somente os usuários `de um determinado tipo`, de acordo com os dados existentes no seu banco

```sql
SELECT * FROM usuario WHERE tipo_usuario = 'admin';
```

7. Consulte somente as notícias que estejam marcadas como `destaque` (ou alguma informação equivalente existente no seu modelo).`

```sql
SELECT * FROM noticia WHERE destaque = 1;
```

8. Escolha uma `categoria` existente no seu banco e consulte as `notícias` pertencentes a ela utilizando seu identificador.

```sql
SELECT * FROM noticia WHERE id_categoria = 1;
```

9. Faça uma consulta utilizando o operador `<>` para excluir do resultado algum tipo de usuário, categoria ou outro valor existente no seu banco.

```sql
SELECT * FROM usuarios WHERE tipo_usuario <> 'admin';
``` 

 ## 3 Combinando condições

 10. Faça uma consulta utilizando `AND` para estabelecer duas condições simultaneamente.

```sql
SELECT * FROM noticias WHERE id_categoria = 2 AND destaque = 1;
```

11. Faça outra consulta utilizando `OR`, na qual um registro possa aparecer se atender a uma condição ou outra.

```sql
SELECT * FROM noticia WHERE id_categoria = 2 OR destaque = 1;
```

## 4 Pesquisas com LIKE

12. Escolha uma palavra ou parte de uma palavra existente nos dados do seu banco e utilize `LIKE` para procurar registros que a contenham.

```sql
SELECT * FROM noticias WHERE titulo LIKE '%tecnologia%';
```
