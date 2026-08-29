# Imagem base: Python enxuto (a primeira camada da nossa pilha)
FROM python:3.12-slim

# Diretório de trabalho dentro do container
WORKDIR /app

# Copiamos SÓ as dependências primeiro: assim, quando apenas o código
# mudar, o build reaproveita a camada (cache) da instalação, que é a lenta.
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Agora sim, o código e o modelo
COPY . .

# Comando executado quando o container inicia
CMD ["uvicorn", "api:app", "--host", "0.0.0.0", "--port", "8000"]
