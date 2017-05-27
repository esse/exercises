# exercises

# Zadanie 1:

Napisz metodę, która dla podanego parametru `n`, obliczy sumę wszystkich liczb nieparzystych w przedziale `0..n`.

Uwaga! Haczyk polega na tym, że ta metoda ma mieć jedną linijkę ;)

Rozwiązanie zapisz w pliku `exercise_1.rb`.

Przykład:
```ruby
odd_sum(10) #=> 25
odd_sum(1) #=> 1
```

# Zadanie 1 - wersja z gwiazdką:

Metoda którą napisaliście, ma drobną wadę. Spójrzmy co się stanie gdy będziemy podawać jej coraz większe parametry, jak będzie zmieniał się czas wykonywania programu (na moim komputerze):

| n | czas w sekundach |
|---|---|
|100|6.0e-05|
|100_000|0.028689|
|100_000_000|39.777206|

Wynika to z tego, że w tym rozwiązaniu czas wykonania rośnie liniowo w zależności od wielkości liczby! Tutaj znajdziecie co nieco informacji o szacowaniu złożności obliczeniowej:
http://coderslab.pl/blog/algorytmy-i-dane/programisto-nie-zapominaj-o-algorytmach-2/

A tutaj dalszy, bardziej zaawansowany materiał:
https://codility.com/media/train/1-TimeComplexity.pdf

To zadanie da się zrobić w stałym czasie - niezależnie od wielkości `n`, też mieszcząc je w jednej linijce (aczkolwiek tutaj nie jest to obowiązkowe). I to jest zadanie z gwiazdką ;)

Kod do bardzo prostego benchmarku:
```ruby
def simple_b
  start = Time.now
  yield
  return Time.now - start
end

def odd_sum(n)
  ###
end

puts simple_b { odd_sum(100) }
puts simple_b { odd_sum(100_000) }
puts simple_b { odd_sum(100_000_000) }
```
