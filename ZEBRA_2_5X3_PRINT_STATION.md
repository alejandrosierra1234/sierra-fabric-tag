# Estación de impresión Zebra — etiqueta 2.5 × 3 in

La aplicación usa por defecto el tamaño solicitado: **2.5 × 3 pulgadas**
(**63.5 × 76.2 mm**) en orientación vertical.

## Preparar la impresora

1. Instala el controlador oficial de la impresora Zebra de etiquetas.
2. Define esa Zebra como impresora predeterminada del sistema.
3. Crea o selecciona en el controlador un tamaño de papel de 2.5 × 3 in
   (63.5 × 76.2 mm), orientación vertical, escala 100 % y sin márgenes.
4. Imprime una etiqueta de prueba para confirmar orientación y alineación.

## Quitar la vista previa de Chrome

La página no puede activar impresión silenciosa por sí misma. En una estación
administrada, configura la política de Chrome `SilentPrintingEnabled` en
`true`. Chrome enviará `window.print()` inmediatamente a la impresora
predeterminada con sus opciones predeterminadas.

Documentación oficial:

- https://chromeenterprise.google/policies/#SilentPrintingEnabled
- https://chromeenterprise.google/policies/#PrintPreviewUseSystemDefaultPrinter

Después de aplicar las políticas, abre `chrome://policy`, pulsa **Reload
policies** y verifica que ambas aparezcan sin errores.

## Operación

1. Abre la aplicación en Chrome.
2. Confirma **Zebra · 2.5 × 3 in** en Formato de impresión.
3. Carga el Excel o completa la etiqueta.
4. Pulsa **Imprimir Zebra**.

Con la política activa el trabajo sale directamente. Sin la política, Chrome
mostrará su vista previa normal.
