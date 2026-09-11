### Utilizando comandos SQL SELECT no  Microblog

##  1 SELECT 
1. Consulte todos os dados de todos os `usuários` cadastrados.
```sql

SELECT * FROM usuario;
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
    data_publicacao AS "publicacao no dia"
FROM noticia;
```

## 2 Utilizando o comando WHERE 

6. Consulte somente os usuários `de um determinado tipo`, de acordo com os dados existentes no seu banco

```sql
SELECT * FROM usuario WHERE tipo_usuario = 'admin';
```

7. Consulte somente as notícias que estejam marcadas como `destaque` (ou alguma informação equivalente existente no seu modelo).`

```sql
SELECT * FROM noticia WHERE destaque = `sim`;
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
SELECT * FROM noticia WHERE 
titulo LIKE '%tecnologia%' OR
resumo LIKE '%tecnologia%' OR
destaque LIKE  '%tecnologia%' OR
nome_imagem LIKE '%tecnologia%';
```

13. Faça uma consulta utilizando `LIKE` para encontrar registros cujo texto comece com determinada letra ou palavra.

```sql
SELECT * FROM noticias WHERE titulo LIKE 'A%';
```

## 5 Ordenação

14. Consulte as notícias organizando o resultado da `mais recente para a mais antiga.`

```sql
SELECT * FROM noticia ORDER BY data_publicacao DESC;
```


15. Escolha uma tabela e faça uma consulta ordenando seus registros em `em ordem alfabetica`

```sql
SELECT * FROM usuario ORDER BY nome ASC;
```

## 6 Funções de agregação

16. Utilize `COUNT()` para descobrir quantos usuários existem cadastrados.

```sql
SELECT COUNT(*) AS total_usuario FROM usuario;
```

17. Utilize `COUNT()` para descobrir quantas notícias existem cadastradas.

```sql
SELECT COUNT(*) AS total_noticia FROM noticia;
```

18. Utilize `MIN() e MAX()` sobre a data das notícias para descobrir a data da notícia mais antiga e da mais recente.`

```sql
SELECT 
    MIN(data_publicacao) AS noticia_mais_antiga,
    MAX(data_publicacao) AS noticia_mais_recente
FROM noticia;
```

## 7 Desafio

19. Crie uma consulta por conta própria combinando pelo menos três recursos estudados nesta aula.

```sql
SELECT titulo AS "titulo da noticia",
       data_publicacao AS "data de publicação"
FROM noticia
WHERE titulo LIKE 'Brasil%'
ORDER BY data_publicacao DESC;
```
