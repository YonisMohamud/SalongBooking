# ✂️ **SalonBook - Bokningssystem för Frisörsalonger** 💇‍♀️💈

## **1. Projektidé**

### **📌 Scenario**
SalonBook är ett bokningssystem för frisörsalonger där kunder kan boka, ändra och avboka tider online. Systemet hanterar även frisörernas scheman och skickar påminnelser 📅 till kunder för att minimera uteblivna besök.

### **🎯 Bakgrund och syfte**
Många frisörsalonger hanterar fortfarande bokningar manuellt, vilket kan leda till dubbelbokningar och ineffektiv administration. Syftet med systemet är att förenkla bokningsprocessen, minimera administration och förbättra kundupplevelsen genom en smidig digital lösning. 💻

### **🌟 Vision & Mål**
**Vision:**
Att skapa ett användarvänligt och effektivt bokningssystem för frisörer och deras kunder.

**Mål:**
- ✅ Kunder ska kunna boka, ändra och avboka tider online.
- ✅ Frisörer ska kunna hantera sina scheman.
- ✅ Systemet ska skicka påminnelser till kunder.
- ✅ Administratörer ska kunna hantera frisörer och tjänster.

## **2. 🏢 Intressentkartläggning**

| 🏷️ Intressent       | 🎭 Roll                                    |
| ---------------- | --------------------------------------- |
| 👤 Kunder           | Bokar tider och hanterar sina bokningar |
| ✂️ Frisörer         | Hanterar sitt schema och kundbokningar  |
| 👨‍💼 Administratör    | Sköter användarhantering och tjänster   |
| 💻 Systemutvecklare | Utvecklar och underhåller systemet      |

## **3. 📜 Kravspecifikation**

### **⚙️ Funktionella krav**

1. 📅 Användare ska kunna skapa, ändra och avboka bokningar.
2. 📩 Systemet ska skicka bokningsbekräftelser och påminnelser via e-post.
3. ✂️ Frisörer ska kunna hantera sina scheman.
4. 🛠️ Administratörer ska kunna hantera frisörer och tjänster.
5. 🔑 Användare ska kunna logga in och hantera sin profil.
6. 💳 Systemet ska stödja betalning för bokningar.
7. 📊 Systemet ska generera rapporter över bokningar.

### **🔐 Icke-funktionella krav**

1. **⚡ Prestanda:** Systemet ska kunna hantera minst 100 samtidiga bokningar.
2. **🔒 Säkerhet:** Krypterad lagring av användardata.
3. **📱 Användbarhet:** Responsiv design och enkel navigering.
4. **🌍 Tillgänglighet:** Systemet ska vara tillgängligt 24/7.
5. **🔗 Integration:** Möjlighet att integrera med Google Kalender.

### **📊 Prioritering av krav (MoSCoW)**

| 📌 Krav                                        | 📌 Prioritet |
| ------------------------------------------- | --------- |
| 📅 Användare kan boka tider                    | Must      |
| 📩 Skicka bokningsbekräftelser och påminnelser | Must      |
| ✂️ Hantera frisörers scheman                   | Must      |
| 🔑 Användare kan logga in                      | Should    |
| 💳 Stöd för betalning                          | Could     |
| 🔗 Integration med Google Kalender             | Won't     |

### **📖 User Stories**

1. 👤 **Som kund** vill jag kunna boka en tid så att jag kan få min klippning vid en passande tidpunkt.
2. ✂️ **Som frisör** vill jag kunna se mitt schema så att jag vet vilka kunder jag har.
3. 👨‍💼 **Som administratör** vill jag kunna lägga till nya frisörer så att verksamheten kan växa.
4. 👤 **Som kund** vill jag kunna avboka min tid så att jag slipper betala för en tid jag inte kan nyttja.
5. 👨‍💼 **Som administratör** vill jag kunna generera rapporter så att jag kan analysera bokningstrender.

### **🎬 Use Cases**
#### **📅 Användningsfall: Boka en tid**
- **Aktör:** 👤 Kund
- **Pre-kondition:** Kunden är inloggad.
- **Huvudflöde:**
  1. Kunden väljer en tjänst ✂️.
  2. Kunden väljer en frisör 👨‍🎨.
  3. Kunden väljer datum och tid 📅.
  4. Systemet verifierar tillgänglighet ✅.
  5. Kunden bekräftar bokningen 📌.
  6. Systemet skickar en bekräftelse 📩.
- **Post-kondition:** Bokningen är sparad i systemet.

## **4. 🖥️ Objektorienterad Modellering**

### **📌 Domänmodell / UML-klassdiagram**

**Klasser:**
- 👤 **Användare** (attribut: namn, e-post, lösenord)
- 👤 **Kund** (subklass av Användare, extra attribut: bokningar)
- ✂️ **Frisör** (subklass av Användare, extra attribut: schema)
- 📅 **Bokning** (attribut: datum, tid, tjänst, frisör, kund)
- 🛠️ **Tjänst** (attribut: namn, pris, varaktighet)

### **📊 Sekvensdiagram (Exempel: Bokningsflöde)**

1. 👤 Kunden loggar in 🔑.
2. Kunden väljer en tjänst ✂️ och en frisör 👨‍🎨.
3. Systemet kontrollerar tillgänglighet ✅.
4. Kunden bekräftar bokningen 📩.
5. Systemet sparar bokningen och skickar bekräftelse 📌.

### **🗂️ ER-Diagram (om databasen används)**
- **Tabeller:** 👤 Användare, ✂️ Frisörer, 📅 Kunder, 📊 Bokningar, 🛠️ Tjänster
- **Relationer:**
  - ✂️ En frisör har flera bokningar.
  - 👤 En kund kan ha flera bokningar.
  - 📅 En bokning är kopplad till en tjänst.

## **5. 🏗️ Projektplanering**

### **🛠️ Arbetsmetod och Verktyg**

**🛠️ Verktyg:**
- Vi använder **Trello** 📋 för att hantera uppgifter och epics:
  - **Epics:** Bokningssystem, Användarhantering, Notifieringar.
  - **Tasks:** Implementera bokningslogik, Skapa UI, Skapa API för bokningar.

**🚀 Arbetsmetod:**
- Vi använder **Scrum** med tvåveckors sprintar där varje sprint inkluderar planering, utveckling och testning.
- Varje sprint avslutas med en demo och retrospektiv för att förbättra arbetsflödet. 🔄


