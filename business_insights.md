Sales Data Analysis
Business Insights Report
Dataset: sales_data_sample.csv  |  2003-2005


1. Dataset Haqqında — Əsasın Statistikası

Ümumi sıra sayı	2,823
Sütun sayı	25
Zaman aralığı	2003-01-06 — 2005-05-31
Ölkə sayı	19
Məhsul xətləri	7 (Classic Cars, Vintage Cars, Motorcycles, Planes, Trucks, Ships, Trains)
SALES — Min	$482.13
SALES — Max	$14,082.80
SALES — Ortalama	$3,553.89
SALES — Median	$3,184.80
Q1 / Q3 / IQR	$2,203 / $4,508 / $2,304
Duplikat sira	0
ORDERDATE tipi	object -> datetime64 (çevrildi)
Missing Values	ADDRESSLINE2 (%71), STATE (%29), TERRITORY (%38), POSTALCODE (%3) — "Unknown" ilə dolduruldu

Qeyd: 2005-ci il datası yalnız yanvar-may (5 ay) ehtiva edir. İllik müqayisədə diqqətli olmaq lazımdır.

2. Status, il, məhsul analizi

STATUS	2003	2004	2005
Shipped	976	1,287	354
Cancelled	16	44	--
Resolved	8	8	31
On Hold	--	6	38
In Process	--	--	41
Disputed	--	--	14

3. Ölkə Üzrə Gəlir — Top 5

#	Ölkə	Sifariş Sayı	Gəlir ($)	Gəlir Payı (%)
1	USA	1,004	3,627,982.83	36.6%
2	Spain	342	1,215,686.92	12.3%
3	France	314	1,110,916.52	11.2%
4	Australia	185	630,623.10	6.4%
5	UK	144	478,880.46	4.8%

Ümumi gəlir (bütün ölkələr): $10032628.85
 TOP 5 ölkənin payı: ~70.3%

4. Ölkəye Gore Ortalama Sifaris Deyeri (AOV)

Ölkə	Sifariş Sayı	AOV ($)	Sira
Denmark	63	3,899.00	1 (1-ci)
Switzerland	31	3,797.21	2
Sweden	57	3,684.46	3
Austria	55	3,673.86	4
USA	1,004	3,613.53	9
Canada	70	3,201.12	19 (ən aşağı)

5. Business Insights

[1]  INSIGHT #1: ABŞ Dominant Bazar Lideridir
Tapıntı:  ABŞ 1,004 sifariş (ümuminin 35.5%-i) və $3,627,982.83 gəlir (ümuminin 36.6%-i) ilə hər iki göstəricidə açıq liderdir. İkinci yerdəki İspaniya ilə aradakı fərq 3 dəfə yaxındır.
Tövsiyə:  ABŞ bazarında mövcud kanal ortaqlıqlarını gücləndirin. Müştəri saxlama proqramları tətbiq edin. Digər bazarlarda böyümək üçün differensial qiymətlən strategiyasını araşdırın.

[2]  INSIGHT #2: Denmark AOV Lideridir — Kiçik, Lakin Yüksək Dəyərli Bazar
Tapıntı:  Denmark cəmi 63 sifariş ilə sifariş sayına görə 11-ci sıradadır, ancaq AOV ($3,899) üzrə birincidir. Yəni: hər bir Danimarka müştərisi digər bazarlara nisbət ən çox xərcləyir.
Tövsiyə:  Denmark, İsveçrə, İsveç, Avstriya üçün premium müştəri proqramları hazırlayın. Bu bazarlara ayrıca account manager təyin edin.

[3]  INSIGHT #3: 2005-ci ildə Cancelled Order Yoxdur
Tapıntı:  2003: 16, 2004: 44 ləğv edilmiş sifariş var. Lakin 2005-ci ildə (5 ay ərzində) heç bir Cancelled order yoxdur. Bu müsbət əməliyyat siqnalı ola bilər.
Tövsiyə:  2005 ləğvetmə azalmasının arxasındakı səbəbi araşdırın. Bu tendensiya 2004 sonundan bəri davam edərsə uğurlu bir dəyişikliyin nəticəsidir.

