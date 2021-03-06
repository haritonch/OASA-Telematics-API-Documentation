webGetLinesWithMLInfo
=====================

Είναι όμοιο με το webGetLines μόνο που στέλνει δύο παραπάνω στοιχεία
το **ml_code** και το **sdc_code**.

Api Endpoint
------------

``http://telematics.oasa.gr/api/?act=webGetLinesWithMLInfo``

Response
--------

.. code-block:: python

   [
   {
   "ml_code":"9",
   "sdc_code":"86",
   "line_code":"815",
   "line_id":"021",
   "line_descr":"\u03a0\u039b\u0391\u03a4\u0395\u0399\u0391 \u039a\u0391\u039d\u0399\u0393\u0393\u039f\u03a3 - \u0393\u039a\u03a5\u0396H",
   "line_descr_eng":"PLATEIA KANIGKOS - GKIZI"
   },
   ....
   ]


Response Breakdown
------------------

*ml_code*: Identifier που έχει να κάνει με την περιοχή έναρξης. (Help needed)
Πιθανότατα το ml αντιστοιχεί στο MasterLine.

*sdc_code*: Identifier για το ωράριο που ακολουθεί η γραμμή, δες getSchedLines και getScheduleDaysMasterLine

*Line_Code*: Το Line_Code είναι ο μοναδικός αριθμός που ορίζει το software της τηλεματικής στην κάθε γραμμή.
Βάσει αυτού του αριθμού γίνονται όλοι συσχετισμοί στην βάση δεδομένων του ΟΑΣΑ. Επίσης φαίνεται να είναι URI.

*line_ID*: Unicode formatted string το οποίο είναι ο αριθμός της γραμμής

*line_descr*: Unicode formatted string, με τον τίτλο της γραμμής, 'ΠΛΑΤΕΙΑ ΚΑΝΙΓΓΟΣ - ΓΚΥΖH(ΚΥΚΛΙΚΗ)'

*line_descr_eng*: Ίδιο με το line_descr αλλά ascii formatted
