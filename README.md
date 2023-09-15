# BD_ZE_DELIVERY
<div align="center">
<img src="https://github.com/Kayquin/BD_ZE_DELIVERY/assets/104329791/ec1296f1-45c6-443b-a40a-092671234c5d" width="1000px" />
</div>
<br> 
<h2>
<b>Entidades:</b>
</h2>
<h3> 1.	Usuário/Cliente (REGISTER)</h3>
•	Login (PK)
  <br>
•	Senha
  <br>
•	Nome
  <br>
•	CPF
  <br>
•	Email
  <br>
•	Endereço
  <br>
•	Telefone
<h3>2. Pedido</h3>
•	Número do pedido (PK)
  <br>
•	Data e hora do pedido
  <br>
•	Tempo de espera
  <br>
•	Valor total
  <br>
•	Status (PEDIDO REALIZADO, EM ANDAMENTO, A CAMINHO, ENTREGUE)
<h3>3. Produto</h3>
•	Código do produto (PK)
  <br>
•	Nome do produto
  <br>
•	Valor do produto
<h3>4.	Fornecedor</h3>
•	Código do fornecedor (PK)
  <br>
•	Nome do fornecedor
<h3>5.	Estoque</h3>
•	Código do produto (PK, FK para Produto)
  <br>
•	Quantidade disponível
<h3>6. Vendedor</h3>
•	Código do vendedor (PK)
  <br>
•	Código da loja física (FK para Loja Física)
  <br>
•	Código do usuário (FK para Usuário/Cliente)
  <br>
•	Nome do vendedor
  <br>
•	Telefone do vendedor
<h3>7. Admin</h3>
•	ADMIN (booleano para permissão de administração)
<h3>8. Loja Física</h3>
•	Código da loja (PK)
  <br>
•	Nome da loja
  <br>
•	Endereço da loja
  <br>
•	Telefone da loja
<h3>9. Relatório de Vendas</h3>
•	Código do relatório (PK)
  <br>
•	Código da loja física (FK para Loja Física)
  <br>
•	Valor total de vendas
  <br>
•	Data de início do relatório
  <br>
•	Data de fim do relatório
<br>
<br>
<h2>Relacionamentos:</h2>
<h3>Cliente (Usuário/Cliente) e Pedido:</h3>
•	Um Cliente (Usuário/Cliente) pode fazer vários Pedidos, o que é representado como [1..*]. Ou seja, um cliente pode fazer um ou mais pedidos.
<br>
•	Um Pedido está associado a um único Cliente, o que é representado como [1]. Cada pedido tem exatamente um cliente associado.
<h3>Pedido e Produto:</h3>
•	Um Pedido pode conter um ou mais Produtos, o que é representado como [0..*]. Isso significa que um pedido pode incluir zero ou mais produtos.
<br>
•	Um Produto pode estar em um ou mais Pedidos, o que também é representado como [0..*]. Isso indica que um produto pode ser pedido em zero ou mais pedidos.
<h3>Produto e Fornecedor:</h3>
•	Um Produto é fornecido por um ou mais Fornecedores, o que é representado como [1..*]. Um produto pode ter um ou mais fornecedores.
<h3>Vendedor e Loja Física:</h3>
•	Cada Vendedor está associado a uma única Loja Física, o que é representado como [1]. Cada vendedor trabalha em uma loja física específica.
<br>
•	Cada Loja Física pode ter um ou mais Vendedores, o que é representado como [0..*]. Isso significa que uma loja física pode ter zero ou mais vendedores.
<h3>Relatório de Vendas e Loja Física:</h3>
•	Cada Relatório de Vendas está associado a uma única Loja Física, o que é representado como [1]. Cada relatório corresponde a uma loja física específica.
<br>
•	Cada Loja Física pode ter um único Relatório de Vendas, o que também é representado como [1]. Isso significa que cada loja tem exatamente um relatório de vendas.
