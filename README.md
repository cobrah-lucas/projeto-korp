# 🚀 Projeto Korp - Servidor HTTP com Monitoramento e Automação

Desafio técnico para a vaga de DevOps/Backend na **Korp**.  
Implementação de um servidor HTTP em Go, containerizado com Docker, monitorado com Prometheus + Grafana e totalmente automatizado com Ansible.

---

## 📦 Tecnologias Utilizadas

- **Go (Golang)** – Servidor HTTP com métricas Prometheus
- **Docker & Docker Compose** – Orquestração dos containers
- **Nginx** – Proxy reverso para o servidor Go
- **Prometheus** – Coleta de métricas (volume de requisições e disponibilidade)
- **Grafana** – Visualização das métricas (dashboard automático)
- **Ansible** – Automação completa do ambiente

---

## ✅ Requisitos Atendidos

| Requisito | Status |
|-----------|--------|
| Servidor HTTP em Go na porta 8080 | ✅ |
| Endpoint `GET /projeto-korp` retornando JSON com horário UTC | ✅ |
| Dockerfile com multi-stage build | ✅ |
| Rede Docker bridge | ✅ |
| Docker Compose com dois containers (Go + Nginx) | ✅ |
| Proxy reverso Nginx (porta 80 → 8080) | ✅ |
| Teste com `curl http://localhost/projeto-korp` | ✅ |
| Métricas: volume de requisições (`http_requests_total`) | ✅ |
| Métricas: disponibilidade do serviço (`service_availability`) | ✅ |
| Prometheus coletando métricas | ✅ |
| Grafana visualizando métricas (dashboard automático) | ✅ |
| Playbook Ansible para automação total | ✅ |

---

## ▶️ Como Executar (via Docker Compose)

```bash
git clone https://github.com/cobrah-lucas/projeto-korp.git

cd projeto-korp
docker-compose up -d
curl http://localhost/projeto-korp    https://github.com/cobrah-lucas/projeto-korp/tree/main/grafana/provisioning/dashboards       
