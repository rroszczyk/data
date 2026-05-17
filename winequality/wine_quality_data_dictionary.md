# Słownik danych Wine Quality

Źródła: `datasets/winequality.names`, `datasets/winequality-red.csv`, `datasets/winequality-white.csv`.

Uwaga o jednostkach: lokalny plik `winequality.names` nie podaje jednoznacznych jednostek dla zmiennych fizykochemicznych. W materiałach kursowych należy unikać dopisywania jednostek bez weryfikacji w dokumentacji źródłowej lub publikacji. Wyjątkiem jest `quality`, opisana jako ocena od 0 do 10, oraz `wine_type`, która jest zmienną dodawaną roboczo.

| Kolumna | Polska nazwa | Opis znaczenia | Typ danych | Jednostka | Rola analityczna | Przykładowe pytania analityczne |
|---|---|---|---|---|---|---|
| `fixed acidity` | kwasowość stała | Miara zawartości kwasów nielotnych w próbce wina. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca | Czy kwasowość stała różni się między czerwonym i białym winem? Czy koreluje z oceną jakości? |
| `volatile acidity` | kwasowość lotna | Miara lotnych kwasów związanych z profilem chemicznym wina. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca | Czy wyższa kwasowość lotna wiąże się z niższą oceną jakości? Czy rozkład jest podobny dla obu typów wina? |
| `citric acid` | kwas cytrynowy | Zawartość kwasu cytrynowego jako jedna z cech fizykochemicznych próbki. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca | Czy kwas cytrynowy odróżnia czerwone i białe wino? Czy występują wartości odstające? |
| `residual sugar` | cukier resztkowy | Ilość cukru pozostającego w winie po fermentacji. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca | Czy cukier resztkowy ma inny rozkład w winie białym niż czerwonym? Jak wpływa na gęstość? |
| `chlorides` | chlorki | Cecha fizykochemiczna związana z zawartością chlorków. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca | Czy wysokie wartości chlorków są związane z niższą jakością? Czy występują obserwacje odstające? |
| `free sulfur dioxide` | wolny dwutlenek siarki | Zawartość wolnej frakcji dwutlenku siarki. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca | Czy wolny dwutlenek siarki różni się między typami wina? Czy koreluje z całkowitym dwutlenkiem siarki? |
| `total sulfur dioxide` | całkowity dwutlenek siarki | Całkowita zawartość dwutlenku siarki w próbce. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca | Jak silna jest zależność między wolnym i całkowitym dwutlenkiem siarki? Czy wartości są wyższe w winach białych? |
| `density` | gęstość | Gęstość próbki wina. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca | Czy gęstość jest związana z cukrem resztkowym lub alkoholem? Czy rozkład gęstości różni się między typami wina? |
| `pH` | pH | Odczyn próbki wina. | liczbowy ciągły | bez jednostki | zmienna objaśniająca | Czy pH różni się między winem czerwonym i białym? Czy pH koreluje z kwasowością? |
| `sulphates` | siarczany | Cecha fizykochemiczna związana z zawartością siarczanów. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca | Czy siarczany są powiązane z oceną jakości? Czy wartości odstające wpływają na średnią? |
| `alcohol` | alkohol | Zawartość alkoholu w próbce. | liczbowy ciągły | nie podano w lokalnej dokumentacji | zmienna objaśniająca lub potencjalna zmienna modelowana | Czy alkohol jest dodatnio skorelowany z `quality`? Czy średnia zawartość alkoholu różni się między typami wina? |
| `quality` | jakość sensoryczna | Ocena jakości wina na podstawie danych sensorycznych; dokumentacja opisuje skalę od 0 do 10. | liczbowy całkowity, porządkowy | skala oceny 0-10 | zmienna celu | Jak rozkładają się oceny jakości? Czy `quality` można modelować regresją? Jakie ograniczenia ma taka interpretacja? |
| `wine_type` | typ wina | Zmienna robocza dodawana po połączeniu zbiorów, wskazująca źródło rekordu: czerwone lub białe wino. | kategoryczny | nie dotyczy | zmienna grupująca, techniczna | Czy rozkłady zmiennych różnią się między `red` i `white`? Czy model powinien uwzględniać typ wina? |
