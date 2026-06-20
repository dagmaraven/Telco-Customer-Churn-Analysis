[Wersja angielska (English version)](README.md)
# Telco-Customer-Churn-Analysis

---
## Zbiór danych
Zbiór danych wykorzystany w tym projekcie pochodzi z platformy Kaggle:
https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data

---
## Wykorzystane Technologie i Architektura
* **Inżynieria i Przetwarzanie Danych:** Python (Pandas)
* **Narzędzie BI i Wizualizacja:** Power BI Desktop
* **Modelowanie Danych:** Model Gwiazdy (Relacje 1:N)
* **Analityka i Miary:** DAX (Data Analysis Expressions)

### Architektura Modelu Danych
W celu zapewnienia błyskawicznego działania raportu oraz profesjonalnej struktury, surowa, płaska tabela została przekształcona w zoptymalizowany **Model Gwiazdy**:
* **Tabela Faktów:** `Fact_Churn` (Przechowuje miary liczbowe: Monthly Charges, Total Charges, Tenure oraz status Churn)
* **Tabele Wymiarów:** `Dim_Demographics`, `Dim_Services`, `Dim_Contracts`

---

## Kluczowe Miary Biznesowe (DAX)
* **Total Customers:** Precyzyjna liczba unikalnych identyfikatorów klientów odzwierciedlająca rzeczywistą wielkość bazy klienckiej.
* **Churn Rate:** Procentowy wskaźnik klientów, którzy zrezygnowali z usług firmy.
* **Lost Revenue:** Skumulowana wartość miesięcznych opłat utraconych w wyniku odejścia klientów, sformatowana w USD ($) z separatorem tysięcy.

---

## Główne Wnioski i Rekomendacje Biznesowe
1. **Krytyczne Pierwsze 12 Miesięcy:** Najwięcej klientów rezygnuje w pierwszym roku stażu (0-12 msc). Kluczowe jest wdrożenie specjalnych programów powitalnych (onboardingowych) oraz wzmożone wsparcie klienta w tym okresie.
2. **Wpływ Typu Umowy:** Umowy z miesiąca na miesiąc (Month-to-month) generują zdecydowaną większość odpływu. Wdrożenie zachęt finansowych skłaniających do przejścia na umowy roczne lub dwuletnie ustabilizuje przychody firmy.
3. **Ryzyko Metod Płatności:** Osoby płacące za pomocą *Electronic Check* odchodzą znacznie częściej niż osoby korzystające z płatności automatycznych (*Karta kredytowa* lub *Przelew bankowy*). Promowanie automatyzacji płatności (np. drobny rabat za podpięcie karty) pomoże utrzymać klientów.

---
