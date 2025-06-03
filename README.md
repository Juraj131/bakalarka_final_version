# bakalarka_final_version
This is my final form of bachelor thesis codes


Tento projekt obsahuje skripty pre pracu s modelmi na rozbalovanie fazy.

drg_best_model.py:
Hlavny skript pre trenovanie a evaluaciu najlepsieho modelu priamej regresie (DRG).
Pouziva dynamicku simulaciu dat pre trening a staticke data pre validaciu a testovanie.
Uklada najlepsi model, metriky a vizualizacie.

dwc_best_model.py:
Hlavny skript pre trenovanie a evaluaciu najlepsieho klasifikacneho modelu Deep Wrap Count (DWC).
Pouziva dynamicku simulaciu dat pre trening, vypocitava k-mapy a pouziva vazenu cross-entropy loss.
Uklada najlepsi model, metriky (presnost k-mapy, MAE rekonstrukcie) a vizualizacie.

drg_optimalization.py:
Skript urceny na optimalizaciu hyperparametrov pre modely priamej regresie (DRG).
Obsahuje funkcie pre dynamicku simulaciu dat, augmentacie, rozne typy loss funkcii (MAE, MSE, GDL)
a spusta viacero experimentov s rozlicnymi konfiguraciami.

dwc_optimalization.py:
Skript urceny na optimalizaciu hyperparametrov pre klasifikacne modely Deep Wrap Count (DWC).
Podobne ako drg_optimalization.py, ale zamerany na DWC. Riesi vypocet k-map,
pouziva specificke datasety a metriky pre klasifikaciu (presnost k-mapy, MAE rekonstrukcie).

drg_evaluate.ipynb:
Jupyter Notebook pre evaluaciu natrenovaneho modelu priamej regresie (DRG).
Nacita model, konfiguraciu a testovacie data. Vypocita metriky ako MAE, MSE, PSNR, SSIM, GDL.
Vizualizuje vysledky, vratane najlepsich/najhorsich pripadov a histogramu chyb.

dwc_evaluate.ipynb:
Jupyter Notebook pre evaluaciu natrenovaneho klasifikacneho modelu Deep Wrap Count (DWC).
Nacita model, konfiguraciu a testovacie data. Vypocita presnost k-mapy a metriky rekonstrukcie
(MAE, PSNR, SSIM) odvodene z predikovanych k-hodnot. Vizualizuje vysledky.
