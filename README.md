# shaderProject

## Proyecto Parcial 1

El proyecto consiste en crear un shader y aplicarlo en un personaje 3D. 

### Contenido
Las herramientas principales fueron Unity y Visual Studio Code.
El shader cuenta con las siguientes características:
+ Un modelo de luz custom basado en Lambert con el sistema Wrap y Phong.
+ Mapa de textura principal y mapa de normales.
+ Efecto de horizonte (rim).
+ Control de la intensidad del mapa de normal.
+ Color principal (Albedo) para dar color a toda la iluminación.
+ Color (Phong color) para pintar el brillo del phong.
+ Técnica "Banded" para modificar el modelo de luz y una Ramp Texture de forma procedural.

### Desarrollo
Lo primero es descargar un modelo 3D en el cual se aplicará el shader, en este caso se utilizó el siguiente modelo: https://assetstore.unity.com/packages/3d/vehicles/free-hot-dog-truck-73014. Después se crea el proyecto en Unity de tipo 3D y un archivo Unlit shader, el cual contiene toda la programación. La estructura básica es el Shader con su nombre, las propiedades, el subshader, tags y cgprogram, es importante agregar el pragma para indicar que trabaje en la superficie. Los trabajos que se han llevado a cabo en el primer parcial de la materia Tópicos de Física sirvieron como base para el proyecto.
El sistema Wrap es el más sencillo y básico, sirve para añadir un fallOff, el cual es el encargado de controlar la caída de la sombra desde lo más claro a lo más oscuro. El Phong es la forma en la que se ve reflejada la luz en el modelo, consiste en añadir las variables: SpecularColor (color de la luz), SpecularPower (intensidad de la luz), SpecularGloss (amplitud del brillo), GlossSteps (agrandar los pasos de cada sección), las cuales sirven para calcular la Specularity. Para agregar el mapa de textura principal y mapa de normales, se necesitan variables de tipo 2D para que soporten la textura, y un rango para controlar la fuerza. El efecto de horizonte se logra añadiendo un color HDR para que tenga mejor definición y un rango para controlar la intensidad. La técnica Banded nos da un efecto visual en el que se pueden apreciar los diferentes tipos de sobra, y se puede controlar su difuminación mediante un slider. El Ramp Texture es de tipo 2D y es parecido al efecto Banded, ya que muestra las sombras en sus diferentes tonos de grises. 
