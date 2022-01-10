# WykopSexChanger
Chcesz zmienić płeć na wykop.pl, ale ułomna moderacja nie chce Ci jej zmienić pomimo poprawnej argumentacji?
Mamy na to sposób!
Ten oto skrypt zmieni Twoją płeć

## Bezpieczeństwo

**Czy skrypt jest bezpieczny?**

Tak! Skrypt ten jest bezpieczny! Można nawet bez problemu obejrzeć kod, ponieważ jest otwartoźródłowy.
Jak nie rozumiesz programowania (albo Shell Scriptu) każda część kodu została podpisana, tak by każdy mógł się dowiedzieć co dokładnie ten kod robi!

## Michał B. i zabezpieczenia API wykop.pl

Jako że ostatnim czasem mają miejsca przejęcia kont na wykop.pl (ten skrypt nie ma z tym nic wspólnego, to wina kijowego wykonania całej strony) administracja serwisu dodała weryfikację Captcha do API wykopu. Bez zweryfikowania się skrypt nie zadziała. Jak temu zaradzić został stworzony specjalny poradnik jak zmienić płeć na wykop.pl (jest na samym dole).

## Wymagania

**JQ**

`sudo apt-get install jq`

**CURL**

`sudo apt-get install curl`


## Zmiana płci

1. Pobierz wszystkie wymagane programy z sekcji Wymagania
2. Uruchom skrypt (nie zadziała)
3. Wejdź na wykop.pl z przeglądarki (https://wykop.pl/)
4. Zweryfikuj Captchę
5. Uruchom skrypt jeszcze raz (teraz zadziała :D)

Po wykonaniu wszystkich kroków płeć powinna zostać zmieniona
