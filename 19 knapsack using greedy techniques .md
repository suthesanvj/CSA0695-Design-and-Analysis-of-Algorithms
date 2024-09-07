#include <stdio.h>

void knapsack(int weight[], int value[], int n, int W) {
    float ratio[n];
    for (int i = 0; i < n; i++) {
        ratio[i] = (float)value[i] / weight[i];
    }
    
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            if (ratio[i] < ratio[j]) {
                int temp = ratio[i];
                ratio[i] = ratio[j];
                ratio[j] = temp;
                
                temp = weight[i];
                weight[i] = weight[j];
                weight[j] = temp;
                
                temp = value[i];
                value[i] = value[j];
                value[j] = temp;
            }
        }
    }
    
    int totalValue = 0;
    for (int i = 0; i < n; i++) {
        if (weight[i] <= W) {
            W -= weight[i];
            totalValue += value[i];
        } else {
            totalValue += value[i] * ((float)W / weight[i]);
            break;
        }
    }
    printf("Maximum value in Knapsack = %d\n", totalValue);
}

int main() {
    int weight[] = {10, 20, 30};
    int value[] = {60, 100, 120};
    int W = 50;
    int n = sizeof(weight) / sizeof(weight[0]);

    knapsack(weight, value, n, W);
    
    printf("\n\n\nsuthesan vj   192210542\n");
    
    return 0;
}
![Screenshot 2024-09-07 152718](https://github.com/user-attachments/assets/7d11b9a8-9594-44ab-83c2-8e3e58eeb63c)
