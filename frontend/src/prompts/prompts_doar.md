Tu misión es diseñar la interfaz de usuario "position" para gestionar visualmente los candidatos de una posición específica utilizando un tablero Kanban. La interfaz debe permitir ver y mover tarjetas de candidatos entre columnas que representan diferentes fases del proceso de contratación. Tu diseño debe cumplir con los siguientes requerimientos y utilizar los endpoints de API disponibles para su funcionamiento.

- **Visualización y diseño:**
  - Muestra el título de la posición en la parte superior con una flecha para regresar al listado de posiciones.
  - Incluye tantas columnas como fases del proceso de contratación.
  - Sitúa cada tarjeta de candidato/a en la fase correspondiente, mostrando el nombre completo y la puntuación media del candidato.
  - Optimiza la vista para dispositivos móviles mostrando las fases en vertical.

- **Datos y funcionalidad:**
  - Usa el endpoint `GET /positions/:id/interviewFlow` para obtener el título de la posición y las fases del proceso de contratación.
  - Usa el endpoint `GET /positions/:id/candidates` para listar candidatos, fases actuales y puntuaciones.
  - Usa el endpoint `PUT /candidates/:id/stage` para actualizar la fase de un candidato al arrastrar su tarjeta a otra columna.

# Steps

1. **Recuperar Información Inicial:**
   - Utiliza `GET /positions/:id/interviewFlow` para cargar el título de la posición y las fases del proceso.
   - Muestra el título con una flecha de regreso en la parte superior.

2. **Cargar y Mostrar Candidatos:**
   - Utiliza `GET /positions/:id/candidates` para listar candidatos actuales.
   - Organiza los candidatos en tarjetas dentro de las columnas correspondientes a su fase.

3. **Interacción de Usuario:**
   - Implementa la funcionalidad de arrastrar y soltar para mover las tarjetas de candidatos entre columnas.
   - Al mover un candidato, usa `PUT /candidates/:id/stage` para actualizar su fase en el proceso de contratación.

4. **Adaptación Móvil:**
   - Asegúrate de que las columnas se vean verticalmente en dispositivos móviles para ocupar todo el ancho.

# Output Format

El diseño y funcionalidad deben estar visibles a través de una interfaz tipo kanban, mostrando columnas para cada fase y tarjetas para cada candidato. Asegúrate de que los datos se actualicen dinámicamente al cambiar las fases de los candidatos.

# Notes

- Asegúrate de manejar cualquier error del API de forma adecuada.
- Ten en cuenta que la estructura global de la página (menú superior, footer) ya existe, así que concéntrate en el contenido central.
- Considera las mejores prácticas de usabilidad para la interacción de arrastrar y soltar, especialmente en dispositivos táctiles.

Optimiza los recursos web minimizando y comprimiendo archivos CSS y JavaScript. Utiliza imágenes optimizadas para la web y considera técnicas como los *image sprites* para reducir las solicitudes HTTP.

- Comprime los archivos CSS y JavaScript para disminuir los tiempos de carga.
- Usa herramientas o bibliotecas de minificación para eliminar datos innecesarios sin afectar la funcionalidad.
- Implementa formatos de imagen optimizados (por ejemplo, WebP) para una carga más rápida.
- Considera convertir múltiples archivos de imágenes individuales en una sola hoja de *image sprite*.
- Aplica estrategias de carga y almacenamiento en caché para mejorar el rendimiento y la carga de recursos.

Optimiza los recursos web implementando técnicas modernas de optimización para mejorar el rendimiento y reducir los tiempos de carga.

- Implementa una **CDN** para recursos estáticos y reduce los tiempos de carga sirviendo recursos desde ubicaciones distribuidas en la red.
- Utiliza **HTTP/2** para mejorar la velocidad de transferencia de recursos mediante la multiplexación de múltiples solicitudes en una sola conexión.
- Configura encabezados de caché apropiados en el servidor backend para aprovechar el almacenamiento en caché del navegador.
- Utiliza imágenes **WebP** con retrocompatibilidad a formatos tradicionales como JPEG/PNG para optimización de imágenes.
- Implementa **lazy loading** para componentes que no sean visibles inmediatamente al cargar la página, posponiendo su carga hasta que sean necesarios.

# Pasos

1. **Configuración de CDN**: Selecciona y configura un proveedor de CDN para alojar recursos estáticos, reduciendo la latencia y mejorando el tiempo de carga.
2. **Utilización de HTTP/2**: Configura el servidor para habilitar **HTTP/2** y permitir descargas paralelas para un mejor rendimiento.
3. **Configuración de Caché**: Implementa encabezados de caché como **Cache-Control** y **ETag** en el servidor para optimizar las políticas de almacenamiento en caché.
4. **Optimización de Imágenes**: Convierte las imágenes al formato **WebP**, asegurando retrocompatibilidad con los formatos **JPEG/PNG** para navegadores no compatibles.
5. **Lazy Loading**: Implementa *lazy loading* para componentes no críticos usando métodos nativos o basados en bibliotecas.

# Formato de Salida

Proporciona un informe detallado que incluya:
- Técnicas y herramientas utilizadas para CDN, HTTP/2 y almacenamiento en caché.
- Reducciones en el tamaño de archivos, mejoras en los tiempos de carga y métricas de rendimiento.
- Desafíos encontrados y soluciones implementadas.
- Resumen de los resultados de pruebas funcionales y visuales después de la optimización.
