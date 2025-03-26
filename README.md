# TESTE_GERENTE
teste cgdf
1.	Configurar o Ambiente de ETL
1.1.	Instalar o Microsoft SQL Server Developer 2017, 2022 ou similar com SSIS (Windows) 
1.2.	Instalar o Microsoft SQL Server Management Studio
1.3.	Instalar o Microsoft Visual Studio 2022 ou similar com extensão/plugin para desenvolvimento de projetos do SSIS (ambiente de Business Intelligence)
2.	Configuração do Banco de Dados (T-SQL)
2.1.	Criar dois bancos de dados com os seguintes nomes: bdDev e bdHom;
2.2.	Criar dois usuários no banco de dados bdDev (usrDevLeitura com permissão de datareader e usrDevAdmin com permissão de ddladmin e datawriter);
2.3.	Criar dois usuários no banco de dados bdHom (usrHomLeitura com permissão de datareader e usrHomAdmin com permissão de ddladmin e datawriter);
2.4.	Criar um schema chamado stg nos bancos bdDev e bdHom;
2.5.	Criar uma tabela no schema stg, dos dois bancos de dados, chamada TB_REMUNERACAO com as colunas tipificadas de acordo com os dados de cada coluna do arquivo “REMUNERACAO.csv”, em anexo, e carrega-lo utilizando o SSIS;
3.	Modelagem Dimensional
3.1.	Criar a modelagem dimensional para suportar os dados do arquivo disponibilizado;
3.2.	Entre as dimensões criadas deve haver pelo menos uma Dimensão de Alteração Lenta (Slowly Changing Dimension - SCD) do tipo 1 e uma com SCD tipo 2;
3.3.	A carga da tabela-fato deve ser incremental, ou seja, a cada execução do processo apenas os registros não carregados devem ser processados;
3.4.	Todas as tabelas tabelas-fato criadas devem conter a coluna DT_CARGA que deve ser preenchida com a data atual (GETDATE);
4.	Processo de Carga (SSIS)
4.1.	Para cada tabela deve-se criar um pacote de carga com o nome PKG_[NOME_DA_TABELA];
4.2.	A conexão com o banco de dados deve ser feita por uma conexão de Projeto;
4.3.	A conexão com o arquivo deve ser feita como conexão de Pacote e presente apenas no pacote que processará o arquivo e carregará a tabela TB_REMUNERACAO;
4.4.	Todas as colunas de texto devem ter os espaços removidos do início e fim da string e devem estar em caixa alta (upper case);
5.	Relatórios (SQLs): https://colab.research.google.com/drive/1gYPBO5hu9HSiSygCqgEK2zdf0-yTG_Nn?usp=sharing
5.1.	Qual o número total de servidores por empresa?
5.2.	Qual o maior salário dentre os servidores da SERVICO DE LIMPEZA URBANA - SLU?
5.3.	Qual o número de servidores admitidos no ano de 2019?
5.4.	Quantos servidores trabalham 40 horas por semana?
5.5.	Qual o número de servidores ativos no mês de março de 2019?
5.6.	Qual a média de salários dos servidores da SECRETARIA DE ESTADO DE JUSTICA E CIDADANIA?
5.7.	Quais são os 10 servidores que possuem o maior salário dentre os servidores ativos e com função?
