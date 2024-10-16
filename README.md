# Ejemplo de Vulnerabilidad XSS

Este proyecto demuestra una vulnerabilidad de Cross-Site Scripting (XSS). La aplicación web muestra el input del usuario sin realizar la sanitización, lo cual permite la inyección de scripts maliciosos.

## Cómo reproducir la vulnerabilidad

1. Clonar el repositorio y abrir `index.html` en un navegador.
2. Ingresar `<img src="x" onerror="alert('XSS!')">` en el campo de texto y hacer clic en "Submit".
3. Se ejecutará un `alert` malicioso.

## Solución

Para evitar la vulnerabilidad XSS, se cambió `innerHTML` por `textContent` para que el input del usuario se trate como texto sin formato en lugar de HTML.

