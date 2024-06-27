# Mesafe farkını hesaplayacağımız noktalarımız
points = [(8, 15), (12, 27), (55, 83), (80, 105)]

# Öklid mesafemiz için bir fonksiyon yazalım, sondaki 0.5 ile üs alma işlemi karekök içine almak içidir.
def euclideanDistance(point1, point2):
    return ((point1[0] - point2[0]) ** 2 + (point1[1] - point2[1]) ** 2) ** 0.5

# Mesafelerin hesaplanması
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)
  
# Minimum mesafeyi bulmak için kodumuz
min_distance = min(distances)
print(f"Minimum mesafe: {min_distance:}")
