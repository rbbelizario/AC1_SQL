CRIAÇÃO DO EMPRESTIMO DO SQL  
CREATE TABLE LIVRO  
(Nome_Livro VARCHAR(70) NULL,  
Copia_Livro INTEGER NOT NULL,  
Status_Livro VARCHAR(20) NULL,  
PRIMARY KEY(Copia_Livro));  

CREATE TABLE CLIENTE  
(ID_Cliente INT IDENTITY(1,1) PRIMARY KEY,  
Nome_Cliente VARCHAR(70) NOT NULL,  
Telefone_Cliente VARCHAR(20) NULL,)  

CREATE TABLE EMPRESTIMO  
(ID_Emprestimo INT IDENTITY(1,1) PRIMARY KEY,  
Copia_Livro integer,  
CONSTRAINT fk_Copia_Livro FOREIGN KEY (Copia_Livro) REFERENCES LIVRO (Copia_Livro),  
ID_Cliente integer not null,  
CONSTRAINT fk_ID_Cliente FOREIGN KEY (ID_Cliente) REFERENCES CLIENTE (ID_Cliente),  
Livro VARCHAR(70) NULL,  
Copia INTEGER NOT NULL,  
Data_Emprestimo date NOT NULL,  
Data_Devolucao_Proposta datetime NOT NULL,  
Data_Devolucao_Efetiva datetime NOT NULL,  
Multa integer )  

