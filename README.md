# Solis Falco Icons

Falco Icons es una fuente de iconos basada en SVG de ligaduras diseñada para el frontEnd y panel de administración de Solis.

Diseñada con Adobe Illustrator y ensamblada con FontForge. Usa una tabla de sustitución de glifos (GSUB) para almacenar todas las ligaduras.

<center>
<img src="./.img/readme/ligas_demo.gif">
</center>

Los iconos están basados en un documento de `100x100` pixeles, usando `8pt` de grosor para el trazo, las esquinas van redondeadas a `6px` y todos los documentos `.ai` incluyen unas guías para mantener el margen de `4pt`, para evitar que el trazo del icono desborde del documento.

En algunas esquinas complejas a `45º`, el trazo suele desbordar con los puntos de ancla, en este caso hay que realizar algunos ajustes.
De la misma forma ocurre con los segmentos que alcanzan los bordes del documento.


## Alineación del glifo
Los glifos deben ir alineados al borde izquierdo del icono en FontForge y el ancho se establece al límite derecho.

Las dimensiones del glifo equivalen al ancho del icono, es decir, no se alinea al centro, se ajusta al borde izquierdo del glifo y después se establece el ancho para que sea igual al del icono.
Esto evita que haya espacios innecesarios cuando se usen los iconos, así mejora la consistencia, si no parecería una fuente monoespaciada.

<center>
<img src="./.img/readme/readme_h_alignment.png">
</center>

Cuando el espaciado está bien establecido, la alineación del icono no tendrá esos espacios vacíos. Esto es especialmente útil a la hora de implementarlo en el frontEnd.

```HTML
<!-- Ejemplo de uso -->
<h1><span>remote_control</span> Remote Control</h1>
```

En este caso, no será lo mismo el espacio que hay inmediatamente después del cierre del `span`, que ese mismo espacio mas el que sobra del borde izquierdo del glifo.

## Documento base

En la carpeta de iconos hay un archivo llamado `base.ai`, este tiene las cuadrícula básica para empezar a diseñar.

Para diseñar un icono, primero hay que crear un documento de `100x100px` como se ha mencionado antes.
Establecer las guías de `4px` para cada borde, usar `8px` de ancho de trazo y asegurarse de redondear las esquinas necesarias a `6px`.
> La esquinas redondeadas influyen mucho en cómo se ve el icono, un diseño orgánico siempre será más agradable a uno con vértices angulados.