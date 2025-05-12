import pygame
from pygame.locals import *
import math

# salvo a pátria: print(eval(string))
Icon = pygame.image.load('Image/4341087.png')

pygame.init()
pygame.display.set_caption('Calculator')
pygame.display.set_icon(Icon)
Screen = pygame.display.set_mode((300, 400))
clock = pygame.time.Clock()

Quantity = []
Noone = False
Result = 0
Working = True

delay = 200


def process(A, B, C, D, E, F, G, H, I, J):
    match A:
        case 1:
            Quantity.append('1')
    match B:
        case 2:
            Quantity.append('2')
    match C:
        case 3:
            Quantity.append('3')
    match D:
        case 4:
            Quantity.append('4')
    match E:
        case 5:
            Quantity.append('5')
    match F:
        case 6:
            Quantity.append('6')
    match G:
        case 7:
            Quantity.append('7')
    match H:
        case 8:
            Quantity.append('8')
    match I:
        case 9:
            Quantity.append('9')
    match J:
        case 0:
            Quantity.append('0')

def ResulT():
    try:
        global Result
        if Noone == True:
            Result = float(round(eval("".join(Quantity)), 2))
            Quantity.clear()
            Quantity.append(str(Result))
        else:
            Result = " ".join(Quantity)
            Quantity.clear()
    except:
        global Working
        Working = False
        Working = True
    
def draw_button_special(form, posX, posY, width, height):
    mouse_posX, mouse_posY = pygame.mouse.get_pos()
    button = pygame.draw.rect(Screen, (20, 20, 20), (posX, posY, width, height))
    if "remove" == form:
        if event.type == pygame.MOUSEBUTTONDOWN or event.type == KEYUP:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                try:
                    global Result
                    Quantity.pop(-1)
                    Result = 0
                    pygame.time.delay(delay)
                except:
                    Quantity.append('')
                    Result = 0
    if "+" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.append("+")
                global Noone
                Noone = True
                Result = 0
                pygame.time.delay(delay)
    if "-" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.append("-")
                Noone = True
                Result = 0
                pygame.time.delay(delay)
    if "÷" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.append("/")
                Noone = True
                Result = 0
                pygame.time.delay(delay)
    if "x" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.append("*")
                Noone = True
                Result = 0
                pygame.time.delay(delay)
    if "=" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                ResulT()
    if "CE" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.clear()
                Result = 0
                pygame.time.delay(delay)
    if "." == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.append(".")
                Result = 0
                pygame.time.delay(delay)
    if "a^x" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.append("**")
                Noone = True
                Result = 0
                pygame.time.delay(delay)
    if "(" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.append("(")
                Noone = True
                Result = 0
                pygame.time.delay(delay)
    if ")" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.append(")")
                Noone = True
                Result = 0
                pygame.time.delay(delay)
    if "log" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                try:
                    Result = float(round(math.log(eval("".join(Quantity)), 10), 2))
                    Result = str(Result)
                    Quantity.clear()
                    Quantity.append(Result)
                    Result = 0
                    pygame.time.delay(delay)
                except:
                    Working = False
                    Working = True
    if "π" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                Quantity.append("3.14")
                Noone = True
                Result = 0
                pygame.time.delay(delay)
    if "√" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                try:
                    Result = float(round(math.sqrt(eval("".join(Quantity))), 2))
                    Result = str(Result)
                    Quantity.clear()
                    Quantity.append(Result)
                    Result = 0
                    pygame.time.delay(delay)
                except:
                    Working = False
                    Working = True
                    Quantity.clear()
                    Result = 0
    if "%" == form:
        if event.type == pygame.MOUSEBUTTONDOWN:
            if posX <= mouse_posX <= posX + width and posY <= mouse_posY <= posY + height:
                try:
                    for i in Quantity:
                        if i == "-":
                            a = Quantity
                            b = "".join(a)
                            b = b.replace('-', ' ')
                            b = b.split()
                            c = float(b[0]) - float(b[-1]) / 100 * float(b[0])
                            Result = round(c, 2)
                            Quantity.clear()
                            Quantity.append(str(c))
                            Result = 0
                            pygame.time.delay(delay)
                        if i == "+":
                            a = Quantity
                            b = "".join(a)
                            b = b.replace('+', ' ')
                            b = b.split()
                            c = float(b[0]) + float(b[-1]) / 100 * float(b[0])
                            Result = round(c, 2)
                            Quantity.clear()
                            Quantity.append(str(c))
                            Result = 0
                            pygame.time.delay(delay)
                        if i == "**":
                            a = Quantity
                            b = "".join(a)
                            b = b.replace('**', ' ')
                            b = b.split()
                            c = float(b[0]) ** float(b[-1]) / 100 * float(b[0])
                            Result = round(c, 2)
                            Quantity.clear()
                            Quantity.append(str(c))
                            Result = 0
                            pygame.time.delay(delay)
                        if i == "/":
                            a = Quantity
                            b = "".join(a)
                            b = b.replace('/', ' ')
                            b = b.split()
                            c = float(b[0]) / float(b[-1]) / 100 * float(b[0])
                            Result = round(c, 2)
                            Quantity.clear()
                            Quantity.append(str(c))
                            Result = 0
                            pygame.time.delay(delay)
                        if i == "*":
                            a = Quantity
                            b = "".join(a)
                            b = b.replace('*', ' ')
                            b = b.split()
                            c = float(b[0]) * float(b[-1]) / 100 * float(b[0])
                            Result = round(c, 2)
                            Quantity.clear()
                            Quantity.append(str(c))
                            Result = 0
                            pygame.time.delay(delay)
                except:
                    Working = False
                    Working = True
                    Quantity.clear()
                    Result = 0

