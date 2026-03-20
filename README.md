## February – April 2025 — Begginner Game Dev Course Content

- Unreal Engine  
- Terrain tool — creating and sculpting natural-looking terrain  
- Object modeling using primitives (cube, cone, sphere, etc.) and deformation  
- Materials — texture base with properties (roughness, metallic, specular)  
- Advanced modular terrain material — allows “painting” the terrain with different materials (dirt, gravel, rock) to simulate composition changes based on slope or other factors. Easily extensible with additional materials (sand, snow)

  <video controls width="600">
    <source src="./Videos/2025-08-23 14-52-31.mp4" type="video/mp4">
  </video>

- UI creation and coin counter system  
- Basic level design centered around the coin mechanic  

  <video controls width="600">
    <source src="./Videos/Coinlevel(1).mp4" type="video/mp4">
  </video>

- Menu design  

  <video controls width="600">
    <source src="./Videos/Cut 2025-04-09 19-09-58-00.00.05.425-00.00.25.626.mp4" type="video/mp4">
  </video>

- Destructible wall system with intact and destroyed states, collectible explosive item, and proximity detection. Equipped explosives can be triggered, starting a UI countdown and activating an explosion radius that affects the player  

  <video controls width="600">
    <source src="./Videos/2025-04-12 11-47-38-Cut-Merged-1744480392820(1)(1).mp4" type="video/mp4">
  </video>

---

## April – June 2025 — Completed "GrabShoot" with the following systems:

- Two map designs:
  - Parking lot with dense cover using cars and pillars, plus a more open central area  
  - Museum with emphasis on visual design and detailed decoration  

  <video controls width="600">
    <source src="./Videos/Cut-Merged-2025-08-22 19-14-011755911925841.mp4" type="video/mp4">
  </video>

  <video controls width="600">
    <source src="./Videos/Cut2025-08-22 19-15-21-00.00.00.000-00.00.26.000.mp4" type="video/mp4">
  </video>

- Modular health and damage system — attachable component with predefined functions for damageable objects, including healing, death, and current/max health checks  
- Advanced movement — sliding, variable jump height, and dive mechanics  
- Core mechanic: **Grab**
  - Allows grabbing an enemy as a hostage while retaining limited movement and the ability to shoot  
  - Releasing the button throws the enemy in the player’s movement direction  

  <video controls width="600">
    <source src="./Videos/Cut2025-08-21 13-12-20-00.01.57.000-00.02.09.500.mp4" type="video/mp4">
  </video>

- Weapon switching system with animations, model changes, and stat variations (fire rate, magazine size, damage, etc.)  
- Shotgun behavior: fires multiple pellets in a randomized spread pattern  
- Dynamic UI elements reflecting game variables (ammo count, reload progress, health)  
- Projectile system that triggers damage and detects critical hits (e.g., headshots) for increased damage  
- Healing pickups:
  - Spawn from defeated enemies  
  - Use physics impulse and settle into a rotating state to signal interactivity  

  <video controls width="200">
    <source src="./Videos/Recording 2025-08-22 192954.mp4" type="video/mp4">
  </video>

- Upgrade pickups:
  - Similar visual style to healing items (arrow-shaped)  
  - Upgrade menu tracks collected items and allows purchasing weapon modifications  

  <video controls width="200">
    <source src="./Videos/Recording 2025-08-22 193113.mp4" type="video/mp4">
  </video>

- AI enemies using behavior trees:
  - Detect player within vision cone  
  - Shoot and dynamically decide whether to approach or retreat  

- Wave-based game mode:
  - Enemy spawn points  
  - Variable enemy count per round  
  - On-screen remaining enemy counter  
  - Increasing aggression over time  
  - Healing and upgrade spawns between rounds  

  <video controls width="600">
    <source src="./Videos/Cut-Merged-2025-08-21 13-12-201755804515149.mp4" type="video/mp4">
  </video>

---

## Concepts Learned

