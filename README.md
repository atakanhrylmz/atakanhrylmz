# Noktaların Tanımlıyoruz
points = [(1, 2), (3, 4), (6, 8), (9, 10)]

# Öklid Mesafesi İçin Bir Fonksiyon Yazma
def euclideanDistance(point1, point2):
    # Öklid mesafesi formülü
    return ((point2[0] - point1[0]) ** 2 + (point2[1] - point1[1]) ** 2) ** 0.5

# Mesafelerin Hesaplanması için
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

# Minimum Mesafenin Bulunması lazım şuan
min_distance = min(distances)

# Sonuçları Yazdırma
print("Tüm Noktalar: ", points)
print("Hesaplanan Mesafeler: ", distances)
print("Minimum Mesafe: ", min_distance)
