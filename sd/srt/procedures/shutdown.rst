.. _nuraghe-shutdown:

*******************
Shutdown di NURAGHE 
*******************

.. index:: single: NURAGHE - Shutdown


- Innanzitutto chiudere la console di nuraghe. Aprire un terminale dal desktop virtuale ``CONSOLE`` di ``nuraghe-obs1`` ::

  $> nuragheConsole --stop

- Dal desktop virtuale ``AS`` di ``nuraghe-mng`` chiudere l'interfaccia grafica della superficie attiva cliccando sul pulsante ``Quit``

- Su ACS Command Center  nel desktop virtuale ``MANAGER`` chiudere i *containers* cliccando il pulsante di chiusura collettiva
  (pulsante con quadrato nero posizionato sotto la lista dei container). In alternativa è possibile chiudere singolarmente ogni container

- Chiudere il container degli oscillatori locali:

  #. selezionare la shell *nuraghe-lo* sul desktop virtuale ``MISC`` di ``nuraghe-mng``
  #. premere il tasto ``enter`` per verificare di avere il controllo del prompt
  #. nel caso in cui non si abbia il controllo del prompt, premere ``ctrl-c``
  #. eseguire il comando::

     $ acsStopContainer LocalOscillatorsContainer

- Chiudere i container relativi alla superficie attiva:
  
  #. selezionare una shell di *nuraghe-as* sul desktop virtuale ``AS`` di nuraghe-mng
  #. premere il tasto ``enter`` per verificare di avere il controllo del prompt
  #. nel caso in cui non si abbia il controllo del prompt, premere ``ctrl-c``
  #. eseguire il comando::

     $ ~/SRTStopActiveSurfaceContainer


- Su ACS Command Center, chiudere l' ``ACS Suite`` premendo il pulsante ``stop`` nell'omonimo riquadro.

.. note:: 

   In certi casi il processo di chiusura di *ACS* può lasciare attivo qualche processo precludendo 
   la chiusura pulita di tutto il sistema. In tal caso eseguire il comando **killACS** e attendere
   il messaggio *Removing ACS_INSTANCE temporary directories ... done*   

