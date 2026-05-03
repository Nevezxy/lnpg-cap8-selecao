# PYTHON
j = -3
i = 0
while i < 3 and j <= 0:
    v = j + 2
    if v == 3 or v == 2:
        j -= 1
    elif v == 0:
        j += 2
    else:
        j = 0

    if j <= 0:
        j = 3 - i
    i += 1

# JAVA
int j = -3;
int i = 0;
while (i < 3 && j <= 0) {
    int v = j + 2;
    if (v == 3 || v == 2) {
        j--;
    } else if (v == 0) {
        j += 2;
    } else {
        j = 0;
    }

    if (j <= 0) {
        j = 3 - i;
    }
    i++;
}

# HASKELL
loop :: Int -> Int -> Int
loop i j
  | i >= 3 || j > 0 = j          -- condição de parada (substitui o break e o limite do for)
  | otherwise       = loop (i + 1) nextJ
  where
    v    = j + 2
    newJ | v == 3 || v == 2 = j - 1   -- cases 3 e 2 (substitui o switch/break)
         | v == 0            = j + 2   -- case 0
         | otherwise         = 0      -- default
    nextJ = if newJ <= 0 then 3 - i else newJ

result :: Int
result = loop 0 (-3)
