def euclideanDistance(point1, point2):
    """
    Calculates the Euclidean distance between two points represented as tuples.
    Args:
        point1 (tuple): First point (x1, y1).
        point2 (tuple): Second point (x2, y2).
    Returns:
        float: Euclidean distance between the two points.
    """
    x1, y1 = point1
    x2, y2 = point2
    return ((x2 - x1) ** 2 + (y2 - y1) ** 2) ** 0.5

# Define points (replace with your own points)
points = [(1, 2), (3, 4), (5, 6), (7, 8)]

# Calculate distances between all point pairs
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)

# Find the minimum distance
min_distance = min(distances)

print(f"Points: {points}")
print(f"Distances: {distances}")
print(f"Minimum distance: {min_distance:.2f}")

     
Points: [(1, 2), (3, 4), (5, 6), (7, 8)]
Distances: [2.8284271247461903, 5.656854249492381, 8.48528137423857, 2.8284271247461903, 5.656854249492381, 2.8284271247461903]
Minimum distance: 2.83
