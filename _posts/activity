---
title: Tarea 996
layout: post
permalink: /Tarea996/
---

<section>
    <h1>Solucion Estratificada de Problemas en TIC</h1>
    <p>Abigail Hernandez Contreras</p>
</section>

<section>
    <h2>1.1 Solucion Estratificada en TIC</h2>
    <p>
        Es el enfoque de dividir la infraestructura tecnologica en capas logicas para aislar problemas, optimizar recursos y facilitar la gestion.
    </p>
    <ol>
        <li><strong>Hardware:</strong> CPU, RAM, Almacenamiento fisico.</li>
        <li><strong>Capa de Virtualizacion:</strong> Abstraccion de los recursos mediante hipervisores o emuladores.</li>
        <li><strong>Sistema Operativo:</strong> Gestion del entorno virtualizado.</li>
        <li><strong>Aplicaciones:</strong> Servicios y procesos ejecutados por el usuario final.</li>
    </ol>
</section>

<section>
    <section>
        <h2>1.1.a Virtualizacion por Interpretacion Pura</h2>
        <p>El nivel mas basico y fundamental de la emulacion.</p>
        <p><em>↓ Usa la flecha abajo para profundizar</em></p>
    </section>

    <section>
        <h2>Descripcion</h2>
        <p>
            El software de virtualizacion actua como un traductor en tiempo real. Toma cada instruccion del sistema invitado y la traduce individualmente a instrucciones que el procesador anfitrion pueda entender y ejecutar de forma secuencial.
        </p>
    </section>

    <section>
        <h2>Caracteristicas</h2>
        <ul>
            <li><strong>Aislamiento total:</strong> El invitado no tiene contacto directo con el hardware subyacente.</li>
            <li><strong>Alta sobrecarga (Overhead):</strong> El proceso de traduccion constante consume altos niveles de procesamiento.</li>
            <li><strong>Independencia de arquitectura:</strong> Permite ejecutar codigo diseñado para un procesador distinto (ej. software ARM en un procesador x86).</li>
        </ul>
    </section>

    <section>
        <h2>Casos de Uso</h2>
        <ul>
            <li>Desarrollo y pruebas de sistemas operativos experimentales multiplataforma.</li>
            <li>Analisis forense y de malware en entornos altamente controlados.</li>
            <li>Ejecucion de software heredado (legacy) de arquitecturas obsoletas.</li>
        </ul>
    </section>

    <section>
        <h2>Ejemplos</h2>
        <ul>
            <li><strong>Bochs:</strong> Emulador de PC altamente portatil.</li>
            <li><strong>QEMU:</strong> En su modo de emulacion pura sin aceleracion KVM.</li>
            <li>Emuladores de consolas retro.</li>
        </ul>
    </section>
</section>

<section>
    <section>
        <h2>1.1.b Virtualizacion por Recompilacion Dinamica</h2>
        <p>Eficiencia a traves de la traduccion inteligente al vuelo.</p>
        <p><em>↓ Usa la flecha abajo para profundizar</em></p>
    </section>

    <section>
        <h2>Descripcion</h2>
        <p>
            En lugar de traducir instruccion por instruccion, el sistema analiza <strong>bloques de codigo</strong> enteros en tiempo de ejecucion, los traduce al lenguaje nativo del hardware anfitrion y los guarda en cache (JIT - Just-In-Time) para no volver a traducirlos en el futuro.
        </p>
    </section>

    <section>
        <h2>Caracteristicas</h2>
        <ul>
            <li><strong>Rendimiento superior:</strong> Mucho mas rapido que la interpretacion pura gracias al uso de memoria cache.</li>
            <li><strong>Optimizacion en tiempo real:</strong> Adapta y mejora la ejecucion del codigo sobre la marcha.</li>
            <li><strong>Mayor complejidad:</strong> El desarrollo del motor de recompilacion es tecnicamente avanzado.</li>
        </ul>
    </section>

    <section>
        <h2>Casos de Uso</h2>
        <ul>
            <li>Emuladores modernos que requieren alto rendimiento y baja latencia.</li>
            <li>Entornos de ejecucion como la Maquina Virtual de Java (JVM).</li>
            <li>Virtualizacion de software en arquitecturas de transicion (ej. Rosetta 2).</li>
        </ul>
    </section>

    <section>
        <h2>Ejemplos</h2>
        <ul>
            <li><strong>QEMU:</strong> Utilizando su motor TCG (Tiny Code Generator).</li>
            <li><strong>Rosetta 2</strong> (Apple).</li>
            <li>Primeras versiones de <strong>VirtualPC</strong>.</li>
        </ul>
    </section>
