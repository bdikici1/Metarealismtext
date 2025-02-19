import numpy as np
import matplotlib.pyplot as plt

# Başlangıç verisi
V = 10  
alpha = 0.3  # Geri besleme oranı
iterations = 50  # Kaç döngü olacak

# Dönüşüm fonksiyonu (örnek olarak basit bir fonksiyon)
def transformation(x):
    return np.sin(x)  # Sin fonksiyonu ile geri besleme ekleniyor

# Veri saklama
history = [V]

for t in range(iterations):
    V = V + alpha * transformation(V)
    history.append(V)

# Sonuçları görselleştirme
plt.plot(history)
plt.xlabel("Iteration")
plt.ylabel("V(t)")
plt.title("Geri Besleme Döngüsü ile Veri Güncelleme")
plt.show()
