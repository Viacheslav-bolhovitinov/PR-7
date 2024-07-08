#include <stdio.h>
#include <math.h>

int main() {
    double x1, y1, r1, x2, y2, r2;
    printf("Введіть координати центрів та радіуси двох кіл (x1, y1, r1, x2, y2, r2): ");
    scanf("%lf %lf %lf %lf %lf %lf", &x1, &y1, &r1, &x2, &y2, &r2);

    double d = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));

    if (x1 == x2 && y1 == y2 && r1 == r2) {
        printf("-1\n");
    } else if (d > r1 + r2 || d < fabs(r1 - r2)) {
        printf("0\n");
    } else if (d == r1 + r2 || d == fabs(r1 - r2)) {
        printf("1\n");
    } else {
        printf("2\n");
    }

    return 0;
}