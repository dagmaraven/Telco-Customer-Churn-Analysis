[Wersja angielska (English version)](README.md)
# Telco-Customer-Churn-Analysis
Projekt koncentruje się na analizie odejść klientów (customer churn) w firmie telekomunikacyjnej z wykorzystaniem języka Python do przygotowania danych oraz Power BI do raportowania i wizualizacji biznesowej.

Celem projektu było zidentyfikowanie czynników najbardziej wpływających na rezygnację klientów z usług, oszacowanie finansowych skutków churnu oraz przedstawienie rekomendacji, które mogłyby pomóc w poprawie retencji klientów. Projekt obejmuje pełny proces analityczny – od czyszczenia danych i eksploracyjnej analizy danych (EDA), przez modelowanie danych i tworzenie miar DAX, aż po budowę interaktywnego dashboardu biznesowego.

---
## Zbiór danych
Zbiór danych wykorzystany w tym projekcie pochodzi z platformy Kaggle:
https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data

Zbiór zawiera informacje demograficzne, subskrybowane usługi, szczegóły umów, informacje o rozliczeniach oraz status odejścia (churn) dla ponad 7 000 klientów firmy telekomunikacyjnej.

---


## Problem Biznesowy
> **Które cechy klientów oraz wzorce korzystania z usług są najsilniej powiązane z ich odejściem i na jakich obszarach firma powinna skoncentrować działania retencyjne?**

---

## Struktura Projektu i Przebieg Prac
### 1. Przygotowanie i Czyszczenie Danych (Python)
Dane zostały oczyszczone, zmodyfikowane i przetworzone za pomocą języka Python i biblioteki **Pandas**. 

Kluczowe kroki inżynierii danych objęły:
* Konwersję kolumny `TotalCharges` na format numeryczny.
* Obsługę brakujących wartości.
* Segmentację klientów na podstawie ich stażu (tenure) w firmie.
* Obliczenie łącznej liczby usług subskrybowanych przez każdego klienta.
* Przeprowadzenie eksploracyjnej analizy danych (EDA).
* Analizę korelacji pomiędzy zmiennymi numerycznymi.
* Eksport oczyszczonego zbioru danych na potrzeby Power BI.

---

### 2. Modelowanie Danych (Power BI)
W celu zapewnienia skalowalności, spójności danych oraz wysokiej wydajności raportowania, pierwotna płaska tabela została przekształcona w **Model Gwiazdy**.

* **Tabela Faktów:** `Fact_Churn`.
* **Tabele Wymiarów:** `Dim_Demographics`, `Dim_Services`, `Dim_Contracts`.
* **Model relacji:** Zastosowano  relacje **Jeden do wielu (1:N)**, w pełni zoptymalizowane pod kątem filtrowania analitycznego i kalkulacji DAX.

---

### 3. Tworzenie Dashboardu
Interaktywny dashboard został zaprojektowany w Power BI, aby zapewnić pełen wgląd w czynniki wpływające na churn oraz monitorować utratę przychodów.

Kluczowe funkcje dashboardu obejmują:
* Dynamiczne filtrowanie według cech demograficznych i atrybutów usług.
* Analizę wskaźnika churn w zależności od stażu klienta.
* Analizę wskaźnika churn w zależności od typu umowy.
* Analizę wskaźnika churn w zależności od metody płatności.
* Analizę wykorzystania usług przez klientów.
* Bieżące monitorowanie utraconych przychodów (revenue loss).

---

## Kluczowe Miary (DAX)

* **Total Customers:** Unikalna liczba klientów w zbiorze danych.
* **Churn Rate:** Procentowy wskaźnik klientów, którzy zrezygnowali z usług firmy.
* **Lost Revenue:** Szacowana wartość miesięcznych opłat utraconych w wyniku odejścia klientów.

---

## Główne Wnioski i Rekomendacje Strategiczne

### Klienci odchodzą najczęściej w ciągu pierwszego roku
Klienci ze stażem poniżej 12 miesięcy wykazują najwyższy wskaźnik odejść.

Wniosek ten jest poparty umiarkowaną ujemną korelacją (-0.35) pomiędzy stażem klienta a wskaźnikiem churn.

**Rekomendacja:**
* Udoskonalenie procesów wdrożeniowych dla nowych klientów (onboarding).
* Wprowadzenie programów lojalnościowych w pierwszym roku korzystania z usług.
* Zwiększenie proaktywnego zaangażowania i wsparcia klienta w ciągu pierwszych 12 miesięcy.

### Typ umowy ma kluczowy wpływ na retencję
Klienci rozliczający się z miesiąca na miesiąc (month-to-month) rezygnowali z usług znacznie częściej niż klienci posiadający długoterminowe zobowiązania.

**Rekomendacja:**
* Zachęcanie klientów do migracji na umowy długoterminowe.
* Oferowanie rabatów retencyjnych przy przejściu na umowy roczne.
* Wprowadzenie benefitów lojalnościowych przy odnawianiu kontraktów.

### Metoda płatności jest powiązana z ryzykiem odejścia
Klienci płacący za pomocą Electronic Check (czek elektroniczny) wykazywali zauważalnie wyższy wskaźnik odpływu niż osoby korzystające z automatycznych metod płatności.

**Rekomendacja:**
* Promowanie rejestracji w usłudze automatycznych płatności (AutoPay).
* Oferowanie drobnych korzyści (np. jednorazowy upust) za przejście na płatności automatyczne.
* Uproszczenie procesu płatności w celu ograniczenia barier transakcyjnych.

---

## Narzędzia i Technologie
* **Python:** Pandas, NumPy, Matplotlib, Seaborn
* **Power BI Desktop:** Power Query, Star Schema Modeling, DAX (Data Analysis Expressions)
