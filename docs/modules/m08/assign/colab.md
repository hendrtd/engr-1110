# Getting Started with Google Colaboratory

This assignment will introduce you to [Google's
Colaboratory](https://colab.google/) (Colab) software, Google's hosted [Jupyter
Notebook](https://en.wikipedia.org/wiki/Project_Jupyter) service. Colab is free
but does require a Google Account.

This is an **individual** assignment, not a team assignment. Each student is
responsible for completing this assignment and submitting their own solution.

## Colab Overview

1. If you don't have a Google account already, create one at the following
   link.
   - [https://accounts.google.com/signup/v2/webcreateaccount?hl=en&flowName=GlifWebSignIn&flowEntry=SignUp](https://accounts.google.com/signup/v2/webcreateaccount?hl=en&flowName=GlifWebSignIn&flowEntry=SignUp)

1. Become familiar with Colab's structure and capabilities by watching the
   following video:
   - [https://youtu.be/inN8seMm7UI](https://youtu.be/inN8seMm7UI) 

1. Interact with a "Getting Started" Colab notebook below:
    - [https://colab.research.google.com/notebooks/welcome.ipynb#scrollTo=5fCEDCU_qrC0](https://colab.research.google.com/notebooks/welcome.ipynb#scrollTo=5fCEDCU_qrC0)

## Create Your Own Colab Notebook

You must create a Colab notebook to perform the data analysis shown in the
graph below, and similar to the one shown in Chapter 12 of the course zyBook.
Follow each step below to ensure that you create the expected Colab notebook.

![](img/plot.png)

1. In the Colab *File* menu, click *New notebook*.

1. The notebook will have a default "untitled" name. Change the name to
   something meaningful.

1. Click the *+Text* button to add a text cell to the notebook.

1. Click the up-arrow button to the right to move the text cell above the
   existing code cell that was already in the notebook.

1. Double-click the text cell and enter the following:
    ```
    # Alcohol Fatalities 1970 - 2012

    This notebook will compare the trend in total highway fatalities to those
    involving alcohol from 1970 through 2012.
    ```

1. Click *+Text* and enter the following in the resulting text cell.
    ```
    Import a Python library for plotting:
    ```

1. Click *+Code* and enter the following in the resulting code cell. After
   entering the Python `import` statement, click the ">" *Run* button at the
   right of the code cell to execute this statement.
    ```python
    import matplotlib.pyplot as plt
    ```

1. Click *+Text* and enter the following in the resulting text cell.
    ```
    Use the [curl](https://en.wikipedia.org/wiki/CURL) command line tool to download a CSV file with data for 1970 through 2012.
    
    *Data for this project is adapted from [http://www.alcoholalert.com/drunk-driving-statistics.html](http://www.alcoholalert.com/drunk-driving-statistics.html).* 
    ```

1. Click *+Code*, enter the following command, and then click the *Run* button
   to execute.
    ```bash
    !curl https://raw.githubusercontent.com/hendrtd/engr-1110/main/docs/data/dd_stats.csv --output dd_stats.csv
    ```

1. Click *+Text* and enter the following in the resulting text cell.
    ```
    Read the data from the downloaded file.
    ```

1. Click *+Code*, enter the following command, and then click the *Run* button
   to execute.
    ```python
    with open('dd_stats.csv') as f:
    total_fatalities = []
    alcohol_fatalities = []
    for line in f:
        total, alcohol = line.split(',')
        total_fatalities.append(int(total))
        alcohol_fatalities.append(int(alcohol))
    ```

1. Click *+Text* and enter the following in the resulting text cell.
    ```
    Plot the data:
    ```

1. Click *+Code*, enter the following command, and then click the *Run* button
   to execute.
    ```python
    years = range(1970, 2012)
    plt.plot(years, total_fatalities, label="Total")
    plt.plot(years, alcohol_fatalities, label="Alcohol-related")

    plt.xlabel('Year')
    plt.ylabel('Number of highway fatalities')
    plt.legend(shadow=True, loc="upper right")

    # Add plot title
    plt.title("Alcohol related fatalities on highways")

    # Add text giving x,y coordinates of the plot
    plt.text(1970.5, 11000, 'Fatalities spike\n in 1970s', color='grey', fontsize=12)

    # Add a vertical line at x-coordinate 1980
    plt.axvline(1980, color='grey')

    # Add annotation
    arrow_properties = {
        'facecolor': 'black',
        'shrink': 0.1,
        'headlength': 10,
        'width': 2
    }

    plt.annotate('Drinking age changed to 21',
                 xy=(1984, 24762),
                 xytext=(1986, 30000),
                 arrowprops=arrow_properties)

    plt.show()
    ```

1. Click *+Text* and enter the following in the resulting text cell.
    ```
    **Acknowledgment:** This notebook is an adaptation of an exercise in a custom [zyBook](zybook.com) for ENGR 1110 Introduction to Software Engineering (zyBook ISBN: 978-1-394-14295-8). [Author Team](https://www.zybooks.com/authoring-team/)
    ```

1. Compare your notebook to the one below. Make any corrections to your notebook to ensure it matches this provided sample.
    - [https://colab.research.google.com/drive/1mjDot4RXf4nIN7xKYfABMgQym2xtXWc-?usp=sharing](https://colab.research.google.com/drive/1mjDot4RXf4nIN7xKYfABMgQym2xtXWc-?usp=sharing)


## Submit Your Work To Be Graded

1. Click the **Share** menu option in the top right of the Colab window.

1. Make sure that *General Access* is set to "Anyone with the link".

1. Click the **Copy Link** button.

1. Use the link you just copied as the submission to this assignment in Canvas.


