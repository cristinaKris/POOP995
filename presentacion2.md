---
marp: true
author: Karen Isidro
size: 4:3
theme: gaia
---
# Marp para presentaciones
Somos del grupo 1
Nuestro horario es de 7am a 9am
Miembros:
- Carolina Figueroa
- Jacqueline Castillo
- Cesar Hernandez
- Karen Isidro
---
## Caracteristicas
- Se pueden escoger temas y fondos de pantalla
para las presentaciones.
- Soporta caracteres UNICODE.
- Se puden escribir ecuaciones matemáticas.
- Se puede exportar a formato PDF

---
## Titulos y subtitulos
Inician con un símbolo numeral «#» seguido de un
espacio y el texto para título principal y
agregando dos o más numerales juntos -sin
espacios- los subtítulos correspondientes (hasta
un máximo de seis subniveles)
## Comentarios
Para insertar un comentario en marp se usa :
«<!— comentario —>»

---

## Enlaces web
Los hipervínculos los podemos declarar de forma implícita y explícita:

De manera implícita: si escribimos «http://» más un caracter cualquiera,se convierte en un enlace a la derecha en la ventana de visualización. 
De forma explícita: Un par de corchetes rectos (opcionales) donde colocaremos el texto del enlace y un par de paréntesis (curvos) donde colocaremos el enlace web en sí mismo.

---
## Agregando diapositivas
Se usan tres guiones seguidos al principio de una
línea, dejando una línea en blanco antes y después
Para agregar el número de diapositiva en la
esquina inferior derecha solo debemos agregar el
siguiente código

---
## Numerando diapositivas
Se usa la instrucción:
"< !-- page_number: true -->"
Las paginas seran enumeradaas desde la
dispositiva donde se coloco la instrucción y hasta
el final.
Si queremos que una diapositiva no sea numerada
le agregaremos a la instruccion anterior un
asterisco para indicar que se le aplique solo a esa
diapositiva.
"< !-- *page_number: true -->"

---

## Directivas
### «$theme» y «template»
Soporta plantillas predeterminadas, de manera
adicional con la directiva "template:invert" se
tiene una inversión en los colores.

---

### «footer».
Establece un pie de página ya sea en todas las
diapositivas o solo en la que le coloquemos la
directiva (usando un asterisco para volverla local)
< !--- footer : footter -->
<!--- footer : footter -->

---

### $size
Para la proporción tenemos «4:3» para monitores
normales y proyectores y, por otra parte «16:9»
para monitores «multimedia»
Esta directiva solamente es global, es
recomendable declararla al principio para un
orden efectivo.

---
 ### $width y $height.
px: píxeles por defecto.
Las siguientes unidades se colocan juntitas sin
espacios
cm: centímetros.
mm: milímetros.
in: pulgadas «inches».
pt: puntos.
pc: picas.

---

### «$prerender».
Hace un preproceso de las imágenes de fondo en el caso de que éstas sean muy grandes, aligera el proceso con una carga previa de datos.
<!– prerender: true –>

---
## Imagenes
Para insertar una imagen, colocamos incluyendo los paréntesis sin los corchetes ni se muestra la imagen. Dentro de los corchetes rectos colocamos el texto alterno.
Dentro de los paréntesis (curvos) pero fuera de las comillas dobles se coloca la direccion de la imagen (ademas de si se obtuvo por web o se encuentra dentro de la memoria).
Si se usa una de internet, entre la URL de la imagen y las comillas dobles se deja un espacio

---
### Imágenes de fondo.
En los corchetes rectos colocamos el comando [ bg]. Dentro de los corchetes rectos acompañando a «bg» más un espacio podemos colocar un procentaje para redimensionar la imagen e
incluso podemos colcoar varias imágenes siempre y cuando los porcentajes sumen 100%

---
## Ecuaciones Matematicas
Marp tiene un suplemento que debemos ingresar
entre par de símbolos de pesos. Cualquier texto
que escribamos lo representa tal cual pero si lo
antecedemos de cierta sintaxis comenzaremos a
escribir nuestras fórmulas

---
### Operadores

Si un texto lo antecedemos con un «_» tendremos
un subíndice.
Con «^» lo convertiremos en superíndice.
Para agrupar estos subíndices o superíndices los
encerramos entre llaves «{}»
Para multiplicar términos: «\cdot».
A «\cdot» le podemos agregar paréntesis para
agrupar más términos.
Para mostrar tres puntos suspensivos: «\cdots».
División: «\div».
Fracción: «\frac{}» -colocamos el numerador entre llaves y el denominador a continuación.
Sumatoria: «\sum» -la podemos combinar con superíndices y subíndices.
Raíz cuadrada: «\sqrt» más el número -o llaves, o paréntesis.
Paréntesis grandes, ideales para encerrar fracciones: «\Bigl(» y «\Bigl)».
Para representar integrales simples: «\int», dobles «\iint», triples «\iiint», integral de superficie «\oint».