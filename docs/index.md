<div style="display: flex; align-items: center; justify-content: center; margin-bottom: 30px;">
  <!-- Logo de tu equipo -->
  <img src="img/logo.jpg" alt="Logo del Equipo" width="150" style="border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.2);">
</div>

# Documentación de Producción Electrónica

Bienvenido a la bitácora de nuestro proyecto de Producción Electrónica. En este sitio web documentamos paso a paso todo el flujo de trabajo técnico necesario para el diseño, simulación y manufactura de placas de circuito impreso (PCBs). 

Desde la concepción lógica del diagrama eléctrico, pasando por la simulación del comportamiento de los componentes, hasta llegar a la generación de trayectorias (CAM) y el fresado físico de la placa, aquí encontrarás guías detalladas y los resultados de nuestras prácticas de laboratorio.

---

## Fases del Proyecto

<div class="grid cards" markdown>

-   📝 **[1. Diseño del Esquemático](esquematico.md)**
    
    ---
    
    Creación del diagrama lógico, selección de componentes y cableado de redes eléctricas.
    
    [Ver documentación ➔](esquematico.md)

-   📐 **[2. Editor de Placas (Layout)](editor-placas.md)**
    
    ---
    
    Diseño físico de la PCB, enrutamiento de pistas, posicionamiento 3D y reglas de diseño.
    
    [Ver documentación ➔](editor-placas.md)

-   💻 **[3. Mods CE (Manufactura CAM)](mods-ce.md)**
    
    ---
    
    Generación de trayectorias de fresado (archivos G-Code/RML) a partir de vectores para la máquina CNC.
    
    [Ver documentación ➔](mods-ce.md)

-   ⚙️ **[4. Operación MonoFab](monoFab.md)**
    
    ---
    
    Configuración, calibración de ejes (X, Y, Z) y uso de la fresadora Roland MonoFab SRM-20.
    
    [Ver documentación ➔](monoFab.md)

-   🔬 **[5. Simulación Multisim](multisim.md)**
    
    ---
    
    Análisis de barrido en DC (DC Sweep), osciloscopios virtuales y validación de circuitos rectificadores.
    
    [Ver documentación ➔](multisim.md)

-   📚 **[6. Referencias y Recursos](recursos.md)**
    
    ---
    
    Material de referencia complementario, hojas de datos (datasheets) y manuales de apoyo.
    
    [Ver documentación ➔](recursos.md)

</div>

---

## Nuestro Equipo de Trabajo
<p style="text-align: center; color: #888; margin-top: -10px;">Proyecto de Electrónica - IBERO Puebla</p>

<!-- Contenedor del equipo ajustado para 2 personas con descripciones -->
<div style="display: flex; justify-content: center; gap: 40px; text-align: center; margin-top: 30px; flex-wrap: wrap;">
  
  <!-- Carlos -->
  <div style="width: 300px; margin-bottom: 20px; background: rgba(0,0,0,0.2); padding: 20px; border-radius: 12px;">
    <img src="img/juan.jpg" style="width: 150px; height: 150px; object-fit: cover; border-radius: 50%; border: 4px solid #e53935; box-shadow: 0 4px 15px rgba(229, 57, 53, 0.4); margin: 0 auto;">
    <h3 style="margin-bottom: 5px; margin-top: 15px; font-size: 1.2em;">Juan Manuel Gaona Serrano</h3>
    <p style="color: #e53935; font-weight: bold; margin: 0; font-size: 0.95em;">Ingeniero Mecatrónico</p>
    <p style="color: #888; font-size: 0.85em; margin-top: 2px; margin-bottom: 15px;">19 años | Puebla, Puebla</p>
    <blockquote style="font-size: 0.9em; color: #bbb; border-left: 3px solid #e53935; text-align: left; padding-left: 15px; margin: 0; font-style: italic;">
      "La carrera es una de mis mayores formas de sentirme bien conmigo mismo y de lograr ser alguien en la vida."
    </blockquote>
  </div>

  <!-- Luis -->
  <div style="width: 300px; margin-bottom: 20px; background: rgba(0,0,0,0.2); padding: 20px; border-radius: 12px;">
    <img src="img/brandon.jpg" style="width: 150px; height: 150px; object-fit: cover; border-radius: 50%; border: 4px solid #e53935; box-shadow: 0 4px 15px rgba(229, 57, 53, 0.4); margin: 0 auto;">
    <h3 style="margin-bottom: 5px; margin-top: 15px; font-size: 1.2em;">Brandon Saul Ruvalcaba Perez Oliva</h3>
    <p style="color: #e53935; font-weight: bold; margin: 0; font-size: 0.95em;">Ingeniero Mecatrónico</p>
    <p style="color: #888; font-size: 0.85em; margin-top: 2px; margin-bottom: 15px;">19 años | Tamaulipas, Tabasco</p>
    <blockquote style="font-size: 0.9em; color: #bbb; border-left: 3px solid #e53935; text-align: left; padding-left: 15px; margin: 0; font-style: italic;">
      "Me gustan crear y aprender cosas nuevas."
    </blockquote>
  </div>

</div>
