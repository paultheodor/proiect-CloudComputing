# Proiect Cloud Computing

&emsp;&emsp;&emsp;Apariția fenomenului, cunoscut sub denumirea de cloud computing, reprezintă o schimbare
fundamentală în felul în care sunt dezvoltate, livrate, actualizate, întreținute și plătite serviciile
IT din cadrul organizațiilor moderne. Cloud computing-ul este conceptul care aduce cele mai mari schimbări în evoluția dinamică a
tehnologiei informației și comunicației (IT&C). Zilnic oamenii generează, accesează,
prelucrează și stochează seturi de date noi, beneficiind de mai multă putere de procesare decât
oricând înainte. Pentru corporații, o consecință profundă a acestui consum digital în creștere
este necesitatea de a investi permanent sume de bani în echipamente de prelucrare și stocare.
Serviciile cloud computing devin adevărate incubatoare pentru noile aplicații, menite să
răspundă cererii de obținere rapidă de informații și acces facil la acestea.
<br/>
&emsp;&emsp;&emsp;Pentru accesul la platformele PaaS, dar și pentru personalizarea aplicațiilor SaaS sau
automatizarea operațiunilor din zonele IaaS, furnizorii de cloud, pun la dispoziția
programatorilor o serie de interfețe de programare a aplicațiilor (API) care permit:
- Definirea structurilor de date ale aplicațiilor și obiectelor;
- Crearea vectorilor necesari manipulării structurilor de date și obiectelor;
- Crearea interogărilor pentru obținerea datelor din zonele de stocare și a stării
obiectelor;
- Implementarea mecanismelor tranzacționale și altele.

