islem_hacmi=1000 # bu dortlu bizim verdigimiz parametreler
listed_orani=10
unique_owner_orani=30
koleksyon_suresi=6

islem_hacmi_input= int(input("islem hacmi ne kadar?")) # bu dortlu nft nin ustteki parametreler hakkinda degerleri
listed_orani_input= int(input("listed orani ne kadar?"))
unique_owner_orani_input= int(input("unique owner orani ne kadar?"))
koleksyon_suresi_input= int(input("koleksyon suresi ne kadar?"))

guvenirlik_orani=0 # bu oranla en son degerlendirme yapiliyor


if islem_hacmi_input>=islem_hacmi:   # bu dortlu if conditionlar degerlendirme yapiyor
    guvenirlik_orani+=1

if listed_orani_input<=listed_orani:
    guvenirlik_orani+=1

if unique_owner_orani_input>=unique_owner_orani:
    guvenirlik_orani+=1

if koleksyon_suresi_input>=koleksyon_suresi:
    guvenirlik_orani+=1


def degerlendirme():                 # bu function aldigimiz degerlendirme sonuca gore belirli havuza gonderir
    global guvenirlik_orani
    if guvenirlik_orani==4:
        print("GÜVENİLİR (1. havuza gönder)")
    elif guvenirlik_orani==3:
        print("AZ GÜVENİLİR (2. havuza gönder)")
    elif guvenirlik_orani==2:
        print("RİSK İÇEREBİLİR (3. havuza gönder)")
    elif guvenirlik_orani==1:
        print("RİSKLİ (4. havuza gönder)")
    else:
        print("ÇOK RİSKLİ (5. havuza gönder)")


degerlendirme()
