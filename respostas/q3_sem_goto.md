#include <stdio.h>

int main() {
    int i, j;

    j = -3;

    for (i = 0; i < 3 && !(j > 0); i++) {

        // Substituição do switch sem break
        if ((j + 2) == 3 || (j + 2) == 2) {
            j--;
        } else if ((j + 2) == 0) {
            j += 2;
        } else {
            j = 0;
        }

        // O "if (j > 0) break" foi absorvido
        // pela condição do for: !(j > 0)
        if (!(j > 0)) {
            j = 3 - i;
        }

    }

    printf("i = %d\n", i);
    printf("j = %d\n", j);

    return 0;
}
