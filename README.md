Alat za vođenje evidencije pristiglih i plaćenih režija.

# UI Elementi
* login stranica
* početna stranica
    * pregled popisa lokacija
        * tipka za dodavanje nove lokacije
    * navigacija:
        * tipka za logout
        * tipka za promjenu korisničkih podataka
* forma za dodavanje nove lokacije
    * unosi se samo naziv lokacije
* stranica lokacije
    * zaglavlje
        * naslov lokacije (click 2 edit)
        * navigacija
            * tipka za logout
            * tipka za povratak na popis lokacija (home button)
    * popis mjeseci
        * infinite scroll
            * najnoviji mjesec na vrhu, najstariji na dnu
        * stavke popisa
            * labela: godina / mjesec
            * grid sa popisom vjerovnika
                * stavka vjerovnika
                    * naziv vjerovnika
                    * iznos dugovanja
                    * link na PDF
                    * oznaka status: nepopunjeno, račun pristigao, plaćeno
                    * tipka za brisanje vjerovnika
                * tipka za dodavanje novog vjerovnika
* stranica vjerovnika
    * naziv vjerovnika (click 2 edit)
    * tipka za upload PDF-a
        * upload automatski postavlja status
    * tipka za brisanje PDF-a
    * polje za unos iznosa (click 2 edit)
    * toggle: plaćeno

# Poslovna logika
* popis vjerovnika se automatski prenosi u idući mjesec
    * prijenos se odrađuje automatski - trigger za tu akciju je user login

# Database
* no-sql DB
* entiteti
    * korisnički račun
    * lokacija
        * godina-mjesec
            * vjerovnik
                * PDF

