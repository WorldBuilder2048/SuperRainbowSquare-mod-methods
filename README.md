# SuperRainbowSquare-mod-methods
List of methods that you can use for SuperRainbowSquare mod-pack

## game_scene class:

### game_scene variables:
game_scene.color:
- Changes color of player in game 🌈
- Example:
```python
game_scene.color = "Красный" 
# Avaible list of colors in game:
# Красный, Оранжевый, Жёлтый, Зелёный, Голубой, Синий, Фиолетовый, Розовый
# It's Red, Orange, Yellow, Green, Cyan, Blue, Purple, Pink
```

game_scene.gamediff:
- Changes game difficult 🌀
- Example:
```python
game_scene.gamediff = 2
```

game_scene.gamediff_setup:
- Changes maximum game diffcult 🌀
- Example:
```python
game_scene.gamediff_setup = 3
```

game_scene.player_x:
- Changes player x 🛣️
- Example:
```python
game_scene.player_x = 64 # Don't recommend changes this value because in game player never moving
```

game_scene.player_y:
- Changes player y 🛣️
- Example:
```python
game_scene.player_y = 64
```

game_scene.player_vy:
- Changes player vy 🛣️
- Example:
```python
game_scene.player_vy = 64
```

game_scene.player_vx:
- Changes player vx 🛣️
- Example:
```python
game_scene.player_vx = 64
```

game_scene.on_ground:
- Changes value is it player on ground  🛣️
- Example:
```python
game_scene.on_ground = True
```

game_scene.score:
- Changes score ⭐
- Example:
```python
game_scene.score = 123
```

game_scene.level_number:
- Changes level number 📈
- Example:
```python
game_scene.level_number = 37
```

game_scene.level_type:
- Changes level type 🔡
- Example:
```python
game_scene.level_type = "dark" # Can be "dark" for dark level and "light" to usually light level
```

### game_scene methods:
game_scene.generate_level:
- Generates level 🏗️
- Params: no
- Example:
```python
game_scene.generate_level()
```

game_scene.respawn:
- Respawn player 🍃
- Params: no
- Example:
```python
game_scene.respawn()
```

game_scene.delete_save_file:
- Deleting save file 🛟
- Params: no
- Example:
```python
game_scene.delete_save_file() # Warning: this method delete only savegame.json of currently user, it don't delete other save files like info.ini etc.
```

game_scene.newgamediff:
- Screen of changing to new game difficult 🌀
- Params: no
- Example:
```python
game_scene.newgamediff()
```

game_scene.endgamediff:
- Screen of last game difficult in version 🌀
- Params: no
- Example:
```python
game_scene.endgamediff()
```

game_scene.update:
- Making update of game, eg. checking collision etc. ☑️
- Params:
- 1. Keys (a, d, RIGHT, LEFT, SPACE) [*More here*](https://www.pygame.org/docs/ref/key.html#pygame.key.get_pressed)
- Example:
```python
keys = pygame.key.get_pressed()
game_scene.update(keys)
```

game_scene.check_achievements:
- Checking your progress to understand do unlock achievements ☑️
- Params: no
- Example:
```python
game_scene.check_achievements()
```

game_scene.draw:
- Draws on screen ✏️
- Params:
- 1. Surface [*More here*](https://www.pygame.org/docs/ref/surface.html)
- Example:
```python
game_scene.draw(WIN)
```

game_scene.save_game:
- Saves game ☑️
- Params: no
- Example:
```python
game_scene.save_game()
```

game_scene.load_game:
- Loading game ☑️
- Params: no
- Example:
```python
game_scene.load_game()
```

## Other variables:

current_scene:
- Current scene 🌉
- Example:
```python
current_scene = "main"
# Can be game, wardrobe, settings, stats, main
```

sprites:
- List of sprites 📋
- Example:
```python
sprites["finish"] = load_img_scaled(sprite_path("coin.png"), (TILE, TILE), ERROR_SPRITE)
```

ERROR_SPRITE:
- Error sprite ❌
- Example:
```python
sprites["finish"] = ERROR_SPRITE
```

TILE:
- Size of tile (usually 16, don't recommended to change) ⬜
- Example:
```python
TILE = 16
```

GRAVITY:
- Using for vy, you can change this value for fun 🙂
- Example:
```python
GRAVITY = 0.5 # 0.5 is usually value for gravity
```

HORIZONTAL_AIR_RESISTANCE:
- Using for changing vx, you can change this value for fun 🙂
- Example:
```python
HORIZONTAL_AIR_RESISTANCE = 0.5 # 0.5 is usually value for horizontal air resistance
```

PLAYER_SPEED:
- Using for changing x, you can change this value for fun 🙂
- Example:
```python
PLAYER_SPEED = 4 # 4 is usually value for player speed
```

JUMP_SPEED:
- Using for changing vy also, you can change this value for fun 🙂
- Example:
```python
JUMP_SPEED = 9 # 9 is usually value for jump speed
```

## Functions:

resource_path:
- Using to make correct path to files or folders, NEVER CHANGE THIS FUNCTION ❌
- Params:
1. Relative path
- Example:
```python
menu_music = resource_path("assets/music/menu.ogg")
```

#### Scene funcions:

main_menu:
- Function of main menu 🏝️
- Params: no

wardrobe_scene:
- Function of wardrobe scene 🏝️
- Params: no

settings_scene:
- Function of settings scene 🏝️
- Params: no

achievements_scene:
- Function of achievements scene 🏝️
- Params: no

stats_scene:
- Function of stats scene 🏝️
- Params: no
