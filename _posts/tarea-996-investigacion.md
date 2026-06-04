---
title: Tarea 996
layout: slide
theme: black
permalink: /Tarea996/
---

# Solucion Estratificada de Problemas en TIC
Abigail Hernandez Contreras

---

## 1.1 Solucion Estratificada en TIC

Es el enfoque de dividir la infraestructura tecnologica en capas logicas para aislar problemas, optimizar recursos y facilitar la gestion.

* **Hardware:** CPU, RAM, Almacenamiento fisico.
* **Capa de Virtualizacion:** Abstraccion de los recursos.
* **Sistema Operativo:** Gestion del entorno virtualizado.
* **Aplicaciones:** Servicios y procesos ejecutados por el usuario final.

---

## 1.1.a Virtualizacion por Interpretacion Pura

El nivel mas basico y fundamental de la emulacion.

--

### Descripcion

El software de virtualizacion actua como un traductor en tiempo real. Toma cada instruccion del sistema invitado y la traduce individualmente a instrucciones que el procesador anfitrion pueda entender y ejecutar de forma secuencial.

--

### Caracteristicas

* **Aislamiento total:** El invitado no tiene contacto directo con el hardware subyacente.
* **Alta sobrecarga (Overhead):** El proceso de traduccion constante consume altos niveles de procesamiento.
* **Independencia de arquitectura:** Permite ejecutar codigo diseñado para un procesador distinto.

--

### Casos de Uso y Ejemplos

**Casos de Uso:**
* Desarrollo y pruebas de sistemas operativos experimentales.
* Analisis forense y de malware en entornos controlados.

**Ejemplos:**
* Bochs
* QEMU (modo de emulacion pura)

---

## 1.1.b Virtualizacion por Recompilacion Dinamica

Eficiencia a traves de la traduccion inteligente al vuelo.

--

### Descripcion

En lugar de traducir instruccion por instruccion, el sistema analiza bloques de codigo enteros en tiempo de ejecucion, los traduce al lenguaje nativo del hardware anfitrion y los guarda en cache (JIT) para no volver a traducirlos en el futuro.

--

### Caracteristicas

* **Rendimiento superior:** Mucho mas rapido que la interpretacion pura gracias al uso de memoria cache.
* **Optimizacion en tiempo real:** Adapta y mejora la ejecucion del codigo sobre la marcha.
* **Mayor complejidad:** El desarrollo del motor de recompilacion es tecnicamente avanzado.

--

### Casos de Uso y Ejemplos

**Casos de Uso:**
* Emuladores modernos que requieren alto rendimiento.
* Entornos de ejecucion como la Maquina Virtual de Java (JVM).

**Ejemplos:**
* QEMU (motor TCG).
* Rosetta 2 (Apple).

---

## 1.1.c Virtualizacion por Hipervision (Bare Metal)

El estandar de la industria empresarial para el maximo rendimiento.

--

### Descripcion

Conocido como Hipervisor Tipo 1. El software de virtualizacion se instala directamente sobre el hardware fisico, eliminando la necesidad de un sistema operativo anfitrion intermedio.

--

### Caracteristicas

* **Rendimiento casi nativo:** La latencia es minima y el uso de recursos es optimo.
* **Alta seguridad y estabilidad:** Aislamiento robusto a nivel de hardware.
* **Soporte de Hardware:** Requiere procesadores con instrucciones de virtualizacion nativas.

--

### Casos de Uso y Ejemplos

**Casos de Uso:**
* Centros de Datos Empresariales.
* Proveedores de Cloud Computing (AWS, Azure, Google Cloud).

**Ejemplos:**
* VMware ESXi
* Microsoft Hyper-V
* Proxmox VE

---

## Comparacion General

| Tecnologia | Rendimiento | Compatibilidad |
| :--- | :--- | :--- |
| Interpretacion Pura | Bajo | Muy Alta |
| Recompilacion Dinamica | Medio - Alto | Alta |
| Hipervision (Bare Metal) | Casi Nativo | Limitada al hardware base |

---

## Conclusiones

* La eleccion del metodo de virtualizacion depende estrictamente del caso de uso.
* La **Interpretacion** prioriza la compatibilidad sobre la velocidad.
* La **Recompilacion** ofrece un balance intermedio para entornos de escritorio.
* El **Bare Metal** es indiscutible para entornos de produccion empresarial.
