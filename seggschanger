#! /bin/sh

{
echo "Login: "   #Zapytanie o login
read varname     #funkcja read zapisuje to co wpisałeś (czyli twój login)
LOGIN=${varname} #zmiana nazwy zmiennej zapisanej przez read na LOGIN
echo "Hasło: "   #Zapytanie o hasło
read varname     #funkcja read zapisuje to co wpisałeś (czyli twoje hasło)
HASLO=${varname} #zmiana nazwy zmiennej zapisanej przez read na HASLO
echo             #puste echo powoduje przerwę między tekstem
echo Twój login to ${LOGIN} a hasło to ${HASLO}   #potwierdzenie jakie dane się wpisało
echo                                              #przerwa
echo Jaką płeć chcesz?                            #Tutaj (wszystkie echo) jest menu wyboru płci
echo "Niebieski Pasek: 1"
echo "Różowy Pasek: 2"
echo "\e[90mpssssst, aby dokonać wyboru musisz wpisać 1 lub 2\e[0m"
echo "\e[34mUWAGA! ZMIANA PŁCI SPOWODUJE USUNIĘCIE DANYCH PROFILU JAK IMIE, NAZWISKO, MIEJSCE ZAMIESZKANIA CZY OPIS (posty i obrazki w tle i profilowe zostaną nieruszone)\e[0m"
read wybor        #zczytanie jaki wybór dokonał użytkownik

if [ ${wybor} -eq 1 ]     #if, czyli z angielskiego jeżeli, w tym przypadku jeżeli wybór równa się jeden wykonaj kod poniżej
then                      #część funkcji if

 echo "Zmienianie płci... (Nie zajmie więcej niż 20 sekund)" #informacja
 
 X=$(curl -s -A "okhttp/9.9.7" "https://a2.wykop.pl/login/appkey/d99b6pFK8f" -d "login=${LOGIN}&password=${HASLO}" | jq -r .data.userkey)   #generowanie userkeya
 
 sleep 5 #funckja sleep powoduje wstrzymanie kodu o podaną ilośc czasu (tu 5 sekund)
 
 curl -s -A "okhttp/9.9.7" "https://a2.wykop.pl/settings/profile/data/full/appkey/d99b6pFK8f/userkey/$X" -d "sex=1" #pierwsza zmiany płci na niebieski pasek
 
 sleep 5 #wstrzymanie kodu na 5 sekund
 
 X=$(curl -s -A "okhttp/9.9.7" "https://a2.wykop.pl/login/appkey/d99b6pFK8f" -d "login=${LOGIN}&password=${HASLO}" | jq -r .data.userkey) #generowanie userkeya (znowu)
 
 sleep 5 #kolejne wstrzymanie kodu
 
 curl -s -A "okhttp/9.9.7" "https://a2.wykop.pl/settings/profile/data/full/appkey/d99b6pFK8f/userkey/$X" -d "sex=1"; #druga próba zmiany płci, przez chujowośc Wykopowego API zmiana płci działa co drugi raz, tzn. za pierwszym uruchomieniem kodu zadziała, drugie nie, trzecie tak, czwarte nie itd itd, w skrócie kod wykonuje się dwa razy dla pewności
 
 echo       #przerwa w tekście
 echo
 echo "Od teraz masz niebieski pasek!"   #brawo! przeszłeś operacje zmiany płci na wykop.pl na męską!
 
fi  #część funkcji if

if [ ${wybor} -eq 2 ]   #To co tutaj poniżej widzisz to to samo co powyżej, tylko sex=2 czyli zmieni Ci płeć na różowy pasek i lekkie zmiany w tekście (możesz porównać)
then

 echo "Zmienianie płci... (Nie zajmie więcej niż 20 sekund)"
 
 X=$(curl -s -A "okhttp/9.9.7" "https://a2.wykop.pl/login/appkey/d99b6pFK8f" -d "login=${LOGIN}&password=${HASLO}" | jq -r .data.userkey)
 
 sleep 5
 
 curl -s -A "okhttp/9.9.7" "https://a2.wykop.pl/settings/profile/data/full/appkey/d99b6pFK8f/userkey/$X" -d "sex=2"
 
 sleep 5
 
 X=$(curl -s -A "okhttp/9.9.7" "https://a2.wykop.pl/login/appkey/d99b6pFK8f" -d "login=${LOGIN}&password=${HASLO}" | jq -r .data.userkey)
 
 sleep 5
 
 curl -s -A "okhttp/9.9.7" "https://a2.wykop.pl/settings/profile/data/full/appkey/d99b6pFK8f/userkey/$X" -d "sex=2";
 
 echo
 echo
 echo "Od teraz masz różowy pasek!"

fi
}
