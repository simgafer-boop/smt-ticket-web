# SMT Ticket — Página para generar billete desde un QR

Esta carpeta contiene una página web estática para que el pasajero escanee un QR dentro del bus, elija **1,20€** o **1,80€**, y **descargue el billete** con fecha y hora actual, el **logo SMT** arriba y el texto **"bon voyage"** abajo.

## Cómo usar
1. Coloca tu logo oficial como `logo_smt.png` (reemplaza el placeholder incluido).
2. Sube esta carpeta a tu hosting (por ejemplo: SharePoint/OneDrive con enlace público, GitHub Pages, o cualquier servidor web).
3. Imprime un QR que apunte a la URL pública, por ejemplo: `https://TU-DOMINIO/ticket/`.
4. (Opcional) Puedes crear 2 QR con preselección de precio:
   - `https://TU-DOMINIO/ticket/?p=1.20`
   - `https://TU-DOMINIO/ticket/?p=1.80`

## Flujo para el pasajero
1. Escanea el QR del bus.
2. Selecciona el precio del billete.
3. Pulsa **Generar billete**.
4. Pulsa **Descargar / Imprimir** y elige **Guardar como PDF** (o imprime).

## Formato de impresión
- Tamaño pensado para ticket: **80mm x 140mm**.
- También se adapta en pantalla; en móvil se recomienda guardar como PDF.

## Validación
- El billete incluye una referencia única `SMT-<epoch>-<rnd>` generada localmente. Si deseas validación online, añade un backend que registre esa referencia.

— Generado el 2026-02-16 15:15:30
