# Renault Kwid 2027 — app de ventas por referido (PWA)

App estilo Toyota para presentar y vender el Renault Kwid 2027 (Intens, Iconic y Outsider) desde el celular, con código de referido para cobrar comisión por cliente.

**En vivo:** https://haroldco45.github.io/renault-kwid/

## Qué trae
- Portada con precio desde $56.190.000 y foto real del Kwid Outsider
- Selector de versión Intens / Iconic / Outsider con precio y equipamiento
- Sección "Hecho en Colombia" (planta Renault-Sofasa, Envigado)
- Galería de fotos reales con visor ampliado
- Video oficial del concesionario + 3 videos de YouTube (cargan solo al tocar)
- Seguridad de serie y ficha técnica completa, con enlace al PDF oficial
- Simulador de cuota (versión, inicial, plazo, tasa editable) que pasa la simulación al formulario
- Formulario de cotización / prueba de ruta que abre WhatsApp con el mensaje listo y un código de referido `VM-REN-AAMMDD-####` en hora Colombia
- No guarda datos de clientes; aviso Ley 1581 de 2012
- Instalable como app (manifest + service worker)

## Precios usados (sugeridos, modelo 2027, octubre de 2026)
| Versión | Precio |
|---|---|
| Intens | $56.190.000 |
| Iconic | $58.190.000 (confirmar con el concesionario) |
| Outsider | $60.190.000 |

Se cambian en el arreglo `VERSIONES` de `index.html`.

## Cuando el concesionario firme
En `index.html`, bloque `CONFIG` al inicio del script:
```js
aliado:{nombre:'Casa Británica',ciudad:'Caucasia',asesor:'Nombre del asesor',whatsapp:'57XXXXXXXXXX'}
```
Mientras `whatsapp` esté vacío, las solicitudes le llegan a Harold (311 770 0431).

## Fotos
Las fotos de la galería y el video oficial se cargan desde el sitio público del concesionario. Si alguna no carga, la app la oculta sola y sigue funcionando. La foto de portada (`carro.jpg`) va dentro del repo.

## Publicar en GitHub Pages
1. Crear el repo `renault-kwid` (todo en minúsculas) en la cuenta `haroldco45`.
2. Subir todos los archivos de esta carpeta a la raíz.
3. Settings → Pages → Branch `main`, carpeta `/ (root)`.

Desarrollada por Vibras Positivas HM — Derechos de Autor Reservados
