# 🛫 IncrementTop
```vb
IncrementTop(Value, Optional Obj As Shape)
```
> Esse método tem dois parâmetros, o valor que pode ser tanto positivo quanto negativo, e o opcional `Obj`, que é se por um acaso quiser mover outro objeto.

## Value
* É bem simples, temos uma função no módulo que é equivalente ao `GetAsyncKeyState`, o `KeyPress` que é menor.
```vb
If KeyPress(vbKeyW) Then SimpleCollision.IncrementTop -3
```
  * Move o jogador para cima (-).

```vb
If KeyPress(vbKeyS) Then SimpleCollision.IncrementTop 3
```
  * Move o jogador para baixo (+).

# Obj
* Caso você ponha algum objeto nesse parâmetro, não vai ser o jogador que irá se mover.
```vb
If KeyPress(vbKeyW) Then SimpleCollision.IncrementTop -3, Shapes("meuObjeto")
```
  * Move o objeto para cima (-).

```vb
If KeyPress(vbKeyS) Then SimpleCollision.IncrementTop 3, Shapes("meuObjeto")
```
  * Move o objeto para baixo (+).

