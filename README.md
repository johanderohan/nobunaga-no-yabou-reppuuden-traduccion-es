# Nobunaga no Yabō: Reppūden with Power-Up Kit — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/playstation/nobunaga-no-yabou-reppuuden)**.

Traducción al **español de España** de *Nobunaga no Yabō: Reppūden with Power-Up Kit*
(信長の野望・烈風伝 with パワーアップキット, PlayStation, Koei), el juego de estrategia del
periodo Sengoku que nunca salió de Japón.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu propia
copia para aplicarlo.

## Estado

Última versión: **[v1.0 — Primera publicación](../../releases/tag/v1.0)**.

| Parte | Estado |
|---|---|
| Guion (diálogos, sucesos históricos, avisos, tutorial, 950 biografías, glosario) | **6.980 mensajes** traducidos |
| Interfaz (menús, órdenes, fichas, listas, tarjeta de memoria) | **2.618 cadenas** traducidas |
| Nombres de generales, castillos, provincias, tesoros, cargos y rangos | traducidos (rōmaji y castellano) |
| Texto dentro de imágenes (botones, rótulos, iconos) | **518 rótulos** redibujados |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « »** |
| Revisión en partida | Parcial (ver abajo) |

Se ha hecho una fuente nueva de ancho variable con el mismo color y sombra que la
original, y se ha adaptado el juego para medir el texto en píxeles (botones centrados,
columnas alineadas, ventanas del ancho correcto). La pantalla de nombre permite
escribir con letras latinas.

El logotipo y los vídeos se quedan como en el original.

### Comprobaciones y trabajo pendiente

La traducción y su revisión se han hecho **con asistencia de IA, sin revisores humanos
independientes**.

Se ha comprobado en emulador (Beetle PSX), siempre desde arranque en frío:

- una partida de 15 años de juego (1546–1561) sin cuelgues, con sucesos, batallas
  delegadas y turnos de la CPU;
- partidas cortas con órdenes de gobierno, diplomacia, personal, formación de ejércitos,
  batallas campales y asedios, y guardar y cargar en la tarjeta de memoria;
- el tutorial completo y los 35 sucesos de la galería de sucesos históricos.

Una auditoría automática comprueba en la imagen montada los límites de memoria del
juego (búfer de mensajes, nombres, fuente, tablas y rutinas modificadas).

**No** se ha jugado una partida completa hasta la unificación, ni se ha probado en
consola real. Hay sucesos, ramas de diálogo y escenarios que no se han visto en
pantalla.

Limitaciones conocidas:

- Algunos rótulos están abreviados porque el hueco es el de dos kanji (unos 4 caracteres):
  «Arm.», «Obr.», «Sal.», «Ash.».
- En la comparativa de ejércitos de la batalla, las cifras del atacante van pegadas a los
  rótulos («700Sol.»): las posiciones son fijas y no se han movido en el código.
- En algunos mensajes con nombres variables la línea se corta un poco antes de tiempo
  (no se pierde texto).
- Las partidas de la versión japonesa y los datos de registro que ya tengas conservan sus
  nombres en japonés.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego japonés **Rev 1 (SLPM-86483)** en formato BIN/CUE de dos
   pistas. El parche solo modifica la **pista 1**; la pista 2 (audio) y el CUE no cambian.
3. **Comprueba que tu pista 1 es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Nobunaga no Yabou - Reppuuden with Power-Up Kit (Japan) (Rev 1) (Track 1).bin` |
   | Tamaño | 159.362.112 bytes |
   | MD5 | `aab72171b9ba0e99875c53f725ec5238` |

   ```bash
   md5sum "…(Track 1).bin"                    # Linux
   md5 "…(Track 1).bin"                       # macOS
   CertUtil -hashfile "…(Track 1).bin" MD5    # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche a la pista 1 con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "pista1 original.bin" parche.xdelta "pista1 traducida.bin"`
5. Para **v1.0**, comprueba que la pista 1 resultante tiene MD5 **`693f72b7e928d1224432bdce46709234`**.
6. Pon la pista traducida en lugar de la original (con el mismo nombre de archivo, o
   cambia el nombre en el CUE) junto a la pista 2 y el CUE originales, y carga el CUE en
   tu emulador.
7. Empieza una partida nueva.

Aplica cada versión sobre la **pista 1 original**, no sobre una ya traducida.

## Cambios por versión

### v1.0

- Primera publicación: guion, interfaz, nombres, tutorial y rótulos de *Reppūden with
  Power-Up Kit* en castellano.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación
alguna con Koei Tecmo. Aquí no se distribuye el juego ni ninguna parte de él: solo un
parche que modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo
hago.
