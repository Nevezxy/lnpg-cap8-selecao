# JAVA
public class exercicio1 {
    public static void main(String[] args) {
        int j = 0;
        int i = 0;
        int k;

        k = (j + 13) / 27;

        while (k <= 10) {
            k = k + 1;
            i = 3 * k - 1;
        }

        // out:
        System.out.println("Valor final de k: " + k);
        System.out.println("Valor final de i: " + i);
    }
}

# PYTHON
j = 5  
k = (j + 13) // 27

i = 0
while k <= 10:
    k += 1
    i = 3 * k - 1

print(f"k = {k}")
print(f"i = {i}")

# HASKELL
module Main where

loop :: Int -> Int
loop k
    | k > 10    = k
    | otherwise = loop (k + 1)

main :: IO ()
main = do
    let j    = 5          -- valor de exemplo
        k0   = (j + 13) `div` 27
        kFinal = loop k0
        i    = 3 * kFinal - 1

    putStrLn $ "k = " ++ show kFinal
    putStrLn $ "i = " ++ show i

# SWIFT
import Foundation

func main() {
    let j: Int = 5  // valor de exemplo
    var k: Int = (j + 13) / 27
    var i: Int = 0

    while k <= 10 {
        k += 1
        i = 3 * k - 1
    }

    print("k = \(k)")
    print("i = \(i)")
}

main()
