**********
Ricevitori
**********

Controllo Temperatura criogenica
================================
Per controllare la temperatura criogenica degli LNA, da una shell di
nuraghe-obs1::

$>tail -f ~/logs/receivers/receivers.log


Verranno visualizzate le temperature. ``ctrl-c`` per uscire.

L'aggiornamento avviene ogni 3 minuti, pertanto nel caso in cui il timestamp
indichi che è trascorso molto tempo dall'ultima lettura occorre verificare che:

#. NURAGHE sia avviato
#. lo script di monitoraggio sia attivo.

Per verificare che lo script di monitoraggio sia attivo, da nuraghe-obs1 dare il comando::

  ps aux | grep receiversmonitor.py

Se è attivo, nella risposta al comando comparirà un messaggio simile al seguente::

    observer  8811  0.1  0.7  62716 14912 pts/25   Sl+  11:57   0:03 /alma/ACS-8.2/Python/bin/python /home/observer/Nuraghe/introot/bin/receiversmonitor.py

Se non dovesse essere attivo:

- aprire una nuova shell (click su 'application -> accessories -> terminal') su
  nuraghe-obs1

- lanciare il comando::

   - receiversmonitor.py &

- chiudere la shell con ``ctrl-d`` o con il comando *exit*   (**NON chiudere la shell cliccando sulla 'x'** in alto a destra)

