# Пересечение отрезков

```
struct p {
    ll x, y;
};

bool f(p p1, p p2, p p3, p p4) {
    double d = (p4.y - p3.y) * (p1.x - p2.x) - (p4.x - p3.x) * (p1.y - p2.y);
    
    if (d == 0) {
        return  (p1.x * p2.y - p2.x * p1.y) * (p4.x - p3.x) - (p3.x * p4.y - p4.x * p3.y) * (p2.x - p1.x) == 0 
        && (p1.x * p2.y - p2.x * p1.y) * (p4.y - p3.y) - (p3.x * p4.y - p4.x * p3.y) * (p2.y - p1.y) == 0;
    }
    
    double a = (p4.x - p2.x) * (p4.y - p3.y) - (p4.x - p3.x) * (p4.y - p2.y);
    double b = (p1.x - p2.x) * (p4.y - p2.y) - (p4.x - p2.x) * (p1.y - p2.y);
    
    double ka = a / d;
    double kb = b / d;
    
    return 0 <= ka && ka <= 1 && 0 <= kb && kb <= 1;
}

```