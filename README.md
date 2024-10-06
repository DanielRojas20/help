Conexiones

Resolución del problema #123: Error al cargar los datos del usuario.
PR dependiente en el repositorio de backend: #456
Descripción
Este PR soluciona un error que provocaba que los datos del usuario no se cargaran correctamente al iniciar sesión. El problema se debía a una consulta mal formada en la base de datos. Se corrigió la consulta y se añadió un manejo de errores para mejorar la experiencia del usuario en caso de que la carga falle.

Pruebas
Se realizaron pruebas unitarias para verificar que la consulta de datos ahora funciona correctamente. También se probaron los casos de error, asegurando que se muestre un mensaje adecuado al usuario si la carga falla. Las pruebas se ejecutaron usando cargo xtask test.

<!-- ¡Gracias por presentar! El archivo de codeowners solicitará automáticamente revisiones de los equipos apropiados. Después de obtener una revisión y haber abordado cualquier comentario, vuelve a solicitar explícitamente una revisión a la persona(s) que revisó tus cambios. Esto asegurará que se vuelva a agregar a su cola de revisión, ¡no nos estás molestando! -->
Lista de verificación

 Ejecutar cargo fmt.
 Ejecutar cargo clippy. Si es aplicable, agregar:
 --target wasm32-unknown-unknown
 --target wasm32-unknown-emscripten
 Ejecutar cargo xtask test para ejecutar pruebas.
 Agregar el cambio a CHANGELOG.md. Consulta las instrucciones simples dentro del archivo.
