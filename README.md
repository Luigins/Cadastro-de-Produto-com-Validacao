# 🛒 Cadastro de Produtos com Validação em PHP e MySQL

Este projeto consiste em uma aplicação web simples desenvolvida em **PHP**, **HTML5** e **MySQL**, criada para demonstrar a captura de dados via formulário, validação de entradas no lado do servidor (backend) e integração com banco de dados relacional.

---

## 📌 Funcionalidades

- **Formulário de Cadastro:** Interface intuitiva para inserção de dados do produto (*Nome* e *Preço*).
- **Validação Server-Side:**
  - Verifica se o nome do produto foi preenchido.
  - Garante que o preço informado é numérico e maior que zero ($> 0$).
- **Integração com Banco de Dados:**
  - Conexão nativa via classe `mysqli`.
  - Inserção dinâmica na tabela de produtos.
  - Tratamento de exceções e erros de conexão utilizando blocos `try-catch`.

---

## 🛠️ Tecnologias Utilizadas

- **Frontend:** HTML5
- **Backend:** PHP 8.x
- **Banco de Dados:** MySQL / MariaDB
- **Ambiente Recomendado:** XAMPP, WAMP, Laragon ou MySQL Server local

---

## 🗄️ Estrutura do Banco de Dados

Antes de rodar a aplicação, certifique-se de criar o banco de dados `exercicio` e a tabela `produtos`. 

Execute o script SQL abaixo no seu gerenciador de banco de dados (ex: phpMyAdmin, DBeaver, MySQL Workbench):

```sql
CREATE DATABASE IF NOT EXISTS exercicio;
USE exercicio;

CREATE TABLE IF NOT EXISTS produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    preco DECIMAL(10, 2) NOT NULL,
    data_criacao TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## 💻 Como Executar o Projeto

1. **Clone ou Baixe o Repositório:**
   Coloque os arquivos do projeto no diretório do seu servidor local (ex: `htdocs` no XAMPP ou `www` no WAMP).

2. **Inicie os Serviços:**
   Inicie os módulos do **Apache** e **MySQL** pelo painel de controle do seu servidor local.

3. **Ajuste as Configurações de Conexão:**
   Se necessário, altere as variáveis de conexão no arquivo PHP para corresponder às suas credenciais locais:
   ```php
   $servername = "localhost";
   $username = "root";
   $password = "SUA_SENHA_AQUI";
   $dbname = "exercicio";
   ```

4. **Acesse a Aplicação:**
   Abra o seu navegador e acesse:
   ```text
   http://localhost/seu-diretorio/index.php
   ```

---

## 🔒 Boas Práticas e Futuras Melhorias

Para aprimorar esta aplicação em versões futuras, recomenda-se:
- [ ] Uso de **Prepared Statements** (Instruções Preparadas) para prevenir potenciais vulnerabilidades de *SQL Injection*.
- [ ] Separação das responsabilidades (código HTML, lógica de validação e conexão em arquivos separados).
- [ ] Estilização visual utilizando **CSS3** ou *frameworks* como Bootstrap/Tailwind CSS.

---

## 📜 Licença

Este projeto é voltado para fins educacionais e de aprendizado. Sinta-se livre para utilizar, modificar e aprimorar o código!
