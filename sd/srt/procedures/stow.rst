.. _stow:
Parcheggio e messa in sicurezza dell'antenna (STOW)
*********************************************

Per parcheggiare in sicurezza l'antenna eseguire la prima di queste procedure. Nel caso in cui non funzionasse, passare alla successiva:

#.  :ref:`Stow mediante NURAGHE <stownuraghe>`
#.  :ref:`Stow mediante pulsante verde auto-stow <stowgreenbutton>`
#.  :ref:`Stow mediante Local Control Panel (LCP) <stowlcp>`


.. _stownuraghe:

STOW mediante NURAGHE
-----------------------------------------

Da ``operator input`` su **nuraghe-mng** eseguire i comandi::

>goTo=*,89d
>servoPark
>asPark

Nel caso si sia usato il derotatore eseguire il comando::

>derotatorPark

Quando l'antenna è arrivata a 89° di elevazione eseguire::

>antennaPark

.. important::
   La procedura è completa quando sulla console  ACU-PCP, compare il riquadro rosso **AXIS BLOCKED**, 
   e gli assi di azimuth ed elevazione sono disattivati.

 



.. _stowgreenbutton:

STOW mediante pulsante verde auto-stow
--------------------------------------


premere il  **pulsante verde**, posizionato sul tavolo in prossimità della console nuraghe-mng

.. note:: La velocità con la quale l'antenna si muove in elevazione verso la posizione di *stow*, con questa procedura, è circa 0.1 deg/s,
   nella peggiore delle ipotesi saranno necessari  15 minuti per raggiungerla. Questo poiché, in caso di vento forte, la bassa velocità
   limita l'assorbimento di corrente. 

.. important::
   La procedura è completa quando sulla console  ACU-PCP, compare il riquadro rosso **AXIS BLOCKED**, 
   e gli assi di azimuth ed elevazione sono disattivati.


.. _stowlcp:

STOW mediante il Local Control Panel (LCP) dell'ACU
------------------------------------------------------

Se né la procedura di STOW mediante NURAGHE, né quella mediante pulsante di auto-stow hanno dato buon esito vuol dire che
qualcosa di serio è accaduto.
Pertanto, occorre:

- verificare tramite ACU-PCP se ci sono condizioni di errori;
- verificare se sono ci sono emergency stop attivi

In caso di errori o emergency stop attivi è necessario analizzare il problema e valutare come procedere.
Se NURAGHE non permette di riconoscere errori o emergency stop è necessario passare alla modalità locale (vedi procedure).

AUTOSTOW (Wind Park)
--------------------

Nel caso in cui il vento di raffica superi i 50 KM/h il software di controllo invia un comando di ``stow`` e l'antenna verrà parcheggiata
in automatico

.. warning:: La responsabilità ultima per la messa in sicurezza del sistema rimane del supervisor on duty, nonostante la procedura di autostow
 
