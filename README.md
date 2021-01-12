# WiFi-Locationing
R | RStudio | Classification
## Project Overview 
Using wireless access point signals, investigate the feasibility of using "wi-fi fingerprinting" to determine a person's location in indoor spaces
<br>
## Code & Resources

<b>R with RStudio</b><br>
<b>Packages:</b> readr, caret, C50, doParallel, tidyr, RMariaDB, RMySQL, ggplot2
<br>
<b>Supervised learning approach:</b> Classification
<br><br>
<b>Data:</b> The dataset was provided by University of Texas at Austin</a>.
The dataset was comprised of the following attributes:  
<ul>
        <li>Strength of wireless access point signal </li>
        <li>Longitude</li>
        <li>Latitude</li>
        <li>Building number</li>
        <li>Floor number</li>
        <li>Room number</li>
        <li>Position of person (inside or outside room)</li>
        <li>User Id (18 individuals) </li>
        <li>Phone ID (18 phones) </li>
        <li>Timestamp</li>
</ul>

## Model Building & Performance

|Building  | Floors        |Rooms  | WAP Locations |
|----------|:-------------:|------:|----------------:
| 1        |4              | 256   | 259            |
| 2        |4              | 152   | 265            |
| 3        |5              | 317   | 409            |
| Comnbined|13             | 725   | 933            |

<br>
Random Forest was the superior model and produced the best results across the board. My recommendation is to maintain the RF models for the individual buildings because the precision was better for building 2 & 3 and the training times are more manageable. 

<br> <br>
Best Model By Building
<br>

|Building  | Model    |Accuracy |  Kappa | Training Time  |
|----------|:--------:|--------:|--------:|---------------:
| 1        |RF        | .770     | .769   |17 minutes    |
| 2        |RF        | .848     | .847   |22 minutes    |
| 3        |RF        | .811     | .810   |45 minutes    |
| Combined |RF        | .796     | .796   |2.7 hours     |
