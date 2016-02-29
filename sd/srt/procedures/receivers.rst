**********
Ricevitori
**********

Controllo Temperatura criogenica
================================


Per controllare la temperatura criogenica degli LNA, da una shell di nuraghe-mng::

$>tail -f ~/logs/receivers.log


verranno visualizzate le temperature. ``ctrl-c`` per uscire.

L'aggiornamento avviene ogni 3 minuti, pertanto nel caso in cui il timestamp
indichi che è trascorso molto tempo dall'ultima lettura occorre verificare che:

#. NURAGHE sia avviato
#. lo script di monitoraggio sia attivo.

Per verificare che lo script di monitoraggio sia attivo, da nuraghe-mng dare il comando::

  ps aux |grep receiversmonitor

Se è attivo, nella risposta al comando comparirà un messaggio simile al seguente::

gavino   19266  0.5  0.1  64260 14708 pts/4    Sl   13:59   0:00 /alma/ACS-8.2/Python/bin/python /home/gavino/Nuraghe/introotTrunk/bin/receiversmonitor.py

Se non dovesse essere attivo:

- aprire una nuova shell (click su 'application -> accessories -> terminal') 

- lanciare il comando ::

   - receiversmonitor.py &

- chiudere la shell con ``ctrl-d`` o con il comando *exit*   (**NON chiudere la shell cliccando sulla 'x'** in alto a destra)



