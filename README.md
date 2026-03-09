# CSE404_Project
This is GitHub repo for CSE404 group project 


# Acquiring data
From https://data.ct.gov/Housing-and-Development/Real-Estate-Sales-2001-2023-GL/5mzw-sjtu/data_preview
Query the online database to reduce the dataset to contain only records 
  on or after October 2nd, 2010 and only for these eight columns:
- List Year (int)
- Date Recorded (mm/dd/yy)
- Town (string)
- Assessed Value (float)
- Sale Amount (float)
- Property Type (one of (Residential, Commercial, Industrial, Apartments, Vacant))
- Residential Type (NULL if Property Type != Residential, else in (Single Family, Two Family, Three Family, Four Family, Condo))
- Location (longitude, latitude) 
    - longitude (vertical LINES) measures left to right. -W/+E
    - latitude (horizontal LINES) measures south to north. -S/+N
    - The points are near (-71, 41) which is 71 degrees West and 41 degrees North

# Making a Jupyter kernel specifically for this project: 
Open the project in VS Code, then open a terminal. pwd should print …/CSE404_Project
Create a virtual environment to act as a python interpreter:
    python -m venv cse404venv 
Activate the environment:
    source cse404venv/bin/activate 
  so now the command line should start with (cse404venv) (base) 
Install the Jupyter kernel in this environment:
    python -m pip install ipykernel 
  now you should be able to run a .ipynb file when this interpreter is selected. 
Register this environment as a Jupyter kernel:
    python -m ipykernel install --user --name cse404 
  Note: cse404 is just a label and has nothing to do with the name of the Python
  environment. You could make it anything and it would still work. 
Installing new packages into this environment:
    source cse404venv/bin/activate
    pip install pandas 
      or 
    pip install pandas scikit-learn numpy. 
Update requirements.txt:
    pip freeze > requirements.txt
Reinstall all requirements (if somebody else updated requirements.txt):
    pip install -r requirements.txt
# Selecting a kernel for the notebook:
Open the notebook in VS Code
Click “select kernel” at the top right > python environments > cse404venv
# To check which Python the kernel uses:
Open a terminal and run
    source cse404venv/bin/activate
Add these lines to a Jupyter cell:
    import sys
    print(sys.executable)
  Run the cell
  Make sure it prints .../CSE404_Project/cse404venv/bin/python




















