[![DOI](https://zenodo.org/badge/246544523.svg)](https://zenodo.org/badge/latestdoi/246544523)

# Analysis of aggregation kinetic data

## What is this notebook for?

This jupyter notebook serves as a template for fast analysis and plotting of aggregation kinetic data. The aim is to provide a tool that can be used to analysise kinetic data files obtained from FLUOstar Omega plate readers (BMG Labtech, Offenburg, Germany). This will provide faster and more efficient data handling and produce publication ready quality figures.

*This document will presumably serve as a supplementary document to a future paper (experimental details will not be included for those reasons)*

## To get started

In order to being able to use this notebook you will need to do the following steps:

1. Install Anaconda3 or miniconda3 in order to install the Jupyter Notebook. (miniconda is smaller)


2. Download the repository from GitHub


3. Navigate to the folder you downloaded from Github


4. Create environment:

    - There is a file in the folder called environment.yml. It contains the required packages.
    - create an environment by writing this command in the terminal:
    
    ```.py
    conda env create -f env_tinna.yml
    ```

5. Activate the environment by the following command:
    ```.py
    conda activate tinna_environment
    ```

6. To make the environment appear in the kernel (within the notebook), you have to do the following in the terminal: 
    ```.py
    pip install --user ipykernel
    ```
    followed by:
    ```.py
    python -m ipykernel install --user --name=tinna_environment
    ```

7. Run Jupyter Notebook. Go into terminal, place yourself in directory where you see the folder that you downloaded from github. Write the following into the terminal:
    ```.py
     jupyter notebook
    ```
8. Go into the notebook, in the bar on the top, select kernel and then change to kernel called "tinna_environment"


For further questions, you are welcome to send to tinna.palmadottir@biochemistry.lu.se




## Useful features of this notebook
I found the library ["Pandas"](https://pandas.pydata.org) very useful tool for data analysis. I think it makes it possible to analysis and work with big and/or complicated data files in a convenient and well understandable way. Using Pandas to process the datafile in this notebook saves the user a lot of time. Students and researchers within the group generally analyse the files by hand in exel, which take much longer time. 
    
In this notebook, the selected data is also exported as a processed text file, that can then be imported to other graphical programs for data visualisation (if preferred). However, I do recommend to use matplotlib, that can be used within the notebook to plot and design the plot according to your needs. I think matplotlib is really useful tool as well. Matplotlib has a [gallery](https://matplotlib.org/3.1.1/gallery/index.html) of examples of plots that can be created with Matplotlib. I recommend visiting the gallery. I found it very useful and inspiring, it gives ideas of good ways to plot and visualise your data.
    
### Response to reviewers:
**Jon Pallbo:** 

Thank you for your review and comments, they were useful and I noticed that you reviewed my work in detail. 
This is what I have implemented from your comments:

-  Added a small sections, where the selected data is combined into one data frame and then exported as a csv file.

-  I changed the environment file, so that it contains much less, just what is needed to run this notebook. The new environment file is called env_tinna.yml. However, I am not sure why the other one looked as it did, each 	package had a lot of numbers behind it. When I made it, I followed the instructions on how the create an environment from the terminal. I noticed that more students had environment files that looked similar to that one. Also when I selected the environment I created before (that did not work for the reviewer) as a kernel in the jupyter notebook, then it worked in my computer. I do not understand why this happens and does not work for others. It would be nice to get a feedback from teacher about why this happens.
      - the older environment file was called. tinna_environment.yml and the new one: env_tinna.yml
      - I keep the old file in the folder, just for the sake of hopefully getting some comments on it, in order to understand better why this happens.
        
-  I did also add instructions about how to get the environment as a kernel within the notebook. see steps 6 and 7 within the sections called “To get started” as well as in the README.

- Figures width was further specified to 18.3 cm wide in inches, 7.2 inches. The ticks (numbers on the axes) were also increased. The last figures were taken out, as it was just another way of showing the same data. I do prefer the previous one as they share the variables names and then it is less of repetition to have the variables name in a box next to the graph and you can also make the text bigger than if the box were within the plots.


***Thank you for your additional comments and suggestions***. 
-  I fixed the spelling mistakes that you pointed to.
-  About the repetition in code cell 7, I agree and had thought about the same thing. I do want to try to design the code so that you can select how many variables are made, by adding an input interactively. That there 		will be a question, where it will be asked how many variables you want to have, and then for each of them you tell which wells correspond to the variable. I have not figured out how I should do that, but it is on my 		future plan. 
- I would appreciate to get some kind of help or input from someone with more experience. If I would manage to implement this, then it would be much more user-friendly for users that are not used to coding and jupyter notebook. 

Thank you,
Tinna

**Eleni**

Thank you for your feedback Eleni, I am glad that you like my project. I did not know that the size of the figure is given in inches, I converted 18.3 cm to inches. I fixed the figure size and changed it to: 
```.py
fig = plt.figure(figsize=(7.2,2.4), dpi=300)
```
I hope that is correct.

Thank you,
Tinna



