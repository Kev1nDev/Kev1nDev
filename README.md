# Kevin Romero
**Ingeniero de Software Cloud & Backend**

---

## Perfil Profesional

Ingeniero en Informática (2026) enfocado en **cloud y backend**: diseño, despliego y automatizo infraestructura en AWS con Terraform, construyo APIs REST con Python (FastAPI, Flask) sobre PostgreSQL y ejecuto inferencia de LLM local con Ollama en instancias GPU. Experiencia en administración de Linux, redes (VPN, WireGuard), endurecimiento de seguridad y optimización de costos en la nube.

- **Cloud e Infraestructura**: AWS (EC2, VPC, IAM, S3, EBS, KMS, Systems Manager), Terraform, Infrastructure as Code
- **Backend**: Python, FastAPI, Flask, APIs REST, SQL, PostgreSQL
- **Redes**: VPN (WireGuard), security groups, NACL, enrutamiento, IPs elásticas
- **IA / ML**: Ollama, modelos Llama, inferencia con GPU (NVIDIA L4/T4)
- **Contacto**: [Envíame un correo](mailto:insaniterecovery67@gmail.com)

## Conecta Conmigo

<div align="center">
  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kevin-romero-10290228b/)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=x&logoColor=white)](https://x.com/DevKev1n)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/kevinjsxr/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Kev1nDev)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:insaniterecovery67@gmail.com)

</div>

## Habilidades Técnicas

### Cloud
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

### Backend
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)

### Bases de Datos
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

### Herramientas
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![WireGuard](https://img.shields.io/badge/WireGuard-88171A?style=for-the-badge&logo=wireguard&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white)

## Ecosistema de Desarrollo

- **Sistema Operativo**: Linux Debian (Trixie)
- **Editores de Código**: Visual Studio Code, Google Antigravity
- **Terminal**: Bash
- **Asistentes AI & Calidad**: Amazon Q, Amazon CodeGuru
- **Gestión de Versiones**: GitKraken, GitHub

## Metas Profesionales 2026

- **Certificación en AWS**: Obtener la certificación AWS Cloud Practitioner y avanzar hacia Associate Solutions Architect.
- **Profundizar en Kubernetes y CI/CD**: Fortalecer competencias en containers, orquestación y pipelines de integración continua.
- **Contribución Open Source**: Participar activamente en proyectos de infraestructura como código y backend.
- **Cultura DevOps**: Consolidar el dominio de Terraform, Docker y automatización de despliegues.

## Proyectos Destacados

### NimbusStream - Infraestructura Cloud de Gaming con GPU Headless en AWS

Proyecto personal insignia: infraestructura completa de cloud gaming en AWS construida con **Terraform** (~33 recursos) y aprovisionada y operada de punta a punta por mí.

- **VPC multi-AZ propia** (10.0.0.0/16) con 3 subnets en 2 zonas de disponibilidad, Internet Gateway, route tables y security groups de mínimos privilegios separando gaming y VPN.
- Instancia EC2 **g6.xlarge (NVIDIA L4 24 GB)** con render headless via Virtual Display Driver, streaming a **720p/60 FPS** y gamepad virtual (ViGEmBus).
- **Túnel WireGuard** como único puerto público: RDP y streaming solo accesibles por VPN; administración 100% sin SSH via **AWS SSM** e IMDSv2 obligatorio.
- Stack de **IA local con Ollama** sirviendo modelos Llama en la GPU para inferencia privada.
- Optimización de costos: sin NAT gateway, ciclo de vida stop/start y limpieza de recursos huérfanos.

**Stack Tecnológico**: Terraform, AWS (VPC, EC2, EBS, KMS, SSM), WireGuard, PowerShell, Ollama

**Estado**: Desplegado | [Ver Repositorio](https://github.com/Kev1nDev/NimbuStream)

---

### Aplicación Móvil de Accesibilidad con IA (Tesis de Ingeniería)

Aplicación móvil que asiste a personas con discapacidad visual describiendo el entorno en tiempo real. Proyecto de tesis de grado en Ingeniería en Informática (completado).

- App móvil **React Native + Expo + TypeScript** con cámara en vivo, retornos por **voz (TTS)** y vibración de alerta.
- **Backend Node.js/Express** con endpoint `POST /describe` que procesa la imagen capturada (base64, redimensionada y comprimida) e invoca el modelo visión **Llama 3.2 Vision (11B)** vía **Groq**, con medición de latencia end-to-end y fallback degradado sin API key.
- Módulos: descripción breve/extendida del entorno, **camino guiado con detección de obstáculos (izquierda/centro/derecha)** via análisis periódico de cámara, y lecturas asistidas.
- Descripción estructurada: resumen, detalle, puntos de interés, incertidumbres y confianza, con **contexto GPS** y modos `balanced | fast | accurate`.

**Stack Tecnológico**: React Native, Expo, TypeScript, Node.js, Express, Llama 3.2 Vision (Groq), Computer Vision, Machine Learning

**Estado**: Completado | [Ver Repositorio](https://github.com/Kev1nDev/Tesis-2025)

---

### TOMOTOMO - E-Commerce de Manga y Cómics

Plataforma de comercio electrónico especializada en la venta de manga y cómics, con carrito de compras, búsqueda en tiempo real, filtrado por categorías y diseño responsivo.

**Stack Tecnológico**: React, Vite, React Router, Framer Motion, Context API

**Estado**: Desplegado | [Ver Demo](https://kev1ndev.github.io/tomotomo-react/)

---

### BakeByCelia - Sitio Web de Pastelería

Sitio web moderno para una pastelería artesanal con diseño responsivo, animaciones fluidas y optimización SEO.

**Stack Tecnológico**: Next.js 15, React 19, TypeScript, Tailwind CSS

**Estado**: En desarrollo | [Ver Repositorio](https://github.com/Kev1nDev/BakeByCelia)

---

Gracias por visitar mi perfil.