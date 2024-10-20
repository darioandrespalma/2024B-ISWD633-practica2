# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.








### Comparación de Conocimientos Antes y Después de la Práctica

Antes de realizar esta práctica, mi conocimiento sobre la gestión y configuración de contenedores Docker era más básico y limitado a la ejecución simple de contenedores. No tenía una comprensión clara sobre temas como la gestión de redes, el uso de variables de entorno en contenedores, y cómo las aplicaciones complejas como WordPress y MySQL podían ser integradas y ejecutadas en conjunto en un entorno de contenedores. Además, mis habilidades en la manipulación de bases de datos desde la línea de comandos, y el uso de herramientas como pgAdmin4, estaban menos desarrolladas.

### Principales Aprendizajes Logrados

1. **Gestión de Redes en Docker:**
Aprendí cómo Docker utiliza redes virtuales para permitir la comunicación entre contenedores. Antes, no entendía claramente cómo Docker creaba estas redes, ni cómo los contenedores podían conectarse entre sí dentro de las mismas. Ahora puedo crear redes personalizadas (como redes de tipo `bridge`) y gestionar las conexiones entre contenedores, lo que me permite diseñar entornos de aplicación más complejos y organizados.

2. **Integración de Servicios:**
Aprendí a configurar y conectar servicios como MySQL y WordPress en diferentes contenedores, utilizando las redes Docker para que estos servicios puedan comunicarse entre sí sin exponer todos los puertos a nivel de host. Esto es esencial en la configuración de aplicaciones multi-contenedor, como las que se usan comúnmente en desarrollo y producción.

4. **Gestión de Bases de Datos en Contenedores:**
Ahora entiendo cómo manejar bases de datos dentro de contenedores, incluyendo la creación de bases de datos y tablas, así como la inserción y consulta de datos directamente desde el contenedor. Esto también incluyó la familiarización con herramientas de administración como `psql` y `pgAdmin`, lo que me permitió tener un mayor control sobre las operaciones dentro de contenedores de bases de datos.

### Solución a Problemas Presentados

Un problema clave que resolví fue la configuración incorrecta de las variables de entorno al ejecutar contenedores. Inicialmente cometí errores en la sintaxis del comando `docker run` (por ejemplo, usando `--e` en lugar de `-e`). Esto me ayudó a revisar más a fondo la documentación oficial y a entender cómo configurar correctamente las variables de entorno. Asimismo, en varias ocasiones, algunos contenedores no se ejecutaban correctamente debido a problemas de configuración de red o errores en los archivos de configuración de la base de datos. Estos obstáculos me llevaron a investigar más a fondo y a mejorar mi capacidad de resolución de problemas en tiempo real.

### Beneficio para mi Formación Profesional

Este ejercicio ha sido un salto significativo en mi formación, ya que me ha proporcionado las habilidades necesarias para trabajar con Docker en un entorno real. Ahora puedo orquestar servicios dentro de contenedores de manera más eficiente, lo que es fundamental en el desarrollo de aplicaciones modernas que requieren entornos portátiles y escalables. Además, estos conocimientos son altamente valorados en la industria del software, y haber resuelto problemas técnicos en un entorno de contenedores me ha dado la confianza para enfrentar desafíos similares en un entorno de producción profesional.











