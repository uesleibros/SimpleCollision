# 🧃 ObjectCollidedShp

> Essa variável retorna o objeto em que o objeto está colidindo atualmente.

Exemplo:

```vba
If IsCollided(Shapes("caixa"), Shapes("botao")) Then
    Debug.Print CollStats.ObjectCollidedShp.Name
End If
```

> Caso o objeto (caixa) esteja colidindo no objeto `botao`, vai retornar o nome do objeto colidido.
>
> Veja outro exemplo:

Vamos supor que eu quero checar todos os objetos contidos no slide, porém, quero filtrar para pegar apenas aqueles que possuem o nome `objetoColisao`.

```vba
If IsObjectCollided(Shapes("caixa")) Then
    If CollStats.ObjectCollidedShp.Name = "objetoColisao" Then
        ....
    End If
End If
```
