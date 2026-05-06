# Causal Inference: Marketinq Kampaniyasının ROI Analizi 📊

Bu layihədə müşahidə məlumatları (observational data) üzərində marketinq kampaniyalarının effektivliyini ölçmək üçün **Causal Inference** (Səbəb-Nəticə əlaqəsi) metodları tətbiq olunmuşdur. Analiz zamanı həm real vəziyyət qiymətləndirilmiş, həm də modelin həssaslığını yoxlamaq üçün simulyasiyalar aparılmışdır.

##  Metodologiya
- **Difference-in-Differences (DID):** Müalicə (Treated) və Nəzarət (Control) qrupları arasındakı fərqi zaman daxilində müqayisə etmək üçün.
- **Bayesian Structural Time Series (CausalImpact):** "Əgər müdaxilə olmasaydı nə olardı?" sualına cavab verən counterfactual proqnozlar qurmaq üçün.

---

##  Analiz və Nəticələr

### 1. Paralel Trendlərin Yoxlanılması
Analizin doğruluğu üçün kampaniyadan əvvəl regionların oxşar trend nümayiş etdirməsi şərtdir.
![Parallel Trends](picture/parallel_trends.png)
*Qrafik 1: Kampaniyadan əvvəlki dövrdə regionların paralel hərəkəti metodun keçərli olduğunu sübut edir.*

### 2. Orijinal Data Analizi (Real Vəziyyət)
Real məlumatlar üzərində aparılan regional analiz kampaniyanın statistik olaraq əhəmiyyətli bir artım yaratmadığını göstərdi.
![Original Regional Analysis](picture/original_regional_analysis.png)
- **P-value:** 0.49 (Nəticə təsadüfidir).
- **True Regional DID Effect:** -0.0206.

### 3. Kanal Bazlı Analizlər
Fərqli marketinq kanallarının (Influencer və Social Media) təsirləri fərdi olaraq yoxlanılmışdır.
![Social Media Analysis](picture/social_media_causal_analysis.png)
![Influencer Analysis](picture/influencer_campaign_analysis.png.png)

### 4. Modelin Validasiyası (Simulyasiya)
Modelin real təsirləri tutma qabiliyyətini yoxlamaq üçün məlumatlara süni 15% artım (lift) əlavə edilmişdir. Model bu dəyişikliyi 100% dəqiqliklə müəyyən etmişdir.
![Simulated Campaign Lift](picture/simulated_campaign_lift.png)
![Regional Causal Impact Sim](picture/regional_causal_impact_sim.png)
*Bu simulyasiya sübut edir ki, metodologiya kifayət qədər həssasdır və real artım olduqda onu dəqiq izolyasiya edə bilir.*

---

##  Texnologiyalar
- **Dil:** Python
- **Kitabxanalar:** `pycausalimpact`, `statsmodels`, `pandas`, `matplotlib`, `seaborn`
- **Platforma:** JupyterLab / Google Colab

##  Layihə Strukturu
- `picture/`: Analiz zamanı əldə olunan bütün vizuallaşdırmalar.
- `Estimate the Causal Impact of Marketing Campaigns.ipynb`: Bütün hesablamaları və kodları özündə cəmləyən əsas notebook.
- `README.md`: Layihə haqqında ümumi məlumat və nəticələrin şərhi.

---

