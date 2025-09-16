# Exemplo: Docker + Django + MySQL

Este repositório contém um projeto de exemplo utilizado em aulas sobre Docker, demonstrando como utilizar o Django como aplicação web e o MySQL como banco de dados relacional.

## Estrutura do Projeto
- **Django**: Framework web em Python, utilizado para construir a aplicação principal.
- **MySQL**: Banco de dados relacional, utilizado para persistência dos dados da aplicação.
- **Docker**: Ferramenta de containerização, utilizada para facilitar o desenvolvimento, deploy e integração dos serviços.
- **Nginx**: Proxy reverso para servir a aplicação Django.

## Como utilizar
1. Clone o repositório:
   ```bash
   git clone <url-do-repositorio>
   ```
2. Configure variáveis e dependências conforme necessário.
3. Execute os containers com Docker Compose:
   ```bash
   docker-compose up --build
   ```
4. Acesse a aplicação Django em `http://localhost:8000` ou via Nginx em `http://localhost`.

## Observações
- O projeto inclui exemplos de configuração de volumes, redes e dependências entre serviços.
- O arquivo `requirements.txt` lista as dependências Python necessárias para o Django e integração com MySQL.
- O script `wait-for-it.sh` pode ser utilizado para garantir que o Django só inicie após o MySQL estar pronto.

## Objetivo
Este projeto serve como base para estudos, testes e demonstrações práticas sobre o uso de Docker com Django e MySQL em ambientes de desenvolvimento e produção.

---

Sinta-se à vontade para modificar e adaptar conforme suas necessidades nas aulas!
