# Objects
> Essa variável é a que define os objetos que vão sofrer colisão.
```vb
SimpleCollision.Objects = Array("<objeto>")
```
- `<objeto>` é o nome do objeto que vai sofrer colisão.

> Você pode por mais de um objeto na lista se quiser, por exemplo:
```vb
SimpleCollision.Objects = Array("meuObjeto", "meuObjeto2"...)
```
- Se tiver mais de um objeto com o mesmo nome, ele não vai pegar. Exemplo:
  > Tem 2 Shapes com o nome `caixa`, ele vai pegar a que foi declarada primeiro com esse nome.
 
## Como pegar todos com o mesmo nome?
* Tem um "segredinho", caso você ponha `#all` no texto, ele vai pegar todos os objetos com esse nome.
```vb
SimpleCollision.Objects = Array("meuObjeto#all")
```
> Todos os objetos que tiver o nome `meuObjeto` vai sofrer a colisão.
