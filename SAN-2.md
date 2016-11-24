#SAN - Mateusz Łysek, Marcin Świerczek, Robert Słuszniak
##Informacje ogólne - opis
SAN (Storage Area Network) to specjalizowana sieć, o wysokiej przepustowości, łącząca serwery i urządzenia pamięci masowej. Nazywana jest często siecią „za serwerami". Sieć SAN pozwala łączyć tworzące ją urządzenia „każdy z każdym", eliminuje tradycyjne, dedykowane połączenie pomiędzy serwerami a urządzeniami 
pamięci masowej oraz koncepcję posiadania przez serwer i zarządzania pamięcią masową. Ponadto niweluje ograniczenia na ilość danych, do których serwer może mieć dostęp — innymi słowy na ilość urządzeń, które mogą być do niego podłączone. SAN wprowadza elastyczność pozwalająca heterogenicznym serwerom na wspóldzielenie zasobów urządzeń, którymi mogą być dyski, napędy taśmowe i optyczne. Wreszcie sieć SAN łamie bariery odległościowe koncepcji DAS — pamięć masowa może być znacznie oddalona od korzystającego z niej serwera.

SAN może być postrzegana jako rozszerzenie magistral urządzeń pamięci masowych, które pozwala na łączenie z nimi serwerów przy użyciu podobnych elementów, jak w sieciach lokalnych czy rozległych: niterów, hubów, przełączników i mostów. SAN może być siecią lokalną, albo rozleglą. Rysunek poniżej przedstawia sieć pamięci masowych na tle sieci lokalnej/rozległej.

