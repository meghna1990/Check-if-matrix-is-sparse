#include <stdio.h>

#define ROWS 3
#define COLS 3

int main() {
    int matrix[ROWS][COLS] = {
        {0, 0, 3},
        {0, 0, 0},
        {5, 0, 0}
    };

    int zero_count = 0;
    int total_elements = ROWS * COLS;

    // Count zeros
    for (int i = 0; i < ROWS; i++) {
        for (int j = 0; j < COLS; j++) {
            if (matrix[i][j] == 0) {
                zero_count++;
            }
        }
    }

    if (zero_count > total_elements / 2) {
        printf("Matrix is sparse\n");
    } else {
        printf("Matrix is not sparse\n");
    }

    return 0;
}
PYHON
# Function to check if matrix is sparse
def is_sparse_matrix(mat):
    rows = len(mat)
    cols = len(mat[0])
    total_elements = rows * cols
    zero_count = 0

    for i in range(rows):
        for j in range(cols):
            if mat[i][j] == 0:
                zero_count += 1

    if zero_count > total_elements / 2:
        return True
    else:
        return False

# Example
matrix = [
    [0, 0, 3],
    [0, 0, 0],
    [5, 0, 0]
]

if is_sparse_matrix(matrix):
    print("Matrix is sparse")
else:
    print("Matrix is not sparse")
OUTPUT
Matrix is sparse
# Check-if-matrix-is-sparse
