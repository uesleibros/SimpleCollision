# 💥 IsCollided

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

{% content-ref url="collstats.md" %}
[collstats.md](collstats.md)
{% endcontent-ref %}

### CheckDirection