![Rysunek SAN](http://tkabus.pl/SAN2.PNG)

##Główne założenia
Sieci SAN pozwalają ominąć „wąskie gardła" technologii sieciowych. Oferują bezpośrednie, szybkie połączenia pomiędzy urządzeniami na trzy możliwe sposoby: 

1. **Serwer — pamięć masowa**: tradycyjny model podłączenia urządzenia pamięci masowej. Zaletą jest fakt, że pamięć masowa w sieci SAN może być używana jednocześnie przez wiele serwerów 

2. **Serwer — serwer**: sieć SAN zapewnia także szybką i wydajną komunikację między serwerami. 

3. **Pamięć masowa — pamięć masowa**: SAN pozwala na przesyłanie danych pomiędzy urządzeniami pamięci masowej bez pośrednictwa serwerów, które mogą w tym czasie realizować inne zadania. Przykładem jest kopiowanie w tle danych z dysku na taśmę magnetyczną bez interwencji serwera. 

##Korzyści
Sieci pamięci masowych wnoszą następujące korzyści: 

- **Konsolidacja i współdzielenie zasobów dyskowych** 

Poprzez wyeliminowanie bezpośredniego zarządzania pamięcią masową przez serwery, zasoby dyskowe w sieci SAN mogą być skonsolidowane. Przekłada się to na lepsze wykorzystanie zasobów, większą elastyczność, efektywne zarządzanie oraz obniżenie kosztów (infrastruktury i zarządzania). Wyróżniana jest fizyczna i logiczna konsolidacja zasobów. W przypadku konsolidacji fizycznej, dane z wielu systemów są przechowywane na macierzach dyskowych klasy enterprise. Przestrzeń dyskowa tych macierzy jest wspóldzielona przez serwery, partycjonowana w zależności od potrzeb serwerów. Pozostała wolna przestrzeń macierzy (jak i przestrzeń przydzielona, ale niewykorzystana przez serwery) może być alokowana dla serwerów potrzebujących większej powierzchni dyskowej. Dodatkową zaletą jest możliwość powiększenia przestrzeni dyskowej macierzy „na gorąco", bez powodowania przerw w pracy. Konsolidacja logiczna pozwala na łączenie niezależnych systemów dyskowych w wirtualną całość (nie dotyczy to pamięci masowej podłączonej bezpośrednio do serwerów). Wirtualna przestrzeń dyskowa może być tak samo zagospodarowana jak w konsolidacji fizycznej. 

- **Udostępnianie danych** 

Udostępnianie danych oznacza replikację danych dla wielu użytkowników, aplikacji, systemów w celu umożliwienia jednoczesnego ich przetwarzania. Replikacja danych jest konieczna w przypadku środowisk heterogenicznych (różne systemy operacyjne, plikowe), w przypadku środowisk homogenicznych wiele serwerów może uzyskać jednoczesny dostęp do pojedynczej kopii danych. Sieć SAN pozwala na efektywne udostępnianie danych, szybką replikację zbiorów (w sposób przezroczysty dla użytkownika) na poziomie sprzętu i oprogramowania urządzeń. 

- **Skalowalność** 

W przypadku sieci SAN wielkość pamięci masowych nie podlega żadnym ograniczeniom wynikającym z zastosowanego protokołu obsługi (jedynymi ograniczeniami są dostępność pomieszczeń oraz koszty). Przestrzeń dyskowa dzięki konsolidacji może być dodawana lub ujmowana w zależności od potrzeb, bez przerywania pracy środowiska. 

- **Udoskonalone kopie zapasowe i odzyskiwanie danych**

W tradycyjnych rozwiązaniach kopie zapasowe danych mogą być wykonywane bezpośrednio na przechowującym je serwerze, lub na wydzielonym serwerze kopii zapasowych, połączonym z innymi serwerami za pomocą sieci lokalnej. Oba sposoby posiadają niezaprzeczalne wady. Wykonywanie kopii zapasowych bezpośrednio na serwerze powoduje konieczność instalacji wielu napędów taśmowych lub optycznych, co pociąga za sobą znaczne koszty infrastruktury oraz zwiększa koszty zarządzania nośnikami kopii. Kopiowanie poprzez sieć LAN pozwala zmniejszyć koszty infrastruktury poprzez instalację dedykowanego serwera kopii zapasowych połączonych z bibliotekami napędów taśmowych lub optycznych, ale skutecznie dociąża sieć. SAN łamie te ograniczenia: urządzenia kopii zapasowych (biblioteki taśmowe lub optyczne) są wspóldzielone przez serwery, co zmniejsza koszty infrastruktury, a dedykowany, szybki szkielet sieci odciąża sieć lokalną od mchu generowanego w momencie sporządzania kopii. 

- **Klastrowanie serwerów Sieci**

SAN pozwalają na tworzenie wysokowydajnych klastrów serwerów (czyli grup niezależnych serwerów połączonych pomiędzy sobą w celu zwiększenia wydajności, łatwiejszego zarządzania, lepszej skalowalności). Szybki szkielet sieci SAN umożliwia tworzenie dużych klastrów (powyżej 100 serwerów), z dynamicznym dopasowaniem ilości serwerów w zależności od potrzeb, co w połączeniu ze wspóldzielonymi i skonsolidowanymi zasobami pozwala tworzyć wielkie ośrodki przetwarzania danych. 

- **Zwiększone bezpieczeństwo danych** 

SAN pozwala na uruchamianie centrów zapasowych znajdujących się w dużej odległości od ośrodka „produkcyjnego". Tym sposobem można obniżyć ryzyko utraty danych w wyniku katastrof naturalnych, zamachów terrorystycznych, błędów ludzkich 

- **Zredukowane koszty** 

Przy znacznych ilościach przetwarzanych danych (dużych centrach obliczeniowych) wydatki przeznaczone na infrastrukturę sieci SAN okazują się znacznie niższe od wydatków na tradycyjne systemy klient-serwer. Wynika to z różnic w cenach np. za 1 GB przestrzeni dyskowej dużych macierzy w stosunku do pojedynczych dysków, ale także z funkcjonalności, elastyczności oraz łatwego zarządzania. 
Infrastruktura sieci SAN opiera się na dedykowanym szkielecie z protokołami obsługi, lub na istniejących technologiach sieci, najczęściej obsługujących protokół IP przy wykorzystaniu protokołów mapujących do lP protokoły obsługi urządzeń pamięci masowych. 

##Fibre Channel

Jeżeli chodzi o pierwszy rodzaj sieci SAN, powstało kompleksowe rozwiązanie — protokół **Fibre Channel** (sieć SAN zbudowana w oparciu o ten standard często określana jest skrótem **FC-SAN**). Standardy tego protokołu określają wykorzystywane media transmisyjne, topologie, prędkości pracy, kodowanie informacji, struktury danych, kontrolę przepływu oraz błędów, wreszcie zasady mapowania protokołów wyższych warstw. Fibre Channel jest protokołem hybrydowym, skupia w sobie cechy protokołów sieciowych (może obsługiwać wiele topologii, ustalać ścieżki pomiędzy urządzeniami) i protokołów kanałowych (zestawia kanały pomiędzy urządzeniami, które cechują się małym nakładem pracy na obsługę). Wynikająca ze struktury hybrydowej wydajność i szybkość w połączeniu z automatyczną konfiguracją topologii, wydajną kontrolą błędów i szerokimi możliwościami mapowania protokołów warstw wyższych plasują to rozwiązanie na najwyższym miejscu. Wadą pozostają duże koszty technologii oraz jej względna młodość (początki standardu FC sięgają roku 1988), dlatego sieci SAN oparte o Fibre Channel dedykowane są dla dużych klientów korporacyjnych. Głównymi producentami rozwiązań FC są: IBM, EMC, Brocade. 
Jeżeli chodzi o sieci pamięci masowych bazujących na szkielecie sieci IP (określane skrótem E-SAN), najnowszym rozwiązaniem jest protokół iSCSI (internet Smali Computer System Interface). Protokół działa w warstwie 5 (warstwa sesji) modelu ISO/OSI i kapsułkuje w pakiety TCP komendy oraz dane protokołu SCSI Specyfikacja protokołu iSCSI wymusza pełną kompatybilność z sieciami LAN, w związku z czym parametry fizyczne łączy, kontrola błędów czy klasy usług pozostają takie same jak w sieci LAN. Niezaprzeczalną zaletą sieci SAN opartych o szkielet IP i protokół iSCSI jest wykorzystywanie dojrzałych, popularnych technologii sieciowych, oferujących wiele funkcji (elastyczne protokoły routingu, jakość usług), łączących duże przepustowości (np. Ethernet 10Gb/s) z niskimi kosztami infrastruktury. Z tego powodu protokół iSCSI stanowi silnego konkurenta dla Fibre Channel (przekonują o tym poczynania producentów rozwiązań FC, takich jak IBM, EMC, Brocade, Cisco, którzy wprowadzają do swojej oferty urządzenia i systemy oparte na iSCS/). 
