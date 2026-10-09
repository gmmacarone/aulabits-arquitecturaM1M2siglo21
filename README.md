# AulaBits — Arquitectura en vivo

Juego multijugador en línea para los módulos 1 y 2 de Arquitectura de Computadoras.

## Uso rápido

1. Publicá `arquitectura-en-vivo.html` en un alojamiento HTTPS. Para GitHub Pages, renombralo a `index.html`, subilo a la raíz de un repositorio y activá **Settings → Pages → Deploy from a branch**.
2. El docente abre el enlace y elige **Soy docente**.
3. Comparte el código de seis dígitos o el QR.
4. Cada alumno abre el mismo enlace, elige **Soy estudiante**, ingresa el código y un nombre.
5. Cuando haya participantes, el docente inicia las 20 preguntas.
6. Al finalizar, puede exportar un CSV con posición, nombre, aciertos y puntaje.

## Requisitos

- Navegadores modernos con JavaScript y WebRTC.
- Conexión a Internet y acceso a `cdn.jsdelivr.net`, `api.fontshare.com` y al servicio de señalización de PeerJS.
- La pestaña del docente debe permanecer abierta: actúa como anfitrión de la partida.

## Alcance técnico

- La comunicación es de navegador a navegador mediante WebRTC; PeerJS Cloud se usa para señalización.
- No hay cuentas, contraseñas ni base de datos. El alumno se identifica con el nombre que escribe para esa sala.
- Los resultados viven en la memoria del navegador docente y se pierden al recargar o cerrar, salvo que se exporte el CSV.
- Algunas redes institucionales estrictas, VPN o firewalls pueden bloquear WebRTC. Probalo antes con la Wi‑Fi real del aula.
- Para uso intensivo o institucional, conviene alojar un PeerServer propio y añadir autenticación persistente.

## Prueba recomendada

Abrí el sitio publicado en una computadora docente y en dos celulares con redes diferentes. Creá una sala, ingresá ambos alumnos, respondé una ronda, verificá explicación, ranking y exportación CSV.
