# 🪣 IsCollided

> Essa função é a principal do módulo, a mais útil entre todas.

```vba
IsCollided(Optional ByVal obj As Shape, CheckDirection As Directions) As Boolean
```

Para começar vamos entender essa função, como o seu nome já diz, ela checa se o **jogador** está colidindo com algum objeto que esteja no Slide.

## Parâmetros

### Obj (Opcional)

> Nesse parâmetro você vai por o objeto que quer a checagem da colisão, por exemplo:

```vba
If SimpleCollision.IsCollided(Shapes("parede")) Then
    ....
End If
```

Nessa linha de código ele checa se o objeto `parede` está colidindo com o jogador em algum momento. Não podemos esquecer que esse parâmetro é **opcional**, ou seja, não é preciso por o objeto que quer a verificação.

{% hint style="info" %}
Caso não ponha o objeto que quer a verificação, ele vai checar qualquer objeto que esteja no slide. Caso alguma esteja colidindo vai retornar `True (verdadeiro)`.
{% endhint %}

```vba
If SimpleCollision.IsCollided Then
    ....
End If
```

> Ele também pode retornar o objeto em que está colidindo, para saber mais sobre essa função vá até a sessão:

{% content-ref url="collstats/" %}
[collstats](collstats/)
{% endcontent-ref %}

{% content-ref url="collstats/collidedshp.md" %}
[collidedshp.md](collstats/collidedshp.md)
{% endcontent-ref %}

### CheckDirection

> Esse parâmetro é bem interessante, por alguns motivos. Caso você queira pegar a posição/local onde o jogador está colidindo com o objeto, você terá mais de 4 opções nesse parâmetro:

```vba
CheckAll -> "Checa se está tocando em qualquer lugar" (Default)
CheckLeft -> "Checa se está tocando no lado esquerdo do objeto"
CheckRight -> "Checa se está tocando no lado direito do objeto"
CheckUp -> "Checa se está tocando no topo do objeto"
CheckDown -> "Checa se está tocando no baixo do objeto"
```

Com isso, dá para fazer um sistema de deslocar o objeto de lugar muito facilmente. Exemplo:

```vba
If IsCollided(Shapes("caixa"), CheckLeft) Then SimpleCollision.IncrementLeft 2, Shapes("caixa")
If IsCollided(Shapes("caixa"), CheckRight) Then SimpleCollision.IncrementLeft -2, Shapes("caixa")
If IsCollided(Shapes("caixa"), CheckUp) Then SimpleCollision.IncrementTop -2, Shapes("caixa")
If IsCollided(Shapes("caixa"), CheckDown) Then SimpleCollision.IncrementTop 2, Shapes("caixa")
```
