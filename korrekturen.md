# Machine Learning für Zeitreihen: Korrekturen

Liebe LeserInnen,  
wie moderne Software lebt auch ein Fachbuch von Hinweisen zu Problemen und Bugs. 
Ich danke deshalb ganz herzlich den LeserInnen für ihre Kommentare!  
Wenn Sie weitere inkorrekte oder unklare Textpassagen im Buch finden, die unten noch nicht aufgeführt sind, eröffnen Sie gerne einen Issue hier auf *GitHub* oder schreiben Sie eine E-Mail an <tplusone@posteo.de>!  
Im Folgenden finden Sie eine Liste mit fehlerhaften oder problematischen Textstellen inkl. Korrektur.  
  
Herzlichen Dank für Ihr Verständnis!  
***
## Korrekturen
**_Kapitel 3, Abschnitt 3.5.2, S. 93_**

In den abgedruckten Formeln sind die _x_-Werte und die Gewichtungen (betas) vertauscht. Die Zahlenwerte (0/1), die die zu modellierenden Situationen bezeichnen, werden als _x_-Werte eingesetzt und nicht als Gewichtungen (betas). Es müsste also heißen:
![Interaktionen](Interaktionen.png)
***
**_Kapitel 5, Abschnitt 5.1.1, S. 151, Bild 5.2_**

In _Bild 5.2_ sind die _y_-Achsenbeschriftungen der Aktivierungsfunktionen zum Teil falsch wiedergegeben. Zum Beispiel werden in der Identity-Funktion die _x_-Werte unverarbeitet auf die _y_-Achse projiziert. Richtig ist also folgende Darstellung:
![Interaktionen](Bild5_2.png)
***
**_Kapitel 5, Abschnitt 5.5.1, S. 205, Bild 5.18_**

In Bild 5.18 sind die _x_-Werte den Gewichten zum Teil falsch zugeordnet. Dargestellt ist die Arbeit des Kernels im Hinblick auf den ersten Bildauszug, der die Werte _x_-Werte 1, 2, 3, 6, 7, 8, 11, 12, 13 bearbeitet. Richtig ist also folgende Darstellung:
![Interaktionen](Bild5_18.png)
***
**_Kapitel 5, Abschnitt 5.6.2, S. 223 Ausgabe oben_**

Hier ist die falsche Shape angegeben. Es müsste heißen:

    (56104, **14**), (14025, **14**), (56104, 1), (14025, 1)  
***
**_Kapitel 5, Abschnitt 5.6.2, S. 226 Code unten_**

Es fehlt der Import der LSTM-Layer. Der Code müsste also lauten:

    1	from tensorflow.keras.models import Sequential
    2	from tensorflow.keras.layers import (Dense, Dropout, Conv1D, 
    3	                                    LSTM, Bidirectional)
    4	from tensorflow.keras.regularizers import l2
    5	reg = l2(0.0001)
    6	model = Sequential()
    7	model.add(Conv1D(filters=32, kernel_size=6, 
    8	                input_shape=(144, 14), 
    9	                activation='relu'))
    10	model.add(Dropout(0.3))
    11	model.add(Bidirectional(LSTM(units=32, dropout=.3, 
    12	            kernel_regularizer=reg)))            
    13	model.add(Dense(units=1, kernel_regularizer=reg))
    14	model.compile(loss='mse', optimizer='adam', metrics=['mae'])

