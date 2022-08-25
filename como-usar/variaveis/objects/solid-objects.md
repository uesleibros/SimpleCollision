# 🪨 Solid Objects
> Essa variável é bastante útil, como seu próprio nome diz, serve para deixar o objeto sólido, ou seja, outros objetos não vão atravessar o objeto.
```vb
SimpleCollision.SolidObjects = Array("objetoSólido")
```
* O `objetoSólido` não poderá ser atravessado por qualquer outro objeto, mas assim como o `Objects`, ele não vai pegar todos com esse nome.
  > Para pegar todos com o nome você precisa por `#all`. Exemplo:
  ```vb
  SimpleCollision.SolidObjects = Array("objetoSólido#all")
  ```
  * Todos os objetos nomeados de `objetoSólido` vão sofrer a colisão com outros objetos.