def draw_button_number(number, posX, posY, width, height):
    mouseX, mouseY = pygame.mouse.get_pos()
    button = pygame.draw.rect(Screen, (51, 0, 51), (posX, posY, width, height))
    global Result
    match number:
        case 1:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(1, 0, 0, 0, 0, 0, 0, 0, 0, -1)
                    Result = 0
                    pygame.time.delay(delay)
        case 2:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(0, 2, 0, 0, 0, 0, 0, 0, 0, -1)
                    Result = 0
                    pygame.time.delay(delay)
        case 3:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(0, 0, 3, 0, 0, 0, 0, 0, 0, -1)
                    Result = 0
                    pygame.time.delay(delay)
        case 4:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(0, 0, 0, 4, 0, 0, 0, 0, 0, -1)
                    Result = 0
                    pygame.time.delay(delay)
        case 5:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(0, 0, 0, 0, 5, 0, 0, 0, 0, -1)
                    Result = 0
                    pygame.time.delay(delay)
        case 6:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(0, 0, 0, 0, 0, 6, 0, 0, 0, -1)
                    Result = 0
                    pygame.time.delay(delay)
        case 7:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(0, 0, 0, 0, 0, 0, 7, 0, 0, -1)
                    Result = 0
                    pygame.time.delay(delay)
        case 8:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(0, 0, 0, 0, 0, 0, 0, 8, 0, -1)
                    Result = 0
                    pygame.time.delay(delay)
        case 9:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(0, 0, 0, 0, 0, 0, 0, 0, 9, -1)
                    Result = 0
                    pygame.time.delay(delay)
        case 0:
            if event.type == pygame.MOUSEBUTTONDOWN and pygame.MOUSEBUTTONUP:
                if posX <= mouseX <= posX + width and posY <= mouseY <= posY + height:
                    process(0, 0, 0, 0, 0, 0, 0, 0, 0, 0)
                    Result = 0
                    pygame.time.delay(delay)

