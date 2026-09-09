## insert tabela usuaria



## UPDATA na tabela usuario
```sql
   UPDATE usuario SET nome= 'Alessandra'
   WHERE id = 1; 
```


## UPDATE na tabela usuário de editor para admin.
```sql
   UPDATE usuario SET nome= 'admin'
   WHERE id = 2; 
```



```sql
INSERT INTO usuario (nome, email, senha, tipo_usuario ) VALUES
('alessandra', 'alessandra@email.com', '123abc', 'editor');

INSERT INTO usuario (nome, email, senha, tipo_usuario) VALUES('Bruno Souza', 'bruno@email.com', 'abc456', 'admin');

INSERT INTO usuario (nome, email, senha, tipo_usuario) VALUES('Carla Mendes', 'carla@email.com', '789xyz', 'editor');

```



## UPDATE na tabela categoria
```sql
   UPDATE categoria SET nome= 'artigos esportivos'
   WHERE id = 3; 
```



## insert tabela categoria
```sql
INSERT INTO categoria (nome) VALUES ('tecnologia');
INSERT INTO categoria (nome) VALUES ('educacao');
INSERT INTO categoria (nome) VALUES ('entretenimento');
```


## insert tabela noticia

## UPDATE na tabela noticia
```sql
   UPDATE noticia SET titulo = 'sexta-feira 13'
   WHERE id = 1; 
```
## UPDATE na tabela noticia
```sql
   UPDATE noticia SET destaque = 'nao'
   WHERE id = 2; 
```

## DELETE para excluir uma das noticias

```sql
DELETE FROM noticia WHERE id = 3;

```

## DELETE para excluir categoria não utilizada

```sql
DELETE FROM categoria WHERE id = 1;

```

## DELETE para excluindo um usuario 

```sql
DELETE FROM usuario WHERE id = 3;

```


```sql
INSERT INTO noticia (titulo, resumo, texto_completo, nome_imagem, destaque, id_usuario, id_categoria) VALUES (
    'IA ganha espaço entre estudantes brasileiros',
    'Brasil deve receber uma cúpula internacional sobre IA, O Brasil foi anunciado como país anfitrião da próxima edição de um congresso internacional dedicado à IA e ao sentido humano da tecnologia.',
    'A Inteligência Artificial (IA) está se tornando cada vez mais presente na vida das pessoas, nas escolas e nas empresas. A tecnologia já é utilizada para estudar, produzir textos, analisar informações, automatizar tarefas e auxiliar profissionais em diversas áreas.',
    'imagem03.png', 
    'sim', 
    1,
    2
);
```

```sql
INSERT INTO noticia (titulo, resumo, texto_completo, nome_imagem, destaque, id_usuario, id_categoria) VALUES (
    'Flamengo assume a liderança do Campeonato Brasileiro',
    'Rubro-Negro vence o Remo e aproveita empate do Palmeiras com o Botafogo para chegar ao primeiro lugar',
    'O Campeonato Brasileiro de 2026 ganhou um novo líder após a 26ª rodada. O Flamengo venceu o Remo por 1 a 0, no domingo (6), em Belém, e chegou aos 54 pontos. O resultado foi ainda mais importante porque o Palmeiras empatou em 0 a 0 com o Botafogo e perdeu a liderança da competição.',
    'imagem01.png',
    'sim',
    1,
    3
);
```


```sql
INSERT INTO noticia (titulo, resumo, texto_completo, nome_imagem, destaque, id_usuario, id_categoria) VALUES (
    'Pisa 2025 mostra desafios e avanços na educação brasileira',
    'Uso de tecnologia cresce entre estudantes, mas desempenho escolar continua sendo um desafio.',
    'Os resultados do Pisa 2025, avaliação internacional organizada pela Organização para a Cooperação e Desenvolvimento Econômico (OCDE), mostram que a educação brasileira continua enfrentando desafios importantes. A avaliação analisa o desempenho de estudantes de aproximadamente 15 anos nas áreas de matemática, leitura e ciências.',
    'imagem04.png',
    'sim',
    3,
    2

);
```