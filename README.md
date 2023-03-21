# SQL_Aniversarios
Este projeto foi desenvolvido em conjunto com os estudos sobre MySQL, aplicando os conceitos inicais aprendidos por mim sobre essa linguagem. Os seguintes conceitos foram aplicados:

- Chave estrangeira e primaria;
- Modelagem seguindo a forma normal;
- Uso de procedures;
- Uso de view;
- Uso de funções do proprio MySQL para formatar a exibição dos dados.

Para fazer o uso desse script é muito simples:
1. Copiar o código ate a linha 301 do **script.sql**;
2. Executar esse trecho copiado no MySQL Workbench;
3. Logo depois cadastre quantas pessoas quiser da seguinte maneira:
	  - Execute a seguinte procedurre **CALL CAD_PESSOA('FULANO', 'DE TAL', 5, 9, 1966);**, onde o primeiro campo é o nome, o segundo o sobrenome, o terceiro é dia de nascimento, o quarto é mes do nascimento e o quinto é o ano do nascimento
4. Depois de cadastrar as pessoas. Conforme a busca que deseja fazer, você pode escolher uma das seguintes procedures:

| O que faz | Como Usar |
|--|--|
|TRAZ OS ANIVERSÁRIANTES DO DIA ESCOLHIDO | CALL RELATORIO_DIA(23); |
|TRAZ OS ANIVERSÁRIANTES DO MÊS ESCOLHIDO| CALL RELATORIO_MES(9);|
|TRAZ AS PESSOAS QUE NASCERAM NO ANO ESCOLHIDO| CALL RELATORIO_ANO(1966);|
|TRAZ AS PESSOAS QUE NASCERAM NO DIA E MÊS ESCOLHIDOS| CALL RELATORIO_DIA_MES(5, 9);|
|TRAZ AS PESSOAS QUE NASCERAM NO DIA E ANO ESCOLHIDOS |CALL RELATORIO_DIA_ANO(5, 1966);|
|TRAZ AS PESSOAS QUE NASCERAM NO MES E ANO ESCOLHIDOS|CALL RELATORIO_MES_ANO(5, 1966);|
|TRAZ AS PESSOAS QUE NASCERAM NA DATA ESCOLHIDA|CALL RELATORIO_DATA(5, 9, 1966);|
|REMOVE UMA PESSOA E O SEU ANIVERSÁRIO COM BASE NO ID DA PESSOA |CALL REMOVE_PESSOA(1);|
|BUSCA POR PESSOAS QUE TENHA ESSE NOME OU ESSE TRECHO DE NOME|CALL BUSCA_PESSOA('MARCELO');|

5. Também temos a opção de relatórios, com os seguintes tipos:

| Relatório | Como Usar |
|--|--|
| RELATÓRIO COM TODOS OS CAMPOS, NA ORDEM QUE FORAM CADASTRADOS  | CALL RELATORIO_GERAL(1);  |
| RELATÓRIO COM TODOS OS CAMPOS, ORDENADO POR DIA DE NASCIMENTO  | CALL RELATORIO_GERAL(2);  |
| RELATÓRIO COM TODOS OS CAMPOS, ORDENADO POR MÊS DE NASCIMENTO  | CALL RELATORIO_GERAL(3);  |
| RELATÓRIO COM TODOS OS CAMPOS, ORDENADO POR ANO DE NASCIMENTO  | CALL RELATORIO_GERAL(4);  |
| RELATÓRIO COM TODOS OS CAMPOS, ORDENADO POR ANO, MÊS E DIA DE NASCIMENTO  | CALL RELATORIO_GERAL(5);  |
| RELATÓRIO COM TODOS OS CAMPOS, ORDENAOD POR NOME  | CALL RELATORIO_GERAL(6);  |
| RELATÓRIO COM TODOS OS CAMPOS, ORDENADO POR SOBRENOME  | CALL RELATORIO_GERAL(7);  |
| TODOS OS CAMPOS(MENOS OS DE ID), ORDENADOS POR NOME E SOBRENOME  | CALL RELATORIO_GERAL(8);  |
| TODOS OS CAMPOS (MENOS OS DE ID), ORDENADOS POR IDADE  | CALL RELATORIO_GERAL(9);  |
| TODOS OS CAMPOS (MENOS OS DE ID), ORDENADOS POR IDADE (DECRESCENTE)  | CALL RELATORIO_GERAL(10);  |
| MENOR IDADE, MAIOR IDADE E MÉDIA DE IDADE DAS PESSOAS DA TABELA  | CALL RELATORIO_GERAL(11);  |

Espero que goste e estou sempre a disposição para receber sugestões de melhoria para esse projeto :)
