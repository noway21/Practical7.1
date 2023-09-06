#include <stdio.h>
#include <math.h>

int main() {
    double x1 = 2, y1 = 4, r1 = 8, x2 = 2, y2 = 4, r2 = 10; // Введені координати та радіуси

    double distance = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));

    int intersectionPoints;

    if (distance == 0 && r1 == r2) {
        intersectionPoints = -1;
    } else if (distance < r1 + r2 && distance > fabs(r1 - r2)) {
        intersectionPoints = 2;
    } else if (distance == r1 + r2 || distance == fabs(r1 - r2)) {
        intersectionPoints = 1;
    } else {
        intersectionPoints = 0;
    }

    printf("Кількість точок перетину кол: %d\n", intersectionPoints);

    return 0;
}
