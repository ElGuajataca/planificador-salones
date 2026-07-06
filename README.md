# Planificador de Salones · Hotel El Guajataca

Herramienta interactiva para diseñar y presentar montajes de eventos a clientes en tiempo real. Dibuja los tres salones del hotel a escala real, con el inventario propio de mesas y sillas, y exporta planos profesionales con membrete para cotizaciones.

## Salones configurados (medidas reales)

| Salón | Medidas | Aforo | Configuración |
|---|---|---|---|
| **Yaitií** | 30'×15' + anexo 15'×8' | 50 | 2 secciones en L, mismo nivel |
| **Casabí** | 67'3"×35'7" + nivel sup. 57'6"×15' | 250 | 2 niveles, escalera a 15' del lado izq. (3'6") |
| **Asua** | Forma irregular · 2,600 ft² (útil ~2,210 ft²) | ~170 banquete · ~276 cóctel · ~315 teatro | 4 zonas según plano a escala (1/8"=1', jul 2026): área principal 56'11"×35'7", front desk 18'2"×11'5", ala derecha 14'6"×14'5", franja de entrada 31'8"×5' |

## Funciones

- **Montaje automático** — banquete, banquete + cabecera, teatro, cóctel y herradura (U), generados según el número de invitados.
- **Inventario real integrado** (orden YC-20240627MA) — 20 mesas redondas 150 cm, 40 rectangulares 180×60, 10 cóctel, mesa de novios, serpentinas, barras doradas, backdrops, etc. Con contador de uso por pieza y **alerta roja de alquiler** cuando un montaje excede el stock.
- **Selector de silla** — YC-SS30, YC-SS26, acrílica YC-A120 o chiavari dorada YC-A120G; queda impreso en el plano.
- **Control de aforo en vivo** — asientos sentados, cóctel de pie y alerta si se excede el máximo del salón.
- **Edición libre** — arrastrar para mover, doble clic para rotar 45°, duplicar, eliminar (tecla Delete).
- **Modo presentación** — pantalla limpia para mostrar al cliente en TV o tablet.
- **Exportar PNG** — plano con membrete del hotel, cliente, fecha, invitados y tipo de silla.
- **Guardar / cargar** montajes como archivos JSON (plantillas reutilizables por tipo de evento).

## Uso

No requiere instalación, servidor ni dependencias. Es un solo archivo HTML.

**Opción A — Local:** descargar `index.html` y abrirlo en cualquier navegador (Chrome, Edge, Safari).

**Opción B — Publicar con GitHub Pages (recomendado):**
1. Subir `index.html` y este `README.md` al repositorio.
2. En el repo: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
3. En 1-2 minutos queda en línea en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/` — accesible desde cualquier tablet o computadora del hotel, sin instalar nada.

## Mantenimiento

Todo se edita en `index.html`:

- **Medidas de salones** → bloque `SALONES` (metros; incluye zonas/niveles y posición de escalera).
- **Inventario, medidas y stock** → bloque `TIPOS` (agregar piezas nuevas es copiar una línea).
- **Colores y marca** → variables CSS en `:root` (verde lago, arena, dorado).

## Notas operativas

- El aviso "Alquilar: X" indica cuánto equipo adicional necesita un evento **antes de cotizar**.
- Los elementos marcados "alquiler" (pista, tarima, DJ) no forman parte del inventario propio.
- Guardar montajes plantilla (boda 100, boda 150, corporativo, cóctel) por salón acelera las citas de ventas: cargar → personalizar → exportar.

---
Hotel El Guajataca · Quebradillas, Puerto Rico
