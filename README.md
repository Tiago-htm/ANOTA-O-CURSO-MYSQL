# RESUMOS DE SEÇÕES CURSO;

**Iniciando resumo do curso MYSQL para iniciantes da UNDEMY feito pelo professor Mathues.**

### Conceitos Banco de dados

   Banco de dados  pode resumir em um guarda roupa, onde o guarda roupa seria o **BANCO** e as gavetas seria as **TABELAS/COLUNAS**. 
Para criar esse guarda roupa precisamos de uma ferramenta que é o SQL e para conseguirmos resgatar ou inserir itens(DADOS) de dentro das gavetas
precisamos de um pegador que é o SGBD. Os principais elementos de um Banco de Dados são: Diagrama do Banco, Banco de dados, Tabelas/Colunas e os Dados. 
   
### COMANDOS SQL;
    
	* CREATE DATABASE <nome do banco>: Cria um novo banco;
	* USE <nome do banco> : Para selecionar o banco;
	* source <arquivo> : Para importar dados de um arquivo;
	* SELECT * FROM <nome da Tabela> : Mostra todos os dados e colunas da tabela;
	* SELECT <column> FROM <table> : Selcionar uma coluna especifica da tabela x;
	* SHOW DATABASES: Exibe todos os bancos dentro SGBD;
	* DROP DATABASES <nome do banco> : Exclui o banco;
	* mysqldump -u root <nome do banco> > <nome_arquivo.sql> : Exportando o banco;
	* CREATE TABLE <nome da Tabela> (<coluna> <tipo de dados> : Criar uma Tabela, obs: para adicionar mais de uma coluna separar por virgula;
	* DROP TABLE <nome da Tabela> : Exclui a Tabela;
	* INSERT INTO <Tabela> (nome da coluna, ...) VALUES ("valores", 21312);
	* ALTER TABLE <tabela> ADD COLUMN <nome> <tipo>: adicionar uma coluna nova na tabela;
	* ALTER TABLE <tabela> MODIFY COLUMN <coluna> <tipo>: Modificar uma coluna;
	* ALTER TABLE <tabela> DROP COLUMN <nome> : Deleta uma coluna;
	* UPDATE <tabela> SET <coluna = valor>;
	* SELECT DISTINCT <coluna> FROM <tabela> : vai voltar apenas valores diferentes da coluna selecionada;
	* ORDER <coluna> BY (DESC OU ASC) : order a qual os itens vão ser exibido, é o ultimo comando a ser exibido;
	* SELECT <coluna> FROM tabela ORDER BY <coluna>  LIMIT (numero) : Para limitar o numero de resultados;
	* SELECT MIN (<coluna>) FROM <tabela> : para exibir o menor valor;
	* SELECT MAX (<coluna>) FROM <tabela> : para exibir o maior valor;
	* SELECT COUNT(*) FROM table : para contar o tanto de valores que existe na coluna;
	* SELECT AVG(coluna) FROM table : para tirar a media de uma coluna;
	* SELECT SUM (coluna) FROM table : para somar os valore de uma coluna;
	* DELETE FROM <tabela> WHERE <condicao> : para deletar os dados;
	* SELECT  *  FROM <tabela> WHERER <coluna> LIKE '%palavra% : para mesclar as palavras pelo nome que ta escrito entre a %.
	* SELECT  *  FROM <tabela> WHERE <coluna> IN ('x', 'y' ,etc ..) : para buscar um conjunto de valores;
	* SELECT * FROM <tabela> WHERE <coluna> 'x' AND 'y' : para pegar conjunto de valores do x ao y;
	* DROP INDEX <nome> ON <tabela> : para remover o index;
	* SELECT <tabela1.coluna>,<tabela2.colunaX>, FROM <tabela> INNER JOIN <tabela> ON tabela.id = tabela2.id2 : para unir as informações de dois banco
	* SELECT <tabela1.coluna>,<tabela2.colunaX>, FROM <tabela> LEFT JOIN <tabela> ON tabela.id = tabela2.id2 : para unir as informações de dois banco, pegando todos os dados da esquerda
	* SELECT <tabela1.coluna>,<tabela2.colunaX>, FROM <tabela> RIGHT JOIN <tabela> ON tabela.id = tabela2.id2 : para unir as informações de dois banco pegando todos os dados 	da direita
	* SELECT <coluna>, COUNT(<coluna>) FROM tabela GROUP BY <coluna> : para agrupar colunas e checar quantidade;
	* SELECT <coluna>, COUNT(<coluna>) FROM tabela WHERE  ID = ANY ( SELECT id FROM TABELA  where salary > 1500000) :  retorna apenas valores que condiz com a condição;
	* SELECT <coluna>, COUNT(<coluna>) FROM tabela WHERE  ID = EXIST ( SELECT id FROM TABELA  where salary > 1500000) :  retorna apenas valores que condiz com a condição;
	
**OBS: PARA UTILIZAR DELETE E UPDATE SEMPRE BOM ULTIZAR O SELECT ANTES PARA CONFIRMAR SE É ISSO MESMO QUE QUER FAZER!**

### UTILIZANDO WHERE: 
		
	O where é fundamental para especificar nossas ações no banco, desse modo evitando fazer algo indesejavel ...
###### Utilizando o WHERE:
		
	*UPDATE tabela SET <coluna = valor,...etc> WHERE <condiçao>;
	*DELETE FROM <tabela> WHERE <condição>;
	*SELECT <coluna>  FROM <tabela>  WHERE <condição>;
**HAVING UTILIZAR QUANDO TIVER DENTRO DE UMA FUNÇÃO**
#### TIPOS DE DADOS:
	
	####### Tipos text
	
	* CHAR(X) : aceita textos/numeros com 0 a 255 caracteres;
	* VARCHAR(X) : aceita textos/numeros com 0 a 65535 caracteres;
		X é a quantidade maxima;
	* TINYTEXT : apenas texto com até 255 caracteres;
	* MEDIUMTEXT : apenas texto com até 16777215 caracteres;
	
	####### Tipos númericos
	
	* BIT(X): 1 A 64 caracteres;
	* TINYINT(x) : 1 a 255 caracteres;
	* BOOL : 0 é falso e 0 > true 0 < true;
	* INT(x) : valores entre -2147483648 a 2147483648;
	
	####### Tipos data
	
	* DATE : YYYY-MM-DD;
	* DATETIME: YYYY-MM-DD;
	* TIMESTAMP : Aceita uma dato no formato de DATETIME, porém apenas entre os anos 1970 a 2038;
		inserir datas entre aspas;

	###### CONSTRAINTS :
	
	* NOT NULL : não deixa a coluna ser nula;
	* UNIQUE : não deixa dados reptidos;
	* PRIMARY KEY : geralmente é o ID;
	* AUTO INCREMENT : para auto incrementar ideal para id
	* FOREIGN KEY : para fazer ligação com outra tabela
	* INDEX : faz a busca ser mais rapida
	
	
##CONCLUSÃO:
	Este arquivo foi feio para futuras consultas e também para ajudar a memorização;
