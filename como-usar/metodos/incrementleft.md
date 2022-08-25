# 🏃‍♂️ IncrementLeft
```vb
IncrementLeft(Value, Optional Obj As Shape)
```
> Esse método tem dois parâmetros, o valor que pode ser tanto positivo quanto negativo, e o opcional `Obj`, que é se por um acaso quiser mover outro objeto.

## Value
* É bem simples, temos uma função no módulo que é equivalente ao `GetAsyncKeyState`, o `KeyPress` que é menor.
```vb
If KeyPress(vbKeyA) Then SimpleCollision.IncrementLeft -3
```
  * Move o jogador para a esquerda (-).

```vb
If KeyPress(vbKeyD) Then SimpleCollision.IncrementLeft 3
```
  * Move o jogador para a direita (+).
