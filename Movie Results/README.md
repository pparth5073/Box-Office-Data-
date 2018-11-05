# themoviedb search results

Hi Team. Finished Running.  Left all the detail in the excel file.   A couple of notes:


**About the Results**
```
    1) All Movies are 1990 and later  
    2) This uses the moviedb API search, which is not perfect:  
        - The ORIGINAL Title is what we searched on  
        - The TITLE is what the database returned  
        - Sometimes they do not match   
```

**---Updated--**

```
On 11/5/2018
    1) Added an ***Oscar Winner*** Field. If the Movie was nominated at all, the value is "Winner!"  
    2) This was based on a datafile from " https://datahub.io/rufuspollock/oscars-nominees-and-winners#data "  
    3) The following categories were not included, since they are individual or studio:
        - ACTOR IN A LEADING ROLE
        - ACTOR IN A SUPPORTING ROLE
        - ACTRESS IN A LEADING ROLE
        - ACTRESS IN A SUPPORTING ROLE
        - AWARD OF COMMENDATION
        - HONORARY AWARD
        - IRVING G. THALBERG MEMORIAL AWARD
        - JEAN HERSHOLT HUMANITARIAN AWARD
        - JOHN A. BONNER MEDAL OF COMMENDATION
        - MEDAL OF COMMENDATION
        - SCIENTIFIC AND TECHNICAL AWARD
        
        
``` 



**About the Code**
```
    1) Loops through each Title in tom's sheet.    
    2) Searches the API for the Movie ID  
    3) Use the Movie ID, gets the movie details  
    4) Throws the results in the dataframe  
    5) Hacks:  
        - If the API gives you a "over the threshold", pause code, and search again in 10 seconds  
        - If the API returns no title,  then skip to next  
        - If the API returns multiple genres, grab the first two!  
```

**File Name is**
```
    1) Movie_API_Results
```
