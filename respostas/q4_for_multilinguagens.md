# PYTHON
def main():
    n = 100
    sum_ = 0  # 'sum' é palavra reservada em Python

    i, j = 0, 17
    while i < n:          # Python não suporta múltiplas variáveis
        sum_ += i * j + 3 # de controle no for, então usamos while
        i += 1
        j -= 1

    print(f"sum = {sum_}")

main()

# C
#include <stdio.h>

int main() {
    int i, j, n = 100;
    int sum = 0;

    for (i = 0, j = 17; i < n; i++, j--)
        sum += i * j + 3;

    printf("sum = %d\n", sum);

    return 0;
}

# KOTLIN
fun main() {
    val n = 100
    var sum = 0
    var j = 17

    for (i in 0 until n) {    // Kotlin não suporta múltiplas variáveis
        sum += i * j + 3      // de controle no for, j é controlado externamente
        j--
    }

    println("sum = $sum")
}

# RUST
fn main() {
    let n = 100;
    let mut sum: i64 = 0;
    let mut j: i64 = 17;

    for i in 0..n {       // Rust usa ranges; j é controlado no corpo
        sum += i * j + 3;
        j -= 1;
    }

    println!("sum = {}", sum);
}

# SWIFT
import Foundation

func main() {
    let n = 100
    var sum = 0
    var j = 17

    for i in 0..<n {      // Swift usa ranges; j é controlado no corpo
        sum += i * j + 3
        j -= 1
    }

    print("sum = \(sum)")
}

main()
