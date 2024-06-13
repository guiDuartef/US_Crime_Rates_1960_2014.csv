import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
import statsmodels.api as sm
from google.colab import files
files.upload()

crimerates = pd.read_csv('US_Crime_Rates_1960_2014.csv')
crimerates.head()
corr1 = np.corrcoef(crimerates['Population'], crimerates['Violent'])[0,1]
print(corr1)
corr2 = np.corrcoef(crimerates['Population'],crimerates['Property'])[0,1]
print(corr2)
corr3 = np.corrcoef(crimerates['Forcible_Rape'],crimerates['Aggravated_assault'])[0,1]
print(corr3)
corr4 = np.corrcoef(crimerates['Violent'],crimerates['Property'])[0,1]
print(corr4)
corr5 = np.corrcoef(crimerates['Violent'],crimerates['Murder'])[0,1]
print(corr5)
corr6 = np.corrcoef(crimerates['Population'],crimerates['Aggravated_assault'])[0,1]
print(corr6)
corr7 = np.corrcoef(crimerates['Population'],crimerates['Burglary'])[0,1]
print(corr7)
corr8 = np.corrcoef(crimerates['Population'],crimerates['Vehicle_Theft'])[0,1]
print(corr8)

#Pergunta de violencia e populçao

media_crimerates = crimerates['Population'].mean()
print("Violent", )


media_crimerates = crimerates['Population'].mean()
print("Média dos crimes: ", media_crimerates)

#populaçao e furto de veiculos 

mediana_crimerates = crimerates['Population'].median()
print("Vehicle_Theft" , )


mediana_crimerates = crimerates['Violent'].median()
print("Vehicle_Theft" , )


mediana_crimerates = crimerates['Violent'].median()
print("Aggravated_assault " , mediana_crimerates)
