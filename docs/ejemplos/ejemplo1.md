# Ejemplo de Proyecto Básico

## Descripción

Este ejemplo muestra cómo crear un proyecto Python básico con documentación usando MkDocs.

## Estructura del Proyecto

```plaintext
ejemplo_proyecto/
├── docs/
│   ├── index.md
│   └── guia/
│       └── uso.md
├── src/
│   └── calculadora.py
├── tests/
│   └── test_calculadora.py
├── mkdocs.yml
└── requirements.txt
```

## Implementación

### Código Fuente

```python
# src/calculadora.py

class Calculadora:
    def sumar(self, a: float, b: float) -> float:
        """Suma dos números."""
        return a + b

    def restar(self, a: float, b: float) -> float:
        """Resta dos números."""
        return a - b

    def multiplicar(self, a: float, b: float) -> float:
        """Multiplica dos números."""
        return a * b

    def dividir(self, a: float, b: float) -> float:
        """Divide dos números."""
        if b == 0:
            raise ValueError("No se puede dividir por cero")
        return a / b
```

### Tests

```python
# tests/test_calculadora.py

import pytest
from src.calculadora import Calculadora

def test_sumar():
    calc = Calculadora()
    assert calc.sumar(2, 3) == 5
    assert calc.sumar(-1, 1) == 0

def test_restar():
    calc = Calculadora()
    assert calc.restar(5, 3) == 2
    assert calc.restar(1, 1) == 0

def test_multiplicar():
    calc = Calculadora()
    assert calc.multiplicar(2, 3) == 6
    assert calc.multiplicar(-2, 3) == -6

def test_dividir():
    calc = Calculadora()
    assert calc.dividir(6, 2) == 3
    assert calc.dividir(5, 2) == 2.5

def test_dividir_por_cero():
    calc = Calculadora()
    with pytest.raises(ValueError):
        calc.dividir(5, 0)
```

### Documentación

```markdown
# Guía de Uso

## Instalación

1. Clona el repositorio:
   
    ```bash
    git clone https://github.com/tu-usuario/ejemplo-proyecto.git
    cd ejemplo-proyecto
    ```

2. Crea un entorno virtual:

    ```bash
    python -m venv venv
    source venv/bin/activate  # En Linux/Mac
    venv\Scripts\activate     # En Windows
    ```

3. Instala las dependencias:

    ```bash
    pip install -r requirements.txt
    ```

## Uso

```python
from src.calculadora import Calculadora

# Crear una instancia
calc = Calculadora()

# Realizar operaciones
resultado = calc.sumar(5, 3)  # 8
resultado = calc.restar(10, 4)  # 6
resultado = calc.multiplicar(2, 3)  # 6
resultado = calc.dividir(10, 2)  # 5.0
```

## Tests

Para ejecutar los tests:

```bash
pytest
```

## Documentación

Para ver la documentación localmente:

```bash
mkdocs serve
```

## Despliegue

Para desplegar la documentación en GitHub Pages:

```bash
mkdocs gh-deploy
```

```

## Archivos de Configuración

### requirements.txt
```txt
pytest==7.4.0
mkdocs-material==9.2.8
```

### mkdocs.yml

```yaml
site_name: Ejemplo de Proyecto
theme:
  name: material
  features:
    - navigation.tabs
    - navigation.sections
    - navigation.expand
    - content.code.copy
```

## Pasos para Implementar

1. Crea la estructura de directorios:

   ```bash
   mkdir -p ejemplo_proyecto/{docs,src,tests}
   ```

2. Crea los archivos de código fuente y tests

3. Configura el entorno virtual:

   ```bash
   python -m venv venv
   source venv/bin/activate  # En Linux/Mac
   venv\Scripts\activate     # En Windows
   ```

4. Instala las dependencias:

   ```bash
   pip install -r requirements.txt
   ```

5. Ejecuta los tests:

   ```bash
   pytest
   ```

6. Inicializa MkDocs:

   ```bash
   mkdocs new .
   ```

7. Configura el archivo `mkdocs.yml`

8. Crea la documentación

9. Verifica localmente:

   ```bash
   mkdocs serve
   ```

10. Despliega en GitHub Pages:

    ```bash
    mkdocs gh-deploy
    ```

## Conclusión

Este ejemplo muestra cómo:
- Estructurar un proyecto Python
- Escribir tests
- Documentar código
- Crear documentación con MkDocs
- Desplegar en GitHub Pages 