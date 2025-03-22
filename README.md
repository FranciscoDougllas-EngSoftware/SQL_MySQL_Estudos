#**100 comandos SQL mais utilizados no MySQL**, organizada do básico ao avançado. 

---

### **1. Comandos Básicos - Gerenciamento de Banco de Dados**
1. `CREATE DATABASE nome_banco;` - Cria um novo banco de dados.
2. `USE nome_banco;` - Seleciona um banco de dados para uso.
3. `DROP DATABASE nome_banco;` - Exclui um banco de dados.
4. `SHOW DATABASES;` - Lista todos os bancos de dados disponíveis.
5. `SHOW TABLES;` - Lista todas as tabelas no banco de dados atual.

---

### **2. Comandos Básicos - Gerenciamento de Tabelas**
6. `CREATE TABLE nome_tabela (coluna1 tipo_dado, coluna2 tipo_dado);` - Cria uma nova tabela.
7. `DROP TABLE nome_tabela;` - Exclui uma tabela.
8. `DESCRIBE nome_tabela;` - Mostra a estrutura de uma tabela (ou `DESC nome_tabela;`).
9. `ALTER TABLE nome_tabela ADD coluna tipo_dado;` - Adiciona uma nova coluna a uma tabela.
10. `ALTER TABLE nome_tabela DROP COLUMN coluna;` - Remove uma coluna de uma tabela.
11. `ALTER TABLE nome_tabela MODIFY coluna novo_tipo_dado;` - Modifica o tipo de dado de uma coluna.
12. `RENAME TABLE nome_antigo TO nome_novo;` - Renomeia uma tabela.

---

### **3. Inserção de Dados**
13. `INSERT INTO nome_tabela (coluna1, coluna2) VALUES (valor1, valor2);` - Insere uma linha na tabela.
14. `INSERT INTO nome_tabela VALUES (valor1, valor2);` - Insere valores em todas as colunas na ordem.
15. `INSERT INTO nome_tabela (coluna1, coluna2) SELECT valor1, valor2 FROM outra_tabela;` - Insere dados de uma consulta.

---

### **4. Consulta de Dados (SELECT Básico)**
16. `SELECT * FROM nome_tabela;` - Seleciona todas as colunas de uma tabela.
17. `SELECT coluna1, coluna2 FROM nome_tabela;` - Seleciona colunas específicas.
18. `SELECT DISTINCT coluna FROM nome_tabela;` - Retorna valores únicos de uma coluna.
19. `SELECT coluna AS alias FROM nome_tabela;` - Define um alias para uma coluna.
20. `SELECT * FROM nome_tabela WHERE condicao;` - Filtra resultados com uma condição.

---

### **5. Condições e Filtros (WHERE)**
21. `SELECT * FROM nome_tabela WHERE coluna = valor;` - Filtra por igualdade.
22. `SELECT * FROM nome_tabela WHERE coluna != valor;` - Filtra por diferença (ou `<>`).
23. `SELECT * FROM nome_tabela WHERE coluna > valor;` - Filtra por maior que.
24. `SELECT * FROM nome_tabela WHERE coluna < valor;` - Filtra por menor que.
25. `SELECT * FROM nome_tabela WHERE coluna BETWEEN valor1 AND valor2;` - Filtra por intervalo.
26. `SELECT * FROM nome_tabela WHERE coluna IN (valor1, valor2);` - Filtra por lista de valores.
27. `SELECT * FROM nome_tabela WHERE coluna LIKE '%valor%';` - Filtra por padrão (ex.: `%` para qualquer sequência).
28. `SELECT * FROM nome_tabela WHERE coluna IS NULL;` - Filtra por valores nulos.
29. `SELECT * FROM nome_tabela WHERE coluna IS NOT NULL;` - Filtra por valores não nulos.

---

### **6. Ordenação e Limitação**
30. `SELECT * FROM nome_tabela ORDER BY coluna ASC;` - Ordena resultados em ordem crescente.
31. `SELECT * FROM nome_tabela ORDER BY coluna DESC;` - Ordena resultados em ordem decrescente.
32. `SELECT * FROM nome_tabela LIMIT 10;` - Limita o número de linhas retornadas.
33. `SELECT * FROM nome_tabela LIMIT 5 OFFSET 10;` - Pula linhas e limita (paginação).

