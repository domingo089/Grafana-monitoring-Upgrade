📊 Grafana + Prometheus Monitoring (MikroTik / Infrastructure)

Proyecto de monitoreo centralizado utilizando Prometheus, Grafana y exportadores para dispositivos de red como MikroTik, servidores Linux y servicios Docker.

🚀 Características
📡 Monitoreo de routers MikroTik
📈 Dashboards en Grafana en tiempo real
🔔 Sistema de alertas con Prometheus
🐳 Despliegue con Docker & Docker Compose
📊 Recolección de métricas de infraestructura
🧠 Configuración modular y escalable
🧰 Tecnologías utilizadas
Prometheus
Grafana
Docker
Docker Compose
MTKXP / MikroTik Exporter
Node Exporter (opcional)
📁 Estructura del proyecto
.
├── docker-compose.yml
├── prometheus.yml
├── alert_rules.yml
├── grafana/
│   └── dashboards/
├── exporters/
│   └── mikrotik/
└── README.md
⚙️ Instalación
1. Clonar el repositorio
git clone https://github.com/USUARIO/REPO.git
cd REPO
2. Levantar servicios con Docker
docker compose up -d
3. Verificar contenedores
docker ps
🌐 Accesos
Servicio	URL
Grafana	http://localhost:3000

Prometheus	http://localhost:9090
📡 Configuración MikroTik

Ejemplo de prometheus.yml:

scrape_configs:
  - job_name: "mikrotik"
    static_configs:
      - targets: ["192.168.1.1:9436"]
🔔 Alertas

Las reglas de alertas se encuentran en:

alert_rules.yml

Ejemplo:

CPU alta
Memoria saturada
Interfaces caídas
Latencia elevada
📊 Dashboards

Los dashboards de Grafana están diseñados para:

Estado de routers MikroTik
Uso de CPU / RAM
Tráfico de red por interfaz
Uptime de dispositivos
🛠️ Mantenimiento

Recargar Prometheus sin reiniciar:

curl -X POST http://localhost:9090/-/reload
📌 Requisitos
Docker instalado
Docker Compose
Acceso a dispositivos de red
Puertos abiertos: 3000, 9090, 9100 (según configuración)
👨‍💻 Autor

Desarrollado por Domingo Tatis

📜 Licencia

Este proyecto es de uso libre para fines educativos y de monitoreo de infraestructura.

⭐ Recomendación

Si te funciona este proyecto, no olvides darle ⭐ en GitHub y mejorarlo con:

Loki (logs)
Alertmanager
HTTPS con Nginx Proxy
Backup automático de dashboards
