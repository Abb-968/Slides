---
title: Tarea 996
layout: post
permalink: /Tarea996/
theme: moon
---

<section>
    <h1>Solucion Estratificada de Problemas en TIC</h1>
    <p>Abigail Hernandez Contreras</p>
</section>

<section>
    <h2>1.1 Solucion Estratificada en TIC</h2>
    <p>
        Este modelo organiza los componentes de TI en niveles jerarquicos y separados. Su proposito es aislar procesos, simplificar la resolucion de fallos y mejorar el manejo de recursos.
    </p>
    <ol>
        <li><strong>Infraestructura Fisica:</strong> Servidores, procesadores y unidades de almacenamiento base.</li>
        <li><strong>Nivel de Abstraccion:</strong> Hipervisores o motores de emulacion.</li>
        <li><strong>Sistema Huesped:</strong> Entorno operativo virtual independiente.</li>
        <li><strong>Capa de Usuario:</strong> Software y aplicaciones finales ejecutadas por el cliente.</li>
    </ol>
</section>

<section>
    <section>
        <h2>1.1.a Virtualizacion por Interpretacion Pura</h2>
        <p>El metodo de emulacion mas tradicional y estricto.</p>
        <p><em>↓ Usa la flecha abajo para profundizar</em></p>
    </section>

    <section>
        <h2>Descripcion</h2>
        <p>
            Funciona como un intermediario que lee las instrucciones del sistema virtualizado una por una y las convierte en comandos que la CPU fisica puede procesar en el momento.
        </p>
    </section>

    <section>
        <h2>Caracteristicas</h2>
        <ul>
            <li><strong>Independencia de hardware:</strong> Capacidad de correr software creado para arquitecturas incompatibles con la maquina fisica.</li>
            <li><strong>Costo de procesamiento alto:</strong> La traduccion continua exige demasiados recursos de la CPU, provocando lentitud.</li>
            <li><strong>Desvinculacion completa:</strong> El entorno virtual esta completamente aislado de los componentes fisicos reales.</li>
        </ul>
    </section>

    <section>
        <h2>Casos de Uso</h2>
        <ul>
            <li>Investigacion de software antiguo o discontinuado.</li>
            <li>Analisis de codigo malicioso en entornos completamente seguros.</li>
            <li>Creacion de sistemas operativos desde cero.</li>
        </ul>
    </section>

    <section>
        <h2>Ejemplos</h2>
        <ul>
            <li><strong>QEMU:</strong> Sin utilizar aceleradores KVM.</li>
            <li><strong>Bochs.</strong></li>
            <li>Emuladores de hardware retro o consolas clasicas.</li>
        </ul>
    </section>
</section>

<section>
    <section>
        <h2>1.1.b Virtualizacion por Recompilacion Dinamica</h2>
        <p>Optimizacion del rendimiento mediante traduccion inteligente en tiempo de ejecucion.</p>
        <p><em>↓ Usa la flecha abajo para profundizar</em></p>
    </section>

    <section>
        <h2>Descripcion</h2>
        <p>
            El emulador toma segmentos completos de codigo, los traduce a las instrucciones nativas del procesador anfitrion y los almacena en una memoria cache. Asi, si el bloque de codigo se repite, se ejecuta instantaneamente sin volver a traducirse.
        </p>
    </section>

    <section>
        <h2>Caracteristicas</h2>
        <ul>
            <li><strong>Rapidez mejorada:</strong> Supera ampliamente a la interpretacion debido a la reutilizacion de codigo guardado en la cache (JIT).</li>
            <li><strong>Ajuste dinamico:</strong> Optimiza el flujo de instrucciones mientras la aplicacion esta funcionando.</li>
            <li><strong>Arquitectura compleja:</strong> Requiere un desarrollo de software avanzado para predecir y traducir los bloques eficientemente.</li>
        </ul>
    </section>

    <section>
        <h2>Casos de Uso</h2>
        <ul>
            <li>Capas de compatibilidad entre diferentes arquitecturas de CPU.</li>
            <li>Maquinas virtuales de lenguajes de programacion.</li>
            <li>Entornos de virtualizacion de escritorio.</li>
        </ul>
    </section>

    <section>
        <h2>Ejemplos</h2>
        <ul>
            <li><strong>Rosetta 2</strong> en ecosistemas macOS.</li>
            <li>Motor TCG de <strong>QEMU</strong>.</li>
            <li>Entornos de ejecucion como ART (Android Runtime) o la JVM.</li>
        </ul>
    </section>
</section>

<section>
    <section>
        <h2>1.1.c Virtualizacion por Hipervision (Bare Metal)</h2>
        <p>La base indiscutible de la infraestructura de nube y servidores empresariales.</p>
        <p><em>↓ Usa la flecha abajo para profundizar</em></p>
    </section>

    <section>
        <h2>Descripcion</h2>
        <p>
            Un hipervisor de Tipo 1 se despliega directamente sobre los componentes fisicos del servidor. No requiere de un sistema operativo base, ya que el mismo administra y distribuye los recursos de hardware hacia las multiples maquinas virtuales.
        </p>
    </section>

    <section>
        <h2>Caracteristicas</h2>
        <ul>
            <li><strong>Latencia minima:</strong> Ejecucion sumamente cercana al nivel nativo del procesador, maximizando el rendimiento.</li>
            <li><strong>Dependencia de hardware:</strong> Necesita que la CPU tenga tecnologias de virtualizacion integradas de fabrica (Intel VT-x o AMD-V).</li>
            <li><strong>Aislamiento robusto:</strong> Provee alta seguridad al separar completamente las maquinas virtuales a nivel estructural.</li>
        </ul>
    </section>

    <section>
        <h2>Casos de Uso</h2>
        <ul>
            <li>Implementacion de infraestructuras de Cloud Computing (IaaS).</li>
            <li>Administracion de centros de datos corporativos.</li>
            <li>Consolidacion masiva de servidores para ahorro de energia y espacio.</li>
        </ul>
    </section>

    <section>
        <h2>Ejemplos</h2>
        <ul>
            <li><strong>VMware vSphere / ESXi.</strong></li>
            <li><strong>Proxmox VE.</strong></li>
            <li><strong>Microsoft Hyper-V Server.</strong></li>
        </ul>
    </section>
</section>

<section>
    <h2>Comparacion de Modelos</h2>
    <table>
        <thead>
            <tr>
                <th>Tecnologia</th>
                <th>Velocidad</th>
                <th>Flexibilidad</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Interpretacion Pura</td>
                <td>Muy Lenta</td>
                <td>Extrema (Multi-plataforma)</td>
            </tr>
            <tr>
                <td>Recompilacion Dinamica</td>
                <td>Aceptable a Rapida</td>
                <td>Alta</td>
            </tr>
            <tr>
                <td>Hipervision (Bare Metal)</td>
                <td>Rendimiento Optimo</td>
                <td>Restringida a CPU compatible</td>
            </tr>
        </tbody>
    </table>
</section>

<section>
    <h2>Resumen Final</h2>
    <ul>
        <li>Cada estrategia de virtualizacion resuelve un problema distinto en la industria TI.</li>
        <li>La <strong>Interpretacion</strong> es ideal para garantizar compatibilidad absoluta y analisis a bajo nivel.</li>
        <li>La <strong>Recompilacion</strong> brinda una solucion rapida para software de usuario y entornos de transicion de hardware.</li>
        <li>La <strong>Hipervision Bare Metal</strong> es la columna vertebral tecnica para el procesamiento de datos y despliegues a nivel empresarial.</li>
    </ul>
</section>
