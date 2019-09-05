.. _descr:


Descrizione Sistema di controllo 
================================

DISCOS è il sistema di controllo di SRT ed è distribuito su 2 server:

#. discos-manager.srt.inaf.it
#. discos-console.srt.inaf.it


DISCOS ha accesso tramite tcp/ip  ad altre risorse:

- ACU (antenna control unit), che si occupa del controllo dei servo sistemi maggiori (assi di elevazione e azimuth e *cable wrap*)
- MSCU (minor servo control unit) 
- Backends (Total Power, XARCOS, DBBC, SARDARA, DFB)
- Terminali VLBI (DBBC + Mark V)
- Schede di controllo dei ricevitori
- Centralina meteo


Postazioni utente
-----------------

Gli SD hanno accesso alle seguenti postazioni utente:

- nuraghe-mng
- nuraghe-as

- ACU-PCP
- ACU-LCP

Le  prime 2 sono collocate in control room, la quinta nella stanza ALER in antenna. 

nuraghe-obs1
~~~~~~~~~~~~


nuraghe-mng
~~~~~~~~~~~

La postazione utente 

- Ospita il manager, ovvero tutti i tool che permettono l'avvio e la gestione dei servizi ACS sui quale si basa NURAGHE
- Consente l'accesso tramite ssh a ``nuraghe-lo`` e ``nuraghe-as``
- Consente l'esecuzione dei tool di diagnostica utili per seguire il corretto svolgimento delle osservazioni
- Contiene i client testuali dei sotto sistemi di nuraghe e la shell di operator input.
- Ospita la console vlbi

ACU-PCP
~~~~~~~

Primary Control Panel, è la replica del ACU_LCP in Control Room. 

Se la modalità di controllo dell'ACU è  impostata su :ref:`remoto <antenna>` 
il pannello è unicamente informativo e pertanto i pulsanti non sortiscono nessuna azione e non aprono finestre informative.


ACU-LCP
~~~~~~~

Local Control Panel.
Situato il ALER, è il pannello di controllo della Antenna Control Unit (ACU), per controllare il comportamento dei servo sistemi principali,
ovvero gli assi di azimuth ed elevazione ed il cable wrap. Eventualmente permette di effettualre la movimentazione se l'ACU è
impostata per il controllo :ref:`locale <antenna>`

