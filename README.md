# Gantt Chart Extractor

Este es un extractor de diagramas Gantt que permite cargar y analizar archivos PDF y MPP (Microsoft Project) para extraer información sobre tareas y sus cronogramas.

## Características

- Carga de archivos PDF y MPP
- Extracción automática de tareas con sus fechas
- Sistema de filtrado avanzado
- Búsqueda por palabras clave
- Guardado y carga de filtros personalizados
- Visualización jerárquica de tareas
- Interfaz gráfica intuitiva

## Requisitos

- Python 3.7+
- Java JDK 8+ (para el procesamiento de archivos MPP)
- Las siguientes bibliotecas de Python:
  - PySide6
  - pdfplumber
  - jpype
  - mpxj

## Instalación

1. Clona este repositorio:
```bash
git clone https://github.com/tu-usuario/gantt-chart-extractor.git
```

2. Instala las dependencias:
```
   **Opción 1 - Instalación directa:**
   ```bash
   pip install PySide6 pdfplumber jpype1 mpxj
   ```

   **Opción 2 - Usando requirements.txt:**
   ```bash
   pip install -r requirements.txt
```

3. Asegúrate de tener configurado JAVA.

## Uso

1. Ejecuta el programa:
```bash
python file_gui.py
```

2. Usa los botones "Cargar PDF" o "Cargar MPP" para abrir archivos.

3. Utiliza las barras de búsqueda y filtro para encontrar tareas específicas:
   - Buscador: búsqueda general de términos
   - Incluir palabras: términos que deben estar presentes
   - Excluir palabras: términos que no deben aparecer

4. Puedes guardar y cargar filtros personalizados usando los botones correspondientes.

## Estructura del Proyecto

- `file_gui.py`: Interfaz gráfica principal
- `pdf_extractor.py`: Manejo de archivos PDF
- `mpp_extractor.py`: Manejo de archivos MPP
- `filter_util.py`: Utilidades de filtrado
- `loading_animation_widget.py`: Widget de animación de carga

## Licencia

[MIT License](LICENSE)

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue primero para discutir los cambios que te gustaría hacer.

---
Para más información o reportar problemas, por favor crea un issue en el repositorio.
