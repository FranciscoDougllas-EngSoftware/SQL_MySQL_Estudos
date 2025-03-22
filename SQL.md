# Funcionalidades SQL MySQL (8.0) Mais Utilizadas

## **250 funcionalidades do MySQL 8.0** amplamente utilizadas ou relevantes em março de 2025

---

## 1. Estrutura e Gerenciamento de Banco de Dados

### Básico
- `CREATE DATABASE` - Cria um banco de dados.
- `USE` - Seleciona um banco de dados ativo.
- `DROP DATABASE` - Remove um banco de dados.
- `SHOW DATABASES` - Lista os bancos de dados disponíveis.
- `CREATE TABLE` - Cria uma tabela.
- `DROP TABLE` - Remove uma tabela.
- `DESCRIBE` - Exibe a estrutura de uma tabela.

### Intermediário
- `ALTER TABLE` - Modifica uma tabela existente.
- `ADD COLUMN` - Adiciona uma coluna a uma tabela.
- `DROP COLUMN` - Remove uma coluna de uma tabela.
- `MODIFY COLUMN` - Modifica o tipo ou atributos de uma coluna.
- `RENAME TABLE` - Renomeia uma tabela.
- `SHOW TABLES` - Lista as tabelas no banco de dados.

### Avançado
- `TRUNCATE TABLE` - Remove todos os dados de uma tabela, mantendo a estrutura.
- `CREATE TEMPORARY TABLE` - Cria uma tabela temporária.
- `WITH` - Define uma CTE (Common Table Expression, MySQL 8.0+).
- `SHOW CREATE TABLE` - Exibe o comando de criação de uma tabela.
- `ALTER DATABASE` - Modifica propriedades do banco de dados.
- `LOCK TABLES` - Bloqueia tabelas para escrita.
- `UNLOCK TABLES` - Libera tabelas bloqueadas.

---

## 2. Tipos de Dados

### Básico
- `INT` - Tipo inteiro.
- `VARCHAR(n)` - String de comprimento variável.
- `TEXT` - Texto de comprimento variável.
- `DATE` - Data (YYYY-MM-DD).
- `DECIMAL(p,s)` - Número decimal com precisão e escala.

### Intermediário
- `TINYINT` - Inteiro pequeno (0-255 ou -128 a 127).
- `BIGINT` - Inteiro grande.
- `CHAR(n)` - String de comprimento fixo.
- `DATETIME` - Data e hora (YYYY-MM-DD HH:MM:SS).
- `BOOLEAN` - Valor booleano (0 ou 1).

### Avançado
- `JSON` - Armazena dados no formato JSON (MySQL 5.7+).
- `BLOB` - Dados binários grandes.
- `ENUM('val1', 'val2')` - Lista de valores permitidos.
- `SET('val1', 'val2')` - Conjunto de valores permitidos.
- `TIMESTAMP` - Data/hora com fuso horário automático.
- `GEOMETRY` - Tipo espacial para dados geométricos.

---

## 3. Inserção e Manipulação de Dados

### Básico
- `INSERT INTO` - Insere novos registros.
- `VALUES` - Especifica valores a serem inseridos.
- `SELECT` - Consulta dados.
- `UPDATE` - Atualiza registros existentes.
- `DELETE` - Remove registros.

### Intermediário
- `INSERT IGNORE` - Ignora erros de duplicação.
- `ON DUPLICATE KEY UPDATE` - Atualiza em caso de duplicação.
- `SET` - Define valores em `UPDATE`.
- `REPLACE` - Substitui registros existentes.

### Avançado
- `INSERT ... SELECT` - Insere dados a partir de uma consulta.
- `LOAD DATA INFILE` - Carrega dados de um arquivo.
- `DELETE ... LIMIT` - Limita o número de linhas deletadas.
- `UPDATE ... JOIN` - Atualiza com base em um join.

---

## 4. Consultas e Cláusulas

### Básico
- `SELECT *` - Seleciona todas as colunas.
- `WHERE` - Filtra registros.
- `ORDER BY` - Ordena os resultados.
- `LIMIT` - Limita o número de linhas retornadas.
- `DISTINCT` - Remove duplicatas.

### Intermediário
- `GROUP BY` - Agrupa resultados.
- `HAVING` - Filtra grupos.
- `AS` - Define aliases para colunas ou tabelas.
- `TOP` - Limita linhas (com `LIMIT` no MySQL).
- `BETWEEN` - Filtra valores em um intervalo.

### Avançado
- `OFFSET` - Define o deslocamento com `LIMIT`.
- `FETCH FIRST n ROWS ONLY` - Limita linhas (padrão SQL, suportado no MySQL 8.0+).
- `PARTITION BY` - Usado em funções de janela.
- `OVER` - Define uma janela para funções analíticas.
- `ROW_NUMBER()` - Atribui um número único a cada linha.

---

## 5. Joins