[4]  INSIGHT #4: Disputed və In Process Yalnız 2005-də Mövcuddur
Tapıntı:  Disputed (14) və In Process (41) statuslu bütün sifarişlər yalnız 2005-ci ildə qeydə alınıb. Data may 31-nə qədər olan dövrü əhatə etdiyindən bu sifarişlər hələ bitməmiş ola bilər.
Tövsiyə:  "In Process" 41 sifarişin cari vəziyyətini yoxlayın — bunların böyük hissəsi gəlirə çevrilə bilər. "Disputed" sifarişlər üçün müştəri ilə əlaqə saxlayın, problemi sürətləndirin.

[5]  INSIGHT #5: Shipped Sifarişlər Üstünlük Təşkil Edir — On Hold 2005-də Artıb
Tapıntı:  Ümumi sifarişlərin 92.6%-i Shipped statusundadır. Lakin On Hold: 2004-də 6, 2005-də 38 — bu artış diqqət tələb edir.qet teleb edir.
Tövsiyə:  "On Hold" artışının səbəbini araşdırın (kredit limiti, inventar, müştəri xahişi?). Hansı ölkə/məhsul xəttinə aid olduğunu müəyyən edin.

[6]  INSIGHT #6: Satış Paylanması Normal Deyil — Sağa Əyilmiş
Tapıntı:  SALES histoqramı sağa əyilmiş paylanma göstərir: Ortalama ($3,553) mediandan ($3,184) yüksəkdir. Q1=$2,203, Q3=$4,508, IQR=$2,304. $10,000+ sifarişlər (16 ədəd) ortalamını yuxarı çəkir.
Tövsiyə:  Seqment analizlərini median əsasında qur. Outlier sifarişləri ($10K+) ayrı VIP kateqoriyada izlə. Small/Medium/Large deal size kateqoriyaları üzrə fərqli strategiyalar tətbiq et.

[7]  INSIGHT #7: Classic Cars Məhsul Xəttinin Dominant Mövqeyi
Tapıntı:  Classic Cars 967 sifariş (34.3%) ilə ən çox satılan məhsul xəttidir. İkinci: Vintage Cars (607, 21.5%), üçüncü: Motorcycles (331, 11.7%). Ən az satılan: Trains (77, 2.7%).
Tövsiyə:  Classic Cars üçün inventar idarəetməsini gücləndirin. Zəif performanslı xətlər (Trains, Ships) üçün birləşdirmə və ya upsell strategiyası tətbiq edin.

[8]  INSIGHT #8: EMEA Əsas Territory-dir, Lakin ABŞ Territory-si Qeyri-Müəyyən
Tapıntı:  TERRITORY üzrə: EMEA (1,407), APAC (221), Japan (121). ABŞ-ın 1,004 sifarişi üçün territory "Unknown", Kanadanın 70 sifarişi üçün də "Unknown".
Tövsiyə:  ABŞ və Kanada sifarişlərinin territory etiketlənməsini tamamlayın. Satış menecerlərinə region üzrə daha dəqiq hədəf təyinləmək üçün bu məlumat vacibdir.

6. İllik Gəlir Müqayisəsi (Diqqət: 2005 Natamamdır)

Göstərici	2003 (tam il)	2004 (tam il)	2005 (5 ay)
Sifariş sayı	1,000	1,345	478
Ümumi gəlir ($)	3,516,979.54	4,724,162.60	1,791,486.71 *
Ən çox sifariş	USA (976 Shipped)	USA (1,287 Shipped)	USA (354 Shipped)

* 2005 gəliri yalnız 5 aylıq dövrü əhatə edir. Əvvəlki illərlə müqayisə yanıltıcı ola bilər. Bu səbəbdən bu dataseti 6 aylıq periodlara ayıraraq yenidən analiz edəcəm.


