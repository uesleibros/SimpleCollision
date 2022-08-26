# 🧱 IsObjectCollided

> Essa função é bem interessante, como o seu nome já diz, ela checa se o objeto está colidindo com outro objeto.

```vba
IsObjectCollided(Obj As Shape, Optional Target As Shape) As Boolean
```

## Parâmetros

### Obj

> Nesse parâmetro você vai por o objeto que quer a checagem da colisão, por exemplo:

```vba
If SimpleCollision.IsObjectCollided(Shapes("parede")) Then
    ....
End If
```

Nessa linha de código ele checa se o objeto `parede` está colidindo com qualquer outro objeto contido no slide em algum momento.

> Ele também pode retornar o objeto em que está colidindo, para saber mais sobre essa função vá até a sessão:

{% content-ref url="iscollided/collstats.md" %}
[collstats.md](iscollided/collstats.md)
{% endcontent-ref %}

{% content-ref url="../variaveis/collstats/objectcollidedshp.md" %}
[objectcollidedshp.md](../variaveis/collstats/objectcollidedshp.md)
{% endcontent-ref %}

### Target (Opcional)

> Esse parâmetro vai ser o objeto em que vai ser checado se está colidindo com o `Obj`.
>
> Por exemplo:

```vba
If IsObjectCollided(Shapes("caixa"), Shapes("botao")) Then
    ....
End If
```

Nesse caso ele checa se o objeto `"caixa"` está colidindo com o objeto `"botão"`. Devemos lembrar que esse parâmetro é opcional, caso você queira verificar se qualquer objeto está colidindo com por exemplo o nosso objeto `"caixa"`, basta fazer:

```vba
If IsObjectCollided(Shapes("caixa")) Then
    ....
End If
```

> Se qualquer objeto estiver colidindo com o objeto `"caixa"`, então vai retornar `True (Verdadeiro)`.
