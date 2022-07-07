# Cancer
Introduction to Data Science Lesson Project

## A. Pandas ile Veri Analizi

**Açıklama:**

-   Çözümlerinizde döngüler yerine `pandas` kütüphanesinin kullanılması
    gerekmektedir.

## Soru A.1:

-   Kanser hastalarının klinik durumlarına ilişkin veriler içeren
    \"clinical.tsv\" dosyasını, `cancer` adlı DataFrame\'e okuyunuz.
    (\"\'\--\" değerlerinin `NaN` olacak şekilde okunmasını sağlayınız.)
-   Tüm değerleri `NaN` olan sütunları siliniz.
-   \'case_submitter_id\', \'age_at_index\', \'days_to_death\',
    \'gender\', \'race\', \'vital_status\', \'year_of_birth\',
    \'year_of_death\', \'age_at_diagnosis\', \'ajcc_pathologic_stage\',
    \'icd_10_code\', \'primary_diagnosis\', \'prior_malignancy\',
    \'prior_treatment\', \'site_of_resection_or_biopsy\',
    \'synchronous_malignancy\', \'tissue_or_organ_of_origin\',
    \'year_of_diagnosis\', \'treatment_type\' sütunları haricindeki
    sütunları siliniz.
-   Sütunlarından herhangi birisinde `NaN` değeri olan satırları
    siliniz. Kaç satır silindi?
-   Sütunlarından herhangi birisinde \"not reported\" ya da \"Not
    Reported\" değerleri olan satırları siliniz.
-   Hasta barkodu (case_submitter_id) aynı olan satırlardan ilki kalacak
    şekilde tekrar edenleri siliniz.
-   Hasta barkodu (case_submitter_id) sütununu DataFrame\'in index\'i
    yapınız.
-   En son oluşan DataFrame\'in satır ve sütun sayısını yazdırınız.

## Soru A.2:

-   En az 10 hasta içeren birincil tanı (primary_diagnosis) kanser
    türlerinin cinsiyete göre dağılımını, yatay yığılmış (stacked) sütun
    grafik olarak gösteriniz.

## Soru A.3:

-   Her bir kanser türünden (primary_diagnosis) kaç hasta olduğunu,
    büyükten küçüğe doğru sıra olarak yazdırınız.
-   Tüm hastaların ve en çok görülen kanser türüne sahip olan hastaların
    yaş (age_at_index) dağılımlarını, aynı figürde yan yana iki
    histogram grafiği (subplot) olarak gösteriniz. Grafiklere uygun
    birer başlık (`title`) atayınız.

## Soru A.4:

Yaşam süresi (days_to_death) ortalaması en yüksek olan kanser türünü
(primary_diagnosis) yazdırınız.

## Soru A.5:

-   Kanserin teşhis yaşı (age_at_diagnosis) ile hastanın kalan ömrü
    (days_to_death) arasındaki ilişkiyi gösteren bir saçılım grafiği
    çiziniz.

## Soru A.6:

-   Kanser hastalarının alkol ve sigara kullanımlarına ilişkin veriler
    içeren \"exposure.tsv\" dosyasını, \'case_submitter_id\' sütunu
    index olacak şekilde `exposure` adlı DataFrame\'e okuyunuz.
    (\"\'\--\" ve \"Not Reported\" değerlerinin `NaN` olacak şekilde
    okunmasını sağlayınız.)
-   Tüm değerleri `NaN` olan sütunları siliniz.
-   Sütunlarından herhangi birisinde `NaN` değeri olan satırları
    siliniz.
-   Oluşan DataFrame\'in satır ve sütun sayısını yazdırınız.
-   \'cancer\' ve \'exposure\' adlı DataFrame\'lerde ortak olan
    hastaların verilerini, hasta barkodu (case_submitter_id)
    aracılığıyla birleştiriniz ve \'cancer_exposure\' adlı yeni bir
    dataframe\'e aktarınız.

## Soru A.7:

Alkol geçmişi olan ve günde 3\'ten fazla sigara içen hastalarda,
kanserin ilk ortaya çıktığı doku veya organların yüzdelerini pasta
grafiği üzerinde gösteriniz.

## B. Scikit-learn ile Makine Öğrenmesi

**Açıklamalar:**

-   Bu bölümde A.1 sorusunda elde edilen DataFrame (\'cancer\')
    kullanılacaktır.
-   Sorularda verilen her problem için aşağıdaki işlemler adım adım
    gerçekleştirilecektir:
    1.  Her model için kullanılması gerektiğini (etkili olduğunu)
        düşündüğünüz öznitelikleri belirleyiniz.
    2.  Kategorik olan sütunları \'one-hot encoding\' yöntemi ile ikili
        vektör temsiline dönüştürünüz.
    3.  Kategorik olmayan sütunlarda normalizasyon işlemi uygulayınız.
    4.  Problem bir **regresyon problemi** ise \'k-fold
        cross-validation\' ile probleme uygun metrik**ler** kullanarak
        tahmin modelinizin performansını değerlendiriniz ve hangi
        özniteliklerin çıktı değişkenini daha fazla etkilediğini
        yorumlayınız. Problem bir **sınıflandırma problemi** ise modelde
        kullanılacak hiper-parametre aramasını (hyper-parameter tunning)
        \'k-fold cross-validation\' ile yapınız (GridSearchCV modülünü
        kullanabilirsiniz) ve test verisi üzerinde probleme uygun
        metrik**ler** kullanarak tahmin modelinizin performansını
        değerlendiriniz.
    5.  Farklı öznitelikler ve/veya makine öğrenmesi yöntemleri
        kullanarak daha iyi performans gösteren 2-3 model daha
        geliştirmeye çalışınız (sarf ettiğiniz eforun görülebilmesi
        amacıyla bu modellere ilişkin kodları silmeyiniz).
-   İşlemleri gerçekleştirirken gerekli gördüğünüz yerleri (tercih
    ettiğiniz birşeyin nedeni v.b. gibi) açıklayınız.

## Soru B.1: Bir hastanın kaç gün ömrü kaldığının (days_to_death) tahminlenmesi

## Soru B.2: Bir hastaya uygulanan tedavi yönteminin (treatment_type) tahminlenmesi
