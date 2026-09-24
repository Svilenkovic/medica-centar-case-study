<a href="https://medicacentar.info/"><img src="media/cover.jpg" alt="Medica Centar, naslovna strana na laptopu i telefonu" width="100%"></a>

# Medica Centar

Nov sajt ginekološke ordinacije u Nišu: 55 strana usluga iz JSON fajlova, 69 preusmerenja sa starog sajta i panel kojim ordinacija sama menja sadržaj.

**[medicacentar.info](https://medicacentar.info/)** · [Studija slučaja](https://svilenkovic.rs/radovi/medica-centar) · [English](README.md)

> [!NOTE]
> Klijentski projekat. Izvorni kod pripada klijentu i čuva se u privatnom repozitorijumu. Ova stranica opisuje šta sam uradio i kako.

<table>
  <tr><td><b>Klijent</b></td><td>Medica Centar</td></tr>
  <tr><td><b>Delatnost</b></td><td>Ginekologija, akušerstvo i laserska kozmetologija</td></tr>
  <tr><td><b>Lokacija</b></td><td>Niš</td></tr>
  <tr><td><b>Vrsta</b></td><td>Sajt sa više strana i admin panelom</td></tr>
  <tr><td><b>Moj deo posla</b></td><td>Redizajn, izrada, selidba, SEO i održavanje</td></tr>
  <tr><td><b>Tehnologije</b></td><td>PHP 8.3, JSON content, AVIF, SVG, Schema.org</td></tr>
</table>

## O projektu

Medica Centar je privatna ginekološko-akušerska ordinacija u Nišu koja od 2002. radi u tri oblasti: ginekologija, vođenje trudnoće i laserska kozmetologija. Stari sajt je bio skup statičnih HTML strana koji nije radio na telefonu. Ipak je nosio duge stručne tekstove lekara ordinacije, 94 rada u PDF-u i 11 video snimaka, pa u selidbi nije smela da se izgubi nijedna adresa.

Nov sajt ima 55 strana usluga (25 u ginekologiji, 10 u trudnoći i 20 u kozmetologiji) i nema bazu. Sadržaj je u JSON fajlovima, po jedan za svaku uslugu i svaku oblast, a prikazuje ga nekoliko zajedničkih šablona. Panel koji sam dodao kasnije upisuje u iste fajlove i čuva poslednjih 25 kopija svakog. Skripta je proverila svih 69 preusmerenja sa starih adresa i po statusu i po odredištu, a arhiva je vraćena tačno na adrese na kojima je bila.

## Šta sam uradio

- Panel sa CSRF zaštitom, zaključavanjem posle pet promašenih prijava u 15 minuta, atomičnim upisom i dnevnikom izmena
- Provera panela koja svaku sekciju pošalje bez izmena i uporedi HTML strane pre i posle; u svih deset sekcija HTML je ostao isti, bajt u bajt
- Miran dizajn sa jednim prigušenim akcentom i otkrivanje naslova reč po reč bez maske sa overflow: hidden, koja je sekla kvačice na š, ć i đ
- Logo precrtan u SVG sa PNG-a od 300 sa 80 piksela, i sve fotografije u AVIF formatu, najveća od 52 KB
- MedicalClinic podaci i BreadcrumbList na 68 strana, a FAQPage na 53 strane, sastavljen od 178 pitanja koja su već bila napisana na stranama usluga
- Kontakt forma preneta na klijentov hosting sa lokalnom kopijom zaštitnog modula na koji se oslanjala, testirana uz privremenog primaoca da ordinacija ne dobije probne poruke

## Snimci ekrana

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Medica Centar, naslovna strana na ekranu širine 1440 px"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Medica Centar, naslovna strana na telefonu"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="Tri oblasti pod jednim krovom: ginekologija, trudnoća i kozmetologija">
<sub>Tri oblasti pod jednim krovom: ginekologija, trudnoća i kozmetologija</sub>

<img src="media/inner-2.webp" alt="Istaknuti blok o HPV-u i kondilomima, pa razlozi zašto Medica Centar">
<sub>Istaknuti blok o HPV-u i kondilomima, pa razlozi zašto Medica Centar</sub>

---

<sub>Izrada: [D. Svilenković](https://svilenkovic.rs).</sub>
