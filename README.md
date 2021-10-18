# Energy-Management-System Phase I

# Description
This project represents a simulation of an energy management system.

# Implementation RO:

Pentru aceasta etapa a proiectului am decis sa construiesc 2 clase principale
si anume :
	- clasa Constructor ce retine informatii utile pentru un consumator
	- clasa Distributor ce retine informatii utile pentru un distribuitor
Aceste clase se pot extinde in functie de tipurile de consumatori si
distribuitori ce pot aparea in viitor si se pot adauga astfel metode specifice
fiecarui tip.

In implementare am introdus si pattern-urile Factory si Singleton, am creat
cate un factory pentru consumatori si distribuitori iar aceste factory-uri 
le-am facut de tipul Singleton pentru ca m-am gandit ca o singura instanta
din fiecare tip de factory este suficienta pentru a genera unul sau mai multe
tipuri de consumatori si distribuitori.

Clasa Input retine toate informatiile primite ca input in program iar 
InputLoader citeste aceste informatii din fisierul de intrare. In clasa 
MonthlyUpdate se citesc update-urile lunare. Asemanator, clasa FileWriter scrie 
rezultatul final dupa terminarea rundelor in fisierul de iesire.

Clasa Main are 2 metode: 
	- metoda main in care se citesc datele de intrare, se simuleaza fiecare 
runda si la final se scrie rezultatul
	- metoda initialround ce simuleaza runda initiala(am preferat folosirea 
acestei metode pentru ca initial pretul contractelor se genereaza pentru fiecare
distribuitor la fel urmand ca mai apoi sa se calculeze in functie de numarul
de clienti al fiecarui distribuitor)

Clasa Distributor contine metoda setContractPrice ce calculeaza pretul
contractului fiecarui distribuitor sau il seteaza la (INF/999999999) in cazul 
in care distribuitorul a dat faliment
