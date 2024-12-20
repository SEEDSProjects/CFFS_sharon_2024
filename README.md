# Climate-Friendly Food Systems (CFFS) Labelling Project

UBC Institute for Resources, Environment and Sustainability (IRES)

## Objective
To implement the Climate-Friendly Food Systems (CFFS) definition at the UBC Campus by producing the weighted metric that informs the choice of icon for each menu item served by UBC Food Services. Currently, this framework conducts the evaluation of greenhouse gas (GHG) emissions, nitrogen loss, freshwater withdrawals, Land use, and stress-weighted water withdrawals of recipes per serving and 100 grams.

## Scope

The Climate-Friendly Food Sustainability (CFFS) labelling is carried out on seven sites, five of which are for UBC Food Services and the last two for AMS. 
- UBC Food Services: Open Kitchen, Gather, Feast, Perugia Cafe, Mercante
- AMS: The Gallery, Blue Chip Cafe

## Python Version

```Python 3.11.10```

## Repository Structure

    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── archive        <- Previous year's data    
    │   ├── cleaning       <- Cleaned datasets
    │   ├── external       <- External dataset for support
    │   ├── final          <- Final calculation results
    │   ├── mapping        <- Dataset with all factors mapped
    │   ├── Misc           <- Miscellanous
    │   ├── New Items      <- New Items in Current Calculation               
    │   ├── preprocessed   <- Preprocessed datasets
    │   └── raw            <- Raw recipes data from Optimal Control
    │
    ├── Misc_Notebooks     <- Miscellaneous Notebooks
    ├── Archived_Notebooks <- Archived Notebooks
    │
    ├── Label_Baseline_Calculation <- Notebooks for Baseline Calculation
    │ 
    ├── Notebooks_UBCFS
    │   └── 1_data_preprocessing.ipynb
    │   └── 2_data_cleaning.ipynb
    │   └── 3_update_info_and_mapping.ipynb
    │   └── 4_data_analysis.ipynb
    │   └── 5_Recipes_Labelling.ipynb
    │
    ├── Notebooks_AMS
    │   └── 1_data_preprocessing.ipynb
    │   └── 2_data_cleaning.ipynb
    │   └── 3_update_info_and_mapping.ipynb
    │   └── 4_data_analysis.ipynb
    │   └── 5_Recipes_Labelling.ipynb
    │
    └── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
        └── figures        <- Generated graphics and figures to be used in reporting

## Instructions

### Baseline Calculation

All baseline calculations are done in ```Label_Baseline_Calculation/baseline_OK.ipynb```. If baseline is updated or a new parameter is added, then please run the file again with updated data files store in ```data/Misc/data_for_calculating_baseline```. 

The baseline numbers are stored in ```data/Misc/baseline.ini``` and are read in during ```5_Recipes_Labelling.ipynb```.

### Label Calculation Process

Although the labelling process is similar between UBCFS and AMS, there are some differences due to different input sources. The detailed explanation for UBCFS and AMS are written in their respective notebooks inside ```Notebook_UBCFS``` and ```Notebook_AMS``` respectively.

```Ingredient_check.ipynb``` is a notebook that generates the ingredients for all products in the current outlet that the calculation is being done for.

For more information, please refer to the tutorial video.

### Miscellaneous Notebooks

1. NLP Model Google Colab Workbook: https://colab.research.google.com/drive/1pckGYAkNr7-rkkefSF6GWSJlBQZN9T--?usp=sharing
2. To automate the manual work of assigning GHG categories to the ingredients list, look at the files inside the ```Misc_Notebooks/Categorizing_IDs_to_GHG_IDs``` directory.
3. Machine Learning Model that deals with Classification into Item IDs inside ```Misc_Notebooks/Machine_Learning_algorithms_solutions/Item_categorization.ipynb```

