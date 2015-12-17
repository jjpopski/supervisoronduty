*************************************
Azioni propedeutiche all'osservazione
*************************************
Prima che inizi l'osservazione, il SoD *deve sempre*:

-  :ref:`nuraghe-is-ready`, altrimenti :ref:`lo si avvii <nuraghe-startup>`
- verificare che non siano attivi emergency stop.

Se sono attivi emergency stop:

- verificare qual è la natura dell'emergency e perché è stato premuto il pulsante
- se l'emergenza si è risolta:
  - rilasciare l'emergecy stop
  - riconoscere che  la condizione di emergenza è stata superata tramite:
    - il comando **antennaReset** se l'ACU è in modalità `locale <antenna>`
    - il pulsante **Interlock Acknowledge**, nel pannello ECP in :ref:`ALER <antenna>` 
      se l'ACU è in modalità `remote <antenna>`



.. important:: Il SoD non deve partire dall'assunzione che il sistema 
   sia funzionante nemmeno nel caso in cui il SoD che ha appena terminato il 
   turno gli garantisca che tutto è OK.
   Quindi **prima che inizi l'osservazione** deve sempre seguire scrupolosamente
   la procedura appena descritta, accertandosi che tutti gli step diano 
   esito positivo.

.. toctree::
   :maxdepth: 2

    startup.rst
   is_ready.rst
  
