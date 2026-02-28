# Teknik Proje: Uzaktan Çalışma Tükenmişlik Analizi ve Tahmini

> [!NOTE]
> Bu proje **Antigravity AI** aracılığıyla hazırlanmıştır.  
> 🎓 **[Senior Değerlendirme Raporu'nu (Audit) inceleyin](docs/evaluation_report.md)** - Projenin Junior, Senior ve Mülakat perspektiflerinden analizi.
> Analizlerde kullanılan veriler **Sentetik Veri** olup, gerçekçi davranış modelleri oluşturmak amacıyla tasarlanmıştır.

## 🚀 Genel Bakış
Bu çalışma, Kaggle üzerinde yer alan [Work From Home Employee Burnout Dataset](https://www.kaggle.com/datasets/sonalshinde123/work-from-home-employee-burnout-dataset) veri kümesini kullanarak uzaktan çalışma ortamlarında çalışanların davranışsal örüntülerini analiz eden, test ve gelişim amaçlı bir veri bilimi projesidir.

## 📊 Temel Bulgular
- **Uyku vs. Tükenmişlik:** Günlük uyku süresi, tükenmişlik riskiyle en güçlü ters korelasyona sahip değişkendir.
- **Ekran Süresi Eşiği:** Günlük 9 saati aşan ekran süresinin, tükenmişlik puanlarını dikey yönde artırdığı gözlemlenmiştir.
- **Üretkenlik Paradoksu:** Yüksek görev tamamlama oranları her zaman refah göstergesi değildir; az uyku ile birleştiğinde "Yüksek Risk" evresinin öncüsü olabilmektedir.

## 🛠️ Kullanılan Teknolojiler
- **Analiz:** `Pandas`, `NumPy`, `SciPy`
- **Görselleştirme:** `Seaborn`, `Matplotlib`, `Plotly` (İnteraktif Grafikler)
- **Makine Öğrenmesi:** `XGBoost`, `LightGBM`, `Scikit-Learn`
- **Açıklanabilir Yapay Zeka (XAI):** `SHAP` (TreeExplainer)

## 🏗️ Metodoloji ve Teknik Zorluklar
Analiz sürecinde tespit edilen **Dengesiz Sınıf Dağılımı** (High Risk sınıfının %5 olması) profesyonel bir veri bilimi yaklaşımıyla yönetilmiştir:
- **Stratified Splitting:** Eğitim ve test setlerinde sınıf oranlarının korunması sağlanmıştır.
- **Recall (Duyarlılık) Önceliği:** Burnout tahmininde "yüksek riskli bir çalışanı gözden kaçırmanın maliyeti" (False Negative) yüksek olduğu için sadece F1-skoruna değil, özellikle High sınıfındaki **Recall** değerine odaklanılmıştır.
- **Özellik Mühendisliği:** Sentetik verinin sunduğu imkanlar dahilinde, risk gruplarını ayrıştıracak türetilmiş metrikler (`Sleep Efficiency Index`) geliştirilmiştir.

> [!TIP]
> **Yapay Zeka ile Stratejik İş Birliği:** Bu proje sadece kod yazımında değil, aynı zamanda **Antigravity AI**'nın bir "Senior Partner" olarak kullanılmasıyla; Junior, Akademik ve Mülakat perspektiflerinden projenin değerlendirilmesi ve stratejik geliştirme tavsiyeleri alınması süreçlerini de içerir. Bu, YZ'nin alışılmışın dışında, "üst düzey danışman" olarak kullanımına dair güçlü bir örnektir.

## 💻 Kurulum ve Kullanım
1. Depoyu klonlayın.
2. Bağımlılıkları yükleyin:
   ```bash
   pip install -r requirements.txt
   ```
3. Notebook'u çalıştırın:
   ```bash
   jupyter notebook Burnout_Analysis.ipynb
   ```