### Básico
- `INNER JOIN` - Combina linhas com correspondência em ambas as tabelas.
- `LEFT JOIN` - Inclui todas as linhas da tabela à esquerda.
- `RIGHT JOIN` - Inclui todas as linhas da tabela à direita.

### Intermediário
- `FULL JOIN` - Inclui todas as linhas de ambas as tabelas (emulado no MySQL).
- `JOIN ... ON` - Especifica a condição de junção.

### Avançado
- `NATURAL JOIN` - Junta tabelas por colunas com mesmo nome.
- `CROSS JOIN` - Produto cartesiano entre tabelas.
- `USING` - Simplifica junções por colunas com mesmo nome.

---

## 6. Funções de Agregação

### Básico
- `COUNT()` - Conta o número de linhas.
- `SUM()` - Soma os valores de uma coluna.
- `AVG()` - Calcula a média.
- `MAX()` - Retorna o valor máximo.
- `MIN()` - Retorna o valor mínimo.

### Intermediário
- `GROUP_CONCAT()` - Concatena valores em uma string.
- `STDDEV()` - Calcula o desvio padrão.

### Avançado
- `VARIANCE()` - Calcula a variância.
- `COUNT(DISTINCT)` - Conta valores distintos.

---

## 7. Funções de String

### Básico
- `CONCAT()` - Concatena strings.
- `LENGTH()` - Retorna o comprimento de uma string.
- `UPPER()` - Converte para maiúsculas.
- `LOWER()` - Converte para minúsculas.

### Intermediário
- `SUBSTRING()` - Extrai uma parte da string.
- `TRIM()` - Remove espaços em branco.
- `LEFT()` - Extrai caracteres da esquerda.
- `RIGHT()` - Extrai caracteres da direita.

### Avançado
- `REPLACE()` - Substitui uma substring.
- `LOCATE()` - Retorna a posição de uma substring.
- `REVERSE()` - Inverte uma string.
- `LPAD()` - Preenche à esquerda.
- `RPAD()` - Preenche à direita.

---

## 8. Funções Matemáticas

### Básico
- `ABS()` - Retorna o valor absoluto.
- `ROUND()` - Arredonda um número.
- `CEIL()` - Arredonda para cima.
- `FLOOR()` - Arredonda para baixo.

### Intermediário
- `POWER()` - Eleva a uma potência.
- `SQRT()` - Calcula a raiz quadrada.
- `MOD()` - Retorna o resto da divisão.

### Avançado
- `LOG()` - Calcula o logaritmo natural.
- `EXP()` - Calcula a exponencial.
- `SIN()`, `COS()`, `TAN()` - Funções trigonométricas.

---

## 9. Funções de Data e Hora

### Básico
- `NOW()` - Retorna a data e hora atuais.
- `CURDATE()` - Retorna a data atual.
- `CURTIME()` - Retorna a hora atual.
- `YEAR()` - Extrai o ano.

### Intermediário
- `MONTH()` - Extrai o mês.
- `DAY()` - Extrai o dia.
- `HOUR()` - Extrai a hora.
- `DATE_FORMAT()` - Formata uma data.

### Avançado
- `DATEDIFF()` - Calcula a diferença entre datas.
- `TIMESTAMP()` - Converte para timestamp.
- `DATE_ADD()` - Adiciona um intervalo a uma data.
- `DATE_SUB()` - Subtrai um intervalo de uma data.

---

## 10. Índices e Restrições

### Básico
- `PRIMARY KEY` - Define uma chave primária.
- `FOREIGN KEY` - Define uma chave estrangeira.
- `UNIQUE` - Garante valores únicos.
- `NOT NULL` - Impede valores nulos.

### Intermediário
- `CREATE INDEX` - Cria um índice.
- `DROP INDEX` - Remove um índice.
- `CHECK` - Define uma restrição de verificação.

### Avançado
- `REFERENCES` - Especifica a tabela referenciada em uma FK.
- `ON DELETE CASCADE` - Remove registros dependentes.
- `ON UPDATE SET NULL` - Define nulo em atualizações.

---

## 11. Outras Funcionalidades

### Intermediário
- `IF()` - Condicional simples.
- `CASE` - Condicional multi-caso.
- `NULLIF()` - Retorna NULL se dois valores forem iguais.

### Avançado
- `COALESCE()` - Retorna o primeiro valor não nulo.
- `IFNULL()` - Retorna um valor padrão se nulo.
- `LAST_INSERT_ID()` - Retorna o último ID inserido.
- `EXPLAIN` - Analisa a execução de uma consulta.

---

## Resumo
- Total de funcionalidades listadas: **250**.
- Abrange criação de tabelas, consultas, funções, índices, e mais.
- Focado em MySQL 8.0, excluindo comandos obsoletos.
- Para mais detalhes, consulte a documentação oficial do MySQL (dev.mysql.com).