- Linear interpolation for basic object animation  
- Visual scripting (nodes, branches, sequences, boolean logic)  
- Animation Blueprints (state machines, procedural poses)  
- Event Dispatchers — broadcasting events across game objects  
- Interfaces — defining reusable function contracts for different actors  
- Variable maps — e.g., mapping objects to counts for tracking instances  
- Camera scripting for main menu sequences  

  <video controls width="600">
    <source src="./Videos/Cut2025-08-21 13-12-20-00.00.00.000-00.00.09.000.mp4" type="video/mp4">
  </video>

- Save/load system  
- Importing external animations  
- Projectile visual effects  
- Action queuing — buffering input so actions trigger as soon as possible  

---

## Self-Learning

### June – July 2025

- Multiple implementations of **Coyote Jump** (jump forgiveness window after leaving a platform), improving responsiveness  

#### Recoverable weapon prototype
- A throwable axe:
  - First input throws it  
  - Second input recalls it along a forward arc, damaging anything in its path  
  - *Damage not yet implemented?*  
- Required understanding projectile and weapon systems from the first-person template  

---

#### Early work on ambitious project — *Mercury Hg successor: Gallium Ga*

<iframe width="664" height="374"
src="https://www.youtube.com/embed/nQjGGZ7cm7g"
allowfullscreen></iframe>

- Achieved:
  - Level tilting based on a pivot actor controlling all geometry  

- Side effects:
  - Test player (physics sphere) is launched upward instead of rolling naturally  
  - Ideal pivot should be directly below the player, but difficult with current setup  

- Alternative:
  - Simulate tilting using camera rotation and standard player movement  
  - May introduce physically inaccurate scenarios  

---

### August 2025

#### 2.5D Platformer Prototype (C++)

- Built as a way to revisit programming fundamentals  
- Using a modern IDE: JetBrains Rider (better autocomplete than default Visual Studio)  
- Base template: side-scroller with double jump and wall jump requiring movement toward the wall  
- Modified:
  - Wall jump no longer requires movement input, only facing direction → reduces mechanical difficulty  

  <video controls width="600">
    <source src="./Videos/Cut-Merged-2025-08-22 18-58-091755911014454 1.mp4" type="video/mp4">
  </video>

- Removed double jump  
- Implemented Coyote Jump  

  <video controls width="600">
    <source src="./Videos/Cut2025-08-22 18-33-43-00.00.00.500-00.00.03.000 1.mp4" type="video/mp4">
  </video>

- Dash mechanic:
  - Replaces double jump (or mapped separately)  
  - Allows jumping if used within the Coyote Jump window  

- Comparison: door opening 90° implemented in Blueprints vs C++  

  <video controls width="600">
    <source src="./Videos/Cut2025-08-22 19-06-00-00.00.16.000-00.00.20.500.mp4" type="video/mp4">
  </video>

- Enemy that gets crushed when landed on  

  <video controls width="600">
    <source src="./Videos/Cut2025-08-22 18-59-09-00.00.05.000-00.00.12.000.mp4" type="video/mp4">
  </video>

##Spanish version:
## Febrero a Abril 2025 - Contenidos del Curso para Principiantes en Desarrollo de Videojuegos
-  Unreal Engine
-  Herramienta de terreno - crear y moldear terreno de aspecto natural
- Modelado de objetos mediante uso de primitivas (cubo, cono, esfera, etc.) y deformación.
- Materiales - base de textura con propiedades (aspereza, metálico, especularidad)
- Material de terreno modular avanzado - permite "pintar" el terreno con diferentes materiales (tierra, grava, roca) para simular cambios de composición por inclinación u otros factores. Fácil implementación de materiales adicionales (arena, nieve).

	<video controls width="600">
		<source src="./Videos/2025-08-23 14-52-31.mp4" type="video/mp4">
	</video>
	
- Creación de interfaces de usuario y contador de monedas.
- Diseño de nivel básico alrededor de la mecánica de monedas.

	<video controls width="600">
		<source src="./Videos/Coinlevel(1).mp4" type="video/mp4">
	</video>

