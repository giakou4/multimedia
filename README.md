# ΣΥΣΤΗΜΑΤΑ ΠΟΛΥΜΕΣΩΝ 2020-2021

## Advanced Audio Encoder 

Η εργασία στοχεύει στην υλοποίηση ενός κωδικοποιητή/αποκωδικοποιητή ήχου κατά το πρότυπο Advanced Audio Coding (AAC). Παραλλαγές του AAC χρησιμοποιούνται από πολλά διεθνή πρότυπα όπως τα MPEG-2, MPEG-4, H.264 κλπ. Η εκδοχή που παρουσιάζεται στην εργασία μοιάζει περισσότερο με τις προδιαγραφές 3GPP TS 26.403 όπου απουσιάζουν κάποια στάδια επεξεργασίας. Εξαίρεση αποτελεί το ψυχοακουστικό μοντέλο, που είναι μία λίγο απλουστευμένη εκδοχή του MPEG AAC. Παρόλες τις απλουστεύσεις, η συγκεκριμένη εκδοχή οδηγεί σε αρκετά καλά αποτελέσματα. Η κωδικοποίηση και αποκωδικοποίηση AAC ανήκει στην κατηγορία waveform compression και επιχειρεί να αναπαραστήσει το αρχικό σήμα με τέτοια μορφή ώστε η αποκωδικοποιημένη εκδοχή του να ακούγεται όσο γίνεται πιο όμοια με το αρχικό σήμα. Σαν κριτήριο πιστότητας χρησιμοποιείται το ψυχοακουστικό μοντέλο που επιτρέπει την εισαγωγή παραμορφώσεων του σήματος (θορύβου λόγω κβαντισμού) ο οποίος είναι κάτω από το κατώφλι ακουστότητας. Για το λόγο αυτό κυρίαρχο ρόλο παίζει ο μηχανισμός Psychoacoustic Model που καθοδηγεί το μηχανισμό Quantizer. Για τη μείωση της περίσσειας πληροφορίας ο AAC χρησιμοποιεί κατά βάση την προσέγγιση κωδικοποίησης μετασχηματισμού που υλοποιείται με τη χρήση του λεγόμενου Modifed Discrete Cosine Transform (MDCT) στη βαθμίδα Filterbank ενώ για κωδικοποίηση εντροπίας χρησιμοποιεί κωδικοποίηση Huffman που υλοποιείται στην ομώνυμη βαθμίδα. Αναλυτικότερα, κατά την κωδικοποίηση το αρχικό σήμα ήχου (για μας stereo με δειγματοληψία 48000 samples/sec) χωρίζεται σε επικαλυπτόμενα κατά 50% τμήματα (frames) μήκους 2048 δειγμάτων. Στη συνέχεια κάθε frame κωδικοποιείται αυτόνομα και συνεπώς το τελικά κωδικοποιημένο bitstream αποτελείται από την παράθεση των ακολουθιών bits που αντιστοιχούν στα διαδοχικά frames. Για την επικύρωση της λειτουργικότητας, εφαρμόζεται ο AAC στο τραγούδι Licor De Calandraca

### Level 1
* AACoder1.m
* iAACoder1.m
* demoAAC1.m
* SSC.m
* filterbank.m
* iFilterbank.m

### Level 2
* AACoder2.m
* iAACoder2.m
* demoAAC2.m
* TNS.m
* iTNS.m
* TableB219.mat

### Level 3
* AACoder3.m
* iAACoder3.m
* demoAAC3.m
* psycho.m
* AACquantizer.m
* iAACquantizer.m
* TableB219.mat
* loadLUT.m
* encodeHuff.m
* decodeHuff.m
* huffCodebooks.mat
* huffCodebookSF.mat

### Report
* report.pdf

### Notes
* Note 1: For Level 2 and 3, the folder are included in code with with command: addpath.
* Note 2: Scripts work only in MATLAB 2020b

## Support

Reach out to me:
- [giakou4's email](mailto:giakonick98@gmail.com "giakonick98@gmail.com")

## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/giakou4/multimedia/LICENSE)
