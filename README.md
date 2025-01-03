import random

print("Ich habe eine Zahl zwischen 1 und 100 gewählt. Rate mal!")

zahl = random.randint(1, 100)  # Zufällige Zahl generieren
versuche = 7  # Anzahl der Versuche

while versuche > 0:
    tipp = int(input("Geben Sie Ihre Schätzung ein: "))
    
    if tipp < zahl:
        print("Zu niedrig! Versuchen Sie es noch einmal.")
    elif tipp > zahl:
        print("Zu hoch! Versuchen Sie es noch einmal.")
    else:
        print("Glückwunsch! Sie haben die richtige Zahl erraten.")
        break
    
    versuche -= 1
    print(f"Verbleibende Versuche: {versuche}")

if versuche == 0:
    print(f"Leider verloren. Die richtige Zahl war: {zahl}")