---

### **7. Atualização e Exclusão de Dados**
34. `UPDATE nome_tabela SET coluna = valor WHERE condicao;` - Atualiza dados em uma tabela.
35. `DELETE FROM nome_tabela WHERE condicao;` - Exclui linhas com base em uma condição.
36. `TRUNCATE TABLE nome_tabela;` - Remove todos os dados da tabela, mantendo a estrutura.

---

### **8. Funções de Agregação**
37. `SELECT COUNT(coluna) FROM nome_tabela;` - Conta o número de linhas ou valores não nulos.
38. `SELECT SUM(coluna) FROM nome_tabela;` - Soma os valores de uma coluna.
39. `SELECT AVG(coluna) FROM nome_tabela;` - Calcula a média dos valores.
40. `SELECT MIN(coluna) FROM nome_tabela;` - Retorna o valor mínimo.
41. `SELECT MAX(coluna) FROM nome_tabela;` - Retorna o valor máximo.

---

### **9. Agrupamento (GROUP BY)**
42. `SELECT coluna, COUNT(*) FROM nome_tabela GROUP BY coluna;` - Agrupa resultados por uma coluna.
43. `SELECT coluna, SUM(valor) FROM nome_tabela GROUP BY coluna HAVING SUM(valor) > 100;` - Filtra grupos com HAVING.

---

### **10. Junções (JOIN)**
44. `SELECT * FROM tabela1 INNER JOIN tabela2 ON tabela1.id = tabela2.id;` - Junção interna.
45. `SELECT * FROM tabela1 LEFT JOIN tabela2 ON tabela1.id = tabela2.id;` - Junção à esquerda.
46. `SELECT * FROM tabela1 RIGHT JOIN tabela2 ON tabela1.id = tabela2.id;` - Junção à direita.
47. `SELECT * FROM tabela1 FULL JOIN tabela2 ON tabela1.id = tabela2.id;` - Junção completa (emulação no MySQL com UNION).
48. `SELECT * FROM tabela1 CROSS JOIN tabela2;` - Produto cartesiano entre tabelas.

---

### **11. Subconsultas**
49. `SELECT * FROM nome_tabela WHERE coluna IN (SELECT coluna FROM outra_tabela);` - Subconsulta com IN.
50. `SELECT * FROM nome_tabela WHERE coluna = (SELECT MAX(coluna) FROM outra_tabela);` - Subconsulta com valor único.
51. `SELECT a.coluna FROM nome_tabela a WHERE EXISTS (SELECT 1 FROM outra_tabela b WHERE b.id = a.id);` - Subconsulta com EXISTS.

---

### **12. Índices**
52. `CREATE INDEX nome_indice ON nome_tabela (coluna);` - Cria um índice em uma coluna.
53. `DROP INDEX nome_indice ON nome_tabela;` - Remove um índice.
54. `SHOW INDEX FROM nome_tabela;` - Lista os índices de uma tabela.

---

### **13. Chaves Primárias e Estrangeiras**
55. `CREATE TABLE nome_tabela (id INT PRIMARY KEY, nome VARCHAR(50));` - Define uma chave primária.
56. `ALTER TABLE nome_tabela ADD PRIMARY KEY (coluna);` - Adiciona uma chave primária.
57. `CREATE TABLE nome_tabela (id INT, FOREIGN KEY (id) REFERENCES outra_tabela(id));` - Define uma chave estrangeira.
58. `ALTER TABLE nome_tabela ADD FOREIGN KEY (coluna) REFERENCES outra_tabela(coluna);` - Adiciona uma chave estrangeira.

---

### **14. Transações**
59. `START TRANSACTION;` - Inicia uma transação.
60. `COMMIT;` - Confirma uma transação.
61. `ROLLBACK;` - Reverte uma transação.
62. `SET AUTOCOMMIT = 0;` - Desativa o commit automático.

---

