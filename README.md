- 👋 Hi, I’m @Sufiansalma
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Sufiansalma/Sufiansalma is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import pygame, sys

# Intializing Pygame
pygame.init()

# Setting the screen size
WIDTH = 800
HEIGHT = 600
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Bike Racing Game")

# Colors
WHITE = (255, 255, 255)
BLACK = (0, 0, 0)

# Bike variables
bike_width = 50
bike_height = 100
bike_x = 375
bike_y = 500
bike_speed = 10

# Creating the bike
def bike(x, y):
    pygame.draw.rect(screen, BLACK, (x, y, bike_width, bike_height))

# Game loop
while True:

    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    keys = pygame.key.get_pressed()
    if keys[pygame.K_LEFT]:
        bike_x -= bike_speed
    if keys[pygame.K_RIGHT]:
        bike_x += bike_speed

    # Drawing