def draw_texts():
    # Not especial
    font = pygame.font.Font(None, 50)
    text = font.render("1", True, (255, 255, 255))
    text_rect = text.get_rect(center=(86, 187))
    Screen.blit(text, text_rect)
    text = font.render("4", True, (255, 255, 255))
    text_rect = text.get_rect(center=(86, 248))
    Screen.blit(text, text_rect)
    text = font.render("7", True, (255, 255, 255))
    text_rect = text.get_rect(center=(86, 308))
    Screen.blit(text, text_rect)
    text = font.render("2", True, (255, 255, 255))
    text_rect = text.get_rect(center=(148, 187))
    Screen.blit(text, text_rect)
    text = font.render("5", True, (255, 255, 255))
    text_rect = text.get_rect(center=(148, 248))
    Screen.blit(text, text_rect)
    text = font.render("8", True, (255, 255, 255))
    text_rect = text.get_rect(center=(148, 308))
    Screen.blit(text, text_rect)
    text = font.render("3", True, (255, 255, 255))
    text_rect = text.get_rect(center=(208, 187))
    Screen.blit(text, text_rect)
    text = font.render("6", True, (255, 255, 255))
    text_rect = text.get_rect(center=(208, 248))
    Screen.blit(text, text_rect)
    text = font.render("9", True, (255, 255, 255))
    text_rect = text.get_rect(center=(208, 308))
    Screen.blit(text, text_rect)
    text = font.render("0", True, (255, 255, 255))
    text_rect = text.get_rect(center=(270, 187))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 70)
    text = font.render("<", True, (255, 255, 255))
    text_rect = text.get_rect(center=(270, 245))
    Screen.blit(text, text_rect)

    # Special
    font = pygame.font.Font(None, 60)
    text = font.render("+", True, (255, 255, 255))
    text_rect = text.get_rect(center=(86, 367))
    Screen.blit(text, text_rect)
    text = font.render("-", True, (255, 255, 255))
    text_rect = text.get_rect(center=(148, 367))
    Screen.blit(text, text_rect)
    text = font.render("÷", True, (255, 255, 255))
    text_rect = text.get_rect(center=(208, 367))
    Screen.blit(text, text_rect)
    text = font.render("x", True, (255, 255, 255))
    text_rect = text.get_rect(center=(270, 367))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 70)
    text = font.render("=", True, (255, 255, 255))
    text_rect = text.get_rect(center=(272, 305))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 45)
    text = font.render("CE", True, (255, 255, 255))
    text_rect = text.get_rect(center=(270, 127))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 80)
    text = font.render(",", True, (255, 255, 255))
    text_rect = text.get_rect(center=(25, 354))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 40)
    text = font.render("%", True, (255, 255, 255))
    text_rect = text.get_rect(center=(27, 188))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 50)
    text = font.render("(", True, (255, 255, 255))
    text_rect = text.get_rect(center=(25, 245))
    Screen.blit(text, text_rect)
    text = font.render(")", True, (255, 255, 255))
    text_rect = text.get_rect(center=(28, 305))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 60)
    text = font.render("√", True, (255, 255, 255))
    text_rect = text.get_rect(center=(208, 128))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 35)
    text = font.render("a^x", True, (255, 255, 255))
    text_rect = text.get_rect(center=(148, 125))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 30)
    text = font.render("log()", True, (255, 255, 255))
    text_rect = text.get_rect(center=(89, 125))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 50)
    text = font.render("π", True, (255, 255, 255))
    text_rect = text.get_rect(center=(28, 123))
    Screen.blit(text, text_rect)
    font = pygame.font.Font(None, 30)
    text = font.render("".join(Quantity), True, (255, 255, 255))
    text_rect = text.get_rect(center=(150, 42))
    Screen.blit(text, text_rect)
    global Result
    if Result != 0:
        try:
            text = font.render(str(Result), True, (255, 255, 255))
            text_rect = text.get_rect(center=(150, 42))
            Screen.blit(text, text_rect)
        except ValueError:
            Quantity.clear()
            font = pygame.font.Font(None, 20)
            text = font.render("Don't put more than this, it's dangerous!", True, (255, 255, 255))
            text_rect = text.get_rect(center=(150, 42))
            Screen.blit(text, text_rect)


