# Lua Object

Modulo para crear objetos y clases en lua utilizando metaTablas. Basado en la libreria "classic.lua" de rxi.

## Uso
El módulo object.lua tiene que estar situado en el proyecto existente y crear el objeto "Object"

```lua
Object = require "object"
```
El módulo retorna el objeto que se utiliza como clase bases para crear nuevos objetos utilizando la funcion "extend()"

### Cómo crear una nueva clase
```lua
Actor = Object:extend()

function Actor:new(x, y)
  self.x = x or 0
  self.y = y or 0
end
```

### Cómo crear un objeto
```lua
Actor a = Point(10, 20)
```

### Extendiendo una clase existente
```lua
Player = Actor:extend()

function Player:new(x, y, width, height)
  Player.super.new(self, x, y)
  self.width = width or 0
  self.height = height or 0
end
```

## License

This module is free software; you can redistribute it and/or modify it under
the terms of the MIT license. See [LICENSE](LICENSE) for details.