### **15. Funções de String**
63. `SELECT CONCAT(coluna1, ' ', coluna2) FROM nome_tabela;` - Concatena strings.
64. `SELECT UPPER(coluna) FROM nome_tabela;` - Converte para maiúsculas.
65. `SELECT LOWER(coluna) FROM nome_tabela;` - Converte para minúsculas.
66. `SELECT SUBSTRING(coluna, 1, 3) FROM nome_tabela;` - Extrai uma substring.
67. `SELECT LENGTH(coluna) FROM nome_tabela;` - Retorna o comprimento de uma string.

---

### **16. Funções de Data e Hora**
68. `SELECT NOW();` - Retorna a data e hora atuais.
69. `SELECT CURDATE();` - Retorna a data atual.
70. `SELECT CURTIME();` - Retorna a hora atual.
71. `SELECT DATE_FORMAT(coluna, '%Y-%m-%d') FROM nome_tabela;` - Formata uma data.
72. `SELECT DATEDIFF(data1, data2) FROM nome_tabela;` - Calcula a diferença entre datas.

---

### **17. Controle de Acesso**
73. `CREATE USER 'usuario'@'localhost' IDENTIFIED BY 'senha';` - Cria um usuário.
74. `GRANT ALL PRIVILEGES ON nome_banco.* TO 'usuario'@'localhost';` - Concede privilégios.
75. `REVOKE ALL PRIVILEGES ON nome_banco.* FROM 'usuario'@'localhost';` - Revoga privilégios.
76. `DROP USER 'usuario'@'localhost';` - Remove um usuário.
77. `SHOW GRANTS FOR 'usuario'@'localhost';` - Mostra privilégios de um usuário.

---

### **18. Comandos Avançados**
78. `CREATE VIEW nome_view AS SELECT * FROM nome_tabela;` - Cria uma visão.
79. `DROP VIEW nome_view;` - Remove uma visão.
80. `CREATE PROCEDURE nome_procedure() BEGIN ... END;` - Cria um procedimento armazenado.
81. `CALL nome_procedure();` - Executa um procedimento.
82. `CREATE TRIGGER nome_trigger BEFORE INSERT ON nome_tabela FOR EACH ROW SET NEW.coluna = valor;` - Cria um gatilho.
83. `DROP TRIGGER nome_trigger;` - Remove um gatilho.
84. `EXPLAIN SELECT * FROM nome_tabela;` - Analisa a execução de uma consulta.

---

### **19. Manipulação de Dados Avançada**
85. `INSERT IGNORE INTO nome_tabela (coluna) VALUES (valor);` - Ignora erros (ex.: duplicatas).
86. `REPLACE INTO nome_tabela (coluna) VALUES (valor);` - Substitui registros duplicados.
87. `ON DUPLICATE KEY UPDATE coluna = valor;` - Atualiza em caso de duplicata.
88. `SELECT COALESCE(coluna, 'valor_padrao') FROM nome_tabela;` - Retorna o primeiro valor não nulo.

---

### **20. Otimização e Diagnóstico**
89. `OPTIMIZE TABLE nome_tabela;` - Otimiza uma tabela.
90. `ANALYZE TABLE nome_tabela;` - Analisa e atualiza estatísticas da tabela.
91. `SHOW PROCESSLIST;` - Lista processos em execução.
92. `KILL id_processo;` - Encerra um processo.
93. `SHOW VARIABLES LIKE 'variavel%';` - Mostra configurações do servidor.

---

### **21. Outros Comandos Úteis**
94. `LOAD DATA INFILE 'arquivo.txt' INTO TABLE nome_tabela;` - Importa dados de um arquivo.
95. `SELECT * INTO OUTFILE 'arquivo.txt' FROM nome_tabela;` - Exporta dados para um arquivo.
96. `SET @variavel = valor;` - Define uma variável de sessão.
97. `SELECT @variavel;` - Usa uma variável em uma consulta.
98. `WITH cte AS (SELECT * FROM nome_tabela) SELECT * FROM cte;` - Usa uma Common Table Expression (CTE).
99. `SHOW WARNINGS;` - Mostra avisos após uma consulta.
100. `FLUSH TABLES;` - Limpa o cache de tabelas.

---

Essa lista cobre desde os comandos mais básicos, como criar tabelas e inserir dados, até funcionalidades avançadas, como triggers, procedimentos armazenados e otimização.