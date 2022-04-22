# Notas

## Primer Entrega

+ Atuendo = combinacion de prendas que tienen sentido juntas. Ej: accesorio+remera+pantalon+zapatillas.
+ Requerimiento: Cargar prendas *validas* para luego armar atuendos.
    - La prenda tiene un tipo: (zapato, camisa, etc)
    - La prenda tiene categoria: (parte superior/inferior, calzado, accesorio).
    - La prenda tiene tela/material.
    - La prenda tiene color principal.
    - La prenda puede tener color secundario.
    - Evitar que haya prendas sin tipo, tela, categoria, o color primario.
    - Evitar que la categoria no se condiga con el tipo(remera no puede ser calzado por ejemplo.).
+ En el diagrama se modela al usuario solo con la accion agregarPrenda(Prenda) ya que acorde a los requerimientos es lo unico que se dice del usuario. Aun que tendria sentido que tenga un username u otros atributos que tienen sentido.
+ El tipo y la categoria de la prenda estan altamente acoplados. Uno es determinado por el otro, podria valer la pena tenerlos juntos y evitar validar por cada combinacion, pero no tiene sentido que sean una clase aparte porque no aportan cambios al comportamiento.
+ Voy a delegar la responsabilidad de validar que la prenda tenga los atributos necesarios y que estos sean validos al constructor cuando se cree en objeto.

## Segunda Entrega
