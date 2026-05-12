# Platforma webowa do zarządzania wynikami i osiągnięciami graczy w architekturze ASP.NET Core

- **Tabela 1: `GameLevels` (Poziomy w grze / Tryby gry)**
    - Zawiera definicje poziomów (np. nazwa poziomu, mnożnik punktów, poziom trudności).
- **Tabela 2: `Scores` (Wyniki rozgrywek)**
    - Przechowuje pojedyncze wyniki. (czas - score- poziom)
    - *Relacje:* Klucz obcy do `Users` (kto zagrał) oraz klucz obcy do `GameLevels` (na jakim poziomie).
- **Tabela 3: `Achievements` (Osiągnięcia / Odznaki)**
    - Słownik osiągnięć do zdobycia (np. "Zdobądź 1000 punktów", "Zagraj 10 razy", opis, ikona).
- **Tabela 4: `UserAchievements` (Odblokowane osiągnięcia)**
    - Tabela łącząca (Many-to-Many).
    - *Relacje:* Klucz obcy do `Users`, klucz obcy do `Achievements` oraz data odblokowania.
