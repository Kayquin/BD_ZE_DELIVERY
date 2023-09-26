# BD_ZE_DELIVERY
<div align="center">
<img src="https://github.com/Kayquin/BD_ZE_DELIVERY/assets/104329791/4024b4eb-bece-494d-8820-c8f5acc35733" width="1000px" />
</div>
<br> 
<h2>
<b>Entidades:</b>
</h2>
<h3> 1.	Usuário/Cliente (REGISTER)</h3>
•	Login (PK) - VARCHAR 
  <br>
•	Senha (FK) - VARCHAR 
  <br>
•	Nome (FK) - VARCHAR 
  <br>
•	CPF/CNPJ (PK) - VARCHAR 
  <br>
•	Email - VARCHAR 
  <br>
•	Endereço - VARCHAR
  <br>
•	Telefone - VARCHAR
<h3>2. Pedido</h3>
•	Número do pedido (PK) - INT
  <br>
•	Data e hora do pedido - DATETIME 
  <br>
•	Tempo de espera - INT 
  <br>
•	Valor total - DECIMAL 
  <br>
•	Status (PEDIDO REALIZADO, EM ANDAMENTO, A CAMINHO, ENTREGUE) - VARCHAR
<h3>3. Itens Pedido</h3>
• Código Itens Pedido - INT
<br>
• Código Pedido - INT
<br>
• Código Produto - INT
<br>
• Quantidade Produto INT
<h3>4. Produto</h3>
•	Código do produto (PK) - INT
  <br>
•	Nome do produto - VARCHAR
  <br>
•	Valor do produto - DECIMAL
<h3>5.	Fornecedor</h3>
•	Código do fornecedor (PK) - INT
  <br>
•	Nome do fornecedor - VARCHAR
<h3>6.	Estoque</h3>
•	Código do produto (PK, FK para Produto) - INT
  <br>
•	Quantidade disponível - INT
<h3>7. Vendedor</h3>
•	Código do vendedor (PK) - INT
  <br>
•	Código da loja física (FK para Loja Física) - INT
  <br>
•	Código do usuário (FK para Usuário/Cliente) - INT
  <br>
•	Nome do vendedor - VARCHAR
  <br>
•	Telefone do vendedor - VARCHAR
<h3>8. Admin</h3>
•	ADMIN (booleano para permissão de administração) - BOOLEAN 
<h3>9. Loja Física</h3>
•	Código da loja (PK) - INT
  <br>
•	Nome da loja - VARCHAR
  <br>
•	Endereço da loja - VARCHAR 
  <br>
•	Telefone da loja - VARCHAR
<h3>10. Relatório de Vendas</h3>
•	Código do relatório (PK) - INT
  <br>
•	Código da loja física (FK para Loja Física) - INT
  <br>
•	Valor total de vendas - DECIMAL
  <br>
•	Data de início do relatório - DATETIME
  <br>
•	Data de fim do relatório - DATETIME
<br>
<br>
<h2>Relacionamentos:</h2>
<h3>Cliente (Usuário/Cliente) e Pedido:</h3>
•	Um Cliente (Usuário/Cliente) pode fazer vários Pedidos, o que é representado como [1..*]. Ou seja, um cliente pode fazer um ou mais pedidos.
<br>
<br>
•	Um Pedido está associado a um único Cliente, o que é representado como [1]. Cada pedido tem exatamente um cliente associado.
<h3>Pedido e Produto:</h3>
•	Um Pedido pode conter um ou mais Produtos, o que é representado como [0..*]. Isso significa que um pedido pode incluir zero ou mais produtos.
<br>
<br>
•	Um Produto pode estar em um ou mais Pedidos, o que também é representado como [0..*]. Isso indica que um produto pode ser pedido em zero ou mais pedidos.
<h3>Produto e Fornecedor:</h3>
•	Um Produto é fornecido por um ou mais Fornecedores, o que é representado como [1..*]. Um produto pode ter um ou mais fornecedores.
<h3>Vendedor e Loja Física:</h3>
•	Cada Vendedor está associado a uma única Loja Física, o que é representado como [1]. Cada vendedor trabalha em uma loja física específica.
<br>
<br>
•	Cada Loja Física pode ter um ou mais Vendedores, o que é representado como [0..*]. Isso significa que uma loja física pode ter zero ou mais vendedores.
<h3>Relatório de Vendas e Loja Física:</h3>
•	Cada Relatório de Vendas está associado a uma única Loja Física, o que é representado como [1]. Cada relatório corresponde a uma loja física específica.
<br>
<br>
•	Cada Loja Física pode ter um único Relatório de Vendas, o que também é representado como [1]. Isso significa que cada loja tem exatamente um relatório de vendas.
<br>
