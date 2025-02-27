# DataInvestor

DataInvestor è un framework di backtesting modulare basato su pianificazione e open source gratuito basato su Python per long-short su azioni e strategie di trading sistematiche basate su ETF.

### Descritto ed utilizzato su TradingQuant.it (www.tradingquant.it)

DataInvestor può essere meglio descritto come una raccolta di moduli liberamente accoppiati per l'esecuzione di backtest end-to-end con meccaniche di trading realistiche.

I moduli predefiniti forniscono funzionalità utili per alcuni tipi di strategie di trading sistematiche e possono essere utilizzati senza modifiche. Tuttavia, l'intento di DataInvestor è che gli utenti estendano, ereditino o sostituiscano completamente ciascun modulo al fine di fornire funzionalità personalizzate per il proprio caso d'uso.

Il software è attualmente in fase di sviluppo attivo ed è fornito con una licenza permissiva "MIT".

E' stato progettato per sopportare versioni di python maggiori alla 3.6


# Installazione

L'installazione richiede un ambiente Python3. L'approccio più semplice è scaricare una distribuzione scientifica autonoma di Python come [Anaconda Individual Edition](https://www.anaconda.com/products/individual#Downloads). È quindi possibile installare DataInvestor in un [ambiente virtuale](https://docs.python.org/3/tutorial/venv.html#virtual-environments-and-packages) isolato tramite pip come mostrato di seguito.

Eventuali problemi con l'installazione devono essere segnalati al team di sviluppo come problemi [qui](https://github.com/tradingquant-it/DataInvestor/issues).


## conda

[conda](https://docs.conda.io/projects/conda/en/latest/) è uno strumento da riga di comando fornito con la distribuzione Anaconda. Ti consente di gestire gli ambienti virtuali e pacchetti _utilizzando lo stesso strumento_.

Il seguente comando creerà un nuovo ambiente chiamato "backtest".

```
conda create -n backtest python
```
Questo utilizzerà la versione Python predefinita di Conda. Al momento della stesura di questo documento si trattava di Python 3.12. Attualmente DataInvestor supporta Python 3.9, 3.10, 3.11 e 3.12. Facoltativamente è possibile specificare una versione Python sostituendo python==3.9 quando si crea l'ambiente vistguale, come segue:

```
conda create -n backtest python==3.9
```

Per iniziare a utilizzare DataInvestor, è necessario attivare questo nuovo ambiente e installare DataInvestor utilizzando pip.

```
conda activate backtest
pip3 install datainvestor
```

## pip

In alternativa, puoi utilizzare [venv](https://docs.python.org/3/tutorial/venv.html#creating-virtual-environments) per gestire la creazione dell'ambiente e [pip](https://docs.python .org/3/tutorial/venv.html#managing-packages-with-pip) per gestire l'installazione del pacchetto.

```
python -m venv backtest
source backtest/bin/activate # È necessario attivare l'ambiente prima di installare il pacchetto
pip3 install datainvestor
```

# Documentazione completa

La documentazione completa e i tutorial per i neofiti di DataInvestor sono disponibili su Tradingquant.it all'indirizzo [https://www.tradingquant.it/datainvestor/](https://www.tradingquant.it/datainvestor/).

# Quickstart

Il repository DataInvestor fornisce alcune semplici strategie di esempio su [/examples](https://github.com/tradingquant-it/DataInvestor/tree/master/examples).

All'interno di questa sezione di avvio rapido, un classico portafoglio di azioni/obbligazioni classico è sottoposto a backtest con ribilanciamento mensile ogni l'ultimo giorno del mese.

Per iniziare, scarica il file [sixty_forty.py](https://github.com/tradingquant-it/DataInvestor/blob/master/examples/sixty_forty.py) e inseriscilo nella directory di tua scelta.

Lo script 60/40 utilizza i dati delle "barra giornaliera" OHLC di Yahoo Finance. In particolare richiede [SPY](https://finance.yahoo.com/quote/SPY/history?p=SPY) e [AGG](https://finance.yahoo.com/quote/AGG/history? p=AGG) dati ETF. Scarica la cronologia completa per ciascuno e salva come file CSV nella stessa directory di ``sixty_forty.py``.

Supponendo che esista un ambiente Python appropriato e che DataInvestor sia stato installato correttamente (vedi **Installazione** sopra), assicurati di attivare l'ambiente virtuale, vai alla directory con ``sixty_forty.py`` e digita:

```
python sixty_forty.py
```

Vedrai quindi alcuni output della console mentre il motore di simulazione del backtest viene eseguito ogni giorno ed esegue la logica di ribilanciamento una volta al mese. Una volta completato il backtest, apparirà un report.

Puoi esaminare il file ``sixty_forty.py`` commentato per vedere l'attuale API di backtesting di DataInvestor.

In caso di domande sull'installazione o sull'utilizzo di esempio, non esitare a inviare un'e-mail a [support@tradingquant.it](mailto:support@tradingquant.it)

# Funzionalità attuali

* **Backtesting Engine** - DataInvestor utilizza un approccio di costruzione del portafoglio basato sulla pianificazione per il trading sistematico. La generazione del segnale è disaccoppiata dalla costruzione del portafoglio, dalla gestione del rischio, dall'esecuzione e dalla contabilità di intermediazione simulata in modo modulare e orientato agli oggetti.

* **Performance Statistics** - DataInvestor fornisce una tipica valutazione delle prestazioni delle strategie a "foglio di lavoro". Supporta anche l'esportazione delle statistiche tramite JSON per consentire al software esterno di utilizzare le metriche dei backtest.

* **Free Open-Source Software** - DataInvestor è stato rilasciato con una licenza MIT open source permissiva. Ciò consente il pieno utilizzo sia nelle applicazioni di ricerca che commerciali, senza restrizioni, ma senza garanzie di alcun tipo (vedere **Licenza** di seguito). DataInvestor è completamente gratuito e non costa nulla da scaricare o utilizzare.

* **Software Development** - DataInvestor è scritto nel linguaggio di programmazione Python per un semplice supporto multipiattaforma. DataInvestor contiene una suite di unit e test di integrazione per la maggior parte dei suoi moduli. I test vengono continuamente aggiunti per nuove funzionalità.

# Termini di Licenza

Copyright (c) 2018-2025 Tradingquant.it


Con la presente viene concessa l'autorizzazione, a titolo gratuito, a chiunque ottenga una copia di questo software e dei file di documentazione associati (il "Software"), di trattare il Software senza restrizioni, inclusi, senza limitazione, i diritti di utilizzo, copia, modifica, unione , pubblicare, distribuire, concedere in licenza e / o vendere copie del Software e consentire alle persone a cui il Software è fornito di farlo, alle seguenti condizioni:

L'avviso di copyright di cui sopra e questo avviso di autorizzazione devono essere inclusi in tutte le copie o parti sostanziali del Software.

IL SOFTWARE VIENE FORNITO "COSÌ COM'È", SENZA GARANZIA DI ALCUN TIPO, ESPLICITA O IMPLICITA, INCLUSE, MA NON SOLO, LE GARANZIE DI COMMERCIABILITÀ, IDONEITÀ PER UNO SCOPO PARTICOLARE E NON VIOLAZIONE. IN NESSUN CASO GLI AUTORI OI TITOLARI DEL COPYRIGHT SARANNO RESPONSABILI PER QUALSIASI RIVENDICAZIONE, DANNO O ALTRA RESPONSABILITÀ, SIA IN UN'AZIONE DI CONTRATTO, TORTO O ALTRIMENTI, DERIVANTE DAL, O IN CONNESSIONE CON IL SOFTWARE O L'USO O ALTRI TRATTAMENTI NEL SOFTWARE.

# Trading Disclaimer

Il trading di azioni a margine comporta un alto livello di rischio e potrebbe non essere adatto a tutti gli investitori. I rendimenti passati non sono indicativi di risultati futuri. L'alto grado di leva finanziaria può funzionare sia contro di te che per te. Prima di decidere di investire in azioni, è necessario considerare attentamente i propri obiettivi di investimento, il livello di esperienza e la propensione al rischio. Esiste la possibilità che tu possa sostenere una perdita di parte o tutto il tuo investimento iniziale e quindi non dovresti investire denaro che non puoi permetterti di perdere. Dovresti essere consapevole di tutti i rischi associati al trading di azioni e chiedere consiglio a un consulente finanziario indipendente in caso di dubbi.
