# bioinformatyka-strukturalna
Zbiór i ocena jakości i aktualności narzędzi do przewidywania struktury drugorzędowej RNA

Cele:
- zebranie informacji na temat metod przewidywania struktury drugorzędowej RNA,
- porównanie metod (dostępność, aktualizacje, dostęp, ograniczenia, szybkość działania, format wejścia i wyjścia, struktury).

<h5>Plan ramowy projektu:</h5>
<p>
1. Wstęp teoretyczny na temat struktury drugorzędowej RNA.<br />
  a) Czym jest RNA?<br/>
    - z czego zbudowane jest RNA?<br/>
  b) Typy RNA<br/>
  c) Struktury RNA:<br/>
    - pierwszorzędowa - kolejność aminokwasów w sekwencji,<br/>
    - drugorzędowa - ułożenie w przestrzeni dwuwymiarowej (płaszczyznie), mogą występować pary,<br/>
2. Opisanie każdej z metod.<br />
3. Zestawienie opcji.<br />
4. Porównanie ich i ocena poszczególnych narzędzi.<br />
5. Podsumowanie i ocena ogólna.<br />
</p>

<h4>Etap I: Zebrane informacje</h4>
Metody lokalne:
- Afold
- Carnac
- DotKnot
- HotKnots
- IPknot
- Pknots
- PknotsRG
- ProbKnot
- McQFold
- MaxExpect
- RNASampler
- RNAfold

Metody webowe:
- CMfinder
- Alterna
- Cylofold

<h4>Etap II: Wykonanie wstępu teoretycznego</h4>
- Co to jest RNA?
- Struktura pierwszorzędowa, drugorzędowa RNA?

<h4>ETAP III: Wykonanie opisu każdej z metod</h4>
Opis każdego z narzędzi zawierający podstawowe informacje.

<h4>Etap IV: Zestawienie</h4>
Wykonanie tabeli. W wierszach będą znajdować się kolejne metody. W kolumnach natomiast będą opcje.

<h4>Etap V: Porówanie</h4>
- Ocena wszystkich narzędzi ze względu na różne parametry, m.in. dostępność, aktualizacje, dostęp, ograniczenia, szybkość działania, format wejścia i wyjścia, struktury.

<h4>Etap VI: Podsumowanie</h4>
- Zbiorcza ocena wszystkich narzędzi.
- Jaki jest planowany rozwój danych metod?


<h4>Bibliografia:</h4>
- Lubert Stryer: Biochemia. Warszawa: Państwowe Wydawnictwo Naukowe
- Aleksey Y. Ogurtsov, Svetlana A. Shabalina, Alexey S. Kondrashov, Mikhail A. Roytberg: Analysis of internal loops within the RNA      secondary structure in almost quadratic time
- Matthew G. Seetin: RNA Structure Prediction: Advancing Both Secondary and Tertiary Structure Prediction
- Matthew G. Seetin and David H. Mathews: TurboKnot: rapid prediction of conserved RNA secondary structures including pseudoknots



<br/><br/><br/><br/>
<h3>Wstęp teoretyczny</h3>
<h4>1. RNA - definicja</h4>
<p>RNA, zwane inaczej kwasem rybonukleinowym, to długa liniowa makrocząsteczka polinukleotydowa.  Nukleotydy połączone są wiązaniami fosfodiestrowymi 3’→ 5’. Każdy nukleotyd zbudowany jest z jednostki cukrowej, przynajmniej jednej reszty fosforanowej oraz zasady azotowej. W przypadku RNA resztą cukrową jest ryboza oraz wyróżniamy cztery podstawowe zasady azotowe: adeninę oznaczaną literą A, guaninę (G), cytozynę (C) i uracyl (U). 
Cząsteczki RNA występują głównie w postaci pojedynczej nici, jednakże łańcuch RNA może się zwinąć i stworzyć strukturę spinki do włosów o budowie dwuniciowej helisy. W tych strukturach adenina tworzy pary z uracylem, a guanina z cytozyną. 
</p>
<h4>2. Struktury RNA</h4>
a) pierwszorzędowa<br/>
  Strukturę pierwszorzędową RNA definiujemy jako ciąg nukleotydów ułożonych jeden po drugim.
  
b) drugorzędowa<br/>
  Strukturę drugorzędową RNA definiujemy jako ułożenie ciągu nukleotydów na płaszczyźnie. Strukturami, jakie możemy zauważyć są m.in. spinki do włosów, wybrzuszenia, pętle wewnętrzne, węzły, pseudowęzły oraz odcinki dwuniciowe.<br/>
  Spinka do włosów (hairpin) - struktura składająca się z części dwuniciowej oraz pętli zewnętrznej. (rysunek)<br/>
  Wybrzuszenie (bulge loop) - struktura składająca się z przynajmniej dwóch niesparowanych nukleotydów tylko na jednej z nici.<br/>
  Pętla wewnętrzna (internal loop) - struktura składająca się z niesparowanych nukleotydów na obu niciach pomiędzy dwoma odcinkami podwójnej helisy. (rysunek)<br/> 
  Węzeł (junction) - rozgałęzienie przynajmniej trzech odcinków podwójnej helisy. (rysunek)<br/>
  Pseudowęzeł (pseudoknot) - struktura opierająca się na oddziaływaniach pomiędzy nukleotydami wchodzącymi w skład innej struktury, np. spinki do włosów, a innymi nukleotydami. (rysunek)<br/>
  
Często zdarza się, że zasady nie tworzą idealnych par typu Watsona-Cricka. Uracyl może tworzyć parę z guaniną, ponieważ występują wiązania wodorowe pomiędzy N3 uracylu i C6 guaniny oraz C2 uracylu i N1 guaniny. Jednakże para guaniny i cytozyny jest od niej silniejsza. 
  
  Najbardziej znanym przykładem struktury drugorzędowej RNA jest tRNA, które wyglądem przypomina liść koniczyny.

<h4>3. Typy RNA</h4>
a) mRNA
b) rRNA
c) tRNA
d) microRNA
e) sRNA            


<h3>Metody</h3>
<h4>Afold</h4>
- złożoność: O(L^3) lub O(M*log^2L), gdzie M<L^2 i oznacza liczbę możliwych par nukleotydów, L oznacza długość łańcucha RNA.
- dostępność: przez serwer ftp na system Linux i Windows.

<h4>Carnac</h4>


<h4>CentroidFold</h4>

<h4>ContraFold</h4>
- strona internetowa: http://contra.stanford.edu/contrafold/
- zaimplementowany w C++,
-	metoda oparta warunkowych modelach logarytmiczno-liniowych, probabilistycznych modelach uogólniających stochastyczną gramatykę bezkontekstową (SCFGs) poprzez funkcje wyższych punktacji,
-	metoda osiąga wysoką dokładność predykcji pojedynczego ciągu,
-	metoda łączy techniki probabilistyczne z fizycznymi. Jest to odpowiedź na lukę pomiędzy metodami probabilistycznymi a termodynamicznymi udowadniając, że procedury uczenia statystycznego mogą stanowić skuteczną alternatywę dla empirycznego pomiaru parametrów termodynamicznych do przewidywania struktury drugorzędowej RNA,
-	wyniki można przesłać sobie bezpośrednio na wcześniej podanego maila lub otworzyć je w przeglądarce od razu po wykonaniu,
-	 mamy dwie opcje do wyboru pod względem parowania się nukleotydów. Możemy wybrać opcję domyślną typu Watsona-Cricka lub dopuścić parowanie się wszystkich możliwych. 