<br/>
&emsp;&emsp;&emsp;În formele cele mai simple API-urile sunt oferite sub forma unor servicii web apelabile printrun URL oferit de furnizor, dar și cele mai complicate modele de API-uri în format SOA folosesc
protocolul de comunicare HTTP/HTTPS și metodele GET, POST, PUT, DELETE. Din punct de vedere al reprezentării, API-urile sunt furnizate în formatele standard XML sau JSON. 
<br/>
&emsp;&emsp;&emsp;Avantajul oferit de API-uri este acela al uniformizării interfețelor de utilizator prin utilizarea unor componente de interfață predefinite și funcții și librării de acțiuni standard ale aplicației (Salvare, Ștergere, Editare etc.)
<br/>
&emsp;&emsp;&emsp;Pentru a veni în sprijinul firmelor producătoare de software, marii furnizori de cloud au început
să pună la dispoziția acestora API-uri și instrumente de gestionare a API-urilor proprii. Putând
fi un cadru suficient de stabil de dezvoltare a aplicațiilor, firmele își dezvoltă propriile sale
module API pentru aplicațiile pe care le creează și dezvoltă asigurând o integrare strânsă între
diferite module, precum și un control al versiunilor superior pe viitor.
<br/>
&emsp;&emsp;&emsp;În contextul modelului de securitate, există încă preocupări legate de securizarea API-urilor
proprii, dar și a modului în care API-urile furnizor sunt utilizate și exploatate în aplicații client
pentru accesul la cloud. De exemplu, fiecare metodă de autentificare printr-un API presupune
ca utilizatorul să fie de acord ca datele sale vor fi accesibile companiei care a realizat aplicația.
Suspiciunile de acces neautorizat sunt de multe ori confirmate de aplicații care nu sunt suficient
testate sau care sunt construite în scopul extragerii datelor personale, iar avertismentele din
momentul instalării sunt ignorate de utilizatori.
## Descriere problemă
&emsp;&emsp;&emsp;În cadrul acestui proiect am vrut să abordez o problemă ce o să apară atunci când pandemia de COVID-19 o să dispară și anume promovarea turismului în România. Astfel, mi-am propus să creez un site web prin intermediul căruia utilizatorii să poată vedea, pe scurt, o prezentare a unui motel, hotel, pensiune sau chiar lanț hotelier, să poată vedea vremea din locația respectivă, să poată să-și verifice programul pentru a putea vedea în ce perioadă se pot duce și cel mai important, pentru a putea vedea principalele puncte de atracție din orașul/zona repsectivă.
<br/>
&emsp;&emsp;&emsp;Astfel, prin intermediul aplicației web se pot realiza lucrurile anterior menționate, toate acestea fiind posibile cu ajutorul a trei API-uri. Astfel, utilizatorii vor putea să reducă timpul atunci când vor dori să-și caute locația și perioada pentru următoarea vacanță deoarece vor avea posibilitatea să vadă prognoza meteo din zona respectivă, vor putea să-și verifice toate evenimentele din calendarul Google și vor putea să vadă atracțiile principale, toate informațiile aflându-se într-o singură pagină.
## Prezentare API-uri utilizate
&emsp;&emsp;&emsp;În cadrul site-ului am folosit trei API-uri diferite, toate fiind utile atunci când vine vorba despre un site destinat unui lanț hotelier.
<br/>
&emsp;&emsp;&emsp;Primul API folosit este openweathermap. OpenWeatherMap este un serviciu online care oferă date meteorologice, inclusiv date meteorologice curente, prognoze și date istorice dezvoltatorilor de servicii web și aplicații mobile. Pentru sursele de date, utilizează servicii de difuzare meteorologică, date brute de la stațiile meteo din aeroport, date brute de la stațiile radar și date brute de la alte stații meteorologice oficiale. Toate datele sunt prelucrate de OpenWeatherMap într-un mod în care încearcă să furnizeze date precise de prognoză online și hărți meteo, cum ar fi cele pentru nori sau precipitații. Dincolo de asta, serviciul este axat pe aspectul social, implicând proprietarii stațiilor meteo în conectarea la acest serviciu și, prin urmare, creșterea preciziei datelor meteo. 
În cadrul proiectului, acest API este pus sub forma unui search bar dar poate să fie configurat astfel încât să afișeze prognoza meteo pe o perioadă de timp într-o anumită locație.
<br/>
&emsp;&emsp;&emsp;Al doilea API folost este Google Maps Javascript API. Prin intermediul acestui api putem să personalizăm hărți(google maps) cu propriul conținut și imagini pentru a le putea afișa pe pagini web și chiar și pe dispozitive mobile dacă dorim. API-ul include patru tipuri de hărți de bază (foaie de parcurs, satelit, hibrid și teren) pe care utilizatorul le poate modifica utilizând straturi și stiluri, controale și evenimente, poze și diverse servicii și biblioteci.
<br/>
&emsp;&emsp;&emsp;Ultimul API folosit este Google Calendar. Milioane de utilizatori folosesc aplicția Google Calendar pentru a urmări evenimentele lor. Prin intermediul acestui API se pot găsi, adăuga și vizualiza evenimente din calendarul public. Dacă utilizatorul are autorizație, poate accesa și modifica evenimente private.
Prin intermediul acestui API, aplicațiile mobile, aplicațiile web și alte sisteme pot crea, afișa sau se pot sincroniza cu datele din calendar.

## Flux de date și exemple de request / response
&emsp;&emsp;&emsp;În cadrul proiectului există trei fluxuri de date diferite, fiecare flux fiind caracteristic unui API după cum urmează:
API-ul OpenWeatherMap primește pe baza unui search bar un șir de caractere care trebuie să fie neapărat denumirea unui oraș, comună sau sat pentru a putea funcționa.
Prin intermediul ajax programul verifică dacă locația introdusă este corectă și prin intermediul unui GET aduce detaliile despre vreme și le afișează. Toate aceste lucruri putând fi vizualizate în cele ce urmează:
```javascript
{
    var city = $("#city").val();
     $.ajax({
              url:'http://api.openweathermap.org/data/2.5/weather',
              dataType:'json',
              type:'GET',
              data:{q:city, appid: key, units: 'metric'},

              success: function(data){
                var wf = '';
                $.each(data.weather, function(index, val){
                  wf += data.name + ' ' + data.main.temp + '&deg;C ' + 
                  ' | ' + val.main + ", " + val.description 

                });
              
               $(".ShowWeatherForcast").html(wf);

                
}

```
<br/>
&emsp;&emsp;&emsp;API-ul Google Maps Javascript este folosit pentru a particulariza o hartă clasică de google maps după bunul plac. Prin intermediul următoarei linie de cod putem particulariza asupra cărei locații să fie centrată harta atunci când utilizatorul accesează site-ul și cât de aprope/departe(zoom) să se afle de acea locație.

