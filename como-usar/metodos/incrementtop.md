# ⛷ IncrementTop

```vba
IncrementTop(Value, Optional Obj As Shape)
```

> Esse método tem dois parâmetros, o valor que pode ser tanto positivo quanto negativo, e o opcional `Obj`, que é se por um acaso quiser mover outro objeto.

## Parâmetros

### Value

* É bem simples, temos uma função no módulo que é equivalente ao `GetAsyncKeyState`, o `KeyPress` que é menor.

```vba
If KeyPress(vbKeyW) Then SimpleCollision.IncrementTop -3
```

* Move o jogador para cima (-).

```vba
If KeyPress(vbKeyS) Then SimpleCollision.IncrementTop 3
```

* Move o jogador para baixo (+).

### Obj (Opcional)

* Caso você ponha algum objeto nesse parâmetro, não vai ser o jogador que irá se mover.

```vba
If KeyPress(vbKeyW) Then SimpleCollision.IncrementTop -3, Shapes("meuObjeto")
```

* Move o objeto para cima (-).

```vba
If KeyPress(vbKeyS) Then SimpleCollision.IncrementTop 3, Shapes("meuObjeto")
```

* Move o objeto para baixo (+).
