.. _nuraghe-startup:


****************
Avvio di Nuraghe
****************

.. index:: single: NURAGHE - Avvio




NURAGHE deve essere avviato dalla console *nuraghe-mng*  (username gavino)

Questa console ha 4 desktops virtuali che hanno le seguenti funzioni:

- **MNG** :math:`\rightarrow`  per eseguire ACS Command Center e gli altri tool ACS
- **CONSOLE** :math:`\rightarrow`  per le finestre della console 
- **AS**  :math:`\rightarrow` per connettersi al server della superficie attiva
- **MISC** :math:`\rightarrow` per varie azioni, come ad esempio l'avvio del *LocalOscillatorsContainer*



- Nel desktop virtuale **MNG** digitare in una shell di terminale::

    $> nuragheStable

  il prompt deve apparire come nella figura qua sotto:
  

.. figure:: images/nuraghe_prompt.png
   :alt: terminal nuraghe 
   :align: center
   

- nella medesima shell digitare::

   $> nuraghe -start

- Apparirà ACS Command Center. Selezionare **localhost(single-machine project)**

Avvio di ACS
--------------------

- Avviare ACS  cliccando il pulsante ``start`` nel riquadro **ACS suite**
- Cliccare sul  *log tab* ``ACS`` in modo da selezionarlo:
            
.. figure:: images/nuraghe_uandr.png
   :scale: 50 %
   :alt: nuraghe up and running
   :align: center

- attendere che nel log tab ACS appaia **ACS is up and running**
  E' necessario, indicativamente, circa un minuto affinché ACS sia *up and running*.

Avvio dei *containers*
----------------------------

- individuare il riquadro **Containers**: contiene la lista dei container necessari, tranne che per il *LocalOscillatorsContainer*
  che necessita di una procedura di avvio separata

- Per ciascuno dei container, cliccare sul triangolo verde (è simile al simbolo tasto play di un lettore di musicassette)
- Con l'avvio del container, viene aperta la log tab con il nome del container, oppure nel caso in cui tale log tab  fosse
  già aperta, viene messa in evidenza

.. note::
  
   la finestra **please wait** può essere chiusa senza attendere se il
   container appare nella apposita lista della finestra *Deployment info*, **oppure** 
   se nel log tab del container appare il messaggio ``ContainerStatusMsg: Ready``
  
Container "Local Oscillators"
+++++++++++++++++++++++++++++++++++

- aprire un terminale vuoto nel desktop virtuale **MISC** digitare ::

   $ lo-ssh

- dopo il login, avviare il container con::
   
   $ acsStartContainer -cpp LocalOscillatorsContainer &

Superficie attiva
+++++++++++++++++++++++++++++

La superficie attiva è gestita dal server *nuraghe-as*, accessibile dal desktop virtuale **AS** su nuraghe-mng dove
sono aperte **due shell**  dalle quali effettuare una connessione *ssh*. Selezionare il desktop virtuale **AS** e 
verificare che siano già aperte due *shell* su ``gavino@nuraghe-as``. Una shell aperta su gavino@nuraghe-as appare  come nella figura:

.. figure: images/nuraghe_as_prompt.png
   :align: center
   :scale: 70 %
   :alt: prompt Nuraghe AS


Nel caso in cui le due shell non fossero già aperte,aprire due terminali in entrambi digitare il comando::

$> as-ssh


Tale comando effettua una connessione ssh verso ``nuraghe-as``. 
Quindi su una shell digitare i comandi::

$> nuragheStable
$> asContainers

Nell'altra shell digitare il comando::

$> nuragheStable
$> SRTActiveSurfaceGUIClient &

La procudura è completata quando nellla prima shell appaiono i messaggi ``sectorX done`` dove ``x`` indica il numero del settore
della superficie attiva. Pertanto appariranno 8 messaggi, con x da uno a 8 (N.B potrebbero non essere in sequenza.


Console di NURAGHE 
+++++++++++++++++++++++++++++++++++++++++++++++

Dal desktop virtuale ``CONSOLE`` di  ``nuraghe-obs1`` aprire una shell ed eseguire il comando::

$> nuragheConsole




     
