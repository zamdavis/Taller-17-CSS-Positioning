# Taller de Posicionamiento en CSS

![Resultado](/images/result.png)

Autor: Eduardo Oviedo Blanco

Para usar este taller efectivamente, clone el código en su ambiente local.
```
git clone https://github.com/edWAR6/CSS-Positioning-Workshop.git
```
Si desea subir el taller en su repositorio personal.
Cree un repositorio en su perfil, luego:
```
git remote set-url origin https://github.com/<tu usuario>/CSS-Positioning-Workshop.git
```

> El nombre del repositorio puede cambiar. Siga las instrucciones y guarde sus cambios.

## Instrucciones

1. Agregue la siguiente propiedad al selector `#div-1`.
```
#div-1 {
  position:static;
}
```
> La posición estática es el valor por defecto de la propiedad. Generalmente no se indica, a menos de que > se desee "reiniciar" su valor por defecto.

2. Modifique el tipo de posición y agregue valores para cambiar su ubicación.
```
#div-1 {
  ...
  position:relative;
  top:20px;
  left:-40px;
}
```
> Los cambios en la posición son relativos a su punto de origen.
> El espacio original y la ubicación de los elementos adyacentes son mantenidos.

3. Observe el resultado.

4. Borre los cambios hechos en `#div-1` y agregue las siguientes propiedades al selector `#div-1a`.
```
#div-1a {
  position:absolute;
  top:0;
  right:0;
  width:200px;
}
```
> Un elemento con posición absoluta se ubicará según su elemento padre.
> El elemento padre será cualquier elemento que lo contenga que **no** tenga posición estática (`position:static;`).
> En caso de que no exista un elemento padre, el elemento absoluto se posicionará según el *viewport*.

5. Observe el resultado.

6. Borre los cambios hechos a `#div-1` y `#div-1a`. Modifique los siguientes selectores para lograr una posición absoluta dentro de un contenedor relativo.
```
#div-1 {
  position:relative;
}
```
```
#div-1a {
  position:absolute;
  top:0;
  right:0;
  width:200px;
}
```
> Observe cómo ahora el padre de `div-1a` es `div-1`. Esto se debe a que la posición del padre no es estática.
> `div-1` se mantiene en su lugar porque no hay propiedades que cambien su ubicación.

7. Puede ahora también hacer *layouts* usando esta técnica.
```
#div-1 {
  position:relative;
}
```
```
#div-1a {
  position:absolute;
  top:0;
  right:0;
  width:50%;
}
```
```
#div-1b {
  position:absolute;
  top:0;
  left:0;
  width:50%;
}
```
> Note como sin embargo esto hace que el siguiente contenido quede debajo de las columnas.

8. Una manera de solucionar esto es asignando un alto fijo al contenedor.
```
#div-1 {
  ...
  position:relative;
  height:250px;
}
```
> Sin embargo el elemento `div-1c` aun está debajo de las columnas y si el contenido de las columnas cambia, el resultado no será bueno.

## Conclusión

Existen varias maneras de hacer *layouts* con CSS, si bien esta no es la mejor, ayuda mucho saber cómo funciona y le puede ayudar a colocar elementos efectivamente.
