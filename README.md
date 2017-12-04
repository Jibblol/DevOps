# Eksamen - DevOps i skyen - 2017

I denne oppgaven har jeg satt opp en løsning som bruker virtuelle maskiner, i Google Cloud, med Jenkins for bygging og utrulling av en applikasjon, og Ansible for konfigurasjonsstyring. Løsningen kjører Ubuntu 14.04.

# Jenkins

I min løsning valgte jeg å installere Jenkins på en VM (compute engine) i Google Cloud. For å installere Jenkins fulgte jeg [Installing Jenkins on Ubuntu](http://wiki.jenkins.io/display/JENKINS/Installing+Jenkins+on+Ubuntu)

Jenkins tar seg av bygging og deployment av applikasjonen ved hjelp av en pipeline. Inne i Jenkins har jeg opprettet en "job" som vil trigge automatisk bygging av prosjektet ved push til GitHub. For å få til dette brukte opprettet jeg en webhook i GitHub som sender en POST-request til Jenkins-jobben, og byggingen vil starte.

![Image](images/pipeline_1_setup.PNG)
![Image](images/pipeline_2_setup.PNG)
![Image](images/Git_webhook.PNG)