Sobre o banco de dados "classicmodels", indique as queries para obter as seguintes informações:

- Quantos registros há na tabela "customers"?
select count(*) from customer

- Na tabela "customers", quantos clientes ("customerName") têm nome iniciado pela letra "M"?
select count(*) from customers where customerName LIKE 'M%'

- Na tabela "customers", crie uma saída que concatene nomes e sobrenomes em uma única coluna.
SELECT CONCAT (contactfirstname, contactlastname) AS concatenado FROM customers

- Agora repita a query acima, mas com todas as letras em maiúsculo, e ordene pelo sobrenome.
SELECT UPPER(CONCAT (contactfirstname, contactlastname)) AS concatenado FROM customers ORDER BY contactlastname

- Na tabela "payments", selecione os registros ordenados por volume ("amount") e data de pagamento ("paymentDate")
SELECT * from payments ORDER BY amount, paymentDate

- Na tabela "employees", indique quantos nomes de cargos ("jobTitle") únicos existem?
SELECT DISTINCT(jobTitle) from employees

- Qual destes cargos ("jobTitle") possuem mais funcionários?
SELECT jobTitle,COUNT(*) as contagem FROM employees GROUP BY jobTitle ORDER BY contagem DESC;