def SatUMinut(sat):
  return sat * 60

def MinutUsat(minut):
  return minut / 60

def RazlikaVremena(S1, M1, S2, M2):
  Minuti1 = SatUMinut(S1) + M1
  Minuti2 = SatUMinut(S2) + M2

  MinutaUkupno = abs(Minuti2 - Minuti1)

  return MinutUsat(MinutaUkupno)

# Učitavanje dužine i širine terena te konverzija u realne brojeve
L = float(input("Unesite dužinu terena u m:\n"))
W = float(input("Unesite širinu terena:\n"))

# Učitavanje vremena početka i završetka košenja te konverzija u cele brojeve
H1 = int(input("Unesite sat kada je započeto košenje: "))
M1 = int(input("Unesite minute kada je započeto košenje: "))

H2 = int(input("Unesite sat kada je završeno košenje: "))
M2 = int(input("Unesite minute kada je završeno košenje: "))

PoTerena = L * W
UtrosakGoriva = PoTerena * 0.005  # Utrošak goriva u litrima
UkupnoVremeRada = RazlikaVremena(H1, M1, H2, M2)
CenaKosenja = UkupnoVremeRada * 500  # Ispravka imena promenljive

print("Ukupna površina terena je:", PoTerena, "kvadratnih metara.")
print("Trošak goriva je:", UtrosakGoriva, "litara.")
print("Ukupno vreme rada je:", UkupnoVremeRada, "sati.")
print("Ukupna cena rada je:", CenaKosenja, "dinara.")