</section>

<section>
    <section>
        <h2>1.1.c Virtualizacion por Hipervision (Bare Metal)</h2>
        <p>El estandar de la industria empresarial para el maximo rendimiento.</p>
        <p><em>↓ Usa la flecha abajo para profundizar</em></p>
    </section>

    <section>
        <h2>Descripcion</h2>
        <p>
            Conocido como Hipervisor Tipo 1. El software de virtualizacion se instala <strong>directamente sobre el hardware fisico</strong>, eliminando la necesidad de un sistema operativo anfitrion intermedio. El hipervisor gestiona los recursos de hardware directamente hacia las Maquinas Virtuales.
        </p>
    </section>

    <section>
        <h2>Caracteristicas</h2>
        <ul>
            <li><strong>Rendimiento casi nativo:</strong> Al no haber un SO intermedio, la latencia es minima y el uso de recursos es optimo.</li>
            <li><strong>Alta seguridad y estabilidad:</strong> Menor superficie de ataque y aislamiento robusto a nivel de hardware.</li>
            <li><strong>Soporte de Hardware:</strong> Requiere procesadores con instrucciones de virtualizacion nativas (Intel VT-x, AMD-V).</li>
        </ul>
    </section>

    <section>
        <h2>Casos de Uso</h2>
        <ul>
            <li>Centros de Datos Empresariales (Data Centers).</li>
            <li>Proveedores de Cloud Computing (IaaS como AWS, Azure, Google Cloud).</li>
            <li>Consolidacion masiva de servidores corporativos.</li>
        </ul>
    </section>

    <section>
        <h2>Ejemplos</h2>
        <ul>
            <li><strong>VMware ESXi.</strong></li>
            <li><strong>Microsoft Hyper-V.</strong></li>
            <li><strong>Proxmox VE</strong> (basado en KVM).</li>
            <li><strong>XenServer.</strong></li>
        </ul>
    </section>
</section>

<section>
    <h2>Comparacion General</h2>
    <table>
        <thead>
            <tr>
                <th>Tecnologia</th>
                <th>Rendimiento</th>
                <th>Compatibilidad</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Interpretacion Pura</td>
                <td>Bajo</td>
                <td>Muy Alta (Multi-arquitectura)</td>
            </tr>
            <tr>
                <td>Recompilacion Dinamica</td>
                <td>Medio - Alto</td>
                <td>Alta</td>
            </tr>
            <tr>
                <td>Hipervision (Bare Metal)</td>
                <td>Casi Nativo</td>
                <td>Limitada al hardware base</td>
            </tr>
        </tbody>
    </table>
</section>

<section>
    <h2>Conclusiones</h2>
    <ul>
        <li>La eleccion del metodo de virtualizacion depende estrictamente del caso de uso y los recursos disponibles.</li>
        <li>La <strong>Interpretacion</strong> prioriza la compatibilidad y la investigacion sobre la velocidad.</li>
        <li>La <strong>Recompilacion</strong> ofrece un balance intermedio para entornos de escritorio.</li>
        <li>El <strong>Bare Metal</strong> es indiscutible para entornos de produccion empresarial y arquitecturas Cloud.</li>
    </ul>
</section>
