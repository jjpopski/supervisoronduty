************
Servo minori
************


.. _ms-setup-problem:

Risolvere un setup non riuscito
===============================

.. index:: minor servo, servoSetup
   unknown, emergency stop, failure, reset, GFR, M3R, SRP, PFP, MSCU

Problema
--------
Dalla console *OperatorInput* è stato eseguito il setup (comando ``setupXXX`` 
oppure ``servoSetup=XXX``) ma dopo qualche minuto nella console *MinorServo* 
il flag ``starting`` è passato da verde a rosso ed il flag ``ready`` è anche 
lui rosso.

.. note:: Inserire una immagine della console sei servo minori che mostra la 
   situazione descritta.

Soluzione
---------
Su *acsCommandCenter* (macchina *nuraghe-mng*), controllare la finestra di log del container dei servo minori.

.. note:: Inserire immagine di tale finestra di log.

Ci sono tre possibili soluzioni, a seconda del messaggio di errore riportato nella finestra di log: 

* se è riportato "**GFR (o SRP o M3R o PFP) in failure**", non ci si può far nulla, se non contattare il 
  responsabile degli impianti (G.Paolo Vargiu) per avvisarlo del malfunzionamento. Questo è un problema
  ricorrente, che spesso si risolve riarmando il differenziale nel quadro elettrico del servo minore
  in avaria
* se è riportato "**GFR (o SRP o M3R o PFP) in emergency stop**", si vada alla sezione :ref:`ms-emergency-stop`
* se è riportato un messaggio diverso dai precedenti, si vada alla sezione :ref:`mscu-restart`

Problemi di puntamento
======================

.. index:: minor servo, SRP, MSCU

Problema
--------
La sorgente non viene puntata o l'errore di puntamento è molto alto. 

Soluzione
---------
Possibilita':

* container servo giù
* Superficie attiva non configurata 
* failure SRP
* messaggio errore differente da failure, in questo caso :ref:`mscu-restart`
