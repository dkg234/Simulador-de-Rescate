# 🤖 Simulador de Rescate Autónomo en Zonas de Desastre

**Materia:** Robótica y Optimización  
**Alumno:** [Tu Nombre Completo]  
**Año:** 2026

## 📝 Descripción del Proyecto
Este proyecto consiste en el desarrollo de un simulador 2D interactivo de un robot (rover) de búsqueda y rescate autónomo. El agente debe navegar por un entorno desconocido y dinámico (afectado por derrumbes), esquivar obstáculos, gestionar su energía de manera eficiente y rescatar a múltiples víctimas, priorizando aquellas que se encuentran en estado crítico.

El simulador fue desarrollado íntegramente en **Python** con **Pygame** y compilado para su ejecución en navegadores web mediante **Pygbag (WebAssembly)**.

## 🎮 Jugar en Línea (Web)
Puedes probar el simulador directamente en tu navegador (PC o dispositivos móviles) haciendo clic en el siguiente enlace:

👉 **[¡Haz clic aquí para jugar al Simulador de Rescate!](https://dkg234.github.io/Simulador-de-Rescate/)**

*(Nota: En dispositivos móviles, se recomienda girar la pantalla en horizontal para una mejor experiencia. El juego cuenta con botones táctiles en pantalla).*

## 🛠️ Características Técnicas Implementadas

*   **Algoritmos de Búsqueda:**
    *   **A* (A-Star):** Utiliza heurística (Distancia Manhattan) para encontrar la ruta más corta, optimizando la exploración del mapa.
    *   **Dijkstra:** Algoritmo exhaustivo implementado como comparativa para demostrar la eficiencia de A*.
*   **Optimización de Rutas (TSP):** Cuando el robot detecta múltiples víctimas, utiliza el Problema del Viajante (*Traveling Salesperson Problem*) para calcular la ruta global más eficiente.
*   **Exploración de Fronteras (Frontier-based):** El robot explora eficientemente zonas desconocidas (niebla de guerra) dirigiéndose a los límites entre lo mapeado y lo no mapeado.
*   **Gestión Predictiva de Energía:**
    *   Modos de velocidad: *Turbo* (rápido, alto consumo), *Normal* y *Eco* (lento, bajo consumo).
    *   Cálculo de supervivencia: El robot aborta misiones de rescate si calcula que no tiene batería suficiente para ir y volver.
    *   Carga de oportunidad: Si se queda sin batería en campo, despliega paneles solares estáticos para recargar, siempre y cuando el terreno sea seguro.
*   **Triaje de Víctimas:** El robot diferencia entre víctimas estables y críticas (estas últimas tienen un temporizador de vida). Las críticas tienen prioridad absoluta.
*   **Reactividad y Evasión:** Si un derrumbe bloquea el camino, el robot recalcula la ruta en tiempo real o ejecuta una evasión local.

## 🕹️ Controles

**En PC (Teclado):**
*   `M` : Volver al Menú Principal.
*   `R` : Reiniciar la misión actual.
*   `1` : Cambiar al algoritmo A*.
*   `2` : Cambiar al algoritmo Dijkstra.
*   `Clic` : Interactuar con los menús y botones.

**En Móviles:**
*   Usa los botones táctiles ubicados en el panel inferior derecho de la pantalla.

## 💻 Tecnologías Utilizadas
*   **Lenguaje:** Python 3.12
*   **Motor Gráfico:** Pygame / Pygame-CE
*   **Compilación Web:** Pygbag (WebAssembly)

## 📂 Estructura del Entorno
*   🟩 **Base:** Punto de recarga de batería.
*   🟦 **Robot:** El agente autónomo (triángulo).
*   🟥 **Víctimas Críticas:** Tienen un temporizador de rescate.
*   🩷 **Víctimas Estables:** Sin límite de tiempo.
*   🟫 **Escombros:** Bloquean el paso y obligan a recalcular.
*   🟧 **Zonas de Peligro:** Consumen mucha batería al transitarlas.

---
*Este proyecto fue desarrollado como trabajo final para la materia de Robótica y Optimización.*
