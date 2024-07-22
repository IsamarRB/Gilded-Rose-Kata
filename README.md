# Gilded Rose Inventory System

Bienvenido al sistema de inventario de Gilded Rose. Este sistema actualiza la calidad y el `sellIn` (días para vender) 
de los artículos diariamente según reglas específicas.

## Descripción del Proyecto

Este proyecto simula el sistema de inventario de la posada Gilded Rose. Los artículos en el inventario tienen 
propiedades `sellIn` y `quality` que se actualizan cada día según reglas específicas.

### Reglas de Actualización

- Todos los artículos tienen una propiedad `sellIn` que denota el número de días que tenemos para venderlo.
- Todos los artículos tienen una propiedad `quality` que denota cuán valioso es el artículo.
- Al final de cada día, el sistema decrementa ambos valores para cada artículo mediante el método `updateQuality()`.
- Una vez que ha pasado la fecha recomendada de venta (`sellIn` < 0), la `quality` se degrada al doble de velocidad.
- La `quality` de un artículo nunca es negativa.
- El "Queso Brie envejecido" (`Aged Brie`) incrementa su `quality` a medida que se pone viejo.
- La `quality` de un artículo nunca es mayor a 50, excepto para "Sulfuras" (`Sulfuras, Hand of Ragnaros`), que tiene 
una `quality` fija de 80 y no cambia.
- Una "Entrada al Backstage" (`Backstage passes`) incrementa su `quality` a medida que se acerca la fecha del concierto:
    - Si faltan 10 días o menos para el concierto, la `quality` se incrementa en 2 unidades.
    - Si faltan 5 días o menos, la `quality` se incrementa en 3 unidades.
    - Después del concierto, la `quality` cae a 0.
- Los objetos "conjurados" (`Conjured`) se degradan en calidad dos veces más rápido que los objetos normales.

## Estructura del Proyecto

- **Item.java**: Clase que representa un artículo en el inventario.
- **GildedRose.java**: Clase que contiene la lógica para actualizar los artículos del inventario.
- **GildedRoseTest.java**: Pruebas unitarias para verificar la correcta funcionalidad del sistema.

