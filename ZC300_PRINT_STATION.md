# Estación de impresión Zebra ZC300

La aplicación usa por defecto el formato físico admitido por la ZC300:
**CR80 horizontal, 85.60 × 53.98 mm**. La opción anterior de 2.5 × 3 in no
corresponde al alimentador de tarjetas de este modelo.

## Preparar la impresora

1. Instala el controlador oficial de Zebra para la ZC300.
2. Define la ZC300 como impresora predeterminada del sistema.
3. En las preferencias del controlador selecciona:
   - tarjeta CR80 / ISO ID-1;
   - orientación horizontal;
   - una cara, salvo que la estación use una ZC300 dúplex;
   - escala 100 % y sin márgenes adicionales.
4. Imprime primero una tarjeta de prueba desde el controlador para confirmar
   orientación, cinta y alineación.

## Quitar la vista previa de Chrome

La página no puede activar impresión silenciosa por sí misma. En una estación
administrada, configura la política de Chrome `SilentPrintingEnabled` en
`true`. Chrome enviará `window.print()` inmediatamente a la impresora
predeterminada con sus opciones predeterminadas.

Documentación oficial:

- https://chromeenterprise.google/policies/#SilentPrintingEnabled
- https://chromeenterprise.google/policies/#PrintPreviewUseSystemDefaultPrinter

Después de aplicar las políticas, abre `chrome://policy`, pulsa **Reload
policies** y verifica que ambas aparezcan sin errores. Mantén la ZC300 como
impresora predeterminada: la impresión silenciosa no permite escoger otro
destino en cada trabajo.

## Operación

1. Abre la aplicación en Chrome.
2. Confirma **Zebra ZC300 · CR80 horizontal** en Formato de impresión.
3. Carga el Excel o completa la etiqueta.
4. Pulsa **Imprimir ZC300**.

Con la política activa el trabajo sale directamente. Sin la política, Chrome
mostrará su vista previa normal; este comportamiento es intencional por
seguridad del navegador.
