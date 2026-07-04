# Netflix Titles — Pandas ilə Data Analizi

Netflix-in kataloqundakı film və serialları `pandas`, `seaborn` və `scipy` istifadə edərək tədqiq edən analiz notebook-u. Data təmizləmə, çoxdəyişənli vizuallaşdırma, zaman trendi və statistik testlər (korrelyasiya, chi-square, effect size) əhatə olunur.

## Nələr var

**Data təmizləmə**
- `director`, `cast`, `country`, `rating`, `date_added` sütunlarındakı boş dəyərlərin idarə edilməsi
- `date_added` ilinin `release_year`-dən kiçik olduğu uyğunsuz sətirlərin aşkarlanması
- Səhvən `rating` sütununda yerləşən `duration` dəyərlərinin (məs. "66 min") düzəldilməsi

**Kateqoriya və zaman analizi**
- `type`, `country`, `rating`, `listed_in` üzrə paylanma
- İllər üzrə Netflix-ə əlavə olunan məzmunun trendi (time-series)
- Çoxdəyişənli analiz: ölkə × tip, rating × tip (`hue` ilə)

**Duration və outlier analizi**
- Filmlər üçün dəqiqə, serial üçün sezon sayı hesablanması
- Təkrar istifadə oluna bilən `detect_outliers()` funksiyası ilə IQR metodu

**Statistik testlər**
- `duration_min` və `release_year` arasında korrelyasiya
- `type` və `rating` arasında chi-square asılılıq testi
- Cramér's V ilə əlaqənin gücünün (effect size) ölçülməsi

## Data
Layihə [Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows) (Kaggle) dataset-indən istifadə edir.

Notebook-u işə salmaq üçün:
1. Dataset-i yuxarıdakı linkdən yükləyin (`netflix_titles.csv`)
2. Faylı bu repo-nun kök qovluğuna qoyun

## Quraşdırma və işə salma
```bash
pip install -r Requirements_Netflix.txt
jupyter notebook Netflix_Analysis.ipynb
```

## Struktur
```
├── Netflix_Analysis.ipynb    ← əsas, interaktiv
├── Netflix_Analysis.html     ← statik baxış üçün
├── Requirements_Netflix.txt  ← Python asılılıqları
├── README.md
```