```
  var options = {
        zoom:16,
        center:{lat:44.714754,lng:26.641742}
      }
      
  var map = new google.maps.Map(document.getElementById('map'), options);
```
&emsp;&emsp;&emsp;De asemenea, prin intermediul acestui API am ales să particularizez harta astfel încât să conțină toate punctele de interes din orașul Urziceni sub forma unor markere. Aceste puncte sunt afișate pe hartă pe baza coordonatelor dintr-un fișier json și conțin o descriere succintă și o imagine preluată de pe site-ul: http://kml4earth.appspot.com/icons.html.
Aceste markere personalizate sunt aduse și afișate pe baza următoarelor linii de cod:
 ```
 let fisier = `./markers.json`
                
        let response = await fetch(fisier)
        let markers = await response.json()
        console.log(markers)
      
      // Parcurgere markere
      for(var i = 0;i < markers.length;i++){
        // adăugare marker
        addMarker(markers[i]);
      }

      // funția de adăugare marker
      function addMarker(props){
        var marker = new google.maps.Marker({
          position:props.coords,
          map:map,
          //icon:props.iconImage
        });
```
&emsp;&emsp;&emsp;Un marker fiind reprezentat în fișierul json sub forma:

 ```
    {
    "coords":{"lat":44.713662,"lng":26.652788},
    "iconImage":"https://developers.google.com/maps/documentation/javascript/examples/full/images/beachflag.png",
    "content":"<h1>Hotel Royal 1</h1>"
    }
 ```
 
<br/>
&emsp;&emsp;&emsp;Ultimul API, Google Calendar, folosește o funcție makeApiCall prin intermediul căreia utilizatorul este redirecționat în aplicație Google Calendar atunci când dorește să introducă un evenimemt. Acest API, poate să fie sincronizat cu aplicația Google Calendar și astfel poate să afișeze toate evenimentele pe care le are utilizatorul. 
 ```
 <button id="btnCreateEvents" class="btn btn-primary" onclick="makeApiCall();"> Create Events</button>  
 ```
## Descriere erori și rezolvarea lor
&emsp;&emsp;&emsp;În cadrul proiectului am întâmpinat destul de multe erori atunci când încercam să dezvolt interfața sau atunci când doream să integrez API-urile în aplicație. Dintre aceste erori, două mi s-au părut destul de simple dar și interesante în momentul în care am găsit soluțiile pentru a le rezolva.
<br/>
&emsp;&emsp;&emsp;Prima eroare pe care am întâmpinat-o a fost din cauza API-ului Google Maps Javascript, acesta neputănd genera hărțile din cauza următoarelor erori: "apinotactivatedmaperror" și "invalidkeymaperror". Partea cea mai bună a fost că google oferă link-uri sub mesajele de eroare care redirecționează utilizatorul într-o pagină de help care are rezolvări pentru toate mesajele de eroare. Mesajele anterior menționate apăreau din cauză că nu aveam generat un AP Key valid și nu aveam API-ul activat pe contul meu de google cloud. Partea interesantă a acestor erori este reprezentată de faptul că harta nu este disponibilă în totalitate, ea fiind "For development purposes only". Acest lucru apare deoarece google dorește ca utilizatorii să înregistreze un card de credit pentru a-i putea taxa în funcție de câți utilizatori interacționează cu harta(pentru site-urile web prețul este de 2$ la fiecare 1000 de utilizatori).
<br/>
&emsp;&emsp;&emsp;A doua eroare am întâmpinat-o în momentul în care am dorit să fac API-ul Google Maps Javascript să preia markerele din fișierul json. Eroarea "unexpected fetch token" apărea din cauză că încercam să preiau datele asincron din fișierul json prin intermediul funcției await dar funcția care crea harta nu era o funcție asincronă. Această problemă a fost rezolvată prin modificarea funcției de creare a hărții astfel încât să fie una asincronă. 
 ```
    //funcția de inițializare a hărții
    async function initMap()
    
    //funcțiile care preiau datele asincron din fișierul json
    let response = await fetch(fisier)
    let markers = await response.json()
    console.log(markers)
```
## Bibliografie
&emsp;&emsp;&emsp;Valerică Greavu-Șerban (2015) Cloud Computing Caracteristici și Modele, București: Editura ASE
