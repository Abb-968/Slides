---
title: Tarea 996
layout: slide
theme: black
permalink: /Tarea996/
---

# Solucion Estratificada de Problemas en TIC
Abigail Hernandez Contreras 
230300968

---

## 1.1 Solucion Estratificada en TIC

Este modelo organiza los componentes de TI en niveles jerarquicos y separados. Su proposito es aislar procesos, simplificar la resolucion de fallos y mejorar el manejo de recursos.

* **Infraestructura Fisica:** Servidores, procesadores y unidades de almacenamiento base.
* **Nivel de Abstraccion:** Hipervisores o motores de emulacion.
* **Sistema Huesped:** Entorno operativo virtual independiente.
* **Capa de Usuario:** Software y aplicaciones finales ejecutadas por el cliente.

---

## 1.1.a Virtualizacion por Interpretacion Pura

El metodo de emulacion mas tradicional y estricto.

--

### Descripcion

Funciona como un intermediario que lee las instrucciones del sistema virtualizado una por una y las convierte en comandos que la CPU fisica puede procesar en el momento.

--

### Caracteristicas

* **Independencia de hardware:** Capacidad de correr software creado para arquitecturas incompatibles con la maquina fisica.
* **Costo de procesamiento alto:** La traduccion continua exige demasiados recursos de la CPU, provocando lentitud.
* **Desvinculacion completa:** El entorno virtual esta completamente aislado de los componentes fisicos reales.

--

### Casos de Uso y Ejemplos

**Casos de Uso:**
* Investigacion de software antiguo o discontinuado.
* Analisis de codigo malicioso en entornos completamente seguros.
* Creacion de sistemas operativos desde cero.

**Ejemplos:**
* QEMU (sin utilizar aceleradores KVM).
* Bochs.
* Emuladores de hardware retro o consolas clasicas.

---

## 1.1.b Virtualizacion por Recompilacion Dinamica

Optimizacion del rendimiento mediante traduccion inteligente en tiempo de ejecucion.

--

### Descripcion

El emulador toma segmentos completos de codigo, los traduce a las instrucciones nativas del procesador anfitrion y los almacena en una memoria cache. Asi, si el bloque de codigo se repite, se ejecuta instantaneamente sin volver a traducirse.

--

### Caracteristicas

* **Rapidez mejorada:** Supera ampliamente a la interpretacion debido a la reutilizacion de codigo guardado en la cache (JIT).
* **Ajuste dinamico:** Optimiza el flujo de instrucciones mientras la aplicacion esta funcionando.
* **Arquitectura compleja:** Requiere un diseño de software avanzado para predecir y traducir los bloques eficientemente.

--

### Casos de Uso y Ejemplos

**Casos de Uso:**
* Capas de compatibilidad entre diferentes arquitecturas de CPU.
* Maquinas virtuales de lenguajes de programacion.
* Entornos de virtualizacion de escritorio.

**Ejemplos:**
* Rosetta 2 en ecosistemas macOS.
* Motor TCG de QEMU.
* Entornos de ejecucion como ART (Android Runtime) o la JVM.

---

## 1.1.c Virtualizacion por Hipervision (Bare Metal)

La base indiscutible de la infraestructura de nube y servidores empresariales.

--

### Descripcion

Un hipervisor de Tipo 1 se despliega directamente sobre los componentes fisicos del servidor. No requiere de un sistema operativo base, ya que el mismo administra y distribuye los recursos de hardware hacia las multiples maquinas virtuales.

--

### Caracteristicas

* **Latencia minima:** Ejecucion sumamente cercana al nivel nativo del procesador, maximizando el rendimiento.
* **Dependencia de hardware:** Necesita que la CPU tenga tecnologias de virtualizacion integradas de fabrica (Intel VT-x o AMD-V).
* **Aislamiento robusto:** Provee alta seguridad al separar completamente las maquinas virtuales a nivel estructural.

--

### Casos de Uso y Ejemplos

**Casos de Uso:**
* Implementacion de infraestructuras de Cloud Computing (IaaS).
* Administracion de centros de datos corporativos.
* Consolidacion masiva de servidores para ahorro de energia y espacio.

**Ejemplos:**
* VMware vSphere / ESXi.
* Proxmox VE.
* Microsoft Hyper-V Server.

---

## Comparacion de Modelos

| Tecnologia | Velocidad | Flexibilidad |
| :--- | :--- | :--- |
| Interpretacion Pura | Muy Lenta | Extrema (Multi-plataforma) |
| Recompilacion Dinamica | Aceptable a Rapida | Alta |
| Hipervision (Bare Metal) | Rendimiento Optimo | Restringida a CPU compatible |

---

## Resumen Final

* Cada estrategia de virtualizacion resuelve un problema distinto en la industria TI.
* La **Interpretacion** es ideal para garantizar compatibilidad absoluta y analisis a bajo nivel.
* La **Recompilacion** brinda una solucion rapida para software de usuario y entornos de transicion de hardware.
* La **Hipervision Bare Metal** es la columna vertebral tecnica para el procesamiento de datos y despliegues a nivel empresarial.
