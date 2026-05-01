# C
#include <stdio.h>

int main() {
    int k = 4; // valor de exemplo
    int j = 0;

    switch (k) {
        case 1:
        case 2:
            j = 2 * k - 1;
            break;
        case 3:
        case 5:
            j = 3 * k + 1;
            break;
        case 4:
            j = 4 * k - 1;
            break;
        case 6:
        case 7:
        case 8:
            j = k - 2;
            break;
        default:
            j = 0; // nenhuma condição satisfeita
            break;
    }

    printf("k = %d\n", k);
    printf("j = %d\n", j);

    return 0;
}

# RUBY
def main
  k = 4  # valor de exemplo
  j = 0

  j = case k
    when 1, 2       then 2 * k - 1
    when 3, 5       then 3 * k + 1
    when 4          then 4 * k - 1
    when 6, 7, 8    then k - 2
    else 0
  end

  puts "k = #{k}"
  puts "j = #{j}"
end

main

# ERLANG
-module(selecao).
-export([main/0]).

calcular_j(K) when K =:= 1; K =:= 2 -> 2 * K - 1;
calcular_j(K) when K =:= 3; K =:= 5 -> 3 * K + 1;
calcular_j(K) when K =:= 4           -> 4 * K - 1;
calcular_j(K) when K =:= 6; K =:= 7; K =:= 8 -> K - 2;
calcular_j(_)                         -> 0.

main() ->
    K = 4,  % valor de exemplo
    J = calcular_j(K),
    io:format("k = ~w~n", [K]),
    io:format("j = ~w~n", [J]).
