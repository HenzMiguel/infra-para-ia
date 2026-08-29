# Aula 1 — Containers

Artefatos da prática: uma API de análise de sentimento em português (FastAPI + scikit-learn) empacotada em um container e executada no Azure (ACR + ACI).

| Arquivo | O que é |
|---|---|
| `api.py` | A API de inferência: `POST /prediz` recebe uma frase e responde o sentimento |
| `modelo.pkl` | Modelo treinado (TF-IDF + regressão logística), pronto para uso |
| `treinar_modelo.py` | Script que gera o `modelo.pkl` — rode para retreinar ou estender o dataset |
| `requirements.txt` | Dependências com versões fixas (reprodutibilidade!) |
| `Dockerfile` | A receita do container, comentada linha a linha |
| `ROTEIRO.md` | **Comece por aqui:** o passo a passo da prática no Azure |

## Executar localmente (opcional, fora da aula)

```bash
pip install -r requirements.txt
uvicorn api:app --host 0.0.0.0 --port 8000
# abra http://localhost:8000/docs
```

## Testar a API

```bash
curl -X POST http://localhost:8000/prediz \
  -H "Content-Type: application/json" \
  -d '{"texto": "adorei o curso!"}'
# {"sentimento": "positivo", "confianca": 0.93...}
```
