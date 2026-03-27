## Läksyt: [h1](https://terokarvinen.com/verkkoon-tunkeutuminen-ja-tiedustelu/#:~:text=Page%20Using%20Github-,h1,-Sniff) - sniff.

1. Karvinen 2025: [Wireshark - getting started](https://terokarvinen.com/wireshark-getting-started/)
   - Wiresharkin asennus ja sen konfigurointia
   - Käyttäjän lisääminen tarkkailua varten
   - Miten avataan wireshark komentokehotteen avulla
   - Pakettien "sniffailua"
   - Valitaan mitä halutaan etsiä
     - "any" valinta valitsee kaiken liikenteen ja helpottaa etsimistä
     - Pakettien kaappauksen pystyy lopettamaan painamalla "Stop". Uuden kaappauksen voi aloittaa menemällä "Capture" menun "Options" kohtaan ja painamalla sinistä hainevää vasemmassa yläkulmassa.

   - Jos paketteja ei näy, kokeile esim. selata webbiä, jos ei vieläkään näy tarkosta, että olet jossain ryhmässä "groups" komennolla.
   - Pakettien tallentaminen ja lataaminen:
     - Tallennetaan paketti: File -> Save as
     - Dialog: Save Capture file as: filenameexample.pcap -> Save as "Wireshark/tcpdump/... -pcap"
     - Tiedoston avaaminen: File -> Open ja painetaan "Select your file"
       - Ladattua tiedostoa voi analysoida samalla tavalla kuin reaaliaikaista pakettien "sniffausta"
   - Statistiikka:
       - Päätepisteet: Lista isännöistä/palvelimista joita voit tarkistella.
       - I/O kaaviot: Millon ns. liikenne palvelimella tapahtui ja kauan paketteja kaapattiin.
       - Protokollan hierarkia: Kertoo, onko jokin HTTPS vai telnet, filterit vaikuttavat mitä täällä näkyy. Nähdäksesi kaiken nollaa filterit.
   - Filteröinti:
     - Voit filteröidä, mitä kaapatusta datasta näytetään:
       - DNS(Domain Name System) Näyttää, mitä DNS käytetään.
       - TLS(Transport layer security) Näyttää tsl-suojatut paketit, tähän sisältyy lähes kaikki internetselailu
       - HTTP(Hypertext transfer protocol)Suojaamattomat HTTP yhteydet
       - tcp.port == 443, etsii portilla 443 ulostulevan ja menevän liikenteen.
       - ip.addr == 192.167.122.7, sama kuin aikaisempi, mutta ip:n kautta.
       - frame contains "terokarvinen.com", hakee kaiken tietyllä merkkijonolla.
     - Voit myös filteröidä painamalla pakettia hiiren oikealla napilla ja valitsemalla "Apply as Filter..." ominaisuuden.
    
  // work in progress.
