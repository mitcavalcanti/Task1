# terraform-gcp-tarea1

Demo para crear un Cluster de Kubernetes en GCP usando el servicio de GKE - Everis Tarea1

## Requerimientos

- Terraform versión v0.12.26.
- Cuenta en GCP.
- Crear una cuenta de servicios y crear una clave del tipo JSON.

## Estructura

- **gcr:** Se usa el módulo de container registry del provider de GCP.
- **gke:** Se usa el módulo de kubernetes engine del provider de GCP.
- **nginx-ingress:** Se usa el provider de Helm para para instalar el chart de nginx.

## Acciones Makefile

- **init:** Inicializa Terraform
- **validate:** Valida .tfs
- **plan:** Ejecuta plan de Terraform
- **apply:** Aplica plan de Terraform
- **destroy:** Planifica y elimina.
- **output:** Muestra el Outout configurado

## Configuración

Los siguientes parámetros son los que se pueden usar en el flujo.

  *Todos son obligatorios*

Parámetro | Descripción
--------- | -----------
`project_id` | ID del proyecto en GCP
`gcp_region` | Region de GCP en la que se va a trabajar
`cluster_name` | GKE Nombre de Cluster
`gke_location` | GKE Location.
`inital_nodes` | Número de nodos iniciales
`node_pool_name` | GKE Node pool name
`node_pool_count` | Número de nodos
`is_preemptible` | Indica si las VM a usar son del tipo preemtible (true - false)
`vm_type` | Tipo de VM
`helm_nginx_name` | Nombre para la instanlación de Helm
`chart_nginx_name` | Nombre del Helm Chart
