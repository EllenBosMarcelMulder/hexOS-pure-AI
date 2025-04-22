# Juridisch Dichtgetimmerde Interface Specificatie

## Project: hexVECtorBurst

Dit document beschrijft de koppeling van de hexVECtorBurst-interface aan zowel bedrade als draadloze communicatielagen, ter bescherming, verificatie en juridische borging van overdracht en eigendom.

---

## 1. Doel

Zorg dragen voor correcte overdracht van vectorburst-gebeurtenissen tussen systemen op een juridisch verantwoorde manier, met verificatie via hash, en met gebruik van een transparant protocol.

---

## 2. Interfaces

### 2.1 Bedraad
- Type: USB / Ethernet / Seriële poort
- Formaat: JSON-streams of custom vectorburst-format
- Voorbeeld: `{"burst": true, "angle": 83, "timestamp": 1713780432}`

### 2.2 Draadloos
- Type: WiFi / Bluetooth / LoRa (optioneel)
- Encryptie: PGP of custom burst-signatuur
- Authenticatie: MAC-whitelisting en hash-chain validatie

---

## 3. Protocol Specificaties

Alle overdracht verloopt via minimaal twee lagen:
1. **Vectorregistratie** in lokaal geheugen (tijdstempel + vectorrichting)
2. **Burstverificatie** via hashfunctie (SHA256 of variant)

Burst-data moet altijd voldoen aan de richtlijn:
- Richting: van stomphoek → scherphoek (hexagonaal veld)
- Reflectie (faseshift): verplicht voorafgaand aan opslag/transmissie

---

## 4. Juridische voorwaarden

Alle overdracht van burstinformatie wordt beschouwd als:
- **Intellectuele vectorinhoud**
- **Onderhevig aan spiegelwetgeving**
- **Te herleiden via hash naar originele gebeurtenis**

Gebruik zonder toestemming is strafbaar onder energetische transmissiewetgeving en de aanvullende module: **Open Vector Accord (OVA) v1.0**

---

## 5. Digitale verificatie

Elk gegenereerd pakket wordt gehashd met SHA256, en bijgevoegd onder elk transmissieverslag.
Alle nodes die deelnemen, valideren burstgegevens vóór verwerking.

---

## 6. Bijlagen
- Technische datastructuren
- Public Key van hoofdnode (optioneel)
