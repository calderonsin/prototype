# Prototype Design Pattern

Copiar un objeto existente en vez de crear uno nuevo desde cero
Permite esconder la complejidad de crear nuevas instancias 
Esta técnica ahorra tiempo y recursos, sobre todo cuando la creación del objeto es un proceso pesado


Participantes del diseño por prototipos


1) Prototipo : El prototipo del objeto.
2)Registro de  prototipo : Es usado como un registro para tener todos los prototipos accesibles con un simple parámetro string
3) Cliente : Será el responsable de usar el registro de prototipos para acceder a las instancias del prototipo


Cuando usar el patrón de diseño prototipo

Cuando un sistema debe ser independiente de cómo se crean, se componen y representar sus productos
Cuando las clases a instanciar se especifican en tiempo de ejecución 

Ventajas:

Añadir y remover productos en tiempo de ejecución– Los prototipos permiten incorporar una nueva clase de producto concreto en un sistema simplemente registrando una instancia prototípica con el cliente. Eso es un poco más flexible que otros patrones de creación, porque un cliente puede instalar y eliminar prototipos en tiempo de ejecución.
Especifica nuevos objetos variando valores 
Especificar nuevos objetos variando estructura – Many applications build objects from parts and subparts. For convenience, such applications often let you instantiate complex, user-defined structures to use a specific subcircuit again and again.
Reduce subclases –   Factory Method produce una jerarquía de clases Creator que es paralela a la jerarquía de clases del producto. El patrón Prototype  permite clonar un prototipo en lugar de pedirle a un método de fábrica que haga un nuevo objeto. Por lo tanto, no necesita una jerarquía de clase Creator en absoluto.

Desventajas:

Exagerar para un proyecto que utiliza muy pocos objetos y / o no tiene un énfasis subyacente en la extensión de las cadenas de prototipos.
Cada subclase del prototipo debe implementar el método clone() el cual puede ser difícil de hacer, cuando la clase a clonar ya existe.
También puede ser difícil implementar clone() cuando hay objetos que no soportan copiar o tienen referencias circulares
