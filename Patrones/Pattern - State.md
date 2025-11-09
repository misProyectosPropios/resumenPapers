## Usos

Este patrón se usa cuando hay una serie de finitos casos (como las máquinas de estados finitos) y queremos que su comportamiento se modifique de acuerdo a las acciones tomadas
## Intent

Permitir a un objeto modificar su comportamiento interno. El objeto va a aparecer como modificada su clase
## Example

Mars-rovers: se mueve de acuerdo a donde apunta. 
Si se mueve a la derecha, entonces se mueve la estructura del movimiento para otro lado. Necesita una jerarquía polimórfica aparte.

## Structure

![[StatePattern.png]]
## How to use it

Find a method that works given some intern state.
Then, the state could be polymorphic and separate it into another polymorphic hierarchy.
