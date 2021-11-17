"# Loan-application" 
# Opis projektu:

Lending Club to firma pożyczkowa typu peer-to-peer, która łączy pożyczkobiorców z inwestorami za pośrednictwem platformy internetowej. Obsługuje osoby, które potrzebują pożyczek osobistych w wysokości od 1000 do 40 000 USD. Pożyczkobiorcy otrzymują pełną kwotę udzielonej pożyczki pomniejszoną o opłatę początkową, która jest uiszczana firmie. Inwestorzy kupują weksle zabezpieczone osobistymi pożyczkami i płacą Lending Club opłatę za usługę. Firma Lending Club udostępnia dane o wszystkich pożyczkach udzielonych za pośrednictwem swojej platformy w określonych okresach.
Na potrzeby tego projektu zostały użyte dane dotyczące pożyczek udzielonych za pośrednictwem Lending Club na przestrzeni lat 2007 -2011. Każda pożyczka jest opatrzona informacją o tym, czy ostatecznie została spłacona (Fully Paid lub Charged off w kolumnie loan_status). 

**Celem projektu jest zbudowanie modelu klasyfikacyjnego, który na podstawie podanych danych będzie przewidywał z określoną dokładnością, czy potencjalny pożyczkobiorca spłaci swój dług z tytułu zaciągniętej pozyczki.**

Poniżej zaprezentowane są poszczególne etapy analizy, których wykonanie jest konieczne do zaliczenia projektu:

* Obróbka danych (Data Processing)
Zmienione kolumny:
    * term
    * grade
    * emp_length
    * home_ownership
    * verification_status
    * loan_status
    * int_rate

Zastosowałam funkcje map i apply lambda.

* EDA + Dodatkowo odpowiedz na poniższe pytania
Odpowiadając na poniższe pytania wykorzystałam działania matematyczne oraz funkcje gropuby, count, apply, pętle for: 
    * W jaki sposób wynik FICO wiąże się z prawdopodobieństwem spłacenia pożyczki przez pożyczkobiorcę?
    * W jaki sposób wiek kredytowy wiąże się z prawdopodobieństwem niewykonania zobowiązania i czy ryzyko to jest niezależne lub związane z wynikiem FICO
    * W jaki sposób status kredytu hipotecznego na dom wiąże się z prawdopodobieństwem niewypłacalności?
    * W jaki sposób roczny dochód wiąże się z prawdopodobieństwem niewykonania zobowiązania?
    * W jaki sposób historia zatrudnienia wiąże się z prawdopodobieństwem niewykonania zobowiązania?
    * Jak wielkość żądanej pożyczki jest powiązana z prawdopodobieństwem niewykonania zobowiązania?

Do Analizy wykorzystałam pandas_profiling. Wygenerowanyplik html jest dostępny wśród plików w folderze.

* Feature Engineering
Kluczowym wskaźnikiem spłaty pożyczki był wynik FICO. W tym kroku zrobiłam segmenty z kolumny last_fico_range_high, za pomocą funkcji appy w oparciu o dane segmenty FICO.
Usuwanie outliersów oraz kolumny indeskującej.
Wykonanie standaryzacji
PCA


* Klasteryzacja
metoda łokcia - elbow-curve
DBSCAN
K-means

* Modelowanie 
Decision Tree
Random Forest
Support Vector Machine (SVM)
REgresja logistyczna

Modele przy użyciu skompresowanych danych PCA