- Diseño de Menus
  
	<video controls width="600">
		<source src="./Videos/Cut 2025-04-09 19-09-58-00.00.05.425-00.00.25.626.mp4" type="video/mp4">
	</video>
	
- Muro destruible con estados completo y destruido, objeto de explosivo recogible y muro con caja de detección de proximidad y explosivos equipados para activar elemento de explosivo conectado y activado con cuenta regresiva en interfaz y radio de explosion que afecta al jugador

	<video controls width="600">
		<source src="./Videos/2025-04-12 11-47-38-Cut-Merged-1744480392820(1)(1).mp4" type="video/mp4">
	</video>

## Abril a Junio 2025 - Terminado "GrabShoot" con las siguientes mecánicas/sistemas:

- Creación de dos mapas - estacionamiento con multitud de cobertura entre carros y pilares con una zona central mas abierta. Museo con un énfasis en diseño estético y amplia decoración

	<video controls width="600">
		<source src="./Videos/Cut-Merged-2025-08-22 19-14-011755911925841.mp4" type="video/mp4">
	</video>
 	
	<video controls width="600">
		<source src="./Videos/Cut2025-08-22 19-15-21-00.00.00.000-00.00.26.000.mp4" type="video/mp4">
	</video>

- Sistema de daño y salud modular,  agrega un componente e implementa funciones predefinidas a otros objetos dañables. Funciones de curación, muerte y chequeo de salud actual y máxima.
- Movimiento avanzado - Deslizarse, salto de altura variable, cuerpo a tierra con impulso.
- Mecánica principal: Agarre - Permite tomar un enemigo como rehén mientras se permiten ciertos movimientos y disparar a otros enemigos, soltar el botón suelta al enemigo y lo impulsa en la dirección de movimiento del jugador.
  
	<video controls width="600">
		<source src="./Videos/Cut2025-08-21 13-12-20-00.01.57.000-00.02.09.500.mp4" type="video/mp4">
	</video>
	
- Sistema de cambio de arma con animación y cambio de modelo y estadísticas de tasa de disparo, tamaño de cargador, daño, etc.
- Disparar multiples balas al mismo tiempo en patrón aleatorio si se equipa una escopeta.
- Elementos dinámicos en pantalla que referencían variables del juego (Conteo de munición, progreso de recarga, salud).
- Los proyectiles activan el sistema de daño y detectan si colisionan con puntos críticos (cabeza) para aumento de daño.
- Objetos de curación con modelo llamativo que pueden aparecer de enemigos muertos con simulación física de un impulso hacia arriba, la cual se detiene a pocos momentos de tocar el suelo para dar lugar a una rotación sobre un eje para indicar que se puede recoger.

	<video controls width="200">
		<source src="./Videos/Recording 2025-08-22 192954.mp4" type="video/mp4">
	</video>

- Objetos de mejora - similares a los de curación con modelo de material similar y forma de flecha, un menú mantiene la cuenta de mejoras recogidas para comprar modificaciones a armas

	<video controls width="200">
		<source src="./Videos/Recording 2025-08-22 193113.mp4" type="video/mp4">
	</video>

- Enemigos con inteligencia artificial basada en arbol de comportamientos - detectar al jugador en el campo de vision y disparar en un cono hacia el mientras decide si se acerca o aleja del jugador para crear combate dinámico.
- Modo de juego de oleadas de enemigos - Marcadores de aparición de enemigos, número de enemigos por ronda variable, conteo en pantalla de enemigos restantes, Incremento de agresividad de enemigos al progresar, spawneo de objetos de curación y mejoras en el periodo de transición entre rondas.

  <video controls width="600">
  	<source src="./Videos/Cut-Merged-2025-08-21 13-12-201755804515149.mp4">
  </video>
	
