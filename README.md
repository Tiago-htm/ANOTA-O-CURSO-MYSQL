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
	*

	

    
