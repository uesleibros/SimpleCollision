# 🐃 CollidedShp

> Essa variável retorna o objeto em que o jogador está colidindo atualmente.

Exemplo:

```vba
If IsCollided(Shapes("arvore")) Then
    Debug.Print CollStats.CollidedShp.Name
End If
```

> Caso o jogador esteja colidindo no objeto `arvore`, vai retornar o nome.
>
> Veja outro exemplo:

Vamos supor que eu quero checar todos os objetos contidos no slide, porém, quero filtrar para pegar apenas aqueles que possuem o nome `objetoColisao`.

```vba
If IsCollided Then
    If CollStats.CollidedShp.Name = "objetoColisao" Then
        ....
    End If
End If
```