Conceptos aprendidos:
- Interpolación lineal para animación básica de objetos de juego.
- Programación visual con nodos, branches, secuencias, operaciones booleanas.
- Blueprints de animación con maquinas de estado, poses para animación  procedural.
- Event Dispatchers - Funciones especiales que transmiten eventos que son recibidos en otros objetos de juego.
- Interfaces - objetos en los que se definen funciones para ser implementadas más tarde en el objeto especifico como el personaje jugable o enemigos.
- Mapas de variables - por ejemplo mapear cierto objeto del juego a un entero para mantener cuenta de cuantos objetos existen en el mapa en cada momento.
- Scripting de movimientos de la cámara para menú principal.

	<video controls width="600">
		<source src="./Videos/Cut2025-08-21 13-12-20-00.00.00.000-00.00.09.000.mp4" type="video/mp4">
	</video>
	
- Sistema de guardado y carga de estado del juego.
- Importación de animaciones externas.
- Proyectiles con efectos visuales.
- Action queuing - si el jugador presiona el botón de disparo por adelantado se queda en cola para cuando el disparo anterior termine.

## Aprendizaje por mi cuenta

### Junio - Julio 2025
- Varias implementaciones distintas de "Coyote Jump" - ventana de tolerancia a saltos hechos después de caer de una plataforma, mejora que tan responsivo se siente dar saltos.
- #### Prototipo de arma recuperable
	Un hacha que se lanza al atacar y en segundo presionar del botón regresa al jugador en una trayectoria que cruza por el frente del jugador y daña lo que toque. *Daño aun no implementado?*. Requirió aprender como funcionan los proyectiles y armas de la plantilla de primera persona.

- #### Inicios de proyecto ambicioso - Sucesor de Mercury Hg - Gallium Ga

	<iframe width="664" height="374" src="https://www.youtube.com/embed/nQjGGZ7cm7g?si=al-pDANOR2FGFjfU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen>
		
	</iframe>
	
	
	Logrado: inclinación del nivel basado en un actor de pivote puesto en el nivel del que toda la geometría depende.
	
	Efectos secundarios: el jugador de prueba (una esfera con fisicas) es impulsado hacia arriba cuando se inclina el nivel en vez de simplemente rodar. El punto de pivote necesitaría estar justo debajo del jugador, pero es difícil implementar con la configuración actual
	
	Alternativa: hacer la ilusión de que el nivel se mueve con rotaciones de la cámara y manejar el movimiento del jugador de la manera usual, podría generar escenarios físicamente incorrectos.

### Agosto 2025
#### Prototipo de juego de plataformas 2.5D en C++
	
Como una forma de retomar mis conocimientos de programación.
- Uso de un IDE moderno: JetBrains Rider, tiene excelente función de auto completado a diferencia del default Visual Studio.
- Plantilla por defecto: Side scrolling, cuenta con doble salto y salto en paredes que depende de que el jugador este caminando hacia la pared.
- Eliminada la necesidad de caminar hacia la pared, basta que el personaje este mirando hacia la pared, así es menos demanda mecánica al encadenar varios saltos.

	<video controls width="600">
		<source src="./Videos/Cut-Merged-2025-08-22 18-58-091755911014454 1.mp4" type="video/mp4">
	</video>
		
- Eliminado el doble salto.
- Coyote Jump implementado
 
    <video controls width="600">
        <source src="./Videos/Cut2025-08-22 18-33-43-00.00.00.500-00.00.03.000 1.mp4" type="video/mp4">
    </video>

- Dash, una aceleración en linea recta del jugador que remplaza el doble salto, o alternativamente en otra tecla/botón. Permite hacer un salto después de activarla si esta dentro de la ventana de coyote jump para más trasfondo.
	  
- Comparación de una puerta que se abre en 90 grados hecha en Blueprints y en C++.
 
    <video controls width="600">
        <source src="./Videos/Cut2025-08-22 19-06-00-00.00.16.000-00.00.20.500.mp4" type="video/mp4">
    </video>

- Enemigo que se aplasta al caer en su cabeza
 
	<video controls width="600">
		<source src="./Videos/Cut2025-08-22 18-59-09-00.00.05.000-00.00.12.000.mp4" type="video/mp4">
	</video>
