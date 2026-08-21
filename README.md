# CyberFinance AR — PoC

PoC WebAR con MindAR usando `targets.mind` generado a partir del toro.

## Qué hace

- Abre la cámara del celular.
- Reconoce la imagen impresa del toro.
- Superpone dos pulsos de luz sobre los ojos.
- La superposición queda anclada al target mientras movés el teléfono.

## Probar rápido

La cámara del navegador requiere HTTPS. No funciona correctamente abriendo `index.html` con `file://`.

### Opción A — GitHub Pages
1. Creá un repositorio nuevo.
2. Subí todo el contenido de esta carpeta a la raíz.
3. Settings → Pages.
4. Deploy from a branch → `main` / root.
5. Abrí la URL publicada desde el celular.

### Opción B — Netlify Drop
Arrastrá la carpeta completa al deploy manual de Netlify y abrí la URL HTTPS resultante.

## Test

1. Imprimí `target.png` o mostrala en otra pantalla.
2. Abrí la URL HTTPS desde el teléfono.
3. Tocá **Iniciar experiencia** y permití la cámara.
4. Apuntá a la imagen completa.
5. Los ojos deberían pulsar y seguir la perspectiva del target.

## Ajuste fino

Las posiciones actuales de los ojos están calibradas de forma aproximada sobre la imagen 1592×2048:

- izquierdo: `position="-0.148 0.219 0.01"`
- derecho: `position="0.100 0.219 0.01"`

Si al probarlo quedan unos milímetros corridos, modificá solo los valores X/Y de esas cuatro entidades (`a-circle` y `a-ring`).

En coordenadas MindAR, aumentar X mueve a la derecha y aumentar Y mueve hacia arriba.
