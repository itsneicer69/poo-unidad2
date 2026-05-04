# poo-unidad2

## Universidad Politécnica Salesiana

### Descripción

Este proyecto implementa un sistema de gestión de contenido audiovisual con las siguientes clases:

#### Clases Base:

- `ContenidoAudiovisual` (clase abstracta)

#### Clases de Contenido:

- `Pelicula` (extiende ContenidoAudiovisual)
- `SerieDeTV` (extiende ContenidoAudiovisual)
- `Documental` (extiende ContenidoAudiovisual)

#### Clases de Relación:

- `Actor` - Relacionada con Película (Asociación)
- `Temporada` - Relacionada con SerieDeTV (Composición)
- `Investigador` - Relacionada con Documental (Asociación)

### Relaciones Implementadas

1. **Actor ↔ Película (Asociación)**

   - Una película puede tener múltiples actores
   - Un actor puede participar en múltiples películas
   - Los actores pueden existir independientemente de las películas

2. **Temporada ↔ SerieDeTV (Composición)**

   - Una serie de TV está compuesta por temporadas
   - Las temporadas no pueden existir sin la serie
   - La eliminación de la serie elimina todas sus temporadas

3. **Investigador ↔ Documental (Asociación)**
   - Un documental puede tener múltiples investigadores
   - Un investigador puede trabajar en múltiples documentales
   - Los investigadores pueden existir independientemente de los documentales

### Estructura del Proyecto

```
poo_unidad2/
├── src/
│   ├── uni1a/
│   │   ├── ContenidoAudiovisual.java
│   │   ├── Pelicula.java
│   │   ├── SerieDeTV.java
│   │   ├── Documental.java
│   │   ├── Actor.java
│   │   ├── Temporada.java
│   │   └── Investigador.java
│   └── poo/
│       ├── PruebaAudioVisual.java
│       └── PruebaRelaciones.java
└── README.md
```

### Compilación y Ejecución

#### Requisitos:

- Java JDK 8 o superior
- Terminal o línea de comando

#### Pasos para compilar:

1. Abrir terminal en la carpeta raíz del proyecto
2. Ejecutar el comando de compilación:
   ```bash
   javac -d . src/uni1a/*.java src/poo/*.java
   ```

#### Pasos para ejecutar:

1. Ejecutar la clase de prueba principal:

   ```bash
   java poo.PruebaRelaciones
   ```

2. O ejecutar la clase de prueba original:
   ```bash
   java poo.PruebaAudioVisual
   ```

### Características de las Clases

#### Actor

- Atributos: nombre, apellido, edad, nacionalidad, especialidad
- Métodos: getters/setters, mostrarInformacion(), getNombreCompleto()

#### Temporada

- Atributos: número de temporada, número de episodios, duración promedio, fechas
- Métodos: gestión de episodios, cálculo de duración total, mostrarInformacion()

#### Investigador

- Atributos: nombre, apellido, especialidad, institución, años de experiencia, título académico
- Métodos: getters/setters, mostrarInformacion(), getCredenciales()

### Ejemplo de Uso

El archivo `PruebaRelaciones.java` contiene ejemplos completos de cómo usar todas las relaciones implementadas, incluyendo:

- Creación de actores y asociación con películas
- Creación de temporadas y composición con series de TV
- Creación de investigadores y asociación con documentales

### Notas de Implementación

- Se utilizan `List<Actor>`, `List<Temporada>` y `List<Investigador>` para manejar las relaciones uno-a-muchos
- Las clases incluyen métodos para agregar, eliminar y mostrar las entidades relacionadas
- Se mantiene la consistencia en el diseño y la documentación del código
