Link: [[Polymorphic Hierarchy.pdf]]

## Introduction

En el código suele haber muchos métodos que hacen lo mismo. Código repetido. Muchos getters y setters, initialization, instance creation.

## Reusing Method Descriptions

Da el ejemplo: ``printOn`` 
+ Menciona el uso de los comentarios de las clases que hereda porque todas hacen lo mismo en definitiva. Menciona `see superimplementor`
Un **subimplementor** debe:
+ Hacer lo mismo que el **superimplementor**
+ tener **mismo protocolo**
### One defining implementor

En una jerarquía, para cada mensaje debe haber una sola descripción (sino no sería polimórfico). Está en la superclase de la jerarquía. Hace ``subclassResponsibility``

> Da el ejemplo de Smalltalk, en donde una implementación de un método que tiene un solo parámetro más lo que hace es llamarlo. Solo hace falta saber que hace el otro

## Anatomy of a Method Description

+ Avoid rephrasing the method name
+ Si el nombre es por ejemplo ``productCode`` no ahce falta decir que devuelve eso, sino poner `Getter` o por el estilo.
+ _Method description_ para describir **todo** el método, no comentar lineas de código porque falto una abstracción 

>  The comment I would have included to explain the code becomes the method’s description.
## Purpose and implementation details

Method description
+ Purpose
	+ El qué hace. Reusable para todas las implementaciones de un método 
+ Implementation (opcional)
	+ El cómo lo hace. No es reusable ya que depende de la implementación

> In every implementor except the topmost one, change the purpose comment to “See superimplementor” since the purpose is always the same



## Description Reuse for Polymorphism

>When I create a subclass, I don’t just think about how the class should work, I think about how it should differ from its superclass.

+ The subclasses may add additional behavior

Ejemplo de reuso: _Collection_ marca que debe hacer aunque todos los demás deben ser diferentes

>The subimplementor should have the same purpose as the superimplementor, but it should do it different

## Purpose is polymorphic

+ Polimorficos: todos los **implementors** de una jerarquía tienen el mismo proposito
+ No nos interesa como está implementado, solo que hace

## Defining polymorphism

+ Para ser polimórficos, los **nombres** deben:
	+ ser **iguales**
	+ deben **comportarse de la misma forma**. 
		+ Generar los mismos **side effects**
		+ Return the same type of result

Las clases no suelen tener la misma interfaz, sino que un **core interface**
+ Interfaz que comparten varias clases de uso intercambiable.



## Making a Hierarchy Polymorphic
+ Menciona que `See superimplementor` lo hizo empezar a pensarlos de forma polimórfica.
+ Métodos más polimorficos -> Jerarquías más polimórficas -> Model more flexible, reusable, extensible, easier to learn.

### What if no superimplementor?
Si veo que ya implementé el mismo métodos en otra clase y que se comporta de la misma manera. 
+ Si una es subimplementor de otra: `Missing a superimplementor`
+ Si son peer clases y no hay superimplementor: agregar una clase nueva que genera la jerarquía

>  La mejora frase: **I don’t want to duplicate any effort I can avoid.** 
## The Template Class Pattern
**Definition**:  The abstract class I introduced to make the hierarchy polymorphic is what I call a “Template Class.” Template Class is a pattern that creates polymorphic hierarchie

+ This leads to a whole hierarchy of classes that are polymorphic with each other

+ Diferencia con Template Method
	+ Defines the interface for a method while deferring the details to subclasses
	+ La Template Class usa muchos Template Methods

### The [[ValueModel]] hierarchy

Da el ejemplo de _ValueModel_ como jerarquía polimórfica

> Las jerarquías polimórifcas son fáciles de crear

## Conclusion

+ Polimorfismo: mismo nombre y semántica
+ Para ser polimórficos: 
	+ Mismo nombre
	+ Mismos parametros
	+ Mismo efectos secundarios
	+ Mismo tipo de retorno
+ Deben estar en el mismo protocolo
+ Method description
	+ Purpose: uno solo (tope de la jerarquía)
	+ Implementation (uno por cada subimplementador)
+ Para ser polimóricas dos clases
	+ Mismo **core interface of polymorphic messages**
+ Jerarquía polimórifca: todas las clases tienen mismo core interface
+ Jerarquía polimórfica definida por un **abstract class** (template class)
+ Jerarquía polimórifca: encapsula código reusable, flexible y extensible