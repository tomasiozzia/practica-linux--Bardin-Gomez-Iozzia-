# ERRORES ENCONTRADOS Y TESTING - GOMEZ (Alumno C)

## 1. PROBLEMA INICIAL:
Command 'docker-compose' not found
**SOLUCIÓN**: sudo apt install -y docker.io docker-compose

## 2. docker-compose up -d:
✅ 6 contenedores creados exitosamente:
- nginx-practica (8081)
- redis-practica (6379) 
- postgres-practica (5432)
- loki-practica (3100)
- prometheus-practica (9090) [Restarting - config prometheus.yml]
- grafana-practica (3000)

## 3. Comandos de debug:
- docker-compose config ✓
- docker-compose logs ✓
- docker ps ✓

## 4. Observaciones:
Prometheus restarting por prometheus.yml (nginx no expone métricas 9113)
