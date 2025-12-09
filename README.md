<html lang="da">

# Multiemediedesign 1. semester

## Tema 3 - Interaktiv touchskærm i Storcenter Nord

#### Indhold i denne readme-fil

1. Mappe struktur
2. Udvalgt forbedringer i min kode

<br><br>

## Mappestruktur

#### I min rodemappe, har jeg mine `.html` filer:

- `index.html`
- `spilleside.html`
- `fiskman.html`

#### Så har jeg en `.css` mappe, hvori der ligger:

- `fiskman.css`
- `spilleside.css`
- `styles.css`

#### En `.js` mappe, hvori der ligger:

- `fiskman.js`
- `script.js`

#### 3 forskællige `img` mapper, som høre til hver deres `.html`:

- `fiskman-img`
- `img`
- `spilleside-img`

#### Udover dem har jeg også tilføjet en `sound` mappe, hvori alle mine lydfiler ligger.

#### For at gøre det nemt og overskuligt, har jeg kaldt filerne inde i mapperne det (næsten) samme som den `.html` de høre sammen med - for at hurtigt kunne navigere rundt.

> ##### Dvs. fx. er jeg i min `fiskman.html` og skal linke over til min tilhørene js - så kan jeg hurtigt se at det er den med samme navn. I det her tilfælde `fiskman.js`.

<br><br>

## Udvalgt forbedringer i min kode

### Jeg har lavet en Pulse animation til spil knappen (og hjem knappen)

#### Koden lyder som følgende:

```
.spillesideBtn {
  animation: pulse 2s infinite ease-in-out;
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.12);
  }
  100% {
    transform: scale(1);
  }
}
```

`0%` → startpunkt: Elementet vises i normal størrelse `scale(1)`. <br><br>
`50%` → midtpunkt: Elementet vokser til 112% af sin størrelse `scale(1.12)`. <br><br>
`100%` → slutpunkt: Elementet kommer tilbage til normal størrelse.

#### Koden viser en 2 sekunders animation. Knappen får en ease-in-out bevægelse, hvor den vokser langsomt op → bliver stort i midten → falder tilbage... Denne har jeg sat til at gentage uendeligt.

<br><br>

### Ekstra spilleside tilføjet

#### Jeg tilføjet en ekstra `.html` side for at kunne tilføje ekstra spil.

#### Før min forbedret version, gik man direkte fra `index.html` til `fiskman.html` (spillet) - men efter min forbedring har jeg tilføjet en side ind imellem.

#### Den nye side `spilleside.html` skal fungere som en "mellemskærm" for brugeren.

#### På skærmen ser man en søstjerne, som giver en tydelig call-to action. Og 5 spil.

#### Ideen er, at når man trykker ind på et af de 5 spil, kommer man så vidre til selve spillet.

> Lige nu er det kun det første spil `fiskman` der virker.

#### How to:

1. Jeg startede med at oprette en ny `spilleside.html`, med tilhørene `spilleside.css` og `spilleside-img`.
2. Derefter gik jeg tilbage til min `index.html` hvor jeg linkede ind til den nye `spilleside.html` - og gav den en class `spillesideBtn`. Jeg indsatte et billedet `spilleside-knap` fra mappen `img` - og sådane er knappen lavet. Koden under viser hvordan:

```
    <a href="spilleside.html" class="spillesideBtn">
      <img src="img/spilleside-knap.png" alt="spilleside knap" />
    </a>
```

3. På samme måde knappen for spillesiden er lavet, har jeg også lavet en `hjem-knap` → som føre hjem til min `index.html` side.
   > På samme måde er mit første spil `fiskman` også lavet på `spilleside`.
   > De andre spil har fået et # ind som placeholder, der hvor linket til den `.html` side der passer til hver spil skulle være (de er ikke oprettet i nu, kun til det første spil `fiskman`).
4. Efter alle knapper og links var tilføjet, gik jeg igang med styling af den nye side `spilleside.html`, som forgik på `spilleside.css`.

</html>
