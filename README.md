import random

print("Sayı Tahmin Oyununa Hoş Geldin!")
print("1 ile 20 arasında bir sayı tuttum. Tahmin etmeye çalış.")

sayi = random.randint(1, 20)  # Bilgisayarın tuttuğu sayı
tahmin_hakki = 5

while tahmin_hakki > 0:
    tahmin = int(input("Tahminini gir: "))
    
    if tahmin == sayi:
        print("Tebrikler! Doğru tahmin ettin 🎉")
        break
    elif tahmin < sayi:
        print("Daha yüksek bir sayı söyle.")
    else:
        print("Daha düşük bir sayı söyle.")
    
    tahmin_hakki -= 1
    print(f"Kalan tahmin hakkın: {tahmin_hakki}")

if tahmin_hakki == 0 and tahmin != sayi:
    print(f"Üzgünüm, doğru sayı {sayi} idi. Tekrar dene!")# menekse
