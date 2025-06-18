¿Qué ventajas observamos al automatizar pruebas con GitHub Actions?
Nos pareció muy útil que las pruebas se ejecuten solas cada vez que subimos cambios. Así no se nos pasa nada por alto y evitamos errores que podrían llegar a producción. Además, al estar todo integrado en GitHub, es más fácil de seguir y revisar los resultados.


¿Qué diferencia a GitHub Actions de Jenkins u otras herramientas CI?
Lo que más notamos es que GitHub Actions ya viene incorporado en GitHub, lo que simplifica mucho las cosas. En cambio, Jenkins necesita instalación, configuración y mantenimiento. Para proyectos pequeños o medianos, Actions nos pareció más rápido de poner en marcha y más fácil de entender.


¿Qué mejoras podríamos agregar a este pipeline?
Podríamos agregar pasos para:
	• Revisar la calidad del código con ESLint.
	• Verificar la cobertura de pruebas (con herramientas como jest --coverage).
	• Ejecutar los tests en varias versiones de Node.js.
	• Agregar notificaciones por correo o en un canal de Slack si alguna prueba falla.


¿Qué consideraciones de seguridad aplicaríamos en proyectos reales?
	• Mantener fuera del código cualquier clave o token, y en su lugar usar secrets de GitHub.
	• Usar herramientas como npm audit para revisar vulnerabilidades en dependencias.
	• Controlar quién puede modificar los workflows o hacer push directo al repositorio.
	• Revisar los pull requests antes de integrarlos y exigir que pasen por los tests.
