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
+ Los requerimientos vienen mas por el lado de como se crea  cada objeto.
+ Tiene sentido posiblemente delegar la creacion, seria meter mucha logica al constructor, ademas de que si se complejiza mas la creacion vamos a estar en problemas para mantener el disenio despues.
+ Muchas cosas siguen tienendo sentido que esten juntas Ej: Trama y tela pero por ahora no se justifica juntarlos en una clase ya que siguen sin modificar el comportamiento de la prenda en si.
+ El borrador queda guardado en PrendaParcial. Podria guardarse en usuario tambien, pero en este caso seria tener algo duplicado sin motivo.
+ El hecho de no poder especificar una trama y que por defecto sea lisa puede ser implementada a traves de codigo. No va a ser visible en el diagrama de clases.
+ Relacionado al bonus:
    - En el caso del primer requisito: Se debera tener un tipo de atuendo que sea uniforme, para poder buscarlos despues por este tipo y poder mostrarlos como sugerencias.
    - En el caso del segundo requisito: Es dificil de determinar la mejor manera, pero podemos tener una subclase de atuendo que sea uniforme y en la creacion del objeto exigir que se cumpla esa regla (en el caso de que no sea la regla por defecto para todos los atuendos, que tendria sentido que lo sea).
    - En este caso, podriamos tener en nuestro sistema usuarios institucionales, que cada vez que creen un atuendo solo puedan crear el atuendo que fue configurado por un administrador.
