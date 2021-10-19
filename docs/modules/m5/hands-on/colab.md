# Getting Started with Google Colaboratory

This activity will introduce you to Google's Colaboratory (Colab) software, a
cloud-based interactive computing environment similar to [Jupyter
Notebooks](https://en.wikipedia.org/wiki/Project_Jupyter). Colab is free but
does require a Google Account.

The following steps are to be completed by each student individually.

## Colab Overview

1. If you do not have a Google account already, create one at the following
   link.
   - [https://accounts.google.com/signup/v2/webcreateaccount?hl=en&flowName=GlifWebSignIn&flowEntry=SignUp](https://accounts.google.com/signup/v2/webcreateaccount?hl=en&flowName=GlifWebSignIn&flowEntry=SignUp)

1. Become familiar with Colab's structure and capabilities by watching the
   following video:
   - [https://youtu.be/inN8seMm7UI](https://youtu.be/inN8seMm7UI) 

1. Interact with a "Getting Started" Colab notebook below:
    - [https://colab.research.google.com/notebooks/welcome.ipynb#scrollTo=5fCEDCU_qrC0](https://colab.research.google.com/notebooks/welcome.ipynb#scrollTo=5fCEDCU_qrC0)

## Create Your Own Colab Notebook

Let's create a Colab notebook to produce the following plot, as shown in section
11.3 of the course zyBook.

![](img/plot.png)

1. In the Colab *File* menu, click *New notebook*.

2. The notebook will have a default "untitled" name. Change the name to
   something meaningful.

3. Click the *+Text* button to add a text cell to the notebook.

4. Click the up-arrow button to the right to move the text cell above the
   existing code cell that was already in the notebook.

5. Double-click the text cell and enter the following:

```
# Alcohol Fatalities 1970 - 2012

This notebook will compare the trend in total highway fatalities to those
involving alcohol from 1970 through 2012.
```

6. Click *+Text* and enter the following in the resulting text cell.

```
Import a Python library for plotting:
```

7. Click *+Code* and enter the following in the resulting code cell. After
   entering the Python `import` statement, click the ">" *Run* button at the
   right of the code cell to execute this statement.
   
```python
import matplotlib.pyplot as plt
```

8. Click *+Text* and enter the following in the resulting text cell.

```
Data for this project is taken from [http://www.alcoholalert.com/drunk-driving-statistics.html](http://www.alcoholalert.com/drunk-driving-statistics.html). 

Download a CSV file with data for 1970 through 2012:
```

9. Click *+Code*, enter the following command, and then click the *Run* button
   to execute.

```
!curl https://raw.githubusercontent.com/hendrtd/engr-1110/main/docs/modules/m5/hands-on/data/dd_stats.csv --output dd_stats.csv
```

10. Continue adding code and text cells to finish creating the rest of the
    notebook at the link below.
    - [https://colab.research.google.com/drive/1mjDot4RXf4nIN7xKYfABMgQym2xtXWc-?usp=sharing](https://colab.research.google.com/drive/1mjDot4RXf4nIN7xKYfABMgQym2xtXWc-?usp=sharing)


