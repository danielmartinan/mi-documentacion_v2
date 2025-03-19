# Configuración del Entorno

## Configuración de VS Code

### Ajustes Básicos

1. Abre la paleta de comandos (Ctrl+Shift+P)
2. Escribe "Preferences: Open Settings (JSON)"
3. Añade las siguientes configuraciones:

```json
{
    "editor.formatOnSave": true,
    "editor.rulers": [80],
    "files.trimTrailingWhitespace": true,
    "files.insertFinalNewline": true,
    "python.linting.enabled": true
}
```

### Configuración de Python

1. Selecciona el intérprete de Python:
   - Ctrl+Shift+P
   - "Python: Select Interpreter"
   - Elige el intérprete de tu entorno virtual

2. Instala las herramientas de desarrollo:
   ```bash
   pip install pylint black
   ```

### Configuración de Git

1. Configura el editor por defecto:
   ```bash
   git config --global core.editor "code --wait"
   ```

2. Configura el merge tool:
   ```bash
   git config --global merge.tool vscode
   ```

## Configuración del Proyecto

### Estructura de Carpetas

```
proyecto/
├── docs/
│   ├── guia/
│   └── ejemplos/
├── src/
├── tests/
├── venv/
└── README.md
```

### Archivos de Configuración

1. `.gitignore`:
```gitignore
venv/
__pycache__/
*.pyc
.pytest_cache/
.coverage
```

2. `requirements.txt`:
```txt
pytest==7.4.0
black==23.7.0
pylint==2.17.4
```

## Configuración de Testing

1. Instala pytest:
   ```bash
   pip install pytest
   ```

2. Crea un archivo `conftest.py`:
```python
import pytest

@pytest.fixture
def sample_data():
    return {"test": "data"}
```

## Verificación de la Configuración

1. Ejecuta los tests:
   ```bash
   pytest
   ```

2. Verifica el formateo:
   ```bash
   black --check .
   ```

3. Verifica el linting:
   ```bash
   pylint src/
   ```

## Consejos Adicionales

- Usa snippets de VS Code para código repetitivo
- Configura atajos de teclado personalizados
- Mantén tus extensiones actualizadas
- Usa la integración de Git de VS Code 