while Working:
    Screen.fill((255, 255, 255))
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            Working = False
        if event.type == KEYDOWN and KEYUP:
            if event.key == K_BACKSPACE:
                try:
                    Quantity.pop(-1)
                    Result = 0
                except:
                    Quantity.append('')
                    Result = 0
            if event.key == K_1:
                process(1, 0, 0, 0, 0, 0, 0, 0, 0, -1)
                Result = 0
            if event.key == K_2:
                process(0, 2, 0, 0, 0, 0, 0, 0, 0, -1)
                Result = 0
            if event.key == K_3:
                process(0, 0, 3, 0, 0, 0, 0, 0, 0, -1)
                Result = 0
            if event.key == K_4:
                process(0, 0, 0, 4, 0, 0, 0, 0, 0, -1)
                Result = 0
            if event.key == K_5:
                process(0, 0, 0, 0, 5, 0, 0, 0, 0, -1)
                Result = 0
            if event.key == K_6:
                process(0, 0, 0, 0, 0, 6, 0, 0, 0, -1)
                Result = 0
            if event.key == K_7:
                process(0, 0, 0, 0, 0, 0, 7, 0, 0, -1)
                Result = 0
            if event.key == K_8:
                process(0, 0, 0, 0, 0, 0, 0, 8, 0, -1)
                Result = 0
            if event.key == K_9:
                process(0, 0, 0, 0, 0, 0, 0, 0, 9, -1)
                Result = 0
            if event.key == K_0:
                process(0, 0, 0, 0, 0, 0, 0, 0, 0, 0)
                Result = 0
            if event.key == K_PLUS:
                Quantity.append("+")
                Noone = True
                Result = 0
            if event.key == K_MINUS:
                Quantity.append("-")
                Noone = True
                Result = 0
            if event.key == K_KP_DIVIDE:
                Quantity.append("/")
                Noone = True
                Result = 0
            if event.key == K_KP_MULTIPLY:
                Quantity.append("*")
                Noone = True
                Result = 0
            if event.key == K_EQUALS or event.key == K_KP_ENTER:
                ResulT()
            if event.key == K_PERIOD:
                Quantity.append(".")
                Result = 0
            if event.key == K_LEFTPAREN:
                Quantity.append("(")
                Noone = True
                Result = 0
            if event.key == K_RIGHTPAREN:
                Quantity.append(")")
                Noone = True
                Result = 0
    Screen_focus = pygame.draw.rect(Screen, (48, 48, 48), (0, 0, 300, 90))
    Screen_extra1 = pygame.draw.rect(Screen, (31, 31, 31), (10, 10, 280, 60))
    Screen_extra2 = pygame.draw.rect(Screen, (0, 0, 80), (0, 80, 300, 16))
    draw_button_special("=", 240, 279, 60, 60)
    draw_button_special("x", 240, 340, 60, 60)
    draw_button_special("÷", 179, 340, 60, 60)
    draw_button_special("-", 118, 340, 60, 60)
    draw_button_special("+", 57, 340, 60, 60)
    draw_button_special("remove", 240, 218, 60, 60)
    draw_button_special("CE", 240, 96, 60, 60)
    draw_button_special("√", 179, 96, 60, 60)
    draw_button_special("a^x", 118, 96, 60, 60)
    draw_button_special("log", 57, 96, 60, 60)
    draw_button_special(".", 0, 340, 56, 60)
    draw_button_special(")", 0, 279, 56, 60)
    draw_button_special("(", 0, 218, 56, 60)
    draw_button_special("%", 0, 157, 56, 60)
    draw_button_special("π", 0, 96, 56, 60)
    draw_button_number(1, 57, 157, 60, 60)
    draw_button_number(4, 57, 218, 60, 60)
    draw_button_number(7, 57, 279, 60, 60)
    draw_button_number(2, 118, 157, 60, 60)
    draw_button_number(5, 118, 218, 60, 60)
    draw_button_number(8, 118, 279, 60, 60)
    draw_button_number(3, 179, 157, 60, 60)
    draw_button_number(6, 179, 218, 60, 60)
    draw_button_number(9, 179, 279, 60, 60)
    draw_button_number(0, 240, 157, 60, 60)
    draw_texts()
    pygame.draw.circle(Screen, (0, 0, 0), center=(0, 0), radius=10, width=100, draw_bottom_right=True, draw_top_left=False, draw_bottom_left=False, draw_top_right=False)
    pygame.draw.circle(Screen, (0, 0, 0), center=(300, 0), radius=10, width=100, draw_bottom_right=False, draw_top_left=True, draw_bottom_left=True, draw_top_right=False)
    pygame.draw.circle(Screen, (0, 0, 0), center=(0, 80), radius=10, width=100, draw_bottom_right=False, draw_top_left=False, draw_bottom_left=False, draw_top_right=True)
    pygame.draw.circle(Screen, (0, 0, 0), center=(300, 80), radius=10, width=100, draw_bottom_right=False, draw_top_left=True, draw_bottom_left=False, draw_top_right=False)
    print(Result)
    print(Quantity)
    print("".join(Quantity))
    pygame.display.update()
    clock.tick(60)

pygame.quit()
