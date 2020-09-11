CRIAÇÃO DO MERCEARIA DO SQL  
CREATE TABLE CLIENTE -- criação da tabela Clientes   
(ID_Cliente INTEGER NOT NULL,   
Nome_Cliente VARCHAR(60) NULL,   
Endereco_Cliente VARCHAR(60) NULL  
PRIMARY KEY (ID_Cliente));  

CREATE TABLE PEDIDO -- criação da tabela Pedido  
(Numero_Pedido integer PRIMARY KEY,  
Datahora datetime NOT NULL,  
ID_Cliente integer,  
CONSTRAINT fk_ID_Cliente FOREIGN KEY (ID_Cliente) REFERENCES CLIENTE (ID_Cliente));  

CREATE TABLE PRODUTO -- criação da tabela Produto  
(ID_Produto INTEGER PRIMARY KEY,  
Nome_Produto VARCHAR(60) NULL);  

CREATE TABLE ITEM_PEDIDO -- criação Item pedido  
(NUMERO_PEDIDO INTEGER,  
ID_PRODUTO INTEGER,  
QTDE INTEGER NOT NULL,  
CONSTRAINT FK_ID_PRODUTO FOREIGN KEY (ID_PRODUTO) REFERENCES PRODUTO (ID_PRODUTO),  
CONSTRAINT FK_NUMERO_PEDIDO FOREIGN KEY (NUMERO_PEDIDO) REFERENCES PEDIDO (NUMERO_PEDIDO));  

CREATE TABLE TELEFONE -- criação da tabela telefone   
(ID_CLIENTE INTEGER,  
NUMERO INTEGER,  
CONSTRAINT FK_ID_CLIETELL FOREIGN KEY (ID_CLIENTE) REFERENCES CLIENTE (ID_CLIENTE));  
