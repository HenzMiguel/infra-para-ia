# Infraestrutura Computacional para IA

Repositório de artefatos das atividades práticas da disciplina de extensão **Infraestrutura Computacional para IA** (curso de extensão em IA Generativa, Unisinos).

Todas as práticas rodam no **Microsoft Azure**, usando apenas o navegador (portal + Cloud Shell). Nada precisa ser instalado no seu computador.

## Estrutura

| Pasta | Aula | Tema |
|---|---|---|
| [`aula1-containers/`](aula1-containers/) | 1 | Containers: build e execução de uma API de IA (ACR + ACI) |
| `aula2-kubernetes/` | 2 | Kubernetes: deploy e escala no AKS *(em breve)* |
| `aula3-iac/` | 3 | Infraestrutura como Código com Terraform *(em breve)* |
| `aula4-storage-orquestracao/` | 4 | Object storage e orquestração gerenciada: Blob + Container Apps *(em breve)* |
| `aula5-kafka/` | 5 | Streaming com protocolo Kafka no Event Hubs *(em breve)* |

## Antes da aula 1

1. Crie sua conta gratuita do Azure (siga o tutorial enviado por e-mail). Faça isso **na semana da aula 1** — o crédito de US$ 200 vale por 30 dias.
2. Consiga fazer login em [portal.azure.com](https://portal.azure.com).

## O fio condutor do curso

Uma mesma aplicação de IA (uma API de análise de sentimento) atravessa as 5 aulas: nasce em um container, ganha escala no Kubernetes, vira código com Terraform, lê dados do object storage rodando de forma gerenciada e, por fim, processa eventos em tempo real com Kafka.

## Regra de ouro

Ao final de cada prática, **apague o resource group da aula** (`az group delete`). Infraestrutura de aula não dorme ligada.
