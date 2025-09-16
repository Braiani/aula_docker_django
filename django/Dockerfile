FROM python:3.11-slim

# Atualiza os pacotes e instala as dependências necessárias para o MySQL
RUN apt-get update && apt-get install -y \
    build-essential \
    pkg-config \
    default-libmysqlclient-dev \
    gcc \
    && pip install --no-cache-dir --upgrade pip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Define o diretório de trabalho
WORKDIR /app

# Copia o arquivo de requisitos e instala as dependências do Python
COPY ./Prover/requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copia o restante do código da aplicação
COPY ./Prover/ /app/

EXPOSE 8000

# Comando para rodar a aplicação
CMD ["sh", "-c", "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"]
