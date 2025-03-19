# Instalación y Configuración

## Requisitos del Sistema

Antes de comenzar, asegúrate de tener instalado:

- Python 3.7 o superior
- Git
- Visual Studio Code

## Instalación de Python

1. Descarga Python desde [python.org](https://www.python.org/downloads/)
2. Durante la instalación, marca la casilla "Add Python to PATH"
3. Verifica la instalación abriendo una terminal y ejecutando:
   ```bash
   python --version
   ```

## Instalación de Git

1. Descarga Git desde [git-scm.com](https://git-scm.com/downloads)
2. Sigue el asistente de instalación con las opciones por defecto
3. Verifica la instalación:
   ```bash
   git --version
   ```

## Instalación de Visual Studio Code

1. Descarga VS Code desde [code.visualstudio.com](https://code.visualstudio.com/)
2. Instala las siguientes extensiones:
   - Python
   - Git
   - Markdown Preview Enhanced

## Configuración Inicial

1. Configura tu identidad en Git:
   ```bash
   git config --global user.name "Tu Nombre"
   git config --global user.email "tu@email.com"
   ```

2. Crea un entorno virtual para tu proyecto:
   ```bash
   python -m venv venv
   ```

3. Activa el entorno virtual:
   - Windows:
     ```bash
     venv\Scripts\activate
     ```
   - Linux/Mac:
     ```bash
     source venv/bin/activate
     ```

## Verificación

Para verificar que todo está correctamente instalado:

1. Abre VS Code
2. Abre una nueva terminal
3. Ejecuta los siguientes comandos:
   ```bash
   python --version
   git --version
   code --version
   ```

Si todos los comandos se ejecutan sin errores, ¡estás listo para comenzar! 