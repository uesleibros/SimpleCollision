# 🚜 Moving Objects

> Essa variável é bem interessante, para entender melhor é recomendado ver as sessões:

{% content-ref url="../../metodos/incrementleft.md" %}
[incrementleft.md](../../metodos/incrementleft.md)
{% endcontent-ref %}

{% content-ref url="../../metodos/incrementtop.md" %}
[incrementtop.md](../../metodos/incrementtop.md)
{% endcontent-ref %}

> Com os objetos em movimento é importante que garanta a colisão com o jogador, afinal, não queremos ver por exemplo um carro passar por dentro do jogador. Veja o exemplo a seguir:

```vba
SimpleCollision.IncrementLeft 100 * DeltaTime, Shapes("carro")
```

Esse código faz com que o objeto `carro` vá para a direita, porém ele vai passar por dentro do jogador. Para evitar isso temos uma variável bastante útil: `SimpleCollision.MovingObjects.ApplyCollision As Boolean`

> Caso você ative ela, qualquer objeto em movimento que colida com o jogador não vai passar por dentro dele. Exemplo:

```vba
SimpleCollision.MovingObjects.ApplyCollision = True
SimpleCollision.IncrementLeft 100 * DeltaTime, Shapes("carro")
```
