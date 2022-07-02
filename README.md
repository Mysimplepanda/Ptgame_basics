# Python-Game
### Python的小遊戲，利用pygame module製作( •̀ ω •́ )y

1.**參考資料~**
  
  1. Pygame Page: http://pygame.org
  2. documentation: http://pygame.org/docs/ref
  3. Icon Archive: https://iconarchive.com/ (下載遊戲角色)
  4. Leshy SFMaker: https://www.leshylabs.com/apps/sfMaker/ (下載音效)
  5. Font Space: https://www.fontspace.com/commercial-fonts (下載字體)
  6. ~~大福媽萬歲 ~~ <br><br>
    
 ------

**_2. _What is pygame:_
  * Pygame提供Display, Sound, Music, Image, Text, Event幫助製作遊戲。
  * Pygame可以做出2.0小遊戲
  * Pygame偵測使用者使用Keyboard, joystick, mouse控制遊戲
  * Pygame提供許多內建的game objects來製作遊戲

**_3. Pygame Basics_**:
| Code | Description |
|:-----:|:----------:|
| _1.py_ | Create my game surface, game loop and drawing. |
| _2.py_ | Blit, font, sound and image objects. |
| _3.py_ | Getting user keyboard and collision dection. |

**_4.Code Snippet_**
```Python
#Create game display
WINDOW_WIDTH,WINDOW_HEIGHT = 1000, 600
displayscreen = pygame.display.set_mode((WINDOW_WIDTH, WINDOW_HEIGHT))
pygame.display.set_caption("Feed The Angry Bird! ")
```
```python
#Blit image object and setting its rec.
player_image        = pygame.image.load("angrybird.png")
player_rect         = player_image.get_rect()
player_rect.left    = 32
player_rect.centery = WINDOW_HEIGHT//2
### while running~
displayscreen.blit(player_image, player_rect)
```
```python
#Key move
keys = pygame.key.get_pressed()
if keys[pygame.K_UP] and player_rect.top > 64:
  player_rect.y -= PLAYER_VELOCITY

if keys[pygame.K_DOWN] and player_rect.bottom < WINDOW_HEIGHT:
  player_rect.y += PLAYER_VELOCITY
```

**_5. Game Assets:_**:
  *[Icon Arxhive: ](https://iconarchive.com/) 網站提供很多遊戲角色下載
  *[Leshy SFMaker: ](https://www.leshylabs.com/apps/sfMaker/) 網站可以下載遊戲特效, 也可以簡單自己製作音效
