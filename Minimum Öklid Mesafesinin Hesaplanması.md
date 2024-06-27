1.
points = [(1, 2), (3, 4), (5, 6), (7, 8)]

2.
def euclideanDistance(point1, point2):
    return ((point1[0] - point2[0]) ** 2 + (point1[1] - point2[1]) ** 2) ** 0.5

3.
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)
  
4.
min_distance = min(distances)
print(f"Minimum mesafe: {min_distance:}")
