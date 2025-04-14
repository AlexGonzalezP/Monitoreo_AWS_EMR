# Monitoreo de Clúster AWS EMR con Prometheus y Grafana

Este proyecto consiste en la implementación de un sistema de monitoreo para un clúster de procesamiento de datos en AWS EMR. Se utilizan herramientas open-source como JMX Exporter, Prometheus y Grafana para la recolección, exposición y visualización de métricas relevantes del clúster.

## Objetivo

Diseñar un sistema que permita supervisar el rendimiento y estado de un clúster EMR en tiempo real, facilitando el análisis operativo mediante métricas visuales y centralizadas.

## Herramientas utilizadas

- **AWS EMR**: Servicio para desplegar clústeres de procesamiento distribuido.
- **JMX Exporter**: Herramienta para exponer métricas de aplicaciones Java.
- **Prometheus**: Sistema de monitoreo y recopilación de métricas.
- **Grafana**: Plataforma de visualización de datos.

## Contenido del repositorio

- `config.yml`: Archivo de configuración base para JMX Exporter.
- `hadoop-env.sh`: Script modificado para incluir el agente JMX Exporter en Hadoop.
- `jmx_prometheus_javaagent-0.16.1.jar`: Agente que expone métricas JMX en formato Prometheus.
- `prometheus.yml`: Configuración del servidor Prometheus para scrapear las métricas del clúster.
- Capturas de pantalla del dashboard en Grafana.
- Manual paso a paso de la práctica.
- Respuestas a las preguntas de reflexión.

## Despliegue

El sistema se compone de un clúster EMR configurado con Hadoop, Spark y Hive, con JMX Exporter instalado en el nodo maestro. Una instancia EC2 separada aloja Prometheus y Grafana para la recolección y visualización de métricas del clúster.

## Métricas visualizadas

- Uso de CPU y memoria.
- Espacio utilizado en HDFS.
- Estado del NameNode.
- Actividad general del clúster.
