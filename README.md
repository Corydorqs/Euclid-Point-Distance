import math

points = [
    (25, 38),
    (9, 12),
    (15, 28),
    (21, 43)
]

def euclideanDistance(point1, point2):
    x1, y1 = point1
    x2, y2 = point2
    distance = math.sqrt((x2 - x1)**2 + (y2 - y1)**2)
    return distance

distances = []

for i in range(len(points)):
    for j in range(i + 1, len(points)):
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)

print("Calculated distances:")
for idx, dist in enumerate(distances, 1):
    print(f"Distance {idx}: {dist}")

min_distance = min(distances)
print("\nMin Distance:", min_distance)
