# Parking System
Hardverarchitektúra
Főbb komponensek:

## Vezérlő:

Arduino Uno

## Érzékelés:

HC-SR04 Ultrahangos távolságmérő(k)
(parkolóhelyek foglaltságának érzékelésére)

## Megjelenítés:

LCD 16x2 (I2C) kijelző
(szabad parkolóhelyek számának megjelenítésére)

## Logikai bővítés:

74HC595 Shift Register
(a kijelző vezérléséhez, lábtakarékossági célból)

## További komponensek:

170 lyukas próbapanel (breadboard)

ellenállások (220Ω a szegmensekhez)

jumper kábelek

## Rendszer működése

A rendszer ultrahangos szenzor(ok) segítségével folyamatosan méri a parkolóhely(ek) előtti távolságot.

Ha a mért távolság egy küszöbérték alá csökken → a parkolóhely foglalt

Ha a távolság nagyobb → a parkolóhely szabad

A mikrokontroller összeszámolja a szabad helyeket, majd az eredményt egy 7-szegmenses kijelzőn jeleníti meg.

A kijelző meghajtása a 74HC595 shift registeren keresztül történik, így kevesebb Arduino láb szükséges.
