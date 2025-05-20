# DATA INGESTION

### Importing data from csv dschool.csv


```python
#importing data from a flat file - excel
import pandas as pd
csv_data = pd.read_csv("dschools.csv")
print(csv_data)
```

          Unnamed: 0                        name         phone  \
    0              0     A. Henderson Elementary  703-670-2885   
    1              1  A.G. Richardson Elementary  540-825-0616   
    2              2       A.M. Davis Elementary  804-674-1310   
    3              3        A.P. Hill Elementary  804-862-7002   
    4              4      A.S. Rhodes Elementary  540-635-4556   
    ...          ...                         ...           ...   
    1983        1983         Yorktown Elementary  757-898-0358   
    1984        1984               Yorktown High  703-228-5400   
    1985        1985             Yorktown Middle  757-898-0360   
    1986        1986           Yowell Elementary  540-825-9484   
    1987        1987             Yuma Elementary  276-386-3109   
    
                      principal grades                              division  
    0        Ms. Suzanne Bevans   PK-5  Prince William County Public Schools  
    1     Mrs. Susan E. Bridges   PK-5        Culpeper County Public Schools  
    2      Dr. Rachel Foglesong   PK-5    Chesterfield County Public Schools  
    3         Mrs. Kori Reddick   KG-5             Petersburg Public Schools  
    4        Mrs. Doris S. Dean   KG-5          Warren County Public Schools  
    ...                     ...    ...                                   ...  
    1983       Karen Washington   KG-5            York County Public Schools  
    1984    Dr. Raymond J. Pasi   9-12       Arlington County Public Schools  
    1985       Dr. Susan Hutton    6-8            York County Public Schools  
    1986     Mrs. Cathy Timmons   PK-5        Culpeper County Public Schools  
    1987      Mrs. Valerie Babb   KG-6           Scott County Public Schools  
    
    [1988 rows x 6 columns]
    

### Importing data from Excel sampled.xls


```python
# install openpyxl to read excel (.xlsx) file
!pip install pandas openpyxl
```

    Requirement already satisfied: pandas in c:\users\cyndi\anaconda3\lib\site-packages (2.2.2)
    Requirement already satisfied: openpyxl in c:\users\cyndi\anaconda3\lib\site-packages (3.1.5)
    Requirement already satisfied: numpy>=1.26.0 in c:\users\cyndi\anaconda3\lib\site-packages (from pandas) (1.26.4)
    Requirement already satisfied: python-dateutil>=2.8.2 in c:\users\cyndi\anaconda3\lib\site-packages (from pandas) (2.9.0.post0)
    Requirement already satisfied: pytz>=2020.1 in c:\users\cyndi\anaconda3\lib\site-packages (from pandas) (2024.1)
    Requirement already satisfied: tzdata>=2022.7 in c:\users\cyndi\anaconda3\lib\site-packages (from pandas) (2023.3)
    Requirement already satisfied: et-xmlfile in c:\users\cyndi\anaconda3\lib\site-packages (from openpyxl) (1.1.0)
    Requirement already satisfied: six>=1.5 in c:\users\cyndi\anaconda3\lib\site-packages (from python-dateutil>=2.8.2->pandas) (1.16.0)
    


```python
# install openpyxl to read excel (.xls) file
pip install xlrd
```

    Requirement already satisfied: xlrd in c:\users\cyndi\anaconda3\lib\site-packages (2.0.1)
    Note: you may need to restart the kernel to use updated packages.
    


```python
import pandas as pd
excel_data = pd.read_excel("sampled.xls")
print(excel_data)
```

         0 First Name   Last Name  Gender        Country  Age        Date    Id
    0    1      Dulce       Abril  Female  United States   32  15/10/2017  1562
    1    2       Mara   Hashimoto  Female  Great Britain   25  16/08/2016  1582
    2    3     Philip        Gent    Male         France   36  21/05/2015  2587
    3    4   Kathleen      Hanner  Female  United States   25  15/10/2017  3549
    4    5    Nereida     Magwood  Female  United States   58  16/08/2016  2468
    5    6     Gaston       Brumm    Male  United States   24  21/05/2015  2554
    6    7       Etta        Hurn  Female  Great Britain   56  15/10/2017  3598
    7    8    Earlean      Melgar  Female  United States   27  16/08/2016  2456
    8    9   Vincenza     Weiland  Female  United States   40  21/05/2015  6548
    9   10     Fallon     Winward  Female  Great Britain   28  16/08/2016  5486
    10  11    Arcelia      Bouska  Female  Great Britain   39  21/05/2015  1258
    11  12   Franklyn      Unknow    Male         France   38  15/10/2017  2579
    12  13    Sherron    Ascencio  Female  Great Britain   32  16/08/2016  3256
    13  14     Marcel   Zabriskie    Male  Great Britain   26  21/05/2015  2587
    14  15       Kina    Hazelton  Female  Great Britain   31  16/08/2016  3259
    15  16   Shavonne         Pia  Female         France   24  21/05/2015  1546
    16  17     Shavon      Benito  Female         France   39  15/10/2017  3579
    17  18   Lauralee     Perrine  Female  Great Britain   28  16/08/2016  6597
    18  19     Loreta      Curren  Female         France   26  21/05/2015  9654
    19  20     Teresa      Strawn  Female         France   46  21/05/2015  3569
    20  21    Belinda     Partain  Female  United States   37  15/10/2017  2564
    21  22      Holly        Eudy  Female  United States   52  16/08/2016  8561
    22  23       Many      Cuccia  Female  Great Britain   46  21/05/2015  5489
    23  24     Libbie       Dalby  Female         France   42  21/05/2015  5489
    24  25     Lester     Prothro    Male         France   21  15/10/2017  6574
    25  26     Marvel        Hail  Female  Great Britain   28  16/08/2016  5555
    26  27    Angelyn        Vong  Female  United States   29  21/05/2015  6125
    27  28  Francesca   Beaudreau  Female         France   23  15/10/2017  5412
    28  29      Garth       Gangi    Male  United States   41  16/08/2016  3256
    29  30      Carla    Trumbull  Female  Great Britain   28  21/05/2015  3264
    30  31       Veta       Muntz  Female  Great Britain   37  15/10/2017  4569
    31  32     Stasia      Becker  Female  Great Britain   34  16/08/2016  7521
    32  33       Jona     Grindle  Female  Great Britain   26  21/05/2015  6458
    33  34      Judie    Claywell  Female         France   35  16/08/2016  7569
    34  35     Dewitt      Borger    Male  United States   36  21/05/2015  8514
    35  36       Nena      Hacker  Female  United States   29  15/10/2017  8563
    36  37     Kelsie     Wachtel  Female         France   27  16/08/2016  8642
    37  38        Sau        Pfau  Female  United States   25  21/05/2015  9536
    38  39    Shanice   Mccrystal  Female  United States   36  21/05/2015  2567
    39  40      Chase      Karner    Male  United States   37  15/10/2017  2154
    40  41     Tommie   Underdahl    Male  United States   26  16/08/2016  3265
    41  42     Dorcas      Darity  Female  United States   37  21/05/2015  8765
    42  43      Angel       Sanor    Male         France   24  15/10/2017  3259
    43  44  Willodean        Harn  Female  United States   39  16/08/2016  3567
    44  45     Weston     Martina    Male  United States   26  21/05/2015  6540
    45  46       Roma  Lafollette  Female  United States   34  15/10/2017  2654
    46  47     Felisa        Cail  Female  United States   28  16/08/2016  6525
    47  48   Demetria       Abbey  Female  United States   32  21/05/2015  3265
    48  49     Jeromy        Danz    Male  United States   39  15/10/2017  3265
    49  50   Rasheeda      Alkire  Female  United States   29  16/08/2016  6125
    

### importing data from mySQL


```python
# in order to connect mySQL, install sqlalchemy
pip install sqlalchemy
```

    Requirement already satisfied: sqlalchemy in c:\users\cyndi\anaconda3\lib\site-packages (2.0.34)
    Requirement already satisfied: typing-extensions>=4.6.0 in c:\users\cyndi\anaconda3\lib\site-packages (from sqlalchemy) (4.11.0)
    Requirement already satisfied: greenlet!=0.4.17 in c:\users\cyndi\anaconda3\lib\site-packages (from sqlalchemy) (3.0.1)
    Note: you may need to restart the kernel to use updated packages.
    


```python
# Reading MySQL tables into a pandas DataFrame
pip install pymysql
```

    Requirement already satisfied: pymysql in c:\users\cyndi\anaconda3\lib\site-packages (1.1.1)
    Note: you may need to restart the kernel to use updated packages.
    


```python
# Import data from mySQL database
import mysql.connector
import pandas as pd

# Connect to the MySQL database
con = mysql.connector.connect(
    host="localhost",
    port = 3306,
    user="root",
    password="123456",
    database="sales_db"
)

# MySQL query
query = "SELECT * FROM customers"

# Load query result into a DataFrame
df = pd.read_sql_query(query, con)

print(df)

# Close the connection
con.close()

```

       CustomerID CustomerName
    0         101     John Doe
    1         102   Jane Smith
    2         103  Bob Johnson
    3         104  Alice Brown
    4         105   Mary Davis
    

    C:\Users\cyndi\AppData\Local\Temp\ipykernel_25060\2417742195.py:17: UserWarning: pandas only supports SQLAlchemy connectable (engine/connection) or database string URI or sqlite3 DBAPI2 connection. Other DBAPI2 objects are not tested. Please consider using SQLAlchemy.
      df = pd.read_sql_query(query, con)
    


```python
# According to the error above, create engine 
import pandas as pd
from sqlalchemy import create_engine

# Create an engine using SQLAlchemy with pymysql for MySQL
engine = create_engine("mysql+pymysql://root:123456@localhost")

# Use pd.read_sql (no warning now!)
customers = pd.read_sql("SELECT * FROM sales_db.customers", con=engine)

# Display rows of data
print(customers)
```

       CustomerID CustomerName
    0         101     John Doe
    1         102   Jane Smith
    2         103  Bob Johnson
    3         104  Alice Brown
    4         105   Mary Davis
    

### importing data from json file


```python

import json
with open('schools.json') as file:
    jsondata = json.load(file)
jsondata
```




    [{'name': 'A. Henderson Elementary',
      'address': '3799 Waterway Dr, Dumfries, VA 22025',
      'phone': '703-670-2885',
      'principal': 'Ms. Suzanne Bevans',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'A.G. Richardson Elementary',
      'address': '18370 Simms Dr, Culpeper, VA 22701',
      'phone': '540-825-0616',
      'principal': 'Mrs. Susan E. Bridges',
      'grades': 'PK-5',
      'division': 'Culpeper County Public Schools'},
     {'name': 'A.M. Davis Elementary',
      'address': '415 S Providence Rd, Richmond, VA 23236-3343',
      'phone': '804-674-1310',
      'principal': 'Dr. Rachel Foglesong',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'A.P. Hill Elementary',
      'address': '1450 Talley Avenue, Petersburg, VA 23803',
      'phone': '804-862-7002',
      'principal': 'Mrs. Kori Reddick',
      'grades': 'KG-5',
      'division': 'Petersburg Public Schools'},
     {'name': 'A.S. Rhodes Elementary',
      'address': '224 W Strasburg Rd, Front Royal, VA 22630',
      'phone': '540-635-4556',
      'principal': 'Mrs. Doris S. Dean',
      'grades': 'KG-5',
      'division': 'Warren County Public Schools'},
     {'name': 'A.W.E. Bassette Elementary',
      'address': '671 Bell St, Hampton, VA 23661',
      'phone': '757-727-1071',
      'principal': 'Mr. Bryce R. Johnson',
      'grades': 'PK-5',
      'division': 'Hampton Public Schools'},
     {'name': "Abb's Valley-Boissevain Elementary",
      'address': "7030 Abb's Valley Road, Bluefield, VA 24605-0000",
      'phone': '276-945-5969',
      'principal': 'Mr. Rodney Gillespie',
      'grades': 'PK-5',
      'division': 'Tazewell County Public Schools'},
     {'name': 'Aberdeen Elementary',
      'address': '1424 Aberdeen Rd, Hampton, VA 23666',
      'phone': '757-825-4624',
      'principal': 'Ms. Karla C. Young',
      'grades': 'PK-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Abingdon Elementary',
      'address': '3035 S Abingdon St, Arlington, VA 22206',
      'phone': '703-228-6650',
      'principal': 'Ms. Joanne Uyeda',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Abingdon Elementary',
      'address': '7087 Powhatan Drvie, Hayes, VA 23072',
      'phone': '804-642-9885',
      'principal': 'Ms. LaQuiche Parrott',
      'grades': 'PK-5',
      'division': 'Gloucester County Public Schools'},
     {'name': 'Abingdon Elementary',
      'address': '19431 Woodland Hills Rd, Abingdon, VA 24210',
      'phone': '276-739-3400',
      'principal': 'Mrs. Megan de Nobriga',
      'grades': 'PK-5',
      'division': 'Washington County Public Schools'},
     {'name': 'Abingdon High',
      'address': '705 Thompson Dr, Abingdon, VA 24210',
      'phone': '276-739-3200',
      'principal': 'Mr. Jimmy King',
      'grades': '9-12',
      'division': 'Washington County Public Schools'},
     {'name': 'Academy at Virginia Randolph',
      'address': '2204 Mountain Rd, Glen Allen, VA 23060',
      'phone': '804-261-5085',
      'principal': 'Ms. Tanika J. Lawson',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'Accawmacke Elementary',
      'address': '26230 Drummondtown Rd, Accomac, VA 23301',
      'phone': '757-787-8013',
      'principal': 'Clara B. Chandler',
      'grades': 'PK-5',
      'division': 'Accomack County Public Schools'},
     {'name': 'Achievable Dream Academy',
      'address': '726 16th St., Newport News, VA 23607',
      'phone': '757-928-6827',
      'principal': 'Ms. Terra Chalmers-Haris',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'Achievable Dream Middle/High',
      'address': '5720 Marshall Ave., Newport News, VA 23605',
      'phone': '757-283-7820',
      'principal': 'Ms. Marylin Sinclair-White',
      'grades': '6-12',
      'division': 'Newport News Public Schools'},
     {'name': 'Achievement, Integrity, And Maturity',
      'address': 'c/o Kathryn Salerno, 2709 Popkins Lane, Alexandria, VA 22306',
      'phone': '703-660-2064',
      'principal': ' ',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Achilles Elementary',
      'address': '9306 Guinea Road, Hayes, VA 23072',
      'phone': '804-642-9140',
      'principal': 'Ms. Molly Broderson',
      'grades': 'PK-5',
      'division': 'Gloucester County Public Schools'},
     {'name': 'Acquinton Elementary',
      'address': '18550 King William Road, King William, VA 23086',
      'phone': '804-769-3434',
      'principal': 'Mrs. Tara Garner',
      'grades': '3-5',
      'division': 'King William County Public Schools'},
     {'name': 'Addison Aerospace Magnet Middle',
      'address': '1220 5th Street NW, Roanoke, VA 24016',
      'phone': '540-853-2681',
      'principal': 'Mr. Robert Johnson',
      'grades': '6-8',
      'division': 'Roanoke Public Schools'},
     {'name': 'Admiral Richard E. Byrd Middle',
      'address': '134 Rosa Lane, Winchester, VA 22602',
      'phone': '540-662-0500',
      'principal': 'Ms. Teresa Ritenour',
      'grades': '6-8',
      'division': 'Frederick County Public Schools'},
     {'name': 'Adult & Career Education Center',
      'address': '141 Goode Street, Danville, VA 24541',
      'phone': '434-799-6471',
      'principal': ' ',
      'grades': '',
      'division': 'Danville Public Schools'},
     {'name': 'Adult Education Center',
      'address': '201 East Nine Mile Road, Highland Springs, VA 23075',
      'phone': '804-328-4095',
      'principal': ' ',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'Adult Learning Ctr.',
      'address': '4160 Virginia Beach Blvd, Virginia Beach, VA 23452-1768',
      'phone': '757-648-6050',
      'principal': ' ',
      'grades': '',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Advanced Technology Center',
      'address': '1800 College Crescent, Virginia Beach, VA 23453',
      'phone': '757-648-5800',
      'principal': 'Mr. Michael D. Taylor',
      'grades': '',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Agnor-Hurt Elementary',
      'address': '3201 Berkmar Drive, Charlottesville, VA 22901-1475',
      'phone': '434-973-5211',
      'principal': 'Mrs. Michele Del Gallo Castner',
      'grades': 'PK-5',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Alanton Elementary',
      'address': '1441 Stephens Rd, Virginia Beach, VA 23454',
      'phone': '757-648-2000',
      'principal': 'Sean Walker',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Albemarle County Community Public Charter School',
      'address': '901 Rose Hill Drive, Charlottesville, VA 22903',
      'phone': '434-972-1607',
      'principal': 'Ms. E. Ashby Kindler',
      'grades': '6-8',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Albemarle High',
      'address': '2775 Hydraulic Road, Charlottesville, VA 22901-8917',
      'phone': '434-975-9300',
      'principal': 'Jay Thomas',
      'grades': '9-12',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Albert Harris Elementary School',
      'address': '710 Smith Road, Martinsville, VA 24112',
      'phone': '276-403-5838',
      'principal': 'Mrs. Felicia Preston',
      'grades': 'KG-5',
      'division': 'Martinsville Public Schools'},
     {'name': 'Albert Hill Middle',
      'address': '3400 Patterson Ave, Richmond, VA 23221-2399',
      'phone': '804-780-6107',
      'principal': 'Mrs. Raquel Jones',
      'grades': '6-8',
      'division': 'Richmond Public Schools'},
     {'name': 'Alberta Smith Elementary',
      'address': '13200 Bailey Bridge Rd, Midlothian, VA 23112-1708',
      'phone': '804-739-6295',
      'principal': 'Elizabeth Stefanko',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'ALC at Bryant',
      'address': '2709 Popkins Ln, Alexandria, VA 22306',
      'phone': '703-660-2101',
      'principal': 'Mr. Larry Johnson',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'ALC at Burke',
      'address': '9645 Burke Lake Road, Burke, VA 20115',
      'phone': '703-426-7300',
      'principal': 'Mrs. Jill Jakulski',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'ALC at Cameron',
      'address': '3434 Campbell Dr, Alexandria, VA 22303',
      'phone': '703-329-2100',
      'principal': 'Ms. Sue Howell',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'ALC at Montrose',
      'address': '6525 Montrose St, Alexandria, VA 22312',
      'phone': '703-426-7340',
      'principal': 'Ms. Sue Howell',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'ALC at Mountain View',
      'address': '5775 Spindle Ct, Centreville, VA 20121',
      'phone': '571-522-6840',
      'principal': 'Ms. Zora Marschall',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Aldie Elementary',
      'address': '23269 Meetinghouse Ln, Aldie, VA 20105',
      'phone': '703-957-4380',
      'principal': 'Shawn Lyons',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Aldrin Elementary',
      'address': '11375 Center Harbor Rd, Reston, VA 20194-2061',
      'phone': '703-904-3800',
      'principal': 'Mr. Shane Wolfe',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Alfred S. Forrest Elementary',
      'address': '1406 Todds Ln, Hampton, VA 23666',
      'phone': '757-825-4627',
      'principal': 'Ms. Tracie W. Albea',
      'grades': 'KG-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Algonkian Elementary',
      'address': '20196 Carter Court, Sterling, VA 20165',
      'phone': '571-434-3240',
      'principal': 'Jennifer Steeprow',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Alleghany High',
      'address': '210 Mountaineer Drive, Covington, VA 24426',
      'phone': '540-863-1700',
      'principal': 'Mr. Fred C. Vaughan Jr.',
      'grades': '9-12',
      'division': 'Alleghany County Public Schools'},
     {'name': 'Altavista Elementary',
      'address': '1003 Lynch Mill Rd, Altavista, VA 24517-1028',
      'phone': '434-369-5665',
      'principal': 'Mrs. Amy Abell',
      'grades': 'PK-5',
      'division': 'Campbell County Public Schools'},
     {'name': 'Altavista High',
      'address': '904 Bedford Avenue, Altavista, VA 24517',
      'phone': '434-369-4768',
      'principal': 'Mr. Ty Gafford',
      'grades': '6-12',
      'division': 'Campbell County Public Schools'},
     {'name': 'Alternative Education Center',
      'address': '4484 Catlett Road, Midland, VA 22728',
      'phone': '540-422-7390',
      'principal': 'Shelly Neibauer',
      'grades': '',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Alternative Education Center',
      'address': '10415 Spotswood Trail, Stanardsville, VA 22973',
      'phone': '434-985-1405',
      'principal': ' ',
      'grades': '',
      'division': 'Greene County Public Schools'},
     {'name': 'Alternative Education Center',
      'address': '175 Mayfield Drive, Boydton, VA 23917',
      'phone': '434-738-6111',
      'principal': 'Mrs. Sandra Wingler-Jones',
      'grades': '',
      'division': 'Mecklenburg County Public Schools'},
     {'name': 'Amelia County Elementary',
      'address': '8533 N Five Forks Rd, Amelia Court House, VA 23002',
      'phone': '804-561-2433',
      'principal': 'John Rokenbrod',
      'grades': 'PK-4',
      'division': 'Amelia County Public Schools'},
     {'name': 'Amelia County High',
      'address': '8500 Otterburn Rd, Amelia Court House, VA 23002',
      'phone': '804-561-2101',
      'principal': 'Mr. Tommy Moon',
      'grades': '9-12',
      'division': 'Amelia County Public Schools'},
     {'name': 'Amelia County Middle',
      'address': '8740 Otterburn Road, Amelia, VA 23002',
      'phone': '804-561-4422',
      'principal': 'Mr. Wes Eary',
      'grades': '5-8',
      'division': 'Amelia County Public Schools'},
     {'name': 'Amelia Street Special Education',
      'address': '1821 Amelia St, Richmond, VA 23220-6696',
      'phone': '804-780-6275',
      'principal': 'Ms. Evelyn B. Waddell',
      'grades': 'PK-12',
      'division': 'Richmond Public Schools'},
     {'name': 'Amelon Elementary',
      'address': '132 Amer Court, Madison Heights, VA 24572',
      'phone': '434-528-6498',
      'principal': 'Mrs. Donna D Lewis',
      'grades': 'PK-5',
      'division': 'Amherst County Public Schools'},
     {'name': 'Amherst County High',
      'address': '139 Lancer Lane, Amherst, VA 24521',
      'phone': '434-946-2898',
      'principal': 'Mr. Haywood Hand',
      'grades': '9-12',
      'division': 'Amherst County Public Schools'},
     {'name': 'Amherst Elementary',
      'address': '156 Davis St, Amherst, VA 24521',
      'phone': '434-946-9704',
      'principal': 'Julie Steele',
      'grades': 'PK-5',
      'division': 'Amherst County Public Schools'},
     {'name': 'Amherst Middle',
      'address': '165 Gordons Fairground Rd, Amherst, VA 24521',
      'phone': '434-946-0691',
      'principal': 'Ms. Christie L. Cundiff',
      'grades': '6-8',
      'division': 'Amherst County Public Schools'},
     {'name': 'Andrew G. Wright Middle',
      'address': '100 Wood Dr, Stafford, VA 22556',
      'phone': '540-658-6240',
      'principal': 'Mr. William R. Boatwright',
      'grades': '6-8',
      'division': 'Stafford County Public Schools'},
     {'name': 'Andrew Lewis Middle',
      'address': '616 South College Ave, Salem, VA 24153-5090',
      'phone': '540-387-2513',
      'principal': 'Dr. Forest Jones',
      'grades': '6-8',
      'division': 'Salem Public Schools'},
     {'name': 'Annandale High',
      'address': '4700 Medford Dr, Annandale, VA 22003',
      'phone': '703-642-4100',
      'principal': 'Mr. Vincent Randazzo',
      'grades': '9-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Annandale Terrace Elementary',
      'address': '7604 Herald St, Annandale, VA 22003',
      'phone': '703-658-5600',
      'principal': 'Ms. Andrea Garris',
      'grades': 'PK-5',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Anne E. Moncure Elementary',
      'address': '75 Moncure Lane, Stafford, VA 22556',
      'phone': '540-658-6300',
      'principal': 'Mr. Gregory R. Machi',
      'grades': 'PK-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Anthony Burns Elementary',
      'address': '60 Gallery Road, Stafford, VA 22554',
      'phone': '540-658-6000',
      'principal': 'Ms. Nancy Coll',
      'grades': 'KG-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Anthony P. Mehfoud Elementary',
      'address': '8320 Buffin Rd, Richmond, VA 23231',
      'phone': '804-795-7020',
      'principal': 'Ms. Stacie S. Carlisle',
      'grades': 'PK-2',
      'division': 'Henrico County Public Schools'},
     {'name': 'Antietam Elementary',
      'address': '12000 Antietam Rd, Woodbridge, VA 22192',
      'phone': '703-497-7619',
      'principal': 'Ms. Latiesa Green',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Appalachia Elementary',
      'address': '3965 Kent Junction Road, Appalachia, VA 24216',
      'phone': '276-565-1115',
      'principal': 'Matthew Dysart',
      'grades': 'PK-8',
      'division': 'Wise County Public Schools'},
     {'name': 'Apple Pie Ridge Elementary',
      'address': '349 Apple Pie Ridge Rd, Winchester, VA 22603',
      'phone': '540-662-4781',
      'principal': 'Mr. Justin Raymond',
      'grades': 'KG-5',
      'division': 'Frederick County Public Schools'},
     {'name': 'Appomattox County High',
      'address': '198 Evergreen Ave., Appomattox, VA 24522',
      'phone': '434-352-7146',
      'principal': 'Mrs. Martha J. Eagle',
      'grades': '9-12',
      'division': 'Appomattox County Public Schools'},
     {'name': 'Appomattox Elementary',
      'address': '198 Evergreen Ave., Appomattox, VA 24522',
      'phone': '434-352-7463',
      'principal': 'Mrs. Karen Cyrus',
      'grades': '3-5',
      'division': 'Appomattox County Public Schools'},
     {'name': 'Appomattox Middle',
      'address': '2020 Church St, Appomattox, VA 24522',
      'phone': '434-352-8257',
      'principal': 'Mr. Todd R Reichert',
      'grades': '6-8',
      'division': 'Appomattox County Public Schools'},
     {'name': 'Appomattox Primary',
      'address': '185 Learning Lane, Appomattox, VA 24522',
      'phone': '434-352-5766',
      'principal': 'Mrs. Heather Mullins',
      'grades': 'PK-2',
      'division': 'Appomattox County Public Schools'},
     {'name': 'Arcadia High',
      'address': '8210 Lankford Highway, Oak Hall, VA 23416',
      'phone': '757-824-5613',
      'principal': 'Rose Taylor',
      'grades': '9-12',
      'division': 'Accomack County Public Schools'},
     {'name': 'Arcadia Middle',
      'address': '29485 Horsey Rd., Oak Hall, VA 23416',
      'phone': '757-824-4862',
      'principal': 'Mr. Brian Tupper',
      'grades': '6-8',
      'division': 'Accomack County Public Schools'},
     {'name': 'Archer Elementary',
      'address': '324 Nutley St NW, Vienna, VA 22180',
      'phone': '703-937-6200',
      'principal': 'Ms. Michelle Makrigiorgos',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Arcola Elementary',
      'address': '41740 Tall Cedars Parkway, Aldie, VA 20105',
      'phone': '703-957-4390',
      'principal': 'Dr. Clark Bowers',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Arlington Mill High',
      'address': '816 S. Walter Reed Dr, Suite 222, Arlington, VA 22203',
      'phone': '703-228-5295',
      'principal': 'Ms. Barbara Thompson',
      'grades': '9-12',
      'division': 'Arlington County Public Schools'},
     {'name': 'Arlington Science Focus School',
      'address': '1501 N. Lincoln Street, Arlington, VA 22201',
      'phone': '703-228-7670',
      'principal': 'Ms. Mary E. Begley',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Arlington Traditional',
      'address': '855 N. Edison St, Arlington, VA 22205',
      'phone': '703-228-6290',
      'principal': 'Ms. Holly Hawthorne',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Armel Elementary',
      'address': '2239 Front Royal Pike, Winchester, VA 22602',
      'phone': '540-869-1657',
      'principal': 'Raegan Rangel',
      'grades': 'KG-5',
      'division': 'Frederick County Public Schools'},
     {'name': 'Armstrong Elementary',
      'address': '11900 Lake Newport Rd, Reston, VA 20194-1500',
      'phone': '703-375-4800',
      'principal': 'Mr. James Quinn',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Armstrong Elementary',
      'address': '3401 Matoaka Rd, Hampton, VA 23661',
      'phone': '757-727-1067',
      'principal': 'Ms. Levia M. Stovall',
      'grades': 'KG-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Armstrong High',
      'address': '2300 Cool Lane, Richmond, VA 23223-4196',
      'phone': '804-780-4449',
      'principal': 'Mrs. April Hawkins',
      'grades': '9-12',
      'division': 'Richmond Public Schools'},
     {'name': 'Arrowhead Elementary',
      'address': '5549 Susquehanna Dr, Virginia Beach, VA 23462-4034',
      'phone': '757-648-2040',
      'principal': 'Constance James',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Arthur Ashe Jr. Elementary',
      'address': '1001 Cedar Fork Road, Richmond, VA 23223',
      'phone': '804-343-6550',
      'principal': 'Ms. Kecia O. Lipscomb',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Arthur R. Ware Elementary',
      'address': '330 Grubert Avenue, Staunton, VA 24401',
      'phone': '540-332-3938',
      'principal': 'Mrs. Sharon Barker',
      'grades': 'KG-5',
      'division': 'Staunton Public Schools'},
     {'name': 'Ashburn Elementary',
      'address': '44062 Fincastle Dr, Ashburn, VA 20147',
      'phone': '571-252-2350',
      'principal': 'Michelle Walthour',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Ashby Lee Elementary',
      'address': '480 Stonewall Lane, Quicksburg, VA 22847-1422',
      'phone': '540-477-2927',
      'principal': 'Steve Povlish',
      'grades': 'PK-5',
      'division': 'Shenandoah County Public Schools'},
     {'name': 'Ashland Elementary',
      'address': '15300 Bowmans Folly Dr., Manassas, VA 20112',
      'phone': '703-583-8774',
      'principal': 'Mr. Andrew Jacks',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Ashlawn Elementary',
      'address': '5950 N. 8th Road, Arlington, VA 22205',
      'phone': '703-228-5270',
      'principal': 'Ms. Judy Apostolico-Buck',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Atkins Elementary',
      'address': '5903 Lee Hwy, Atkins, VA 24311',
      'phone': '276-783-3366',
      'principal': 'Mr. Gary L. Roberts',
      'grades': 'PK-5',
      'division': 'Smyth County Public Schools'},
     {'name': 'Atlee High',
      'address': '9414 Atlee Station Road, Mechanicsville, VA 23116',
      'phone': '804-723-2100',
      'principal': 'Ms. Jennifer Cohodas',
      'grades': '9-12',
      'division': 'Hanover County Public Schools'},
     {'name': 'Auburn Elementary',
      'address': '1760 AUBURN SCHOOL DR., Riner, VA 24149',
      'phone': '540-381-6521',
      'principal': 'Ms. Marcia Settle',
      'grades': 'PK-5',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Auburn High',
      'address': '1650 AUBURN SCHOOL DR, Riner, VA 24149',
      'phone': '540-382-5160',
      'principal': 'Mr. Carl R. Pauli',
      'grades': '9-12',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Auburn Middle',
      'address': '7270 Riley Rd., Warrenton, VA 20187',
      'phone': '540-428-3750',
      'principal': 'Mr. Steve Kadilak',
      'grades': '6-8',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Auburn Middle',
      'address': '4069 Riner Rd, Riner, VA 24149',
      'phone': '540-382-5165',
      'principal': 'Mrs. Guylene Wood-Setzer',
      'grades': '6-8',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Axton Elementary',
      'address': '1500 Axton School Road, Axton, VA 24054',
      'phone': '276-650-1193',
      'principal': 'Mrs. Jo Ellen Hylton',
      'grades': 'PK-5',
      'division': 'Henry County Public Schools'},
     {'name': 'Azalea Gardens Middle',
      'address': '7721 Azalea Garden Rd, Norfolk, VA 23518',
      'phone': '757-531-3000',
      'principal': 'Dr. Reuthenia Clark',
      'grades': '6-8',
      'division': 'Norfolk Public Schools'},
     {'name': 'B.C. Charles Elementary',
      'address': '701 Menchville Road, Newport News, VA 23602',
      'phone': '757-886-7750',
      'principal': 'Mr. Clyde (Reggie) Alston',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'B.M. Williams Primary',
      'address': '1100 Battlefield Blvd N, Chesapeake, VA 23320',
      'phone': '757-547-0238',
      'principal': 'Mr. Thomas P. Moyer',
      'grades': 'PK-2',
      'division': 'Chesapeake Public Schools'},
     {'name': 'B.T. Washington Middle',
      'address': '3700 Chestnut Ave, Newport News, VA 23607',
      'phone': '757-928-6860',
      'principal': 'Ms. Deborah L. Fields',
      'grades': '6-8',
      'division': 'Newport News Public Schools'},
     {'name': 'Back Creek Elementary',
      'address': '7130 Bent Mountain Rd, Roanoke, VA 24018',
      'phone': '540-772-7565',
      'principal': 'Ms. Virginia Sharp',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Bacon District Elementary',
      'address': '840 Bacon School Rd, Saxe, VA 23967',
      'phone': '434-735-8612',
      'principal': 'Mrs. Sylvia R. Lockett',
      'grades': 'KG-5',
      'division': 'Charlotte County Public Schools'},
     {'name': 'Badger Vocational Education Center - North',
      'address': '8210 Lankford Highway, Oak Hall, VA 23416',
      'phone': '757-824-6386',
      'principal': ' ',
      'grades': '',
      'division': 'Accomack County Public Schools'},
     {'name': 'Badger Vocational Education Center - South',
      'address': '26350 Lankford Highway, Onley, VA 23418',
      'phone': '757-787-4522',
      'principal': ' ',
      'grades': '',
      'division': 'Accomack County Public Schools'},
     {'name': 'Bailey Bridge Middle',
      'address': '12501 Bailey Bridge Rd, Midlothian, VA 23112-1803',
      'phone': '804-739-6200',
      'principal': 'Kume Goranson',
      'grades': '6-8',
      'division': 'Chesterfield County Public Schools'},
     {'name': "Bailey's Elementary School for the Arts and Sciences",
      'address': '6111 Knollwood Dr, Falls Church, VA 22041',
      'phone': '703-575-6800',
      'principal': 'Ms. Marie M. Lemmon',
      'grades': 'PK-5',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Baker-Butler Elementary',
      'address': '2740 Proffit Road, Charlottesville, VA 22911',
      'phone': '434-974-7777',
      'principal': 'Mr. David Cushman',
      'grades': 'PK-5',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Baldwin Elementary',
      'address': '9705 Main St, Manassas, VA 20110-5799',
      'phone': '571-377-6100',
      'principal': 'Dr. Ashley Cramp',
      'grades': 'KG-4',
      'division': 'Manassas Public Schools'},
     {'name': "Ball's Bluff Elementary",
      'address': '821 Battlefield Pkwy NE, Leesburg, VA 20176',
      'phone': '571-252-2880',
      'principal': 'Dr. Melinda D. Carper',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Banneker Elementary',
      'address': '35231 Snake Hill Rd, Middleburg, VA 20117',
      'phone': '540-751-2480',
      'principal': 'Deborah Lee',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Barcroft Elementary',
      'address': '625 S Wakefield St, Arlington, VA 22204',
      'phone': '703-228-5838',
      'principal': 'Ms. Colette Bounet',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Barrett Elementary',
      'address': '4401 N Henderson Rd, Arlington, VA 22203',
      'phone': '703-228-6288',
      'principal': 'Mr. Dan Redding',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Barron Elementary',
      'address': '45 Fox Hill Rd, Hampton, VA 23669',
      'phone': '757-850-5100',
      'principal': 'Ms. Andrea L. Riddick',
      'grades': 'PK-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Bassett High',
      'address': '85 Riverside Dr, Bassett, VA 24055-9307',
      'phone': '276-629-1731',
      'principal': 'Mr. John M. Gibbs',
      'grades': '9-12',
      'division': 'Henry County Public Schools'},
     {'name': 'Bass-Hoover Elementary',
      'address': '471 Aylor Road, Stephens City, VA 22655',
      'phone': '540-869-4700',
      'principal': 'Mr. Joseph C. Strong',
      'grades': 'KG-5',
      'division': 'Frederick County Public Schools'},
     {'name': 'Bath County High',
      'address': '464 Charger Lane, Hot Springs, VA 24445',
      'phone': '540-839-2431',
      'principal': 'Mrs. Sarah Rowe',
      'grades': '8-12',
      'division': 'Bath County Public Schools'},
     {'name': 'Battlefield Elementary',
      'address': '11108 Leavells Rd, Fredericksburg, VA 22407',
      'phone': '540-786-4532',
      'principal': 'Mrs. Susan C. Fines',
      'grades': 'PK-5',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Battlefield High',
      'address': '15000 Graduation Dr., Haymarket, VA 20169',
      'phone': '571-261-4400',
      'principal': 'Amy S. Ethridge-Conti',
      'grades': '9-12',
      'division': 'Prince William County Public Schools'},
     {'name': 'Battlefield Middle',
      'address': '11120 Leavells Rd, Fredericksburg, VA 22407',
      'phone': '540-786-4400',
      'principal': 'Mrs. Sheila B. Smith',
      'grades': '6-8',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Battlefield Park Elementary',
      'address': '5501 Mechanicsville Turnpike, Mechanicsville, VA 23111',
      'phone': '804-723-3600',
      'principal': 'Ms. Judy L. Bradley',
      'grades': 'PK-5',
      'division': 'Hanover County Public Schools'},
     {'name': 'Bay View Elementary',
      'address': '1434 Bay View Blvd, Norfolk, VA 23503',
      'phone': '757-531-3030',
      'principal': 'Dr. Deborah Mansfield',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'Bayside Elementary',
      'address': '5649 Bayside Rd, Virginia Beach, VA 23455-3410',
      'phone': '757-648-2080',
      'principal': 'Catherine Brumm',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Bayside High',
      'address': '4960 Haygood Rd, Virginia Beach, VA 23455-5299',
      'phone': '757-648-5200',
      'principal': 'James D Miller',
      'grades': '9-12',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Bayside Middle',
      'address': '965 Newtown Rd, Virginia Beach, VA 23462',
      'phone': '757-648-4400',
      'principal': 'Ms. Paula Johnson',
      'grades': '6-8',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Baywood Elementary',
      'address': '247 Grammar Lane, Galax, VA 24333',
      'phone': '276-236-4868',
      'principal': 'Mr. Clark Nuckolls',
      'grades': 'PK-5',
      'division': 'Grayson County Public Schools'},
     {'name': 'Beaverdam Elementary',
      'address': '15485 Beaverdam School Road, Beaverdam, VA 23015',
      'phone': '804-449-6373',
      'principal': 'Mr. Charles E. Joseph',
      'grades': 'PK-5',
      'division': 'Hanover County Public Schools'},
     {'name': 'Bedford County Alternative Education Center',
      'address': '600 Edmund Street, Bedford, VA 24523',
      'phone': '540-586-1270',
      'principal': 'Mr. Gus Exstrom',
      'grades': '',
      'division': 'Bedford County Public Schools'},
     {'name': 'Bedford Elementary',
      'address': '806 Burks Hill Rd, Bedford, VA 24523',
      'phone': '540-586-0275',
      'principal': 'Mrs. Elizabeth A. Winter',
      'grades': '2-5',
      'division': 'Bedford County Public Schools'},
     {'name': 'Bedford Hills Elementary',
      'address': '4330 Morningside Dr, Lynchburg, VA 24503-4325',
      'phone': '434-384-2221',
      'principal': 'Faye E. James',
      'grades': 'PK-5',
      'division': 'Lynchburg Public Schools'},
     {'name': 'Bedford Middle',
      'address': '503 Longwood Ave, Bedford, VA 24523',
      'phone': '540-586-7735',
      'principal': 'Mrs. Rhetta J. Watkins',
      'grades': '6-8',
      'division': 'Bedford County Public Schools'},
     {'name': 'Bedford Primary',
      'address': '807 College St, Bedford, VA 24523',
      'phone': '540-586-8339',
      'principal': 'Ms. Lisa Dellis',
      'grades': 'PK-1',
      'division': 'Bedford County Public Schools'},
     {'name': 'Beech Tree Elementary',
      'address': '3401 Beechtree Ln, Falls Church, VA 22042',
      'phone': '703-531-2600',
      'principal': 'Karim Daugherty',
      'grades': 'PK-5',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Bel Air Elementary',
      'address': '14151 Ferndale Road, Woodbridge, VA 22193',
      'phone': '703-670-4050',
      'principal': 'Clint Mitchell',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Belfast Elk Garden Elementary',
      'address': '646 Belfast School Rd., Rosedale, VA 24280',
      'phone': '276-880-2283',
      'principal': 'Ms. Georgia McCoy',
      'grades': 'KG-5',
      'division': 'Russell County Public Schools'},
     {'name': 'Belfield Elementary',
      'address': '515 Belfield Rd, Emporia, VA 23847-8065',
      'phone': '434-634-5566',
      'principal': 'Ms. Mary Person',
      'grades': '5',
      'division': 'Greensville County Public Schools'},
     {'name': 'Belle Heth Elementary',
      'address': '151 George Street, Radford, VA 24141',
      'phone': '540-731-3653',
      'principal': 'Mr. Jack McKinley',
      'grades': '3-6',
      'division': 'Radford Public Schools'},
     {'name': 'Belle View Elementary',
      'address': '6701 Fort Hunt Rd, Alexandria, VA 22307',
      'phone': '703-660-8300',
      'principal': 'Mr. Thomas P. Kuntz',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Bellevue Elementary',
      'address': '2301 E Grace St, Richmond, VA 23223-7151',
      'phone': '804-780-4417',
      'principal': 'Mrs. Regina T. Farr',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'Bellwood Elementary',
      'address': '9536 Dawnshire Rd, Richmond, VA 23237-3455',
      'phone': '804-743-3600',
      'principal': 'Jennifer Rudd',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Belmont Elementary',
      'address': '751 Norwood Ln, Woodbridge, VA 22191',
      'phone': '703-494-4945',
      'principal': 'Ms. Roxana Hudson',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Belmont Ridge Middle',
      'address': '19045 Upper Belmont Place, Leesburg, VA 20176',
      'phone': '571-252-2220',
      'principal': 'Ryan Hitchman',
      'grades': '6-8',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Belmont Station Elementary',
      'address': '20235 Nightwatch St., Ashburn, VA 20147',
      'phone': '571-252-2240',
      'principal': 'Lori Mercer',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Belvedere Elementary',
      'address': '6540 Columbia Pike, Falls Church, VA 22041',
      'phone': '703-916-6800',
      'principal': 'Ms. Cecilia Vanderhye',
      'grades': 'PK-5',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Belview Elementary',
      'address': '3187 Peppers Ferry Rd, Radford, VA 24141',
      'phone': '540-633-3200',
      'principal': 'Ms. Tara Grant',
      'grades': 'PK-5',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Benjamin F. Yancey Elementary',
      'address': '7625 Porters Road, Esmont, VA 22937-9732',
      'phone': '434-974-8060',
      'principal': 'Craig Dommer',
      'grades': 'PK-5',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Benjamin Franklin Middle-East',
      'address': '375 Middle School Rd, Rocky Mount, VA 24151',
      'phone': '540-483-5105',
      'principal': 'Brenda Muse',
      'grades': '6',
      'division': 'Franklin County Public Schools'},
     {'name': 'Benjamin Franklin Middle-West',
      'address': '225 Middle School Road, Rocky Mount, VA 24151',
      'phone': '540-483-5105',
      'principal': 'Brenda Muse',
      'grades': '7-8',
      'division': 'Franklin County Public Schools'},
     {'name': 'Benjamin Syms Middle',
      'address': '170 Fox Hill Rd, Hampton, VA 23669',
      'phone': '757-850-5050',
      'principal': 'Ms. Sharon S. Slater',
      'grades': '6-8',
      'division': 'Hampton Public Schools'},
     {'name': 'Bennett Elementary',
      'address': '8800 Old Dominion Dr, Manassas, VA 20110',
      'phone': '703-361-8261',
      'principal': 'Mr. Matthew Ritter',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Bensley Elementary',
      'address': '6600 Strathmore Rd, Richmond, VA 23237-1129',
      'phone': '804-743-3610',
      'principal': 'Mrs. Bessie Cooper',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Berkeley Elementary',
      'address': '5979 Partlow Road, Spotsylvania, VA 22553',
      'phone': '540-582-5141',
      'principal': 'Mr. K. Michael Brown',
      'grades': 'PK-5',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Berkeley Glenn Elementary',
      'address': '1020 Jefferson Ave, Waynesboro, VA 22980',
      'phone': '540-946-4680',
      'principal': 'Ms. Sharon B. Tooley',
      'grades': 'KG-5',
      'division': 'Waynesboro Public Schools'},
     {'name': 'Berkeley Middle',
      'address': '1118 Ironbound Rd, Williamsburg, VA 23185',
      'phone': '757-229-8051',
      'principal': 'Karen Swann',
      'grades': '6-8',
      'division': 'Williamsburg-James City County Public Schools'},
     {'name': 'Berkley/Campostella Early Childhood Education Center',
      'address': '1530 Cypress St, Norfolk, VA 23523-1902',
      'phone': '757-494-3870',
      'principal': 'Dr. Doreatha White',
      'grades': 'PK',
      'division': 'Norfolk Public Schools'},
     {'name': 'Bessie Weller Elementary',
      'address': '600 Greenville Ave, Staunton, VA 24401-4873',
      'phone': '540-332-3940',
      'principal': 'Mrs. Linda Mahler',
      'grades': 'KG-5',
      'division': 'Staunton Public Schools'},
     {'name': 'Bethel Elementary',
      'address': '2991 Hickory Fork Rd, Gloucester, VA 23061',
      'phone': '804-693-2360',
      'principal': 'Ms. Eileen Kersmarki',
      'grades': 'PK-5',
      'division': 'Gloucester County Public Schools'},
     {'name': 'Bethel High',
      'address': '1067 Big Bethel Rd, Hampton, VA 23666',
      'phone': '757-825-4400',
      'principal': 'Mr. Ralph J. Saunders',
      'grades': '9-12',
      'division': 'Hampton Public Schools'},
     {'name': 'Bethel Manor Elementary',
      'address': '1797 First St, Langley A F B, VA 23665',
      'phone': '757-867-7439',
      'principal': 'Dr. Elizabeth B. Poulsen',
      'grades': 'KG-5',
      'division': 'York County Public Schools'},
     {'name': 'Bettie Weaver Elementary',
      'address': '3600 James River Rd, Midlothian, VA 23113-3718',
      'phone': '804-378-2540',
      'principal': 'Dr. Holly Richard',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Beulah Elementary',
      'address': '4216 Beulah Rd, Richmond, VA 23237-1450',
      'phone': '804-743-3620',
      'principal': 'Ms. Mary Jean Hunt',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Beverley Manor Elementary',
      'address': '116 Cedar Green Rd, Staunton, VA 24401',
      'phone': '540-885-8024',
      'principal': 'Mrs. Dawn P. Young',
      'grades': 'PK-5',
      'division': 'Augusta County Public Schools'},
     {'name': 'Beverley Manor Middle',
      'address': '58 Cedar Green Rd, Staunton, VA 24401',
      'phone': '540-886-5806',
      'principal': 'Mrs. Forrest O. Burgdorf',
      'grades': '6-8',
      'division': 'Augusta County Public Schools'},
     {'name': 'Big Island Elementary',
      'address': '1114 Schooldays Rd, Big Island, VA 24526',
      'phone': '434-299-5863',
      'principal': 'Mr. Wayne Lyle Jr.',
      'grades': 'PK-6',
      'division': 'Bedford County Public Schools'},
     {'name': 'Binford Middle',
      'address': '1701 Floyd Ave, Richmond, VA 23220-4623',
      'phone': '804-780-6231',
      'principal': ' ',
      'grades': '6-8',
      'division': 'Richmond Public Schools'},
     {'name': 'Birdneck Elementary',
      'address': '957 S Birdneck Rd, Virginia Beach, VA 23451-5801',
      'phone': '757-648-2120',
      'principal': 'Mr. Irv Beard',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Blacksburg High',
      'address': '3401 Bruin Lane, Blacksburg, VA 24060',
      'phone': '540-951-5706',
      'principal': 'Mr. Brian Kitts',
      'grades': '9-12',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Blacksburg Middle',
      'address': "3109 Price's Fork Rd., Blacksburg, VA 24060",
      'phone': '540-951-5800',
      'principal': 'Mr. John Wheeler',
      'grades': '6-8',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Blackstone Primary',
      'address': '615 East Street, Blackstone, VA 23824',
      'phone': '434-292-5300',
      'principal': 'Mrs. Ruth Ann Horn',
      'grades': 'PK-4',
      'division': 'Nottoway County Public Schools'},
     {'name': 'Blackwell Elementary',
      'address': '1600 Everett St, Richmond, VA 23224-3896',
      'phone': '804-780-5078',
      'principal': 'Mr. Reginald Williams',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'Blair Middle',
      'address': '730 Spotswood Ave, Norfolk, VA 23517',
      'phone': '757-628-2400',
      'principal': 'Dr. Jannette Martin',
      'grades': '6-8',
      'division': 'Norfolk Public Schools'},
     {'name': 'Bland Elementary',
      'address': '31 Rocket Drive, Bland, VA 24315',
      'phone': '276-688-3621',
      'principal': 'Mrs. Diana Tibbs',
      'grades': 'KG-7',
      'division': 'Bland County Public Schools'},
     {'name': 'Bland High',
      'address': '31 Rocket Drive, Bland, VA 24315-0014',
      'phone': '276-688-3621',
      'principal': 'Mr. Temple Musser',
      'grades': '8-12',
      'division': 'Bland County Public Schools'},
     {'name': 'Blandford Academy',
      'address': '816 E Bank St, Petersburg, VA 23803',
      'phone': '804-862-7078',
      'principal': 'Mr. Giron Wooden',
      'grades': '',
      'division': 'Petersburg Public Schools'},
     {'name': 'Blue Ridge Elementary',
      'address': '5135 Ararat Hwy, Ararat, VA 24053',
      'phone': '276-251-5271',
      'principal': 'Mrs. Sandra Clement',
      'grades': 'KG-7',
      'division': 'Patrick County Public Schools'},
     {'name': 'Blue Ridge Middle',
      'address': '551 East A St, Purcellville, VA 20132',
      'phone': '540-751-2520',
      'principal': 'Brion Bell',
      'grades': '6-8',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Bluestone High',
      'address': '6825 Skipwith Road, Skipwith, VA 23968',
      'phone': '434-372-5177',
      'principal': 'Christopher Coleman',
      'grades': '9-12',
      'division': 'Mecklenburg County Public Schools'},
     {'name': 'Bluestone Middle',
      'address': '250 Middle School Road, Skipwith, VA 23968',
      'phone': '434-372-3266',
      'principal': 'Mary Shores',
      'grades': '6-8',
      'division': 'Mecklenburg County Public Schools'},
     {'name': 'Body Camp Elementary',
      'address': '3420 Body Camp Rd, Bedford, VA 24523',
      'phone': '540-297-7391',
      'principal': 'Mr. Scott Graham',
      'grades': 'PK-5',
      'division': 'Bedford County Public Schools'},
     {'name': 'Bon Air Elementary',
      'address': '8701 Polk St, Bon Air, VA 23235-3403',
      'phone': '804-560-2700',
      'principal': 'Mr. Bruce C. Tetlow',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Bonnie Brae Elementary',
      'address': '5420 Sideburn Rd, Fairfax, VA 22032',
      'phone': '703-321-3900',
      'principal': 'Ms. Kathy Bruce',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Bonsack Elementary',
      'address': '5437 Crumpacker Dr, Roanoke, VA 24019',
      'phone': '540-977-5870',
      'principal': 'Ms. Melissa Jones',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Booker Elementary',
      'address': '160 Apollo Dr, Hampton, VA 23669',
      'phone': '757-850-5096',
      'principal': 'Ms. Milicent Y. Rogers',
      'grades': 'KG-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Booker T. Washington Elementary',
      'address': '204 Walnut Street, Suffolk, VA 23434',
      'phone': '757-934-6226',
      'principal': 'Dr. David Reitz',
      'grades': 'PK-5',
      'division': 'Suffolk Public Schools'},
     {'name': 'BOOKER T. WASHINGTON HIGH SCHOOL',
      'address': '1111 Park Ave, Norfolk, VA 23504',
      'phone': '757-628-3575',
      'principal': 'Mrs. Adrian Day',
      'grades': '9-12',
      'division': 'Norfolk Public Schools'},
     {'name': 'Boones Mill Elementary',
      'address': '265 Taylors Rd, Boones Mill, VA 24065',
      'phone': '540-334-4000',
      'principal': 'Ms. Tomeka Campbell',
      'grades': 'PK-5',
      'division': 'Franklin County Public Schools'},
     {'name': 'Boonsboro Elementary',
      'address': '1234 Eagle Circle, Lynchburg, VA 24503',
      'phone': '434-384-2881',
      'principal': 'Elizabeth Williams',
      'grades': 'KG-5',
      'division': 'Bedford County Public Schools'},
     {'name': 'Botetourt Elementary',
      'address': '6361 Main Street, Gloucester, VA 23061-9712',
      'phone': '804-693-2151',
      'principal': 'Dr. Bambi L. Thompson',
      'grades': 'PK-5',
      'division': 'Gloucester County Public Schools'},
     {'name': 'Botetourt Technical Education Center',
      'address': '253 Poor Farm Rd, Fincastle, VA 24090',
      'phone': '540-473-8216',
      'principal': 'Mr. Joe Harden',
      'grades': '',
      'division': 'Botetourt County Public Schools'},
     {'name': 'Bowling Green Elementary',
      'address': '17502 New Baltimore Road, Milford, VA 22514',
      'phone': '804-633-6401',
      'principal': 'Mr. Jason Mack',
      'grades': 'PK-5',
      'division': 'Caroline County Public Schools'},
     {'name': 'Boyce Elementary',
      'address': '119 W Main St, Boyce, VA 22620',
      'phone': '540-955-6115',
      'principal': 'Mrs. Susan Catlett',
      'grades': 'KG-5',
      'division': 'Clarke County Public Schools'},
     {'name': 'Braddock Elementary',
      'address': '7825 Heritage Dr, Annandale, VA 22003',
      'phone': '703-914-7300',
      'principal': 'Ms. Cindy Botzin',
      'grades': 'PK-5',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Brandon Middle',
      'address': '1700 Pope St, Virginia Beach, VA 23464',
      'phone': '757-648-4450',
      'principal': 'Christy McQueeney',
      'grades': '6-8',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Breckinridge Elementary',
      'address': '331 Springwood Rd, Fincastle, VA 24090',
      'phone': '540-473-8386',
      'principal': 'Ms. Debra D. Deitrich',
      'grades': 'PK-5',
      'division': 'Botetourt County Public Schools'},
     {'name': 'Breckinridge Middle',
      'address': '3901 Williamson Rd NW, Roanoke, VA 24012',
      'phone': '540-853-2251',
      'principal': 'Ms. Tracey Anderson',
      'grades': '6-8',
      'division': 'Roanoke Public Schools'},
     {'name': 'Bren Mar Park Elementary',
      'address': '6344 Beryl Rd, Alexandria, VA 22312',
      'phone': '703-914-7200',
      'principal': 'Ms. Anita Lynch',
      'grades': 'PK-5',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Brentsville District High',
      'address': '12109 Aden Rd, Nokesville, VA 20181',
      'phone': '703-594-2161',
      'principal': 'Ms. Katherine Meints',
      'grades': '9-12',
      'division': 'Prince William County Public Schools'},
     {'name': 'Briar Woods High',
      'address': '22525 Belmont Ridge Road, Ashburn, VA 20148',
      'phone': '703-957-4400',
      'principal': 'Mr. Edward A. Starzenski',
      'grades': '9-12',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Brighton Elementary',
      'address': '1100 Portsmouth Blvd., Portsmouth, VA 23704-5630',
      'phone': '757-393-8870',
      'principal': 'Mrs. Barbara J Shears-Walker',
      'grades': 'KG-6',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Bristow Run Elementary',
      'address': '8990 Worthington Dr, Bristow, VA 20136',
      'phone': '703-753-7741',
      'principal': 'Jessica Parker',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Broad Rock Elementary',
      'address': '4615 Ferguson Ln, Richmond, VA 23234-1999',
      'phone': '804-780-5048',
      'principal': 'Mrs. Carmen E. Rush',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'Broad Run High',
      'address': '21670 Ashburn Rd, Ashburn, VA 20147',
      'phone': '571-252-2300',
      'principal': 'Doug Anderson',
      'grades': '9-12',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Broadus Wood Elementary',
      'address': '185 Buck Mountain Road, Earlysville, VA 22936-2009',
      'phone': '434-973-3865',
      'principal': 'Kendra King',
      'grades': 'PK-5',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Broadway High',
      'address': '269 Gobbler Dr, Broadway, VA 22815',
      'phone': '540-896-7081',
      'principal': 'Mr. Bryan Huber',
      'grades': '9-12',
      'division': 'Rockingham County Public Schools'},
     {'name': 'Brock Road Elementary',
      'address': '10207 Brock Rd, Spotsylvania, VA 22553',
      'phone': '540-972-3870',
      'principal': 'Barbara Dickinson',
      'grades': 'PK-5',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Brooke Point High',
      'address': '1700 Courthouse Rd, Stafford, VA 22554',
      'phone': '540-658-6080',
      'principal': 'Mr. Scott W. McClellan',
      'grades': '9-12',
      'division': 'Stafford County Public Schools'},
     {'name': 'Brookfield Elementary',
      'address': '4200 Lees Corner Rd, Chantilly, VA 20151-2826',
      'phone': '703-814-8700',
      'principal': 'Mrs. Mary L Miller',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Brookland Middle',
      'address': '9200 Lydell Dr, Richmond, VA 23228',
      'phone': '804-261-5000',
      'principal': 'Mr. Derrick D. Deloatch',
      'grades': '6-8',
      'division': 'Henrico County Public Schools'},
     {'name': 'Brookneal Elementary',
      'address': '133 Charlotte St., Brookneal, VA 24528',
      'phone': '434-376-2042',
      'principal': 'Wendy Thomas',
      'grades': 'PK-5',
      'division': 'Campbell County Public Schools'},
     {'name': 'Brookville High',
      'address': '100 Laxton Rd, Lynchburg, VA 24502',
      'phone': '434-239-2636',
      'principal': 'Mr. Tom Cole',
      'grades': '9-12',
      'division': 'Campbell County Public Schools'},
     {'name': 'Brookville Middle',
      'address': '320 Bee Dr, Lynchburg, VA 24502',
      'phone': '434-239-9267',
      'principal': 'Mr. Edwin R. Martin',
      'grades': '6-8',
      'division': 'Campbell County Public Schools'},
     {'name': 'Brookwood Elementary',
      'address': '601 S Lynnhaven Rd, Virginia Beach, VA 23452-6598',
      'phone': '757-648-2160',
      'principal': 'Mike Taylor',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Brosville Elementary',
      'address': '195 Bulldog Ln., Danville, VA 24541',
      'phone': '434-685-7787',
      'principal': 'Mrs. Felita F. Atkins',
      'grades': 'PK-5',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Brownsville Elementary',
      'address': '5870 Rockfish Gap Turnpike, Crozet, VA 22932-3401',
      'phone': '434-823-4658',
      'principal': 'India Haun',
      'grades': 'PK-5',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Brunswick High',
      'address': '2171 Lawrenceville Plank Rd, Lawrenceville, VA 23868',
      'phone': '434-848-2716',
      'principal': 'Dr. Virginia Glass Berry',
      'grades': '9-12',
      'division': 'Brunswick County Public Schools'},
     {'name': 'Bruton High',
      'address': '185 East Rochambeau Dr, Williamsburg, VA 23188',
      'phone': '757-220-4050',
      'principal': 'Alexis Swanson',
      'grades': '9-12',
      'division': 'York County Public Schools'},
     {'name': 'Bryant Alternative High',
      'address': '2709 Popkins Ln, Alexandria, VA 22306',
      'phone': '703-660-2001',
      'principal': 'Mr. Larry Jones',
      'grades': '7-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Buchanan County Technical & Career Center',
      'address': '1124 Almarine Drive, Slate Creek Rd, State Rt. 83, Grundy, VA 24614',
      'phone': '276-935-4541',
      'principal': 'Mrs. Sandra S. Cook',
      'grades': '',
      'division': 'Buchanan County Public Schools'},
     {'name': 'Buchanan Elementary',
      'address': '255 Schoolhouse Rd, Buchanan, VA 24066',
      'phone': '540-254-2084',
      'principal': 'Ms. Debbie H. Garrett',
      'grades': 'PK-5',
      'division': 'Botetourt County Public Schools'},
     {'name': 'Buckingham Co Elementary',
      'address': '40 Frank Harris Raod, Dillwyn, VA 23936',
      'phone': '434-505-0000',
      'principal': "Mrs. Cindy O'Brien",
      'grades': '3-5',
      'division': 'Buckingham County Public Schools'},
     {'name': 'Buckingham Co prekindergarten center</strong>, ',
      'address': '434-969-4490',
      'phone': ' ',
      'principal': 'PK',
      'grades': 'Buckingham County Public Schools',
      'division': ''},
     {'name': 'Buckingham Co Primary',
      'address': '128 Frank Harris Road, Dillwyn, VA 23936',
      'phone': '434-505-0001',
      'principal': 'Mrs. Pennie Allen',
      'grades': 'KG-2',
      'division': 'Buckingham County Public Schools'},
     {'name': 'Buckingham County High',
      'address': '78 Knights Rd., Buckingham, VA 23921',
      'phone': '434-969-6160',
      'principal': 'Mr. Roger Coleman III',
      'grades': '9-12',
      'division': 'Buckingham County Public Schools'},
     {'name': 'Buckingham County Middle',
      'address': '1184 High School Rd., Buckingham, VA 23921',
      'phone': '434-969-1044',
      'principal': 'Mr. J.B. Heslip',
      'grades': '6-8',
      'division': 'Buckingham County Public Schools'},
     {'name': 'Buckland Mills Elementary',
      'address': '10511 Wharfdale Place, Gainesville, VA 20155',
      'phone': '703-530-1560',
      'principal': 'Ms. Connie S. Balkcom',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Bucknell Elementary',
      'address': '6925 University Dr, Alexandria, VA 22307',
      'phone': '703-660-2900',
      'principal': 'Mr. Timothy H Slayter',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Buffalo Gap High',
      'address': '1800 Buffalo Gap Hwy, Swoope, VA 24479',
      'phone': '540-337-6021',
      'principal': 'Mr. William R. Deardorff',
      'grades': '9-12',
      'division': 'Augusta County Public Schools'},
     {'name': 'Buffalo Trail Elementary',
      'address': '42190 Seven Hills Drive, Aldie, VA 20105',
      'phone': '703-722-2780',
      'principal': 'Alisa Rogaliner',
      'grades': 'KG-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Buford Middle',
      'address': '1000 Cherry Avenue, Charlottesville, VA 22903-3852',
      'phone': '434-245-2411',
      'principal': 'Mr. Eric D. Johnson',
      'grades': '7-8',
      'division': 'Charlottesville Public Schools'},
     {'name': 'Bull Run Elementary',
      'address': '15301 Lee Hwy, Centreville, VA 20121',
      'phone': '703-227-1400',
      'principal': 'Ms. Patrice Brown',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Bull Run Middle',
      'address': '6308 Catharpin Rd., Gainesville, VA 20155',
      'phone': '703-753-9969',
      'principal': 'Mr. Matthew T. Phythian',
      'grades': '6-8',
      'division': 'Prince William County Public Schools'},
     {'name': 'Burke School',
      'address': '9645 Burke Lake Rd, Burke, VA 22015',
      'phone': '703-426-7300',
      'principal': 'Mrs. Jill Jakulski',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Burkeville Elementary',
      'address': '507 Miller St, Burkeville, VA 23922',
      'phone': '434-767-5236',
      'principal': 'Mrs. Carrie Gravely',
      'grades': 'PK-KG',
      'division': 'Nottoway County Public Schools'},
     {'name': 'Burlington Elementary',
      'address': '6533 Peters Creek Rd, Roanoke, VA 24019',
      'phone': '540-561-8165',
      'principal': 'Ms. Amy Shank',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Burnley-Moran Elementary',
      'address': '1300 Long Street, Charlottesville, VA 22901-4936',
      'phone': '434-245-2413',
      'principal': 'Dr. Dawn M. Locasale',
      'grades': 'PK-4',
      'division': 'Charlottesville Public Schools'},
     {'name': 'Burnt Chimney Elementary',
      'address': '80 Burnt Chimney Road, Wirtz, VA 24184',
      'phone': '540-721-2936',
      'principal': 'Mr. Derek Bryant',
      'grades': 'PK-5',
      'division': 'Franklin County Public Schools'},
     {'name': 'Burton Center for Arts and Technology',
      'address': '1760 Boulevard, Salem, VA 24153',
      'phone': '540-857-5000',
      'principal': ' ',
      'grades': '',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Bush Hill Elementary',
      'address': '5927 Westchester St, Alexandria, VA 22310',
      'phone': '703-924-5600',
      'principal': 'Ms. Cecelia K Breazeale',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Butts Road Intermediate',
      'address': '1571 Mt Pleasant Rd, Chesapeake, VA 23322',
      'phone': '757-482-4566',
      'principal': 'Mrs. Mindy Green',
      'grades': '3-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Butts Road Primary',
      'address': '1000 Mt Pleasant Rd, Chesapeake, VA 23322',
      'phone': '757-482-5820',
      'principal': 'Mr. James S. Lewter',
      'grades': 'PK-2',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Byrd Elementary',
      'address': '2704 Hadensville Fife Rd, Goochland, VA 23063',
      'phone': '804-556-5380',
      'principal': 'Mr. James B. Hopkins',
      'grades': 'PK-5',
      'division': 'Goochland County Public Schools'},
     {'name': 'C. Alton Lindsay Middle',
      'address': '1636 Briarfield Rd, Hampton, VA 23661',
      'phone': '757-825-4560',
      'principal': 'Ms. Angela N. Byrd-Wright',
      'grades': '6-8',
      'division': 'Hampton Public Schools'},
     {'name': 'C. Hunter Ritchie Elementary',
      'address': '4416 Broad Run Church Rd, New Baltimore, VA 20187',
      'phone': '540-422-7650',
      'principal': 'Christy Thorpe',
      'grades': 'PK-5',
      'division': 'Fauquier County Public Schools'},
     {'name': 'C.A. Sinclair Elementary',
      'address': '7801 Garner Dr, Manassas, VA 20109',
      'phone': '703-361-4811',
      'principal': 'Donna T. Fagerholm',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'C.C. Wells Elementary',
      'address': '13101 S. Chester Rd., Chester, VA 23831-4553',
      'phone': '804-768-6265',
      'principal': 'Ms. Robin Morgan',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'C.D. Hylton High',
      'address': '14051 Spriggs Rd, Woodbridge, VA 22193',
      'phone': '703-580-4000',
      'principal': 'Mr. David Cassady',
      'grades': '9-12',
      'division': 'Prince William County Public Schools'},
     {'name': 'C.E. Curtis Elementary',
      'address': '3600 W Hundred Rd, Chester, VA 23831-1926',
      'phone': '804-768-6175',
      'principal': 'Susan Pereira',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'C.M. Bradley Elementary',
      'address': '674 Hastings Ln, Warrenton, VA 20186',
      'phone': '540-422-7510',
      'principal': 'Banks Beth',
      'grades': 'PK-5',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Callaghan Elementary',
      'address': '4050 Midland Trail, Covington, VA 24426',
      'phone': '540-965-1810',
      'principal': 'Mrs. Nancy M. Moga',
      'grades': 'KG-5',
      'division': 'Alleghany County Public Schools'},
     {'name': 'Callaway Elementary',
      'address': '8451 Callaway Rd, Callaway, VA 24067',
      'phone': '540-483-0364',
      'principal': 'Mr. Jason Guilliams',
      'grades': 'PK-5',
      'division': 'Franklin County Public Schools'},
     {'name': 'Camelot Elementary',
      'address': '2901 Guenevere Dr, Chesapeake, VA 23323',
      'phone': '757-558-5347',
      'principal': 'Dr. Karen Cooper-Collins',
      'grades': 'PK-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Camelot Elementary',
      'address': '8100 Guinevere Dr, Annandale, VA 22003',
      'phone': '703-645-7000',
      'principal': 'Ms. Aileen K Flaherty',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Cameron Elementary',
      'address': '3434 Campbell Dr, Alexandria, VA 22303',
      'phone': '703-329-2100',
      'principal': 'Jeannie McCurry',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Camp Allen Elementary',
      'address': '501 C St., Norfolk, VA 23505',
      'phone': '757-451-4170',
      'principal': 'Ms. Deena Copeland',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'Campbell County Technical Center',
      'address': '194 Dennis Riddle Rd, Rustburg, VA 24588',
      'phone': '434-821-6213',
      'principal': 'Mr. Jon Hardie',
      'grades': '',
      'division': 'Campbell County Public Schools'},
     {'name': 'Campbell Court Elementary',
      'address': '220 Campbell Ct, Bassett, VA 24055',
      'phone': '276-629-5344',
      'principal': 'Mrs. Pattie B. Walmsley',
      'grades': 'PK-5',
      'division': 'Henry County Public Schools'},
     {'name': 'Campbell Elementary',
      'address': '737 S. Carlin Springs Rd., Arlington, VA 22204',
      'phone': '703-228-6770',
      'principal': 'Ms. Maureen Nesselrode',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Campostella Elementary',
      'address': '2600 E Princess Anne Rd, Norfolk, VA 23504',
      'phone': '757-628-2555',
      'principal': 'Dr. Rhonda Ambrose',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'Canterbury Woods Elementary',
      'address': '4910 Willet Dr, Annandale, VA 22003',
      'phone': '703-764-5600',
      'principal': 'Ms. Barbara Messinger',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Capron Elementary',
      'address': '18414 Southampton Pky, Capron, VA 23829',
      'phone': '434-658-4348',
      'principal': 'Mrs. Allison Francis',
      'grades': 'PK-5',
      'division': 'Southampton County Public Schools'},
     {'name': 'Captain John Smith Elementary',
      'address': '379 Woodland Rd, Hampton, VA 23669',
      'phone': '757-850-5088',
      'principal': 'Ms. Elizabeth W. Franks',
      'grades': 'PK-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Cardinal Forest Elementary',
      'address': '8600 Forrester Blvd, Springfield, VA 22152',
      'phone': '703-923-5200',
      'principal': 'Ms. Karen H. Kenna',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Career & Technical Education Center',
      'address': '255 Stanley St, Abingdon, VA 24210',
      'phone': '276-739-3100',
      'principal': 'Mr. Brian Johnson',
      'grades': '',
      'division': 'Washington County Public Schools'},
     {'name': 'Carl B. Hutcherson Building',
      'address': '2401 High Street, Lynchburg, VA 24501',
      'phone': '434-522-3756',
      'principal': 'Ms. Polly P. Smith',
      'grades': '',
      'division': 'Lynchburg Public Schools'},
     {'name': 'Carlin Springs Elementary',
      'address': '5995 South 5th Road, Arlington, VA 22204',
      'phone': '703-228-6645',
      'principal': 'Ms. Corina Coronel',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Caroline High',
      'address': '19155 Rodgers Clark Blvd, Milford, VA 22514',
      'phone': '804-633-9886',
      'principal': 'Mr. Jeff Wick',
      'grades': '9-12',
      'division': 'Caroline County Public Schools'},
     {'name': 'Caroline Middle',
      'address': '13325 Devils Three Jump Road, Milford, VA 22514',
      'phone': '804-633-6561',
      'principal': 'Angela Wright',
      'grades': '6-8',
      'division': 'Caroline County Public Schools'},
     {'name': 'Carroll County Education Center',
      'address': '205 Oak Street, Hillsville, VA 24343',
      'phone': '276-728-9055',
      'principal': 'Mr. Jesse DA Woods',
      'grades': '',
      'division': 'Carroll County Public Schools'},
     {'name': 'Carroll County High',
      'address': '100 Cavs Lane, Hillsville, VA 24343',
      'phone': '276-728-2125',
      'principal': 'Mr. Charles T. Thompson',
      'grades': '9-12',
      'division': 'Carroll County Public Schools'},
     {'name': 'Carroll County Middle School',
      'address': '1036 N. Main Street, Hillsville, VA 24343',
      'phone': '276-728-4211',
      'principal': 'Mr. Marc G. Quesenberry',
      'grades': '6-8',
      'division': 'Carroll County Public Schools'},
     {'name': 'Carrollton Elementary',
      'address': '14440 New Towne Haven Ln, Carrollton, VA 23314',
      'phone': '757-238-2452',
      'principal': 'Mr. Kevin Goetz',
      'grades': 'PK-3',
      'division': 'Isle of Wight County Public Schools'},
     {'name': 'Carrsville Elementary',
      'address': '5355 Carrsville Hwy, Carrsville, VA 23315',
      'phone': '757-562-4054',
      'principal': 'Ms. Laura Matthews',
      'grades': 'PK-5',
      'division': 'Isle of Wight County Public Schools'},
     {'name': 'Carson Middle',
      'address': '13618 McLearen Rd, Herndon, VA 20171',
      'phone': '703-925-3600',
      'principal': 'Mr. August Frattali',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Carter G. Woodson Middle',
      'address': '1000 Winston Churchill Drive, Hopewell, VA 23860',
      'phone': '804-541-6404',
      'principal': 'Mr. Shannon Royster',
      'grades': '6-8',
      'division': 'Hopewell Public Schools'},
     {'name': 'Carver Elementary',
      'address': '220 Trott Circle, Martinsville, VA 24112',
      'phone': '276-957-2226',
      'principal': 'Mrs. Judy Edmonds',
      'grades': 'PK-5',
      'division': 'Henry County Public Schools'},
     {'name': 'Carver Elementary',
      'address': '6160 Jefferson Ave, Newport News, VA 23605',
      'phone': '757-591-4950',
      'principal': 'Ms. Izzie Brown',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'Carver Middle',
      'address': '3800 Cougar Trail, Chester, VA 23831',
      'phone': '804-524-3620',
      'principal': 'Mr. Donald Ashburn',
      'grades': '6-8',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Carysbrook Elementary',
      'address': '9172 James Madison Highway, Fork Union, VA 23055',
      'phone': '434-842-1241',
      'principal': 'Mr. Donald Stribling',
      'grades': '3-4',
      'division': 'Fluvanna County Public Schools'},
     {'name': 'Cashell Donahoe Elementary',
      'address': '1801 Graves Rd, Sandston, VA 23150',
      'phone': '804-328-4035',
      'principal': 'Mr. Joseph D. Koontz',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Cassell Elementary',
      'address': '1301 Rockfish Rd, Waynesboro, VA 22980',
      'phone': '540-946-7635',
      'principal': 'Dr. Mindy G. Garber',
      'grades': 'PK-5',
      'division': 'Augusta County Public Schools'},
     {'name': 'Castlewood Elementary',
      'address': '242 Blue Devil Circle, Castlewood, VA 24224',
      'phone': '276-762-2315',
      'principal': ' ',
      'grades': '1-7',
      'division': 'Russell County Public Schools'},
     {'name': 'Castlewood High',
      'address': '304 Blue Devil Circle, Castlewood, VA 24224',
      'phone': '276-762-9449',
      'principal': 'Dr. Thomas Graves',
      'grades': '8-12',
      'division': 'Russell County Public Schools'},
     {'name': 'Catoctin Elementary',
      'address': '311 Catoctin Circle SW, Leesburg, VA 20175',
      'phone': '571-252-2940',
      'principal': 'Ms. Jennifer Rueckert',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Cave Spring Elementary',
      'address': '5404 Springlawn Ave, Roanoke, VA 24018',
      'phone': '540-772-7558',
      'principal': 'Ms. Jodi Poff',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Cave Spring High',
      'address': '3712 Chaparral Dr, Roanoke, VA 24018',
      'phone': '540-772-7550',
      'principal': 'Mr. Steve Spangler',
      'grades': '9-12',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Cave Spring Middle',
      'address': '4880 Brambleton Ave, Roanoke, VA 24018',
      'phone': '540-772-7560',
      'principal': 'Mr. Steve Boyer',
      'grades': '6-8',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Cedar Bluff Elementary',
      'address': '1089 Cedar Valley Drive, Cedar Bluff, VA 24609-1400',
      'phone': '276-963-5765',
      'principal': 'Ms. Charity McDaniel',
      'grades': 'PK-5',
      'division': 'Tazewell County Public Schools'},
     {'name': 'Cedar Forest Elementary',
      'address': '3412 Massaponax Church Road, Fredericksburg, VA 22408',
      'phone': '540-834-4569',
      'principal': 'Mr. David O. Strawn II',
      'grades': 'PK-5',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Cedar Lane Elementary',
      'address': '43700 Tolamac Dr, Ashburn, VA 20147',
      'phone': '571-252-2120',
      'principal': 'Robert Marple',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Cedar Lane School',
      'address': '101 Cedar Ln SW, Vienna, VA 22180',
      'phone': '703-208-2400',
      'principal': 'Mr. Thomas P. Lundy',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Cedar Lee Middle',
      'address': '11138 Marsh Road, Bealeton, VA 22712',
      'phone': '540-439-3207',
      'principal': 'Mr. Steven Parker',
      'grades': '6-8',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Cedar Point Elementary',
      'address': '12601 Braemar Parkway, Bristow, VA 20136',
      'phone': '703-365-0963',
      'principal': 'Mark Anthony Marinoble',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Cedar Road Elementary',
      'address': '1605 Cedar Rd, Chesapeake, VA 23322',
      'phone': '757-547-0166',
      'principal': 'Mr. Michael R. Bailey',
      'grades': 'PK-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Center for Diversified Studies',
      'address': '2204 Mountain Road, Glen Allen, VA 23060',
      'phone': '804-261-5058',
      'principal': ' ',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'Centerville Elementary',
      'address': '2201 Centerville Tnpk, Virginia Beach, VA 23464-5040',
      'phone': '757-648-2200',
      'principal': 'Mr. Thomas H. Chowns',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Central Academy Middle',
      'address': '367 Poor Farm Rd, Fincastle, VA 24090',
      'phone': '540-473-8333',
      'principal': 'Mr. Timothy A. McClung',
      'grades': '6-8',
      'division': 'Botetourt County Public Schools'},
     {'name': 'Central Elementary',
      'address': '575 Union Hill Rd, Amherst, VA 24521',
      'phone': '434-946-9700',
      'principal': 'Mrs. Kathleen M Pierce',
      'grades': 'PK-5',
      'division': 'Amherst County Public Schools'},
     {'name': 'Central Elementary',
      'address': '3340 Central Plains Road, Palmyra, VA 22963',
      'phone': '434-589-8318',
      'principal': 'Ms. Sue Davies',
      'grades': '1-2',
      'division': 'Fluvanna County Public Schools'},
     {'name': 'Central Elementary School',
      'address': '85 Central Road, Lexington, VA 24450',
      'phone': '540-463-4500',
      'principal': 'Mr. Ryan N. Barber',
      'grades': 'PK-5',
      'division': 'Rockbridge County Public Schools'},
     {'name': 'Central High',
      'address': '17024 The Trail, King And Queen C H, VA 23085',
      'phone': '804-785-6102',
      'principal': 'Mr. Antione Monroe',
      'grades': '8-12',
      'division': 'King and Queen County Public Schools'},
     {'name': 'Central High',
      'address': '131 K-V Rd, Victoria, VA 23974-9518',
      'phone': '434-696-2137',
      'principal': 'Mrs. Frances Ball',
      'grades': '9-12',
      'division': 'Lunenburg County Public Schools'},
     {'name': 'Central High',
      'address': '1147 Susan Avenue, Woodstock, VA 22664',
      'phone': '540-459-2161',
      'principal': 'Ms. Melissa D Hensley',
      'grades': '9-12',
      'division': 'Shenandoah County Public Schools'},
     {'name': 'Central High',
      'address': '301 Industrial Park Road, Norton, VA 24273',
      'phone': '276-328-8015',
      'principal': 'Charles W. Collins',
      'grades': '9-12',
      'division': 'Wise County Public Schools'},
     {'name': 'Central Middle',
      'address': '250 Statesman Dr, Charlotte Court House, VA 23923',
      'phone': '434-542-4536',
      'principal': 'Mr. Scott Shep Critzer',
      'grades': '6-8',
      'division': 'Charlotte County Public Schools'},
     {'name': 'Centre Ridge Elementary',
      'address': '14400 New Braddock Rd, Centreville, VA 20121-3440',
      'phone': '703-227-2600',
      'principal': 'Ms. Margo R Pareja',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Centreville Elementary',
      'address': '14330 Green Trails Blvd, Centreville, VA 20121-3879',
      'phone': '703-502-3500',
      'principal': 'Mr. Dwayne Young',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Centreville High',
      'address': '6001 Union Mill Rd, Clifton, VA 20124-1131',
      'phone': '703-802-5400',
      'principal': 'Mr. Martin E Grimm',
      'grades': '9-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Cesar Tarrant Elementary',
      'address': '1589 Wingfield Dr, Hampton, VA 23666',
      'phone': '757-825-4639',
      'principal': 'Mr. John C. Elling',
      'grades': 'PK-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Chamberlayne Elementary',
      'address': '8200 St Charles Rd, Richmond, VA 23227',
      'phone': '804-261-5030',
      'principal': 'Ms. Muriel L. Brinkley',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Chancellor Elementary',
      'address': '5995 Plank Rd, Fredericksburg, VA 22407',
      'phone': '540-786-6123',
      'principal': 'Shawn D. Hudson',
      'grades': 'PK-5',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Chancellor High',
      'address': '6300 Harrison Rd, Fredericksburg, VA 22407',
      'phone': '540-786-2606',
      'principal': 'Mrs. Jacqueline M. Bass-Fortune',
      'grades': '9-12',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Chancellor Middle',
      'address': '6320 Harrison Rd, Fredericksburg, VA 22407',
      'phone': '540-786-8099',
      'principal': 'Cynthia L. Franzen',
      'grades': '6-8',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Chantilly High',
      'address': '4201 Stringfellow Rd, Chantilly, VA 20151-2600',
      'phone': '703-222-8100',
      'principal': 'Ms. Teresa L Johnson',
      'grades': '9-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Chantilly High School Academy',
      'address': '4201 Stringfellow Rd, Chantilly, VA 20151',
      'phone': '703-222-8100',
      'principal': ' ',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Charles Barrett Elementary',
      'address': '1115 Martha Custis Dr, Alexandria, VA 22302',
      'phone': '703-824-6960',
      'principal': 'Mr. Seth Kennard',
      'grades': 'KG-5',
      'division': 'Alexandria Public Schools'},
     {'name': 'Charles City County Elementary',
      'address': '10049 Courthouse Rd, Charles City, VA 23030-3440',
      'phone': '804-829-9256',
      'principal': 'Ms. Latonia Y. Anderson',
      'grades': 'PK-5',
      'division': 'Charles City County Public Schools'},
     {'name': 'Charles City County High',
      'address': '10039 Courthouse Rd, Charles City, VA 23030-3440',
      'phone': '804-829-9249',
      'principal': 'Mrs. Stephannie F. Crutchfield',
      'grades': '9-12',
      'division': 'Charles City County Public Schools'},
     {'name': 'Charles City County Middle',
      'address': '10035 Courthouse Rd, Charles City, VA 23030-3440',
      'phone': '804-829-9252',
      'principal': 'Dr. Brenda M. Petteway',
      'grades': '6-8',
      'division': 'Charles City County Public Schools'},
     {'name': 'Charles M. Johnson Elementary',
      'address': '5600 Bethlehem Rd, Richmond, VA 23230',
      'phone': '804-673-3735',
      'principal': 'Ms. Kimberly L. Sower',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Charlottesville Alternative',
      'address': '715 Henry Avenue, Charlottesville, VA 22903-5225',
      'phone': '434-245-2406',
      'principal': 'Mr. Troy N Duke',
      'grades': '',
      'division': 'Charlottesville Public Schools'},
     {'name': 'Charlottesville High',
      'address': '1400 Melbourne Road, Charlottesville, VA 22901-3148',
      'phone': '434-245-2410',
      'principal': 'Mrs. Jill Dahl',
      'grades': '9-12',
      'division': 'Charlottesville Public Schools'},
     {'name': 'Chase City Elementary',
      'address': '5450 Highway Forty-Seven, Chase City, VA 23924',
      'phone': '434-372-4770',
      'principal': 'Mr. Frederick Taylor',
      'grades': 'PK-5',
      'division': 'Mecklenburg County Public Schools'},
     {'name': 'Chatham Elementary',
      'address': '245 Chatham Elementary Lane, Chatham, VA 24531',
      'phone': '434-432-6461',
      'principal': 'Mrs. Jenny D. Eaton',
      'grades': 'PK-5',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Chatham High',
      'address': '100 Cavalier Cir, Chatham, VA 24531',
      'phone': '434-432-8305',
      'principal': 'Mr. Randy T. Foster',
      'grades': '9-12',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Chatham Middle',
      'address': '11650 US Highway 29 North, Chatham, VA 24531',
      'phone': '434-432-2169',
      'principal': 'Mr. Cedric J. Hairston',
      'grades': '6-8',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Check Elementary',
      'address': '6810 Floyd Highway North, Check, VA 24072',
      'phone': '540-745-9464',
      'principal': 'Mrs. Jessica Cromer',
      'grades': 'PK-7',
      'division': 'Floyd County Public Schools'},
     {'name': 'Cherry Run Elementary',
      'address': '9732 Ironmaster Dr, Burke, VA 22015',
      'phone': '703-923-2800',
      'principal': 'Mr. Mark E Bibbee',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Chesapeake Alternative',
      'address': '605 Providence Road, Chesapeake, VA 23325',
      'phone': '757-578-7046',
      'principal': 'Dr. Penny K. Schultz',
      'grades': '',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Chesapeake Center for Science &Technology',
      'address': '1617 Cedar Rd, Chesapeake, VA 23322',
      'phone': '757-547-0134',
      'principal': 'Mr. William O. Joe',
      'grades': '',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Chesterbrook Elementary',
      'address': '1753 Kirby Rd, Mclean, VA 22101',
      'phone': '703-714-8200',
      'principal': 'Mr. Robert Fuqua',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Chesterfield Academy Elementary',
      'address': '2915 Westminster Ave, Norfolk, VA 23504',
      'phone': '757-628-2544',
      'principal': 'Dr. Sandra Witcher',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'Chesterfield Community High',
      'address': '12400 Branders Bridge Road, Chester, VA 23831',
      'phone': '804-768-6156',
      'principal': 'Dr. Kenneth Butta',
      'grades': '9-12',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Chesterfield Tech.',
      'address': '10101 Courthouse Rd, Chesterfield, VA 23832-0010',
      'phone': '804-768-6160',
      'principal': 'Dr. Colleen Bryant',
      'grades': '',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Chickahominy Middle',
      'address': '9450 Atlee Station Road, Mechanicsville, VA 23116',
      'phone': '804-723-2160',
      'principal': 'Mr. Mark Beckett',
      'grades': '6-8',
      'division': 'Hanover County Public Schools'},
     {'name': 'Chilhowie Elementary',
      'address': '130 Lee Hwy, Chiilhowie, VA 24319',
      'phone': '276-646-8220',
      'principal': 'Mr. Sanders Henderson',
      'grades': 'PK-5',
      'division': 'Smyth County Public Schools'},
     {'name': 'Chilhowie High',
      'address': '1160 Lee Hwy, Chilhowie, VA 24319',
      'phone': '276-646-8966',
      'principal': 'Mr. Michael L. Sturgill',
      'grades': '9-12',
      'division': 'Smyth County Public Schools'},
     {'name': 'Chilhowie Middle',
      'address': '1160 Lee Hwy, Chilhowie, VA 24319',
      'phone': '276-646-3942',
      'principal': 'Mr. Sam Blevins',
      'grades': '6-8',
      'division': 'Smyth County Public Schools'},
     {'name': 'Chimborazo Elementary',
      'address': '3000 E Marshall St, Richmond, VA 23223-7499',
      'phone': '804-780-8392',
      'principal': 'Mrs. Cheryl L. Burke',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'Chincoteague Elementary',
      'address': '6078 Hallie Whealton Smith Dr, Chincoteague, VA 23336',
      'phone': '757-336-5545',
      'principal': 'Ms. Karen Riner',
      'grades': 'PK-5',
      'division': 'Accomack County Public Schools'},
     {'name': 'Chincoteague High',
      'address': '4586 Main St, Chincoteague, VA 23336',
      'phone': '757-336-6166',
      'principal': 'Mr. Warren C. Holland',
      'grades': '6-12',
      'division': 'Accomack County Public Schools'},
     {'name': 'Christiansburg Elementary',
      'address': '160 Wades Lane, Christiansburg, VA 24073',
      'phone': '540-382-5172',
      'principal': 'Ms. Kelly Roark',
      'grades': '3-5',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Christiansburg High',
      'address': '100 Independence Blvd, Christiansburg, VA 24073',
      'phone': '540-382-5178',
      'principal': 'Dr. Kevin Siers',
      'grades': '9-12',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Christiansburg Middle',
      'address': '1205 Buffalo Drive, NW, Christiansburg, VA 24073',
      'phone': '540-394-2180',
      'principal': 'Mr. Mark B Baetz',
      'grades': '6-8',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Christiansburg Primary',
      'address': '240 Betty Drive, Christiansburg, VA 24073',
      'phone': '540-382-5175',
      'principal': 'Mr. Oliver Lewis',
      'grades': 'PK-2',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Christopher C. Kraft Elementary',
      'address': '600 Concord Dr, Hampton, VA 23666',
      'phone': '757-825-4634',
      'principal': 'Ms. Brenda E. McIntyre-Odoms',
      'grades': 'KG-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Christopher Farms Elementary',
      'address': '2828 Pleasant Acres Dr, Virginia Beach, VA 23453',
      'phone': '757-648-2240',
      'principal': 'Teri A. Breaux',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Churchill Road Elementary',
      'address': '7100 Churchill Rd, Mclean, VA 22101',
      'phone': '703-288-8400',
      'principal': 'Mr. Donald Hutzel',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Churchland Academy Elementary',
      'address': '4061 River Shore Rd, Portsmouth, VA 23703-2001',
      'phone': '757-686-2527',
      'principal': 'Mrs. Karen D Clark',
      'grades': 'KG-6',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Churchland Elementary',
      'address': '5601 Michael Ln, Portsmouth, VA 23703-3822',
      'phone': '757-686-2523',
      'principal': 'Miss Michele P Ramey',
      'grades': 'KG-6',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Churchland High',
      'address': '4301 Cedar Ln, Portsmouth, VA 23703-2074',
      'phone': '757-686-2500',
      'principal': 'Dr. Susan S Bechtol',
      'grades': '9-12',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Churchland Middle',
      'address': '4051 River Shore Rd, Portsmouth, VA 23703-2001',
      'phone': '757-686-2512',
      'principal': 'Dr. Eric M Fischer',
      'grades': '7-8',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Churchland Preschool Center',
      'address': '4061 River Shore Road, Portsmouth, VA 23703',
      'phone': '757-686-2533',
      'principal': 'Mrs. Frances J. Gill',
      'grades': 'PK',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Churchland Primary & Intermediate',
      'address': '5700 Hedgerow Ln, Portsmouth, VA 23703-1504',
      'phone': '757-686-2519',
      'principal': 'Mrs. Cora M Freeman',
      'grades': 'KG-6',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Churchville Elementary',
      'address': '3710 Churchville Ave, Churchville, VA 24421',
      'phone': '540-337-6036',
      'principal': 'Mrs. Laura Hodges',
      'grades': 'PK-5',
      'division': 'Augusta County Public Schools'},
     {'name': 'Clara Byrd Baker Elementary',
      'address': '3131 Ironbound Rd, Williamsburg, VA 23185',
      'phone': '757-221-0949',
      'principal': 'Phyllis Dorsey',
      'grades': 'KG-5',
      'division': 'Williamsburg-James City County Public Schools'},
     {'name': 'Claremont Immersion',
      'address': '4700 S. Chesterfield Rd., Arlington, VA 22206',
      'phone': '703-228-2500',
      'principal': 'Ms. Jessica Panfil',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Clark Elementary',
      'address': '1000 Belmont Avenue, Charlottesville, VA 22902-5908',
      'phone': '434-245-2414',
      'principal': 'Dr. Daphne R. Keiser',
      'grades': 'PK-4',
      'division': 'Charlottesville Public Schools'},
     {'name': 'Clarke County High',
      'address': '627 Mosby Blvd., Berryville, VA 22611',
      'phone': '540-955-6130',
      'principal': 'Dr. Jeffrey Jackson',
      'grades': '9-12',
      'division': 'Clarke County Public Schools'},
     {'name': 'Clarksville Elementary',
      'address': '1696 Noblin Farm Road, Clarksville, VA 23927',
      'phone': '434-374-8668',
      'principal': 'Mrs. Ann Dalton',
      'grades': 'PK-5',
      'division': 'Mecklenburg County Public Schools'},
     {'name': 'Claude Thompson Elementary',
      'address': '3284 Rectortown Rd, Marshall, VA 20115',
      'phone': '540-422-7690',
      'principal': 'Ms. Marypat Warter',
      'grades': 'PK-5',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Clays Mill Elementary',
      'address': '1011 Clays Mill School Dr, Scottsburg, VA 24589',
      'phone': '434-476-3022',
      'principal': 'Mrs. Sherry H. Cowan',
      'grades': 'KG-5',
      'division': 'Halifax County Public Schools'},
     {'name': 'Clearbrook Elementary',
      'address': '5205 Franklin Rd, Roanoke, VA 24014',
      'phone': '540-772-7555',
      'principal': 'Ms. Karen Pendleton',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Clearview Early Childhood Center',
      'address': '800 Ainsley Street, Martinsville, VA 24112',
      'phone': '276-403-5800',
      'principal': 'Mrs. Sheilah W. Williams',
      'grades': 'PK',
      'division': 'Martinsville Public Schools'},
     {'name': 'Clearview Elementary',
      'address': '12635 Builders Rd, Herndon, VA 20170-2999',
      'phone': '703-708-6000',
      'principal': 'Ms. Kimberly Willison',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Clermont Elementary',
      'address': '5720 Clermont Dr, Alexandria, VA 22310',
      'phone': '703-921-2400',
      'principal': 'Ms. Anne Stokowski',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Clifton Middle',
      'address': '1000 Riverview Farm Road, Covington, VA 24426',
      'phone': '540-863-1726',
      'principal': 'Mrs. Brenda H. Siple',
      'grades': '6-8',
      'division': 'Alleghany County Public Schools'},
     {'name': 'Clintwood Elementary School',
      'address': '150 Elementary Circle, Clintwood, VA 24228-0585',
      'phone': '276-926-6088',
      'principal': 'Mrs. Janie Vanover',
      'grades': 'PK-4',
      'division': 'Dickenson County Public Schools'},
     {'name': 'Clintwood High',
      'address': '141 Greenwave Drive, Clintwood, VA 24288-0577',
      'phone': '276-926-8400',
      'principal': 'Mr. Rodney L. Compton',
      'grades': '9-12',
      'division': 'Dickenson County Public Schools'},
     {'name': 'Clover Hill Elementary',
      'address': '5700 Woodlake Village Pkwy, Midlothian, VA 23112-2434',
      'phone': '804-739-6220',
      'principal': 'Catherine Hines',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Clover Hill High',
      'address': '13301 Kelly Green Lane, Midlothian, VA 23112-2004',
      'phone': '804-739-6230',
      'principal': 'Dr. Deborah Marks',
      'grades': '9-12',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Cloverdale Elementary',
      'address': '833 Cougar Drive, Cloverdale, VA 24077',
      'phone': '540-992-1086',
      'principal': 'Ms. Jessica L. Martin',
      'grades': 'KG-5',
      'division': 'Botetourt County Public Schools'},
     {'name': 'Cluster Springs Early Learning Center',
      'address': '1011 Cluster Springs Elementary Road, South Boston, VA 24592',
      'phone': '434-572-4121',
      'principal': 'Mrs. Priscilla E. Price',
      'grades': 'PK',
      'division': 'Halifax County Public Schools'},
     {'name': 'Cluster Springs Elementary',
      'address': '7091 Huell Matthews Hwy., Alton, VA 24520',
      'phone': '434-517-2600',
      'principal': 'Mrs. Lisa M. Long',
      'grades': 'KG-5',
      'division': 'Halifax County Public Schools'},
     {'name': 'Coates Elementary',
      'address': '2480 River Birch Rd., Herndon, VA 20171',
      'phone': '703-713-3000',
      'principal': 'Ms. Toni J Rose',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Coeburn Middle',
      'address': '518 Centre Ave NE, Coeburn, VA 24230',
      'phone': '276-395-2135',
      'principal': 'Scott Keith',
      'grades': '5-8',
      'division': 'Wise County Public Schools'},
     {'name': 'Coeburn Primary',
      'address': '332 School House Hill Dr., Coeburn, VA 24230',
      'phone': '276-395-6100',
      'principal': 'Susan Mullins',
      'grades': 'PK-4',
      'division': 'Wise County Public Schools'},
     {'name': 'Cold Harbor Elementary',
      'address': '6740 Cold Harbor Road, Mechanicsville, VA 23111',
      'phone': '804-723-3620',
      'principal': 'Dr. Cheryl E. Fisher',
      'grades': 'PK-5',
      'division': 'Hanover County Public Schools'},
     {'name': 'Coleman Place Elementary',
      'address': '2445 Palmyra St., Norfolk, VA 23513',
      'phone': '757-852-4641',
      'principal': 'Mrs. Pamela Tatem',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'Coles Elementary',
      'address': '7405 Hoadly Rd, Manassas, VA 20112',
      'phone': '703-791-3141',
      'principal': 'Ms. Kathryn Forgas',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'College Park Elementary',
      'address': '1110 Bennington Rd, Virginia Beach, VA 23464-3764',
      'phone': '757-648-2280',
      'principal': 'Sheila Wynn',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Collinsville Primary',
      'address': '15 Primary School Rd, Collinsville, VA 24078',
      'phone': '276-647-8932',
      'principal': 'Mrs. Lisa Millner',
      'grades': 'PK-2',
      'division': 'Henry County Public Schools'},
     {'name': 'Colonial Beach Elementary',
      'address': '315 Douglas Ave., Colonial Beach, VA 22443',
      'phone': '804-224-9897',
      'principal': 'Mrs. Mary Fisher',
      'grades': 'KG-7',
      'division': 'Colonial Beach Public Schools'},
     {'name': 'Colonial Beach High',
      'address': '100 First St., Colonial Beach, VA 22443',
      'phone': '804-224-7166',
      'principal': 'Mr. Andrew S. Hipple',
      'grades': '8-12',
      'division': 'Colonial Beach Public Schools'},
     {'name': 'Colonial Elementary',
      'address': '2941 Webster Rd, Blue Ridge, VA 24064',
      'phone': '540-977-6773',
      'principal': 'Ms. Tammy M. Riggs',
      'grades': 'PK-5',
      'division': 'Botetourt County Public Schools'},
     {'name': 'Colonial Forge High',
      'address': '550 Courthouse Rd, Stafford, VA 22554',
      'phone': '540-658-6115',
      'principal': 'Mr. Gregory O. Daniel',
      'grades': '9-12',
      'division': 'Stafford County Public Schools'},
     {'name': 'Colonial Heights High',
      'address': '3600 Conduit Rd, Colonial Heights, VA 23834-3798',
      'phone': '804-524-3405',
      'principal': 'Kristin Janssen',
      'grades': '9-12',
      'division': 'Colonial Heights Public Schools'},
     {'name': 'Colonial Heights Middle',
      'address': '500 Conduit Rd, Colonial Heights, VA 23834-3798',
      'phone': '804-524-3420',
      'principal': 'Mr. William Hortz',
      'grades': '6-8',
      'division': 'Colonial Heights Public Schools'},
     {'name': 'Colonial Heights Technical Center',
      'address': '3451 Conduit Road, Colonial Heights, VA 23834',
      'phone': '804-524-3405',
      'principal': ' ',
      'grades': '',
      'division': 'Colonial Heights Public Schools'},
     {'name': 'Colonial Trail Elementary',
      'address': '12101 Bacova Drive, Glen Allen, VA 23059',
      'phone': '804-364-0055',
      'principal': 'Mr. Kirk B. Eggleston',
      'grades': 'KG-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Columbia Elementary',
      'address': '6720 Alpine Dr, Annandale, VA 22003',
      'phone': '703-916-2500',
      'principal': 'Mr. Michael Cunningham',
      'grades': 'PK-5',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Colvin Run Elementary',
      'address': '1400 Trap Rd., Vienna, VA 22182',
      'phone': '703-757-3000',
      'principal': 'Mr. Kenneth J. Junge',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Community Based Education',
      'address': '7423 Camp Alger Ave, Falls Church, VA 22042',
      'phone': '703-208-7823',
      'principal': 'Mr. Paul Wardinski',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Concord Elementary',
      'address': '9339 Village Hwy, Concord, VA 24538',
      'phone': '434-993-2257',
      'principal': 'Mr. Daniel L. Frazier',
      'grades': 'PK-5',
      'division': 'Campbell County Public Schools'},
     {'name': 'Conway Elementary',
      'address': '105 Primmer House Road, Fredericksburg, VA 22405',
      'phone': '540-361-1455',
      'principal': 'Mr. William S. Raybold',
      'grades': 'PK-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Cool Spring Elementary',
      'address': '9964 Honey Meadows Rd, Mechanicsville, VA 23116',
      'phone': '804-723-3560',
      'principal': 'Dr. Paula P. Brown',
      'grades': 'PK-5',
      'division': 'Hanover County Public Schools'},
     {'name': 'Cool Spring Elementary',
      'address': '501 Tavistock Dr SE, Leesburg, VA 20175',
      'phone': '571-252-2890',
      'principal': 'Ms. Jill M. Broaddus',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Cool Spring Primary',
      'address': '7301 Acquinton Church Rd., King William, VA 23086',
      'phone': '804-769-3434',
      'principal': 'Mrs. Lisa Thompson',
      'grades': 'PK-2',
      'division': 'King William County Public Schools'},
     {'name': 'Cooper Middle',
      'address': '977 Balls Hill Rd, Mclean, VA 22101',
      'phone': '703-442-5800',
      'principal': 'Ms. Arlene Randall',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Cople Elementary',
      'address': '7114 Cople Highway, Hague, VA 22469',
      'phone': '804-472-2081',
      'principal': 'Ms. Sharon Almond',
      'grades': 'PK-5',
      'division': 'Westmoreland County Public Schools'},
     {'name': 'Copper Creek Elementary',
      'address': '23894 U.S. highway 58, Castlewood, VA 24224',
      'phone': '276-794-9306',
      'principal': ' ',
      'grades': 'PK-KG',
      'division': 'Russell County Public Schools'},
     {'name': 'Cora Kelly Magnet Elementary',
      'address': '3600 Commonwealth Ave, Alexandria, VA 22305',
      'phone': '703-706-4420',
      'principal': 'Brandon Davis',
      'grades': 'KG-5',
      'division': 'Alexandria Public Schools'},
     {'name': 'Cornerstone Learning Center',
      'address': '194 Dennis Riddle Dr., Rustburg, VA 24588',
      'phone': '434-332-8638',
      'principal': 'Mr. E. Denton Sisk',
      'grades': '',
      'division': 'Campbell County Public Schools'},
     {'name': 'Corporate Landing Elementary',
      'address': '1590 Corporate Landing Pkwy, Virginia Beach, VA 23454-5604',
      'phone': '757-648-2370',
      'principal': 'Mr. Benjamin L. Gillikin',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Corporate Landing Middle',
      'address': '1597 Corporate Landing Pkwy, Virginia Beach, VA 23454',
      'phone': '757-648-4500',
      'principal': 'Mr. Freddie P. Alarcon Jr.',
      'grades': '6-8',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Cosby High',
      'address': '14300 Fox Club Parkway, Midlothian, VA 23112',
      'phone': '804-639-8340',
      'principal': 'Dr. Brenda Mayo',
      'grades': '9-12',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Cougar Elementary',
      'address': '9330 Brandon St., Manassas Park, VA 20111',
      'phone': '703-392-1317',
      'principal': 'Ms. Pamela Terry',
      'grades': 'PK-2',
      'division': 'Manassas Park Public Schools'},
     {'name': 'Council Elementary/Middle',
      'address': '7608 Helen Henderson Hwy, Honaker, VA 24260',
      'phone': '276-859-9329',
      'principal': 'Mrs. Maretta Lester',
      'grades': 'PK-7',
      'division': 'Buchanan County Public Schools'},
     {'name': 'Council High',
      'address': '7802 Helen Henderson Hwy, Honaker, VA 24620',
      'phone': '276-859-2627',
      'principal': 'Mrs. Karen Taylor',
      'grades': '8-12',
      'division': 'Buchanan County Public Schools'},
     {'name': 'Countryside Elementary',
      'address': '20624 Countryside Blvd., Sterling, VA 20165',
      'phone': '571-434-3250',
      'principal': 'Richard Rudnick',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Courthouse Academy Program',
      'address': '7409 Brock Road, Spotsylvania, VA 22553',
      'phone': '540-582-5242',
      'principal': 'Janet B. Hodges',
      'grades': '',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Courthouse Road Elementary',
      'address': '9911 Courthouse Rd, Spotsylvania, VA 22553',
      'phone': '540-891-0400',
      'principal': ' ',
      'grades': 'PK-5',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Courtland Elementary',
      'address': '6601 Smith Station Rd, Spotsylvania, VA 22553',
      'phone': '540-898-5422',
      'principal': 'Mrs. Sherri L. Steele',
      'grades': 'PK-5',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Courtland High',
      'address': '6701 Smith Station Rd, Spotsylvania, VA 22553',
      'phone': '540-898-4445',
      'principal': 'Mr. Larry Marks',
      'grades': '9-12',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Coventry Elementary',
      'address': '200 Owen Davis Blvd, Yorktown, VA 23693',
      'phone': '757-898-0403',
      'principal': 'Mrs. Paula Sasin',
      'grades': 'KG-5',
      'division': 'York County Public Schools'},
     {'name': 'Covington High',
      'address': '606 S. Lexington Avenue, Covington, VA 24426',
      'phone': '540-965-1410',
      'principal': ' ',
      'grades': '8-12',
      'division': 'Covington Public Schools'},
     {'name': 'Cradock Middle',
      'address': '21 Alden Ave, Portsmouth, VA 23702-2268',
      'phone': '757-393-8788',
      'principal': 'Mrs. E. Ann Horne',
      'grades': '7-8',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Cradock Technical & Career Center',
      'address': '4300 George Washington Highway, Portsmouth, VA 23702',
      'phone': '757-393-8117',
      'principal': ' ',
      'grades': '',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Craig County High',
      'address': '25239 Craigs Creek Road, Hwy 615, New Castle, VA 24127',
      'phone': '540-864-5185',
      'principal': 'Robert N. Stump',
      'grades': '6-12',
      'division': 'Craig County Public Schools'},
     {'name': 'Craigsville Elementary',
      'address': '100 East First St, Craigsville, VA 24430',
      'phone': '540-997-9184',
      'principal': 'Mrs. Fonda H. Morris',
      'grades': 'PK-5',
      'division': 'Augusta County Public Schools'},
     {'name': 'Creeds Elementary',
      'address': '920 Princess Anne Rd, Virginia Beach, VA 23457-1498',
      'phone': '757-426-7792',
      'principal': 'Mr. Robin D. Davenport',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Creekside Elementary',
      'address': '1000 Bennetts Creek Park Road, Suffolk, VA 23435',
      'phone': '757-923-4251',
      'principal': 'Mrs. Katrina Rountree-Bowers',
      'grades': 'PK-5',
      'division': 'Suffolk Public Schools'},
     {'name': "Creighton's Corner Elementary",
      'address': '23171 Minerva Drive, Ashburn, VA 20148',
      'phone': '703-957-4480',
      'principal': 'Mr. Christopher Knott',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Crestview Elementary',
      'address': '1901 Charles St, Richmond, VA 23226',
      'phone': '804-673-3775',
      'principal': 'Ms. Karen H. Rawlyk',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Crestwood Elementary',
      'address': '7600 Whittington Dr., Richmond, VA 23225-2137',
      'phone': '804-560-2710',
      'principal': 'Michael Courtney',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Crestwood Elementary',
      'address': '6010 Hanover Ave, Springfield, VA 22150',
      'phone': '703-923-5400',
      'principal': 'Mr. Tim M. Kasik',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Crestwood Intermediate',
      'address': '1240 Great Bridge Blvd, Chesapeake, VA 23320',
      'phone': '757-494-7565',
      'principal': 'Mrs. Eva Renee Carney',
      'grades': '3-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Crestwood Middle',
      'address': '1420 Great Bridge Blvd, Chesapeake, VA 23320',
      'phone': '757-494-7560',
      'principal': 'Mr. Michael R. Ward',
      'grades': '6-8',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Crewe Primary',
      'address': '1953 Sunnyside Rd, Crewe, VA 23930',
      'phone': '434-645-8149',
      'principal': 'Mr. Tommy Coleman',
      'grades': '1-4',
      'division': 'Nottoway County Public Schools'},
     {'name': 'Crittenden Middle',
      'address': '6158 Jefferson Ave, Newport News, VA 23605',
      'phone': '757-591-4900',
      'principal': 'Ms. Felicia Barnett',
      'grades': '6-8',
      'division': 'Newport News Public Schools'},
     {'name': 'Critzer Elementary',
      'address': '100 Critzer Dr, Pulaski, VA 24301',
      'phone': '540-643-0274',
      'principal': 'Michael L Grim',
      'grades': 'PK-5',
      'division': 'Pulaski County Public Schools'},
     {'name': 'Crossfield Elementary',
      'address': '2791 Fox Mill Rd, Herndon, VA 20171-2000',
      'phone': '703-295-1100',
      'principal': 'Mr. Robert Yoshida',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Crossroads School',
      'address': '8021 Old Ocean View Rd., Norfolk, VA 23505',
      'phone': '757-531-3050',
      'principal': 'Mrs. Kristen Nichols',
      'grades': 'PK-7',
      'division': 'Norfolk Public Schools'},
     {'name': 'Crozet Elementary',
      'address': '1407 Crozet Avenue, Crozet, VA 22932-3401',
      'phone': '434-823-4800',
      'principal': 'Gwedette Crummie',
      'grades': 'PK-5',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Crystal Spring Elementary',
      'address': '2620 Carolina Ave SW, Roanoke, VA 24014',
      'phone': '540-853-2976',
      'principal': 'Ms. Kathleen Tate',
      'grades': 'PK-5',
      'division': 'Roanoke Public Schools'},
     {'name': 'Cub Run Elementary',
      'address': '5301 Sully Station Dr, Centreville, VA 20120-1367',
      'phone': '703-633-7500',
      'principal': 'Ms. Jennifer Coakley',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Cub Run Elementary',
      'address': '1451 South Montevideo Circle, Penn Laird, VA 22846',
      'phone': '540-289-5854',
      'principal': 'Mr. Kenny Boyers',
      'grades': 'PK-5',
      'division': 'Rockingham County Public Schools'},
     {'name': 'Culpeper County High',
      'address': '14240 Achievement Drive, Culpeper, VA 22701',
      'phone': '540-825-8310',
      'principal': 'Mr. Jeffrey J Dietz',
      'grades': '9-12',
      'division': 'Culpeper County Public Schools'},
     {'name': 'Culpeper Middle',
      'address': '14300 Achievement Dr, Culpeper, VA 22701',
      'phone': '540-825-4140',
      'principal': 'Mrs. Margery Southard',
      'grades': '6-8',
      'division': 'Culpeper County Public Schools'},
     {'name': 'Cumberland Elementary',
      'address': '60 School Rd, Cumberland, VA 23040',
      'phone': '804-492-4212',
      'principal': 'Mr. Mark Mabey',
      'grades': 'PK-4',
      'division': 'Cumberland County Public Schools'},
     {'name': 'Cumberland High',
      'address': '15 School Rd, Cumberland, VA 23040',
      'phone': '804-492-4212',
      'principal': 'Mr. Jeff Scales',
      'grades': '9-12',
      'division': 'Cumberland County Public Schools'},
     {'name': 'Cumberland Middle',
      'address': '16 School Road, Cumberland, VA 23040',
      'phone': '804-492-4212',
      'principal': 'Mr. Jeff Dingeldein',
      'grades': '5-8',
      'division': 'Cumberland County Public Schools'},
     {'name': 'Cunningham Park Elementary',
      'address': '1001 Park St SE, Vienna, VA 22180',
      'phone': '703-255-5600',
      'principal': 'Ms. Rebecca Baenig',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'D.G. Cooley Elementary',
      'address': '34 Westwood Rd, Berryville, VA 22611',
      'phone': '540-955-6120',
      'principal': 'Mr. Hubert Carmichael',
      'grades': 'PK-5',
      'division': 'Clarke County Public Schools'},
     {'name': 'D.J. Montague Elementary',
      'address': '5380 Centerville Rd, Williamsburg, VA 23188',
      'phone': '757-258-3022',
      'principal': 'Lynn Turner',
      'grades': 'KG-5',
      'division': 'Williamsburg-James City County Public Schools'},
     {'name': 'Dale City Elementary',
      'address': '14450 Brook Dr, Woodbridge, VA 22193',
      'phone': '703-670-2208',
      'principal': 'Ms. Cinthia Crowe-Miller',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Damascus Middle',
      'address': '32101 Government Rd, Damascus, VA 24236',
      'phone': '276-739-4100',
      'principal': 'Mrs. Dixie Hunter',
      'grades': '6-8',
      'division': 'Washington County Public Schools'},
     {'name': 'Dan River High',
      'address': '100 Dan River Wildcat Cir, Ringgold, VA 24586',
      'phone': '434-822-7081',
      'principal': 'Mr. Steven D. Mayhew',
      'grades': '9-12',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Dan River Middle',
      'address': '5875 Kentuck Rd., Ringgold, VA 24586',
      'phone': '434-822-6027',
      'principal': 'Mrs. Emily S. Reynolds',
      'grades': '6-8',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Daniel Morgan Middle',
      'address': '48 S Purcell Ave, Winchester, VA 22601',
      'phone': '540-667-7171',
      'principal': 'Sarah Kish',
      'grades': '5-8',
      'division': 'Winchester Public Schools'},
     {'name': 'Daniels Run Elementary',
      'address': '3705 Old Lee Hwy, Fairfax, VA 22030',
      'phone': '703-279-8400',
      'principal': 'Mr. Adam Erbrecht',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Dare Elementary',
      'address': '300 Dare Rd, Yorktown, VA 23692',
      'phone': '757-898-0324',
      'principal': 'Lindsey Caccavale',
      'grades': 'KG-5',
      'division': 'York County Public Schools'},
     {'name': 'David A. Dutrow Elementary',
      'address': '60 Curtis Tignor Rd, Newport News, VA 23608',
      'phone': '757-886-7760',
      'principal': 'Mrs. Marguerite A. Pittman',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'David A. Harrison Elementary',
      'address': '12900 E Quaker Rd, Disputanta, VA 23842',
      'phone': '804-991-2242',
      'principal': "Dr. Sharon O'Neill",
      'grades': 'PK-5',
      'division': 'Prince George County Public Schools'},
     {'name': 'David A. Kaechele Elementary School',
      'address': '5680 Pouncey Tract Road, Glen Allen, VA 23059',
      'phone': '804-364-0055',
      'principal': 'Ms. Cynthia Patterson',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Davis Career Center',
      'address': '7731 Leesburg Pike, Falls Church, VA 22043',
      'phone': '703-714-5600',
      'principal': 'Mr. Brandon G. Wolfe',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Day Treatment Program',
      'address': '351 Old Airport Road, Bristol, VA 24201',
      'phone': '276-645-4722',
      'principal': 'Mr. Mike Nash',
      'grades': '',
      'division': 'Bristol Public Schools'},
     {'name': 'Dearington Elementary/Innovation',
      'address': '210 Smyth St, Lynchburg, VA 24501-1539',
      'phone': '434-522-3757',
      'principal': 'Mr. Daniel J. Rule',
      'grades': 'PK-5',
      'division': 'Lynchburg Public Schools'},
     {'name': 'Deep Creek Central Elementary',
      'address': '2448 Shipyard Rd, Chesapeake, VA 23323',
      'phone': '757-558-5356',
      'principal': 'Mrs. Barbara A. Fortner',
      'grades': 'PK-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Deep Creek Elementary',
      'address': '2809 Forehand Dr, Chesapeake, VA 23323',
      'phone': '757-558-5333',
      'principal': 'Dr. D. Jean Jones',
      'grades': 'PK-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Deep Creek High',
      'address': '2900 Margaret Booker Dr, Chesapeake, VA 23323',
      'phone': '757-558-5302',
      'principal': 'Ms. J. Page Bagley',
      'grades': '9-12',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Deep Creek Middle',
      'address': '1955 Deal Dr, Chesapeake, VA 23323',
      'phone': '757-558-5321',
      'principal': 'Dr. Muriel P. Barefield',
      'grades': '6-8',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Deep Run High',
      'address': '4801 Twin Hickory Rd., Glen Allen, VA 23059',
      'phone': '804-364-8000',
      'principal': 'Mr. Leonard G. Pritchard',
      'grades': '9-12',
      'division': 'Henrico County Public Schools'},
     {'name': 'Deer Park Elementary',
      'address': '15109 Carlbern Dr, Centreville, VA 20120-1432',
      'phone': '703-802-5000',
      'principal': 'Ms. Carol Larsen',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Deer Park Elementary',
      'address': '11541 Jefferson Ave, Newport News, VA 23601',
      'phone': '757-591-7470',
      'principal': 'Ms. Mary Jo Anastasio',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'Denbigh Early Childhood Center',
      'address': '15638 Warwick Blvd., Newport News, VA 23608',
      'phone': '757-886-7789',
      'principal': 'Ms. Lorie Dildy',
      'grades': 'PK',
      'division': 'Newport News Public Schools'},
     {'name': 'Denbigh High',
      'address': '259 Denbigh Blvd, Newport News, VA 23608',
      'phone': '757-886-7700',
      'principal': 'Mr. Anthony Vladu',
      'grades': '9-12',
      'division': 'Newport News Public Schools'},
     {'name': 'Diamond Springs Elementary',
      'address': '5225 Learning Circle, Virginia Beach, VA 23462',
      'phone': '757-648-4240',
      'principal': 'Ms. Gloria F. Coston',
      'grades': 'PK-1',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Dickenson County Career Center',
      'address': '335 Vocational Drive, Clinchco, VA 24266-9701',
      'phone': '276-835-8049',
      'principal': 'Mr. George Brian Baker',
      'grades': '',
      'division': 'Dickenson County Public Schools'},
     {'name': 'Dinwiddie County High School',
      'address': '11501 Boisseau Road, Dinwiddie, VA 23841',
      'phone': '804-469-4280',
      'principal': 'Mr. Randal W. Johnson',
      'grades': '9-12',
      'division': 'Dinwiddie County Public Schools'},
     {'name': 'Dinwiddie County Middle School',
      'address': '11608 Courthouse Road, Dinwiddie, VA 23841',
      'phone': '804-469-5430',
      'principal': 'Mr. Alfred M. Cappellanti III',
      'grades': '6-8',
      'division': 'Dinwiddie County Public Schools'},
     {'name': 'Dinwiddie Elementary School',
      'address': '13811 Boydton Plank Rd, Dinwiddie, VA 23841',
      'phone': '804-469-4580',
      'principal': 'Mrs. Danielle Moore-Winn',
      'grades': 'KG-5',
      'division': 'Dinwiddie County Public Schools'},
     {'name': 'Discovery Elementary School',
      'address': '44020 Grace Bridge Drive, Ashburn, VA 20147',
      'phone': '571-252-2370',
      'principal': 'James Dallas',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Dogwood Elementary',
      'address': '12300 Glade Dr., Reston, VA 20191',
      'phone': '703-262-3100',
      'principal': 'Mr. Terry J. Dade',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Dominion High',
      'address': '21326 Augusta Dr., Sterling, VA 20164',
      'phone': '571-434-4400',
      'principal': 'Dr. W. John Brewer',
      'grades': 'PK-12',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Dominion Trail Elementary',
      'address': '44045 Bruceton Mills Circle, Ashburn, VA 20147',
      'phone': '571-252-2340',
      'principal': 'Jeff Joseph',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Donald B. Dixon-Lyle R. Smith Middle',
      'address': '503 Deacon Road, Fredericksburg, VA 22405',
      'phone': '540-899-0860',
      'principal': 'Ms. Lisa M. Besceglia',
      'grades': '6-8',
      'division': 'Stafford County Public Schools'},
     {'name': 'Douglas Macarthur Elementary',
      'address': '1101 Janneys Ln, Alexandria, VA 22302',
      'phone': '703-461-4190',
      'principal': 'Rae Covey',
      'grades': 'KG-5',
      'division': 'Alexandria Public Schools'},
     {'name': 'Douglas S. Freeman High',
      'address': '8701 Three Chopt Rd, Richmond, VA 23229',
      'phone': '804-673-3700',
      'principal': 'Mrs. Anne L. Poates',
      'grades': '9-12',
      'division': 'Henrico County Public Schools'},
     {'name': 'Douglass Park Elementary',
      'address': '34 Grand St, Portsmouth, VA 23701-3012',
      'phone': '757-393-8646',
      'principal': 'Mrs. Renee P Hailes',
      'grades': 'KG-6',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Douglass School',
      'address': '407 E. Market St., Leesburg, VA 20176',
      'phone': '571-252-2060',
      'principal': 'Dr. John H. Robinson',
      'grades': '',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Dranesville Elementary',
      'address': '1515 Powells Tavern Pl, Herndon, VA 20170-2832',
      'phone': '703-326-5200',
      'principal': 'Ms. Kathy N Manoatl',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Drew Model Elementary',
      'address': '3500 South 23rd Street, Arlington, VA 22206-2501',
      'phone': '703-228-5825',
      'principal': 'Ms. Jackie Smith',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Drewry Mason Elementary',
      'address': '45 Drewry Mason Drive, Ridgeway, VA 24148',
      'phone': '276-956-3154',
      'principal': 'Dr. Sherri G. Lewis',
      'grades': 'PK-5',
      'division': 'Henry County Public Schools'},
     {'name': 'Driver Elementary',
      'address': '4270 Driver Lane, Suffolk, VA 23435',
      'phone': '757-923-4106',
      'principal': 'Ms. Melodie Griffin',
      'grades': '2-5',
      'division': 'Suffolk Public Schools'},
     {'name': 'Dryden Elementary',
      'address': '176 School House Ridge Road, Dryden, VA 24243',
      'phone': '276-546-4443',
      'principal': 'Ms. Mona Marie Baker',
      'grades': 'PK-5',
      'division': 'Lee County Public Schools'},
     {'name': 'Dublin Elementary',
      'address': '600 Dunlap St, Dublin, VA 24084',
      'phone': '540-643-0337',
      'principal': 'Dr. Michael Perry',
      'grades': 'PK-5',
      'division': 'Pulaski County Public Schools'},
     {'name': 'Dublin Middle',
      'address': '650 Giles Ave, Dublin, VA 24084',
      'phone': '540-643-0367',
      'principal': 'Ms. Robin Keener',
      'grades': '6-8',
      'division': 'Pulaski County Public Schools'},
     {'name': 'Dudley Elementary',
      'address': '7250 Brooks Mill Rd, Wirtz, VA 24184',
      'phone': '540-721-2621',
      'principal': 'Ms. Lisa Newell',
      'grades': 'PK-5',
      'division': 'Franklin County Public Schools'},
     {'name': 'Dudley Primary',
      'address': '1840 Tazewell Ave, Bluefield, VA 24605-1199',
      'phone': '276-326-1507',
      'principal': 'Mrs. Susan Maupin',
      'grades': 'PK-2',
      'division': 'Tazewell County Public Schools'},
     {'name': 'Duffield-Pattonsville Primary',
      'address': '663 Duffield-Pattonsville Highway, Highway 23 and St. Rte 58, Duffield, VA 24244',
      'phone': '276-431-2244',
      'principal': 'Mr. Travis Nickels',
      'grades': 'KG-4',
      'division': 'Scott County Public Schools'},
     {'name': 'Dumbarton Elementary',
      'address': '9000 Hungary Spring Rd, Richmond, VA 23228',
      'phone': '804-756-3030',
      'principal': 'Mr. Scott D. Thorpe',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Dumfries Elementary',
      'address': '3990 Cameron St, Dumfries, VA 22026',
      'phone': '703-221-3101',
      'principal': 'Ms. Melvina Michie',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Dungannon Intermediate',
      'address': '113 Fifth Avenue, Highway 65 and St. Rte 72, Dungannon, VA 24245',
      'phone': '276-467-2281',
      'principal': 'Ms. Jennifer Meade',
      'grades': '4-7',
      'division': 'Scott County Public Schools'},
     {'name': 'Dunn Loring E.C. Resource Ctr.',
      'address': '2334 Gallows Rd, Dunn Loring, VA 22027',
      'phone': '703-876-5291',
      'principal': 'Ms. Michele L Lawrence',
      'grades': 'PK',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Dupont Elementary',
      'address': '1000 Winston Churchill Drive, Hopewell, VA 23860',
      'phone': '804-541-6406',
      'principal': 'Mrs. Carla M. Fizer',
      'grades': 'KG-5',
      'division': 'Hopewell Public Schools'},
     {'name': 'E. Wilson Morrison Elementary',
      'address': '40 Crescent St, Front Royal, VA 22630',
      'phone': '540-635-4188',
      'principal': 'Mrs. Margaret S. Holmes',
      'grades': 'KG-5',
      'division': 'Warren County Public Schools'},
     {'name': 'E.B. Stanley Middle',
      'address': '297 Stanley St, Abingdon, VA 24210',
      'phone': '276-739-3300',
      'principal': 'Mr. Scott Allen',
      'grades': '6-8',
      'division': 'Washington County Public Schools'},
     {'name': 'E.C. Glass High',
      'address': '2111 Memorial Ave, Lynchburg, VA 24501-5599',
      'phone': '434-522-3712',
      'principal': 'Dr. Tracy S. Richardson',
      'grades': '9-12',
      'division': 'Lynchburg Public Schools'},
     {'name': 'E.H. Marsteller Middle',
      'address': '14000 Sudley Manor Dr, Bristow, VA 20136',
      'phone': '703-393-7608',
      'principal': 'Roberta Knetter',
      'grades': '6-8',
      'division': 'Prince William County Public Schools'},
     {'name': 'E.S.H. Greene Elementary',
      'address': '1745 Catalina Dr, Richmond, VA 23224-4899',
      'phone': '804-780-5082',
      'principal': 'Linda L Sims',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'Eagle Ridge Middle',
      'address': '42901 Waxpool Rd, Ashburn, VA 20148',
      'phone': '571-252-2140',
      'principal': 'Scott Phillips',
      'grades': '6-8',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Eagle Rock Elementary',
      'address': '145 Eagles Nest Dr, Eagle Rock, VA 24085',
      'phone': '540-884-2421',
      'principal': 'Ms. Sandy Gould',
      'grades': 'PK-5',
      'division': 'Botetourt County Public Schools'},
     {'name': 'Eagle View Elementary',
      'address': '4500 Dixie Hill Road, Fairfax, VA 22030',
      'phone': '703-322-3100',
      'principal': 'Ms. Patricia A. Granada',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Early Learning Center',
      'address': '401 Thomas Jefferson Hwy., Charlotte Court House, VA 23923',
      'phone': '434-542-4463',
      'principal': 'Mrs. Carolyn M. Baker',
      'grades': 'PK',
      'division': 'Charlotte County Public Schools'},
     {'name': 'East Rockingham High',
      'address': '250 Eagle Rock Road, Elkton, VA 22827',
      'phone': '540-298-7450',
      'principal': 'Mr. Eric Baylor',
      'grades': '9-12',
      'division': 'Rockingham County Public Schools'},
     {'name': 'East Salem Elementary',
      'address': '1765 Boulevard, Salem, VA 24153-6489',
      'phone': '540-375-7001',
      'principal': 'Mrs. Diane D. Rose',
      'grades': 'PK-5',
      'division': 'Salem Public Schools'},
     {'name': 'Eastern Elementary/Middle',
      'address': '6899 Virginia Ave, Pembroke, VA 24136',
      'phone': '540-626-7281',
      'principal': 'Mr. Gregory M. Canaday',
      'grades': 'KG-7',
      'division': 'Giles County Public Schools'},
     {'name': 'Eastern Montgomery Elementary',
      'address': '4580 Eastern Montgomery Ln., Elliston, VA 24087',
      'phone': '540-268-1147',
      'principal': 'Ms. Denise E. Boyle',
      'grades': 'PK-5',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Eastern Montgomery High',
      'address': '4695 Crozier Rd, Elliston, VA 24087',
      'phone': '540-268-3010',
      'principal': 'Mr. Daniel G. Knott',
      'grades': '9-12',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Eastern View High',
      'address': '16332 Cyclone Way, Culpeper, VA 22701',
      'phone': '540-825-0621',
      'principal': 'Mr. E.G. Bradshaw',
      'grades': '9-12',
      'division': 'Culpeper County Public Schools'},
     {'name': 'Easton Preschool',
      'address': '6045 Curlew Dr, Norfolk, VA 23502',
      'phone': '757-892-3290',
      'principal': ' ',
      'grades': 'PK',
      'division': 'Norfolk Public Schools'},
     {'name': 'Eastside High',
      'address': '3207 Deacon Drive (Temp), 314 School House Hill Dr, Coeburn 24230 (Perm), St. Paul (Temp), VA 24283',
      'phone': '276-395-3389',
      'principal': 'Dante Lee',
      'grades': '9-12',
      'division': 'Wise County Public Schools'},
     {'name': 'Echo Lake Elementary',
      'address': '5200 Francistown Rd, Glen Allen, VA 23060',
      'phone': '804-527-4672',
      'principal': 'Ms. Cynthia E. Foust',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Ecoff Elementary',
      'address': '5200 Ecoff Ave., Chester, VA 23831-1516',
      'phone': '804-768-6185',
      'principal': 'Dr. Joshua Cole',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Edgemont Primary',
      'address': '574 West Indian Valley Road, Covington, VA 24426',
      'phone': '540-965-1420',
      'principal': 'Ms. Ruth F. Fleming',
      'grades': 'PK-3',
      'division': 'Covington Public Schools'},
     {'name': 'Edison High',
      'address': '5801 Franconia Rd, Alexandria, VA 22310',
      'phone': '703-924-8000',
      'principal': 'Ms. Pamela E. Brumfield',
      'grades': '9-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Edison High School Academy',
      'address': '5801 Franconia Rd, Alexandria, VA 22310',
      'phone': '703-924-8000',
      'principal': ' ',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Edward E. Drew Jr. Middle',
      'address': '501 Cambridge St, Falmouth, VA 22405',
      'phone': '540-371-1415',
      'principal': 'Ms. Tammara M. Hanna',
      'grades': '6-8',
      'division': 'Stafford County Public Schools'},
     {'name': 'Edward G. Clymore Elementary',
      'address': '184 Fort Defiance Rd, Fort Defiance, VA 24437',
      'phone': '540-245-5043',
      'principal': 'Mrs. Jane Wright',
      'grades': 'PK-5',
      'division': 'Augusta County Public Schools'},
     {'name': 'Edward W. Wyatt Middle',
      'address': '206 Slagles Lake Rd, Emporia, VA 23847-8007',
      'phone': '434-634-5159',
      'principal': 'Mr. Noah Rogers',
      'grades': '5-8',
      'division': 'Greensville County Public Schools'},
     {'name': 'Edwin A. Gibson Elementary School',
      'address': '1215 Industrial Avenue, Danville, VA 24541',
      'phone': '434-799-6426',
      'principal': 'Mrs. Kimberly K. Agnor',
      'grades': 'KG-5',
      'division': 'Danville Public Schools'},
     {'name': 'Edwin W. Chittum Elementary',
      'address': '2008 Dock Landing Rd, Chesapeake, VA 23321',
      'phone': '757-465-6300',
      'principal': 'Mrs. Sharon W. Miles',
      'grades': 'PK-5',
      'division': 'Chesapeake Public Schools'},
     {'name': "Elephant's Fork Elementary",
      'address': '2316 William Reid Dr, Suffolk, VA 23434',
      'phone': '757-923-5250',
      'principal': 'Mr. Andre Skinner',
      'grades': 'PK-5',
      'division': 'Suffolk Public Schools'},
     {'name': 'Elizabeth D. Redd Elementary',
      'address': '5601 Jahnke Rd, Richmond, VA 23225-2829',
      'phone': '804-780-5061',
      'principal': 'Mrs. Sherry Wharton-Carey',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'Elizabeth Davis Middle',
      'address': '601 Corvus Court, Chester, VA 23836',
      'phone': '804-541-4700',
      'principal': 'Dr. Tameshia V Grimes',
      'grades': '6-8',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Elizabeth Holladay Elementary',
      'address': '7300 Galaxie Rd, Richmond, VA 23228',
      'phone': '804-261-5040',
      'principal': 'Ms. Kimberly A. Olsen',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Elizabeth Scott Elementary',
      'address': '813 Beginners Trail Loop, Chester, VA 23836',
      'phone': '804-541-4660',
      'principal': 'Joan Temple',
      'grades': 'KG-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Elizabeth Vaughan Elementary',
      'address': '2200 York Dr, Woodbridge, VA 22191',
      'phone': '703-494-3220',
      'principal': 'Glynis Taylor',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Elk Knob Elementary',
      'address': '148 Hornet Loop, Pennington Gap, VA 24277',
      'phone': '276-546-1837',
      'principal': 'Ms. Lisa Willis',
      'grades': 'PK-5',
      'division': 'Lee County Public Schools'},
     {'name': 'Elkhardt Middle',
      'address': '6300 Hull Street Rd, Richmond, VA 23224-2632',
      'phone': '804-745-3600',
      'principal': 'Mr. Eric Jones',
      'grades': '6-8',
      'division': 'Richmond Public Schools'},
     {'name': 'Elko Middle',
      'address': '5901 Elko Road, Sandston, VA 23150',
      'phone': '804-328-4110',
      'principal': 'Ms. Cheryl L. Guempel',
      'grades': '6-8',
      'division': 'Henrico County Public Schools'},
     {'name': 'Elkton Elementary',
      'address': '302 B Street, Elkton, VA 22827',
      'phone': '540-298-1511',
      'principal': 'Mr. Robert Dansey',
      'grades': 'PK-5',
      'division': 'Rockingham County Public Schools'},
     {'name': 'Elkton Middle',
      'address': '21063 Blue And Gold Dr, Elkton, VA 22827',
      'phone': '540-298-1228',
      'principal': 'Dr. Ramona R. Pence',
      'grades': '6-8',
      'division': 'Rockingham County Public Schools'},
     {'name': 'Elmont Elementary',
      'address': '12007 Cedar Lane, Ashland, VA 23005',
      'phone': '804-365-8100',
      'principal': 'Mr. Larry W. Hardy',
      'grades': 'PK-5',
      'division': 'Hanover County Public Schools'},
     {'name': 'Elon Elementary',
      'address': '147 Younger Dr, Madison Heights, VA 24572',
      'phone': '434-528-6496',
      'principal': 'Kimberly L Anderson',
      'grades': 'PK-5',
      'division': 'Amherst County Public Schools'},
     {'name': 'Elydale Elementary',
      'address': '128 Elydale Road, Ewing, VA 24248',
      'phone': '276-445-4439',
      'principal': 'Ms. Tara E. Williams',
      'grades': '5-7',
      'division': 'Lee County Public Schools'},
     {'name': 'Emerald Hill Elementary',
      'address': '11245 Rixeyville Rd, Culpeper, VA 22701',
      'phone': '540-937-7361',
      'principal': 'Mrs. Renee Wootten',
      'grades': 'PK-5',
      'division': 'Culpeper County Public Schools'},
     {'name': 'Emerick Elementary',
      'address': '440 S Nursery Ave, Purcellville, VA 20132',
      'phone': '540-571-2440',
      'principal': 'Mrs. Dawn E. Haddock',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Emily Spong Preschool Center',
      'address': '2200 Piedmont Ave., Portsmouth, VA 23704-5408',
      'phone': '757-393-5247',
      'principal': 'Mrs. Venessa P Whichard-Harris',
      'grades': 'PK',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Empowerment Academy',
      'address': '5915 Nine Mile Road, Henrico, Virginia, VA 23223',
      'phone': '804-328-4280',
      'principal': ' ',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'Enderly Heights Elementary',
      'address': '101 Woodland Ave, Buena Vista, VA 24416',
      'phone': '540-261-6151',
      'principal': 'Christy Harris',
      'grades': '2-4',
      'division': 'Buena Vista Public Schools'},
     {'name': 'Enon Elementary',
      'address': '2001 E. Hundred Rd., Chester, VA 23836-3503',
      'phone': '804-530-5720',
      'principal': 'Mr. Michael Crusco',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Enterprise Elementary',
      'address': '13900 Lindendale Rd, Woodbridge, VA 22193',
      'phone': '703-590-1558',
      'principal': 'Ms. Melanie McClure',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Ervinton Elementary',
      'address': '195 Ervinton Circle, Nora, VA 24272-0519',
      'phone': '276-835-8423',
      'principal': 'Mr. Dennis Deel',
      'grades': 'PK-8',
      'division': 'Dickenson County Public Schools'},
     {'name': 'Essex High',
      'address': '833 High School Circle, Tappahannock, VA 22560',
      'phone': '804-443-4301',
      'principal': 'Ms. Angela Mosley',
      'grades': '9-12',
      'division': 'Essex County Public Schools'},
     {'name': 'Essex Intermediate',
      'address': '912 Intermediate School Circle, Tappahannock, VA 22560',
      'phone': '804-443-3040',
      'principal': 'Mrs. Angela Gross',
      'grades': '5-8',
      'division': 'Essex County Public Schools'},
     {'name': 'Ethel M. Gildersleeve Middle',
      'address': '1 Minton Dr, Newport News, VA 23606',
      'phone': '757-591-4862',
      'principal': 'Ms. Courtney Mompoint',
      'grades': '6-8',
      'division': 'Newport News Public Schools'},
     {'name': 'Ettrick Elementary',
      'address': '20910 Chesterfield Ave., Ettrick, VA 23803-1904',
      'phone': '804-520-6005',
      'principal': 'Teressa Clary',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Eureka Elementary',
      'address': '315 Eureka School Rd, Keysville, VA 23947',
      'phone': '434-736-8458',
      'principal': 'Mr. W. Brian Hamilton',
      'grades': 'KG-5',
      'division': 'Charlotte County Public Schools'},
     {'name': 'Evendale Elementary',
      'address': '220 Rosa Lane, Winchester, VA 22602',
      'phone': '540-662-0531',
      'principal': 'Mrs. Sue Ellen Gossard',
      'grades': 'KG-5',
      'division': 'Frederick County Public Schools'},
     {'name': 'Evening School of Excellence',
      'address': '2204 Mountain Rd., Glen Allen, VA 23060',
      'phone': '804-652-3717',
      'principal': ' ',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'Evergreen Elementary',
      'address': '1701 Evergreen East Pkwy., Midlothian, VA 23114',
      'phone': '804-378-2400',
      'principal': 'Mr. Matthew Maher',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Evergreen Mill Elementary',
      'address': '491 Evergreen Mill Rd SE, Leesburg, VA 20175',
      'phone': '571-252-2900',
      'principal': 'Mr. Michael A. Pellegrino',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'F.W. Kling Jr. Elementary',
      'address': '3400 Lombardy Ave, Buena Vista, VA 24416',
      'phone': '540-261-6717',
      'principal': 'Sherrie Wheeler',
      'grades': 'KG-1',
      'division': 'Buena Vista Public Schools'},
     {'name': 'Fair Oaks Elementary',
      'address': '201 Jennings Rd, Highland Springs, VA 23075',
      'phone': '804-328-4085',
      'principal': 'Mrs. Pamela E. Harvey',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Fairfax County Adult High',
      'address': '4105 Whitacre Rd, Room T108, Fairfax, VA 22032',
      'phone': '703-503-6407',
      'principal': 'Ms. Jane Cruz',
      'grades': '9-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fairfax High',
      'address': '3501 Rebel Run, Fairfax, VA 22030',
      'phone': '703-219-2200',
      'principal': 'Mr. David M Goldfarb',
      'grades': '9-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fairfax High School Academy',
      'address': '3501 Rebel Run, Fairfax, VA 22030',
      'phone': '703-219-2200',
      'principal': ' ',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fairfax Villa Elementary',
      'address': '10900 Santa Clara Dr, Fairfax, VA 22030',
      'phone': '703-267-2800',
      'principal': 'Ms. Gail Kinsey',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fairfield Court Elementary',
      'address': '2510 Phaup St, Richmond, VA 23223-4199',
      'phone': '804-780-4639',
      'principal': 'Craig Mayo',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'Fairfield Elementary',
      'address': '5428 Providence Rd, Virginia Beach, VA 23464',
      'phone': '757-648-2480',
      'principal': 'Mr. Douglas Knapp',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Fairfield Elementary School',
      'address': '20 Fairfield School Rd, Fairfield, VA 24435',
      'phone': '540-348-5202',
      'principal': 'Ms. Vicki W. Stevens',
      'grades': 'PK-5',
      'division': 'Rockbridge County Public Schools'},
     {'name': 'Fairfield Middle',
      'address': '5121 Nine Mile Rd, Richmond, VA 23223',
      'phone': '804-328-4020',
      'principal': 'Mr. Arthur G. Raymond',
      'grades': '6-8',
      'division': 'Henrico County Public Schools'},
     {'name': 'Fairhill Elementary',
      'address': '3001 Chichester Ln, Fairfax, VA 22031',
      'phone': '703-208-8100',
      'principal': 'Ms. Pamela Clayborne-Morgan',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fairlawn Elementary',
      'address': '1132 Wade St, Norfolk, VA 23502',
      'phone': '757-892-3260',
      'principal': 'Ms. Michele Logan',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'Fairview Elementary',
      'address': '5815 Ox Rd, Fairfax Station, VA 22039',
      'phone': '703-503-3700',
      'principal': 'Ms. Lynn A Mayer',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fairview Elementary',
      'address': '2323 Fairview Rd, Galax, VA 24333',
      'phone': '276-236-2365',
      'principal': 'Mr. Michael Reavis',
      'grades': 'KG-5',
      'division': 'Grayson County Public Schools'},
     {'name': 'Fairview Elementary',
      'address': '648 Westwood Blvd NW, Roanoke, VA 24017',
      'phone': '540-853-2978',
      'principal': 'Ms. April Plympton',
      'grades': 'PK-5',
      'division': 'Roanoke Public Schools'},
     {'name': 'Falling Branch Elementary',
      'address': '735 Falling Branch Rd, Christiansburg, VA 24073',
      'phone': '540-381-6145',
      'principal': 'Ms. Julie Vanidestine',
      'grades': 'PK-5',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Falling Creek Elementary',
      'address': '4800 Hopkins Rd., Richmond, VA 23234-3659',
      'phone': '804-743-3630',
      'principal': 'Pam Johnson',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Falling Creek Middle',
      'address': '4724 Hopkins Rd., Richmond, VA 23234-3657',
      'phone': '804-743-3640',
      'principal': 'Melanie Knowles',
      'grades': '6-8',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Fallon Park Elementary',
      'address': '502 19th St SE, Roanoke, VA 24013',
      'phone': '540-853-2535',
      'principal': 'Ms. Cindy Delp',
      'grades': 'PK-5',
      'division': 'Roanoke Public Schools'},
     {'name': 'Falls Church E.C. Resource Ctr.',
      'address': '7521 Jaguar Trail, Falls Church, VA 22042',
      'phone': '703-207-4000',
      'principal': ' ',
      'grades': 'PK',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Falls Church High',
      'address': '7521 Jaguar Trail, Falls Church, VA 22042',
      'phone': '703-207-4000',
      'principal': 'Mr. Michael Yohe',
      'grades': '9-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Falls Church High School Academy',
      'address': '7521 Jaguar Trail, Falls Church, VA 22042',
      'phone': '703-207-4000',
      'principal': ' ',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Falmouth Elementary',
      'address': '1000 Forbes St, Falmouth, VA 22405',
      'phone': '540-373-7458',
      'principal': 'Mrs. Gayle J. Thyrring',
      'grades': 'PK-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Family Education Center For Parenting Teens',
      'address': '1644 N. McKinley Rd #2, Arlington, VA 22205',
      'phone': '703-228-2700',
      'principal': ' ',
      'grades': '',
      'division': 'Arlington County Public Schools'},
     {'name': 'Fancy Gap Elementary School',
      'address': '63 Winding Ridge Rd, Fancy Gap, VA 24328',
      'phone': '276-728-7504',
      'principal': 'Dr. Jeanne D. Edwards',
      'grades': 'PK-5',
      'division': 'Carroll County Public Schools'},
     {'name': 'Fannie W. Fitzgerald Elementary',
      'address': '15500 Benita Fitzgerald Drive, Woodbridge, VA 22193',
      'phone': '703-583-4195',
      'principal': 'Ms. Bridget Outlaw',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Farmington Elementary',
      'address': '500 Sunset Ln, Culpeper, VA 22701',
      'phone': '540-825-0713',
      'principal': 'Mrs. Gail R. Brewer',
      'grades': 'PK-5',
      'division': 'Culpeper County Public Schools'},
     {'name': 'Farmwell Station Middle',
      'address': '44281 Gloucester Pkwy, Ashburn, VA 20147',
      'phone': '571-252-2320',
      'principal': 'Ms. Sherryl D. Loya',
      'grades': '6-8',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Fauquier High',
      'address': '705 Waterloo Rd, Warrenton, VA 20186',
      'phone': '540-347-6100',
      'principal': 'Mr. Roger A. Sites',
      'grades': '9-12',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Featherstone Elementary',
      'address': '14805 Blackburn Rd, Woodbridge, VA 22191',
      'phone': '703-491-1156',
      'principal': 'Mr. Felicia Norwood',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Ferrum Elementary',
      'address': '660 Ferrum School Rd, Ferrum, VA 24088',
      'phone': '540-365-7194',
      'principal': 'Mrs. Jennifer Talley',
      'grades': 'PK-5',
      'division': 'Franklin County Public Schools'},
     {'name': 'Ferry Farm Elementary',
      'address': '20 Pendleton Rd, Fredericksburg, VA 22405',
      'phone': '540-373-7366',
      'principal': 'Mr. Robert D. Freeman',
      'grades': 'PK-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Fieldale-Collinsville Middle',
      'address': '645 Miles Road, Collinsville, VA 24078',
      'phone': '276-647-3841',
      'principal': 'Mrs. Wendy S. Durham',
      'grades': '6-8',
      'division': 'Henry County Public Schools'},
     {'name': 'First Colonial High',
      'address': '1272 Mill Dam Rd, Virginia Beach, VA 23454-2322',
      'phone': '757-648-5300',
      'principal': 'Dr. Nancy Farrell',
      'grades': '9-12',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Fishburn Park Elementary',
      'address': '3057 Colonial Ave SW, Roanoke, VA 24015',
      'phone': '540-853-2931',
      'principal': 'Ms. Judy Lackey',
      'grades': 'PK-5',
      'division': 'Roanoke Public Schools'},
     {'name': 'Flat Rock Elementary',
      'address': '2210 Batterson Road, Powhatan, VA 23139',
      'phone': '804-598-5743',
      'principal': 'Mrs. Tanja Nelson',
      'grades': 'PK-4',
      'division': 'Powhatan County Public Schools'},
     {'name': 'Flatwoods Elementary',
      'address': '205 Flatwoods School Road, Jonesville, VA 24263',
      'phone': '276-346-2799',
      'principal': 'Dr. Renia Clark',
      'grades': 'PK-5',
      'division': 'Lee County Public Schools'},
     {'name': 'Flint Hill Elementary</strong>br/>Street address:, 2444 Flint Hill Rd, Vienna, VA 22181',
      'address': '703-242-6100',
      'phone': 'Mr. Salvador Rivera',
      'principal': 'PK-6',
      'grades': 'Fairfax County Public Schools',
      'division': ''},
     {'name': 'Florence Bowser Elementary',
      'address': '4540 Nansemond Pkwy, Suffolk, VA 23435',
      'phone': '757-923-4164',
      'principal': ' ',
      'grades': 'PK-1',
      'division': 'Suffolk Public Schools'},
     {'name': 'Floris Elementary',
      'address': '2708 Centreville Rd, Herndon, VA 20171-3599',
      'phone': '703-561-2900',
      'principal': 'Ms. Gail Porter',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Floyd County High',
      'address': '721 Baker St. SW, Floyd, VA 24091',
      'phone': '540-745-9450',
      'principal': 'Mr. Tony Deibler',
      'grades': '8-12',
      'division': 'Floyd County Public Schools'},
     {'name': 'Floyd Elementary',
      'address': '531 Oak Hill Drive, Floyd, VA 24091',
      'phone': '540-745-9440',
      'principal': 'Mrs. Jill Lane',
      'grades': 'PK-7',
      'division': 'Floyd County Public Schools'},
     {'name': 'Floyd Kellam High',
      'address': '2323 Holland Rd, Virginia Beach, VA 23456-3599',
      'phone': '757-648-5400',
      'principal': 'Mr. Bruce A. Biehl',
      'grades': '9-12',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Floyd T. Binns Middle',
      'address': '205 Grandview Ave., Culpeper, VA 22201',
      'phone': '540-829-6894',
      'principal': 'Mrs. Sherri Harkness',
      'grades': '6-8',
      'division': 'Culpeper County Public Schools'},
     {'name': 'Fluvanna County High',
      'address': '1918 Thomas Jefferson Parkway, Palmyra, VA 22963',
      'phone': '434-589-3666',
      'principal': 'Mr. James H. Barlow Jr.',
      'grades': '8-12',
      'division': 'Fluvanna County Public Schools'},
     {'name': 'Fluvanna Middle',
      'address': '3717 Central Plains Road, Palmyra, VA 22963',
      'phone': '434-510-1000',
      'principal': 'Dr. Yardley Farquharson',
      'grades': '5-7',
      'division': 'Fluvanna County Public Schools'},
     {'name': 'Forest Edge Elementary',
      'address': '1501 Beacontree Ln, Reston, VA 20190',
      'phone': '703-925-8000',
      'principal': 'Ms. Kim Price',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Forest Elementary',
      'address': 'One Scholar Lane, Forest, VA 24551',
      'phone': '434-525-2681',
      'principal': 'Mrs. Lorri B. Manley',
      'grades': 'KG-5',
      'division': 'Bedford County Public Schools'},
     {'name': 'Forest Glen Middle',
      'address': '200 Forest Glen Dr, Suffolk, VA 23434',
      'phone': '757-925-5780',
      'principal': 'Mr. Melvin Bradshaw',
      'grades': '6-8',
      'division': 'Suffolk Public Schools'},
     {'name': 'Forest Grove Elementary',
      'address': '46245 Forest Ridge Dr., Sterling, VA 20164',
      'phone': '703-434-4560',
      'principal': 'Mr. Lance C. Pace',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Forest Hills Elementary',
      'address': '155 Mountain View Ave, Danville, VA 24541',
      'phone': '434-799-6430',
      'principal': 'Ms. Catherine Lassiter',
      'grades': 'KG-5',
      'division': 'Danville Public Schools'},
     {'name': 'Forest Middle',
      'address': '100 Ashwood Dr, Forest, VA 24551',
      'phone': '434-525-6630',
      'principal': 'Mr. Scott Simmons',
      'grades': '6-8',
      'division': 'Bedford County Public Schools'},
     {'name': 'Forest Park Academy',
      'address': '2730 Melrose Avenue, NW, Roanoke, VA 24017',
      'phone': '540-853-2923',
      'principal': 'Mr. Eric Anderson',
      'grades': '',
      'division': 'Roanoke Public Schools'},
     {'name': 'Forest Park High',
      'address': '15721 Forest Park Drive, Woodbridge, VA 22193',
      'phone': '703-583-3200',
      'principal': 'Eric V. Brent',
      'grades': '9-12',
      'division': 'Prince William County Public Schools'},
     {'name': 'Forestdale Elementary',
      'address': '6530 Elder Ave, Springfield, VA 22150',
      'phone': '703-313-4300',
      'principal': 'Ms. Cheryl A Toth',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Forestville Elementary',
      'address': '1085 Utterback Store Rd, Great Falls, VA 22066',
      'phone': '703-404-6000',
      'principal': 'Mr. Todd Franklin',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fort Belvoir Elementary',
      'address': '5970 Meeres Rd, Fort Belvoir, VA 22060',
      'phone': '703-781-2700',
      'principal': 'Mrs. Theresa Carhart',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fort Blackmore Primary',
      'address': '214 Big Stoney Creek Road, Fort Blackmore, VA 24250',
      'phone': '276-995-2471',
      'principal': 'Mrs. Jennifer Meade',
      'grades': 'KG-3',
      'division': 'Scott County Public Schools'},
     {'name': 'Fort Chiswell High',
      'address': '#1 Pioneer Trail, Max Meadows, VA 24360',
      'phone': '276-637-3711',
      'principal': 'Mr. Robbie T. Patton',
      'grades': '9-12',
      'division': 'Wythe County Public Schools'},
     {'name': 'Fort Chiswell Middle',
      'address': '101 Pioneer Trail, Max Meadows, VA 24360',
      'phone': '276-637-4400',
      'principal': 'Mr. David Brett Booher',
      'grades': '6-8',
      'division': 'Wythe County Public Schools'},
     {'name': 'Fort Defiance High',
      'address': '195 Fort Defiance Rd, Fort Defiance, VA 24437',
      'phone': '540-245-5050',
      'principal': 'Mr. Larry K. Landes',
      'grades': '9-12',
      'division': 'Augusta County Public Schools'},
     {'name': 'Fort Hunt Elementary',
      'address': '8832 Linton Ln, Alexandria, VA 22308',
      'phone': '703-619-2600',
      'principal': 'Ms. Barbara A. Leibbrandt',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fort Lewis Elementary',
      'address': '3115 West Main St, Salem, VA 24153',
      'phone': '540-387-6594',
      'principal': 'Ms. Cindy Klimaitis',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Fox Mill Elementary',
      'address': '2611 Viking Dr, Herndon, VA 20171-2498',
      'phone': '703-262-2700',
      'principal': 'Ms. Mie O Devers',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Frances Hazel Reid Elementary',
      'address': '800 N. King St., Leesburg, VA 20176',
      'phone': '571-252-2050',
      'principal': 'Brenda Jochems',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Francis Asbury Elementary',
      'address': '140 Beach Rd, Hampton, VA 23664',
      'phone': '757-850-5075',
      'principal': 'Ms. Susan K. Johnson',
      'grades': 'KG-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Francis C. Hammond Middle',
      'address': '4646 Seminary Rd, Alexandria, VA 22304',
      'phone': '703-461-4100',
      'principal': 'DeBerry Goodwin',
      'grades': '6-8',
      'division': 'Alexandria Public Schools'},
     {'name': 'Francis Hammond 2 Middle',
      'address': '4646 Seminary Road, Alexandria, VA 22304',
      'phone': '703-461-4100',
      'principal': 'Jason Sutton',
      'grades': '6-8',
      'division': 'Alexandria Public Schools'},
     {'name': 'Francis Hammond 3 Middle',
      'address': '4646 Seminary Road, Alexandria, VA 22304',
      'phone': '703-461-4100',
      'principal': 'Andrea Sparks-Brown',
      'grades': '6-8',
      'division': 'Alexandria Public Schools'},
     {'name': 'Francis Scott Key Elementary',
      'address': '2300 Key Blvd, Arlington, VA 22201',
      'phone': '703-228-4210',
      'principal': 'Dr. Marjorie Myers',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Francis W. Jones Magnet Middle',
      'address': '1819 Nickerson Blvd, Hampton, VA 23663',
      'phone': '757-850-7900',
      'principal': 'Dr. Daniel L. Bowling',
      'grades': '6-8',
      'division': 'Hampton Public Schools'},
     {'name': 'Franconia Elementary',
      'address': '6301 Beulah St, Alexandria, VA 22310',
      'phone': '703-822-2200',
      'principal': 'Ms. Merrell Dade',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Frank W. Cox High',
      'address': '2425 Shorehaven Dr, Virginia Beach, VA 23454-1749',
      'phone': '757-648-5250',
      'principal': 'Dr. Randi R. Riesbeck',
      'grades': '9-12',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Franklin County High School',
      'address': '700 Tanyard Rd, Rocky Mount, VA 24151',
      'phone': '540-483-0221',
      'principal': 'Ms. Debora L. Decker',
      'grades': '9-12',
      'division': 'Franklin County Public Schools'},
     {'name': 'Franklin High',
      'address': '310 Crescent Dr, Franklin, VA 23851-2399',
      'phone': '757-562-5187',
      'principal': 'Mr. Travis Felts',
      'grades': '9-12',
      'division': 'Franklin Public Schools'},
     {'name': 'Franklin Middle',
      'address': '3300 Lees Corner Rd, Chantilly, VA 20151-3100',
      'phone': '703-904-5100',
      'principal': 'Ms. Sharon L. Eisenberg',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Franklin Military Academy',
      'address': '701 North 37th Street, Richmond, VA 23223',
      'phone': '804-780-4968',
      'principal': 'Mrs. Sheron Carter-Gunter',
      'grades': '6-12',
      'division': 'Richmond Public Schools'},
     {'name': 'Fred D. Thompson Middle',
      'address': '7824 Forest Hill Ave, Richmond, VA 23225-1999',
      'phone': '804-272-7554',
      'principal': 'Rickie Hopkins',
      'grades': '6-8',
      'division': 'Richmond Public Schools'},
     {'name': 'Fred M. Lynn Middle',
      'address': '1650 Prince William Parkway, Woodbridge, VA 22191',
      'phone': '703-494-5157',
      'principal': 'Mr. Jorge Neves',
      'grades': '6-8',
      'division': 'Prince William County Public Schools'},
     {'name': 'Frederick County Middle',
      'address': '441 Linden Dr, Winchester, VA 22601',
      'phone': '540-667-4233',
      'principal': 'Ms. Susan Brinkmeier',
      'grades': '6-8',
      'division': 'Frederick County Public Schools'},
     {'name': 'Frederick Douglass Elementary',
      'address': '510 Principal Drummond Way, SE, Leesburg, VA 20175',
      'phone': '571-252-1920',
      'principal': 'Mr. Timothy Martino',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Frederick Douglass Elementary',
      'address': '100 Cedarmeade Ave, Winchester, VA 22601',
      'phone': '540-662-7656',
      'principal': 'Stephanie Downey',
      'grades': 'KG-4',
      'division': 'Winchester Public Schools'},
     {'name': 'Freedom High',
      'address': '25450 Riding Center Drive, South Riding, VA 20152',
      'phone': '703-957-4300',
      'principal': 'Douglas Fulton',
      'grades': '9-12',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Freedom High',
      'address': '15201 Neabsco Mills Rd., Woodbridge, VA 22191',
      'phone': '703-583-1405',
      'principal': 'Inez Bryant',
      'grades': '9-12',
      'division': 'Prince William County Public Schools'},
     {'name': 'Freedom Hill Elementary',
      'address': '1945 Lord Fairfax Rd, Vienna, VA 22182',
      'phone': '703-506-7800',
      'principal': 'Mr. Scott E. Bloom',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Freedom Middle',
      'address': '7315 Smith Station Rd., Fredericksburg, VA 22407',
      'phone': '540-548-1030',
      'principal': 'Mr. Alan C. Jacobs',
      'grades': '6-8',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Fresh Start Center',
      'address': '23190 Sedley Road, Franklin, VA 23851',
      'phone': '757-562-2903',
      'principal': ' ',
      'grades': '',
      'division': 'Southampton County Public Schools'},
     {'name': 'Fries School',
      'address': '114 E Main St, Fries, VA 24330',
      'phone': '276-744-7201',
      'principal': 'Mrs. Elizabeth Brown',
      'grades': 'PK-7',
      'division': 'Grayson County Public Schools'},
     {'name': 'Frost Middle',
      'address': '4101 Pickett Rd, Fairfax, VA 22032',
      'phone': '703-426-5700',
      'principal': 'Ms. Marti Jackson',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Fulks Run Elementary',
      'address': '11089 Brocks Gap Rd, Fulks Run, VA 22830',
      'phone': '540-896-7635',
      'principal': 'Dr. C. David Wenger',
      'grades': 'PK-5',
      'division': 'Rockingham County Public Schools'},
     {'name': 'G.A. Treakle Elementary',
      'address': '2500 Gilmerton Rd, Chesapeake, VA 23323',
      'phone': '757-558-5361',
      'principal': 'Mrs. Shelia Johnson',
      'grades': 'PK-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'G.H. Reid Elementary',
      'address': '1301 Whitehead Rd, Richmond, VA 23225-7299',
      'phone': '804-745-3550',
      'principal': 'Mr. Vincent Darby',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'G.L.H. Johnson Elementary',
      'address': '680 Arnett Blvd, Danville, VA 24540',
      'phone': '434-799-6433',
      'principal': 'Mrs. Tonya Jackson',
      'grades': 'KG-5',
      'division': 'Danville Public Schools'},
     {'name': 'G.W. Carver Elementary',
      'address': '6 Fourth St, Salem, VA 24153-5079',
      'phone': '540-387-2492',
      'principal': 'Dr. Joseph T, Coleman',
      'grades': 'KG-5',
      'division': 'Salem Public Schools'},
     {'name': 'Gainesboro Elementary',
      'address': '4651 N Frederick Pike, Winchester, VA 22603',
      'phone': '540-888-4550',
      'principal': 'Mrs. Kathleen M Weiss',
      'grades': 'KG-5',
      'division': 'Frederick County Public Schools'},
     {'name': 'Gainesville Middle',
      'address': '8001 Limestone Dr, Gainesville, VA 20155',
      'phone': '703-753-1702',
      'principal': 'Dr. Sally E. MacLean',
      'grades': '6-8',
      'division': 'Prince William County Public Schools'},
     {'name': 'Galax Elementary',
      'address': '225 Academy Drive, Galax, VA 24333',
      'phone': '276-236-6159',
      'principal': 'Charles Brian Stuart',
      'grades': 'KG-4',
      'division': 'Galax Public Schools'},
     {'name': 'Galax High',
      'address': '200 Maroon Tide Dr, Galax, VA 24333',
      'phone': '276-236-2991',
      'principal': 'Mr. Justin P. Iroler',
      'grades': '8-12',
      'division': 'Galax Public Schools'},
     {'name': 'Galax Middle',
      'address': '202 Maroon Tide Dr, Galax, VA 24333',
      'phone': '276-236-6124',
      'principal': 'Mrs. Kristina C. Legg',
      'grades': '5-7',
      'division': 'Galax Public Schools'},
     {'name': 'Galbreath-Marshall Building',
      'address': '1401 Old Fredericksburg Rd., Culpeper, VA 22701',
      'phone': '540-825-3677',
      'principal': ' ',
      'grades': 'PK',
      'division': 'Culpeper County Public Schools'},
     {'name': 'Galileo Magnet High',
      'address': '230 S. Ridge St., Danville, VA 24541',
      'phone': '434-773-8186',
      'principal': 'Mr. William J. Lancaster',
      'grades': '9-12',
      'division': 'Danville Public Schools'},
     {'name': 'Garden City Elementary',
      'address': '3718 Garden City Blvd SE, Roanoke, VA 24014',
      'phone': '540-853-2971',
      'principal': 'Ms. Rebecah Smith',
      'grades': 'PK-5',
      'division': 'Roanoke Public Schools'},
     {'name': 'Garfield Elementary',
      'address': '7101 Old Keene Mill Rd, Springfield, VA 22150',
      'phone': '703-923-2900',
      'principal': 'Christine M Slattery',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Gar-Field High',
      'address': '14000 Smoketown Rd, Woodbridge, VA 22192',
      'phone': '703-730-7000',
      'principal': 'Dr. Cherif Sadki',
      'grades': '9-12',
      'division': 'Prince William County Public Schools'},
     {'name': 'Garland R. Quarles Elementary',
      'address': '1310 S Loudoun St, Winchester, VA 22601',
      'phone': '540-662-3575',
      'principal': 'Joan Hovatter',
      'grades': 'PK-4',
      'division': 'Winchester Public Schools'},
     {'name': 'Garrisonville Elementary',
      'address': '100 Wood Dr, Stafford, VA 22556',
      'phone': '540-658-6260',
      'principal': 'Ms. Alexis M. White',
      'grades': 'PK-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Gate City High',
      'address': '178 Harry Fry Dr., Gate City, VA 24251',
      'phone': '276-386-7522',
      'principal': 'Mr. William Gregory Ervin',
      'grades': '10-12',
      'division': 'Scott County Public Schools'},
     {'name': 'Gate City Middle',
      'address': '170 Harry Fry Drive, Gate City, VA 24251',
      'phone': '276-386-6065',
      'principal': 'Mrs. Cynthia Dorton',
      'grades': '7-9',
      'division': 'Scott County Public Schools'},
     {'name': 'Gates - Alternative High School Program',
      'address': '8020 River Stone Drive, Fredericksburg, VA 22407',
      'phone': '540-582-6831',
      'principal': 'Mr. William A. Ball Jr.',
      'grades': '',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Gateway Academy',
      'address': '7409 Brock Road, Spotsylvania, VA 22553',
      'phone': '540-582-3498',
      'principal': ' ',
      'grades': '',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Gatewood Academy',
      'address': '1241 Gatewood Rd., Newport News, VA 23601',
      'phone': '757-591-4963',
      'principal': 'Ms. Heather Jankovich',
      'grades': 'PK',
      'division': 'Newport News Public Schools'},
     {'name': 'Gayton Elementary',
      'address': '12481 Church Rd, Richmond, VA 23233',
      'phone': '804-360-0820',
      'principal': 'Mrs. Peggy C. Wingfield',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'General Academic Development',
      'address': '201 E. Nine Mile Road, Highland Springs, VA 23075',
      'phone': '804-652-3717',
      'principal': ' ',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'General Stanford Elementary',
      'address': '929 Madison Ave., Ft. Eustis, VA 23604',
      'phone': '757-888-3200',
      'principal': 'Ms. Diane Willis',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'Generating Recovery of Academic Direction',
      'address': '2915 Williamsburg Road, Henrico, VA 23231',
      'phone': '804-555-1212',
      'principal': ' ',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'George Carr Round Elementary',
      'address': '10100 Hastings Dr, Manassas, VA 20110-6092',
      'phone': '571-377-6400',
      'principal': 'Ms. Kara Mills',
      'grades': 'PK-4',
      'division': 'Manassas Public Schools'},
     {'name': 'George F. Baker Elementary',
      'address': '6651 Willson Rd, Richmond, VA 23231',
      'phone': '804-226-8755',
      'principal': 'Dr. Beverly B. Allen-Hardy',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'George G. Tyler Elementary',
      'address': '14500 John Marshall Hwy, Gainesville, VA 20155',
      'phone': '703-754-7181',
      'principal': 'Ms. Jennifer Perilla',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'George H. Moody Middle',
      'address': '7800 Woodman Rd, Richmond, VA 23228',
      'phone': '804-261-5015',
      'principal': 'Mr. Paul E. Llewellyn',
      'grades': '6-8',
      'division': 'Henrico County Public Schools'},
     {'name': 'George J. McIntosh Elementary',
      'address': '185 Richneck Rd, Newport News, VA 23608',
      'phone': '757-886-7767',
      'principal': 'Ms. Ethel Francis',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'George Mason Elementary',
      'address': '2601 Cameron Mills Rd, Alexandria, VA 22302',
      'phone': '703-706-4470',
      'principal': 'Kevin West',
      'grades': 'KG-5',
      'division': 'Alexandria Public Schools'},
     {'name': 'George Mason Elementary',
      'address': '813 N 28th St, Richmond, VA 23223-6699',
      'phone': '804-780-4401',
      'principal': 'Sandra Bynum',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'George Mason High',
      'address': '7124 Leesburg Pike, Falls Church, VA 22043',
      'phone': '703-248-5500',
      'principal': 'Mr. Tyrone Byrd',
      'grades': '9-12',
      'division': 'Falls Church Public Schools'},
     {'name': 'George P. Mullen Elementary',
      'address': '8000 Rodes Dr, Manassas, VA 20109',
      'phone': '703-330-0427',
      'principal': 'Ms. Kathy Notyce',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'George P. Phenix Elementary',
      'address': '1061 Big Bethel Road, Hampton, VA 23666',
      'phone': '757-268-3500',
      'principal': 'Ms. Anita M. Owens',
      'grades': 'PK-8',
      'division': 'Hampton Public Schools'},
     {'name': 'George W. Carver Elementary',
      'address': '1110 W Leigh St, Richmond, VA 23220-3199',
      'phone': '804-780-6247',
      'principal': 'Mrs. Kiwana Yates',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'George W. Carver Intermediate',
      'address': '2601 Broad St, Chesapeake, VA 23324',
      'phone': '757-494-7505',
      'principal': 'Mrs. Angela L. Isbell',
      'grades': 'PK-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'George W. Watkins Elementary',
      'address': '6501 New Kent Hwy, Quinton, VA 23141',
      'phone': '804-966-9660',
      'principal': 'Mr. Russ Macomber',
      'grades': 'PK-5',
      'division': 'New Kent County Public Schools'},
     {'name': 'George Washington 2 Middle',
      'address': '1005 Mt. Vernon Avenue, Alexandria, VA 22301',
      'phone': '703-706-4500',
      'principal': 'Pierrette Hall',
      'grades': '6-8',
      'division': 'Alexandria Public Schools'},
     {'name': 'George Washington High',
      'address': '701 Broad St, Danville, VA 24541',
      'phone': '434-799-6410',
      'principal': 'Mr. Withers Jackson',
      'grades': '9-12',
      'division': 'Danville Public Schools'},
     {'name': 'George Washington Middle',
      'address': '1005 Mt Vernon Ave, Alexandria, VA 22301',
      'phone': '703-706-4500',
      'principal': 'Gregory Tardieu',
      'grades': '6-8',
      'division': 'Alexandria Public Schools'},
     {'name': 'George Wythe High',
      'address': '4314 Crutchfield St, Richmond, VA 23225-4767',
      'phone': '804-780-5037',
      'principal': 'Ms. Reva Green Jr.',
      'grades': '9-12',
      'division': 'Richmond Public Schools'},
     {'name': 'George Wythe High',
      'address': '1 Maroon Way, Wytheville, VA 24382',
      'phone': '276-228-3157',
      'principal': 'Mr. Richard W. Skeens Jr.',
      'grades': '9-12',
      'division': 'Wythe County Public Schools'},
     {'name': 'Georgetown Primary',
      'address': '436 Providence Rd, Chesapeake, VA 23325',
      'phone': '757-578-7060',
      'principal': 'Mrs. Terry A. Reitz',
      'grades': 'PK-3',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Gereau Center for Applied Technology & Career Exploration',
      'address': '150 Technology Dr, Rocky Mount, VA 24151',
      'phone': '540-483-5446',
      'principal': 'Matthew J. Brain',
      'grades': '8',
      'division': 'Franklin County Public Schools'},
     {'name': 'Ghent K-8',
      'address': '200 Shirley Ave, Norfolk, VA 23517',
      'phone': '757-628-2565',
      'principal': 'Dr. Thomas McAnulty',
      'grades': 'KG-8',
      'division': 'Norfolk Public Schools'},
     {'name': 'Gilbert Linkous Elementary',
      'address': '813 Toms Creek Rd, Blacksburg, VA 24060',
      'phone': '540-951-5726',
      'principal': 'Mrs. Carol P. Kahler',
      'grades': 'KG-5',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Giles County Tech. Center',
      'address': '1827 Wenonah Avenue, Pearisburg, VA 24134',
      'phone': '540-921-1166',
      'principal': ' ',
      'grades': '',
      'division': 'Giles County Public Schools'},
     {'name': 'Giles High',
      'address': '1825 Wenonah Avenue, Pearisburg, VA 24134',
      'phone': '540-921-1711',
      'principal': 'Mr. Jason D Mills',
      'grades': '8-12',
      'division': 'Giles County Public Schools'},
     {'name': 'Ginter Park Elementary',
      'address': '3817 Chamberlayne Ave, Richmond, VA 23227-4196',
      'phone': '804-780-8193',
      'principal': 'Ms. Indira Williams',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'Givens Elementary',
      'address': '8153 Swords Creek Rd., Swords Creek, VA 24649',
      'phone': '276-991-0001',
      'principal': 'Mrs. Rebecca T Dye',
      'grades': 'PK-2',
      'division': 'Russell County Public Schools'},
     {'name': 'Glade Hill Elementary',
      'address': '8081 Old Franklin Trnpk, Glade Hill, VA 24092-3854',
      'phone': '540-576-3010',
      'principal': 'Mrs. Kimberly Poindexter',
      'grades': 'PK-5',
      'division': 'Franklin County Public Schools'},
     {'name': 'Glade Spring Middle',
      'address': '33474 Stage Coach Rd, Glade Spring, VA 24340',
      'phone': '276-739-3800',
      'principal': 'Mr. Kelly Holmes',
      'grades': '6-8',
      'division': 'Washington County Public Schools'},
     {'name': 'Gladesboro Elementary School',
      'address': '7845 Snake Creek, Hillsville, VA 24343',
      'phone': '276-398-2493',
      'principal': 'Mrs. Samantha S Reed',
      'grades': 'PK-5',
      'division': 'Carroll County Public Schools'},
     {'name': 'Gladeville Elementary School',
      'address': '3117 Glendale Rd, Galax, VA 24333',
      'phone': '276-236-5449',
      'principal': 'Mrs. Mary Jane Carico',
      'grades': 'PK-5',
      'division': 'Carroll County Public Schools'},
     {'name': 'Glasgow Middle',
      'address': '4101 Fairfax Pkwy, Alexandria, VA 22312',
      'phone': '703-813-8700',
      'principal': 'Ms. Penny M. Gros',
      'grades': '6-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Glebe Elementary',
      'address': '1770 N. Glebe Road, Arlington, VA 22207',
      'phone': '703-228-6280',
      'principal': 'Ms. Jamie Borg',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Glen Allen Elementary',
      'address': '11101 Mill Rd, Glen Allen, VA 23060',
      'phone': '804-756-3040',
      'principal': 'Ms. Melissa R. Halquist-Pruden',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Glen Allen High',
      'address': '10700 Staples Mill Road, Glen Allen, VA 23060',
      'phone': '804-501-3300',
      'principal': 'Mrs. Tracie A. Weston',
      'grades': '9-12',
      'division': 'Henrico County Public Schools'},
     {'name': 'Glen Cove Elementary',
      'address': '5901 Cove Rd, Roanoke, VA 24019',
      'phone': '540-561-8135',
      'principal': 'Dr. Jan Nichols',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Glen Forest Elementary',
      'address': '5829 Glen Forest Dr, Falls Church, VA 22041',
      'phone': '703-578-8000',
      'principal': 'Ms. Cynthia F. Choate',
      'grades': 'PK-5',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Glen Lea Elementary',
      'address': '3909 Austin Ave, Richmond, VA 23222',
      'phone': '804-228-2725',
      'principal': 'Ms. Kimberly D. Lee',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Glenkirk Elementary',
      'address': '8584 Sedge Wren Drive, Gainesville, VA 20155',
      'phone': '703-753-1702',
      'principal': 'Lisa Gilkerson',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Glenvar Elementary',
      'address': '4507 Malus Dr, Salem, VA 24153',
      'phone': '540-387-6540',
      'principal': 'Mr. Danny Guard',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Glenvar High',
      'address': '4549 Malus Dr, Salem, VA 24153',
      'phone': '540-387-6536',
      'principal': 'Mr. Joe Hafey',
      'grades': '9-12',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Glenvar Middle',
      'address': '4555 Malus Dr, Salem, VA 24153',
      'phone': '540-387-6322',
      'principal': 'Mr. Jamie Soltis',
      'grades': '6-8',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Glenwood Elementary',
      'address': '2213 Round Hill Dr, Virginia Beach, VA 23464',
      'phone': '757-648-2520',
      'principal': 'Ms. Susan W. Stuhlman',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Gloucester High',
      'address': '6680 Short Lane, Gloucester, VA 23061-9291',
      'phone': '804-693-2526',
      'principal': 'Dr. Layton (Tony) H Beverage',
      'grades': '9-12',
      'division': 'Gloucester County Public Schools'},
     {'name': 'Goochland Elementary',
      'address': '3150 River Road West, Goochland, VA 23063',
      'phone': '804-556-5321',
      'principal': 'Tina McCay',
      'grades': 'PK-5',
      'division': 'Goochland County Public Schools'},
     {'name': 'Goochland High',
      'address': '3250A River Road West, Goochland, VA 23063',
      'phone': '804-556-5322',
      'principal': 'Mr. Mike Newman',
      'grades': '9-12',
      'division': 'Goochland County Public Schools'},
     {'name': 'Goochland Middle',
      'address': '3250B River Road West, Goochland, VA 23063',
      'phone': '804-556-5320',
      'principal': 'Jennifer M. Smith',
      'grades': '6-8',
      'division': 'Goochland County Public Schools'},
     {'name': 'Goodview Elementary',
      'address': '1374 Rivermont Academy Rd, Goodview, VA 24095',
      'phone': '540-892-5674',
      'principal': 'Mr. Edwin L. Zimmerman',
      'grades': 'PK-5',
      'division': 'Bedford County Public Schools'},
     {'name': 'Gordon-Barbour Elementary',
      'address': '500 W Baker Street, Gordonsville, VA 22942',
      'phone': '540-661-4500',
      'principal': 'Katrina Richardson',
      'grades': 'PK-5',
      'division': 'Orange County Public Schools'},
     {'name': 'Grace E. Metz Middle',
      'address': '9950 Wellington Road, Manassas, VA 20110-5895',
      'phone': '571-377-6800',
      'principal': 'Ms. Angela Burnett',
      'grades': '7-8',
      'division': 'Manassas Public Schools'},
     {'name': 'Grace Miller Elementary',
      'address': '6248 Catlett Rd, Bealeton, VA 22712',
      'phone': '540-439-1913',
      'principal': 'Mrs. Judith Williams',
      'grades': 'PK-5',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Grafton Bethel Elementary',
      'address': '410 Lakeside Dr, Grafton, VA 23692',
      'phone': '757-898-0350',
      'principal': 'Dr. Karen Grass',
      'grades': 'KG-5',
      'division': 'York County Public Schools'},
     {'name': 'Grafton High',
      'address': '403 Grafton Dr, Yorktown, VA 23692',
      'phone': '757-898-0530',
      'principal': 'Mr. Royce Hart',
      'grades': '9-12',
      'division': 'York County Public Schools'},
     {'name': 'Grafton Middle',
      'address': '405 Grafton Dr, Yorktown, VA 23692',
      'phone': '757-898-0525',
      'principal': 'Dr. Karen Cagle',
      'grades': '6-8',
      'division': 'York County Public Schools'},
     {'name': 'Grafton Village Elementary',
      'address': '501 Deacon Rd, Falmouth, VA 22405',
      'phone': '540-373-5454',
      'principal': 'Mr. Michael B. Sidebotham',
      'grades': 'PK-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Graham High',
      'address': '210 Valleydale, Bluefield, VA 24605-9400',
      'phone': '276-326-1235',
      'principal': "Mr. John O'Neal",
      'grades': '9-12',
      'division': 'Tazewell County Public Schools'},
     {'name': 'Graham Intermediate',
      'address': '808 Greever Ave, Bluefield, VA 24605-1519',
      'phone': '276-326-3737',
      'principal': 'Mr. Todd Baker',
      'grades': '3-5',
      'division': 'Tazewell County Public Schools'},
     {'name': 'Graham Middle',
      'address': '#1 Academic Cir, Bluefield, VA 24605-9220',
      'phone': '276-326-1101',
      'principal': 'Lee Salyers',
      'grades': '6-8',
      'division': 'Tazewell County Public Schools'},
     {'name': 'Graham Park Middle',
      'address': '3613 Graham Park Rd, Triangle, VA 22172',
      'phone': '703-221-2118',
      'principal': 'Gary J. Anderson',
      'grades': '6-8',
      'division': 'Prince William County Public Schools'},
     {'name': 'Graham Road Elementary',
      'address': '2831 Graham Rd, Falls Church, VA 22042',
      'phone': '571-226-2700',
      'principal': 'Ms. Tamara B. Ballou',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Granby Elementary',
      'address': '7101 Newport Ave, Norfolk, VA 23505',
      'phone': '757-451-4150',
      'principal': 'Mr. Rohan Cumberbatch-Smith',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'Granby High',
      'address': '7101 Granby St, Norfolk, VA 23505',
      'phone': '757-451-4110',
      'principal': 'Mr. Edward L. Daughtrey Jr.',
      'grades': '9-12',
      'division': 'Norfolk Public Schools'},
     {'name': 'Grandin Court Elementary',
      'address': '2815 Spessard Ave SW, Roanoke, VA 24015',
      'phone': '540-853-2867',
      'principal': 'Ms. Theresa Pritchard',
      'grades': 'KG-5',
      'division': 'Roanoke Public Schools'},
     {'name': 'Grange Hall Elementary',
      'address': '19301 Hull Street Rd., Moseley, VA 23120-1412',
      'phone': '804-739-6265',
      'principal': 'Dr. Randi Smith',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Grassfield Elementary',
      'address': '2248 Averill Dr., Chesapeake, VA 23323',
      'phone': '757-558-8923',
      'principal': 'Mr. Robert Sander',
      'grades': 'PK-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Grassfield High',
      'address': '2007 Grizzly Trail, Chesapeake, VA 23323',
      'phone': '757-558-4749',
      'principal': 'Mr. Michael N. Perez',
      'grades': '9-12',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Grayson County High',
      'address': '110 Blue Devil Drive, Independence, VA 24348-0828',
      'phone': '276-773-2131',
      'principal': 'Mrs. Brandi Ray',
      'grades': '8-12',
      'division': 'Grayson County Public Schools'},
     {'name': 'Grayson County High Career & Technical Education',
      'address': '110 Blue Devil Drive, Independence, VA 24348-0707',
      'phone': '276-773-2951',
      'principal': 'Mrs. Karen Blevins',
      'grades': '',
      'division': 'Grayson County Public Schools'},
     {'name': 'Grayson Highlands School',
      'address': '6459 Troutdale Hwy., Troutdale, VA 24378',
      'phone': '276-579-2235',
      'principal': 'Mr. Marlin Campbell',
      'grades': 'PK-7',
      'division': 'Grayson County Public Schools'},
     {'name': 'Great Bridge High',
      'address': '301 West Hanbury Rd, Chesapeake, VA 23322',
      'phone': '757-482-5191',
      'principal': 'Mrs. Michelle K. Porter',
      'grades': '9-12',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Great Bridge Intermediate',
      'address': '253 West Hanbury Rd, Chesapeake, VA 23322',
      'phone': '757-482-4405',
      'principal': 'Mrs. Heather D. Martin',
      'grades': '3-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Great Bridge Middle',
      'address': '441 Battlefield Blvd S, Chesapeake, VA 23322',
      'phone': '757-482-5128',
      'principal': 'Mr. Craig K. Mills',
      'grades': '6-8',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Great Bridge Primary',
      'address': '408 Cedar Rd, Chesapeake, VA 23322',
      'phone': '757-547-1135',
      'principal': 'Mrs. Theresa L. Myers',
      'grades': 'PK-2',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Great Falls Elementary',
      'address': '701 Walker Rd, Great Falls, VA 22066',
      'phone': '703-757-2100',
      'principal': 'Mr. Raymond Lonnett',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Great Neck Middle',
      'address': '1848 North Great Neck Rd, Virginia Beach, VA 23454',
      'phone': '757-648-4550',
      'principal': 'Dr. Eugene F. Soltner',
      'grades': '6-8',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Green Run Collegiate',
      'address': '1700 Dahlia Drive, Attn: Barhara Winn, Virginia Beach, VA 23453',
      'phone': '757-263-1264',
      'principal': 'Ms. Barbara Winn',
      'grades': '9-12',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Green Run Elementary',
      'address': '1200 Green Garden Circle, Virginia Beach, VA 23456',
      'phone': '757-648-2560',
      'principal': 'Ms. Joy Byrd-Butler',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Green Run High',
      'address': '1700 Dahlia Dr, Virginia Beach, VA 23456-2199',
      'phone': '757-648-5350',
      'principal': 'Mr. Todd Tarkenton',
      'grades': '9-12',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Green Valley Elementary',
      'address': '3838 Overdale Rd, Roanoke, VA 24018',
      'phone': '540-772-7556',
      'principal': 'Ms. Ashley McCallum',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Greenbriar East Elementary',
      'address': '13006 Point Pleasant Dr, Fairfax, VA 22033',
      'phone': '703-633-6400',
      'principal': 'Ms. Linda Cohen',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Greenbriar West Elementary',
      'address': '13300 Poplar Tree Rd, Fairfax, VA 22033',
      'phone': '703-633-6700',
      'principal': 'Ms. Lori M. Cleveland',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Greenbrier Elementary',
      'address': '2228 Greenbrier Drive, Charlottesville, VA 22901-2918',
      'phone': '434-245-2415',
      'principal': 'Mr. James E. Kyner',
      'grades': 'PK-4',
      'division': 'Charlottesville Public Schools'},
     {'name': 'Greenbrier Intermediate',
      'address': '1701 River Birch Run N, Chesapeake, VA 23320',
      'phone': '757-578-7080',
      'principal': 'Mr. Keith C. Hyater',
      'grades': '3-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Greenbrier Middle',
      'address': '1016 Greenbrier Pkwy, Chesapeake, VA 23320',
      'phone': '757-548-5309',
      'principal': 'Mr. Michael Mustain',
      'grades': '6-8',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Greenbrier Primary',
      'address': '1551 Eden Way South, Chesapeake, VA 23320',
      'phone': '757-436-3428',
      'principal': 'Mrs. Elizabeth S. Stublen',
      'grades': 'PK-2',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Greendale Elementary',
      'address': '13092 McGuffie Rd, Abingdon, VA 24210',
      'phone': '276-739-3500',
      'principal': 'Mrs. Allyson Willis',
      'grades': 'PK-5',
      'division': 'Washington County Public Schools'},
     {'name': 'Greene County Primary',
      'address': '64 Monroe Drive, Stanardsville, VA 22973',
      'phone': '434-985-5279',
      'principal': 'Mr. Mike Coiner',
      'grades': 'PK-2',
      'division': 'Greene County Public Schools'},
     {'name': 'Greene County Technical Education Center',
      'address': '10415 Spotswood Trail, Standardsville, VA 22973',
      'phone': '434-985-5239',
      'principal': 'Mr. Harry A. Daniel',
      'grades': '',
      'division': 'Greene County Public Schools'},
     {'name': 'Greenfield Elementary',
      'address': '288 Etzler Rd, Troutville, VA 24175',
      'phone': '540-992-4416',
      'principal': "Ms. Laura R. O'Neil-Camp",
      'grades': 'PK-5',
      'division': 'Botetourt County Public Schools'},
     {'name': 'Greenfield Elementary',
      'address': '10751 Savoy Rd., Richmond, VA 23235-3651',
      'phone': '804-560-2720',
      'principal': 'Mary Dunn',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Greensville County High',
      'address': '403 Harding St, Emporia, VA 23847-2529',
      'phone': '434-634-2195',
      'principal': ' ',
      'grades': '9-12',
      'division': 'Greensville County Public Schools'},
     {'name': 'Greensville Elementary',
      'address': '1101 Sussex Dr, Emporia, VA 23847',
      'phone': '434-336-0907',
      'principal': 'Mr. Curtis W. Young',
      'grades': 'PK-5',
      'division': 'Greensville County Public Schools'},
     {'name': 'Greenville Elementary',
      'address': 'Academic Avenue, Nokesville, VA 20181',
      'phone': '540-422-7570',
      'principal': 'Margie Riley',
      'grades': 'PK-5',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Greenwood Elementary',
      'address': '10960 Greenwood Rd., Glen Allen, VA 23059',
      'phone': '804-261-2970',
      'principal': 'Dr. Debra S. Smith',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Greenwood Mill Elementary',
      'address': '281 Channing Drive, Winchester, VA 22602',
      'phone': '540-667-7863',
      'principal': 'Mrs. Kristin Waldrop',
      'grades': 'KG-5',
      'division': 'Frederick County Public Schools'},
     {'name': 'Gretna Elementary',
      'address': '302 Franklin Blvd South, Gretna, VA 24557',
      'phone': '434-656-2231',
      'principal': 'Mrs. Dianne C. Travis',
      'grades': 'PK-5',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Gretna High',
      'address': '100 Gretna Hawk Cir, Gretna, VA 24557',
      'phone': '434-656-2246',
      'principal': 'Mr. Kenyon G. Scott',
      'grades': '9-12',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Gretna Middle',
      'address': '201 Coffey Street, Gretna, VA 24557',
      'phone': '434-656-2217',
      'principal': 'Ms. Vera F. Glass',
      'grades': '6-8',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Grove Hill Preschool Academy',
      'address': '7979 US Highway 340, Shenandoah, VA 22849',
      'phone': '540-652-8544',
      'principal': ' ',
      'grades': 'PK',
      'division': 'Page County Public Schools'},
     {'name': 'Grove Park Preschool',
      'address': '1070 S Main St, Danville, VA 24541',
      'phone': '434-799-6437',
      'principal': 'Ms. Sandra Andrews',
      'grades': 'PK',
      'division': 'Danville Public Schools'},
     {'name': 'Groveton Elementary',
      'address': '6900 Harrison Ln, Alexandria, VA 22306',
      'phone': '703-718-8000',
      'principal': 'Mr. Richard Pollio',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Grundy High',
      'address': '1300 Golden Wave Drive, Grundy, VA 24614',
      'phone': '276-935-2106',
      'principal': 'Mrs. Leslie Horne',
      'grades': '9-12',
      'division': 'Buchanan County Public Schools'},
     {'name': 'Guilford Elementary',
      'address': '600 W Poplar Rd, Sterling, VA 20164',
      'phone': '571-434-4550',
      'principal': 'David Stewart',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Gunston Elementary',
      'address': '10100 Gunston Rd, Lorton, VA 22079',
      'phone': '703-541-3600',
      'principal': 'Mr. Jovon Rogers',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Gunston Middle',
      'address': '2700 S Lang St, Arlington, VA 22206',
      'phone': '703-228-6900',
      'principal': 'Ms. Lori Wiggins',
      'grades': '6-8',
      'division': 'Arlington County Public Schools'},
     {'name': 'Guy K. Stump Elementary',
      'address': '115 Draft Ave, Stuarts Draft, VA 24477',
      'phone': '540-337-1549',
      'principal': 'Mr. David K. Shriver',
      'grades': 'PK-5',
      'division': 'Augusta County Public Schools'},
     {'name': 'H.H. Poole Middle',
      'address': '800 Eustace Rd, Stafford, VA 22554',
      'phone': '540-658-6190',
      'principal': 'Robert Bingham',
      'grades': '6-8',
      'division': 'Stafford County Public Schools'},
     {'name': 'H.M. Pearson Elementary',
      'address': '9347 Bastable Mill Rd, Catlett, VA 20119',
      'phone': '540-788-9071',
      'principal': 'Mrs. Cyndy Carter',
      'grades': 'PK-5',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Halifax County Career Center',
      'address': '315 S Main St, Halifax, VA 24558',
      'phone': '434-476-5515',
      'principal': 'Mr. David C. Riddle',
      'grades': '',
      'division': 'Halifax County Public Schools'},
     {'name': 'Halifax County High',
      'address': 'High School Cir, South Boston, VA 24592',
      'phone': '434-572-4977',
      'principal': 'Mr. Albert T. Randolph',
      'grades': '9-12',
      'division': 'Halifax County Public Schools'},
     {'name': 'Halifax County Middle',
      'address': '1011 Middle School Cir, South Boston, VA 24592',
      'phone': '434-572-4100',
      'principal': 'Mrs. Faye O. Bruce',
      'grades': '6-8',
      'division': 'Halifax County Public Schools'},
     {'name': 'Halley Elementary',
      'address': '8850 Cross Chase Circle, Fairfax Station, VA 22039',
      'phone': '703-551-5700',
      'principal': 'Mrs. Jamey E. Chianetta',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Hamilton Elementary',
      'address': '54 S Kerr St, Hamilton, VA 20158',
      'phone': '540-751-2570',
      'principal': 'Ms. Teri Finn',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Hamilton Holmes Middle',
      'address': '18444 King William Road, King William, VA 23086',
      'phone': '804-769-3434',
      'principal': 'Mrs. Beverly Young',
      'grades': '6-8',
      'division': 'King William County Public Schools'},
     {'name': 'Hampton High',
      'address': '1491 W Queen St, Hampton, VA 23669',
      'phone': '757-825-4430',
      'principal': 'Dr. Sharmaine D. Grove',
      'grades': '9-12',
      'division': 'Hampton Public Schools'},
     {'name': 'Hampton Oaks Elementary',
      'address': '107 Northampton Blvd, Stafford, VA 22554',
      'phone': '540-658-6280',
      'principal': 'Ms. Daria Groover',
      'grades': 'PK-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Hanover High',
      'address': '10307 Chamberlayne Rd., Mechanicsville, VA 23116',
      'phone': '804-723-3700',
      'principal': 'Dr. Dana E. Gresham',
      'grades': '9-12',
      'division': 'Hanover County Public Schools'},
     {'name': 'Hardin Reynolds Elementary',
      'address': '3597 Dogwood Rd, Critz, VA 24082',
      'phone': '276-694-3631',
      'principal': 'Shannon D. Brown',
      'grades': '4-7',
      'division': 'Patrick County Public Schools'},
     {'name': 'Harding Avenue Elementary',
      'address': '429 Harding Avenue, Blacksburg, VA 24060',
      'phone': '540-951-5732',
      'principal': 'Ms. Meggan Marshall',
      'grades': 'KG-5',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Hardy Elementary',
      'address': '9311 Hardy Cir, Smithfield, VA 23430',
      'phone': '757-357-3204',
      'principal': 'Mrs. Tawana Ford',
      'grades': 'PK-3',
      'division': 'Isle of Wight County Public Schools'},
     {'name': 'Harmony Middle',
      'address': '38174 W. Colonial Highway, Hamilton, VA 20158',
      'phone': '540-751-2500',
      'principal': 'Mr. Eric L. Stewart',
      'grades': '6-8',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Harold Macon Ratcliffe Elementary',
      'address': '2901 Thalen St, Richmond, VA 23223',
      'phone': '804-343-6535',
      'principal': 'Ms. Felicia R. Burkhalter',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Harper Park Middle',
      'address': '701 Potomac Station Dr NE, Leesburg, VA 20176',
      'phone': '571-252-2820',
      'principal': 'Elizabeth Beth Robinson',
      'grades': '6-8',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Harrington Waddell Elementary',
      'address': '100 Pendleton Place, Lexington, VA 24450',
      'phone': '540-463-5353',
      'principal': 'Mrs. Lisa Clark',
      'grades': 'KG-5',
      'division': 'Lexington Public Schools'},
     {'name': 'Harrison Road Elementary',
      'address': '6230 Harrison Road, Fredericksburg, VA 22407',
      'phone': '540-548-4864',
      'principal': 'Ms. Deborah H. Frazier',
      'grades': 'PK-5',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'Harrisonburg High',
      'address': '1001 Garbers Church Road, Harrisonburg, VA 22801',
      'phone': '540-433-2652',
      'principal': 'Mr. Tracy Shaver',
      'grades': '9-12',
      'division': 'Harrisonburg Public Schools'},
     {'name': 'Harrowgate Elementary',
      'address': '15501 Harrowgate Rd., Chester, VA 23831-7127',
      'phone': '804-520-6015',
      'principal': 'Patrice Wilson',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Harry E. James Elementary',
      'address': '1807 Arlington Rd, Hopewell, VA 23860',
      'phone': '804-541-6408',
      'principal': 'Mrs. Sandra B. Morton',
      'grades': 'KG-5',
      'division': 'Hopewell Public Schools'},
     {'name': 'Harry F. Byrd Middle',
      'address': '9400 Quioccasin Rd, Richmond, VA 23233',
      'phone': '804-750-2630',
      'principal': 'Dr. Gwen E. Miller',
      'grades': '6-8',
      'division': 'Henrico County Public Schools'},
     {'name': 'Hartwood Elementary',
      'address': '14 Shackleford Well Rd, Hartwood, VA 22406',
      'phone': '540-752-4441',
      'principal': 'Mr. Scott S. Elchenko',
      'grades': 'PK-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Harvie Elementary',
      'address': '3401 Harvie Road, Richmond, VA 23223',
      'phone': '804-343-7010',
      'principal': 'Dr. Pam B. Bell',
      'grades': 'KG-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Haycock Elementary',
      'address': '6616 Haycock Rd, Falls Church, VA 22043',
      'phone': '703-531-4000',
      'principal': 'Ms. Kelly L. Sheers',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Hayfield Elementary',
      'address': '7633 Telegraph Rd, Alexandria, VA 22315',
      'phone': '703-924-4500',
      'principal': ' ',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Hayfield Secondary',
      'address': '7630 Telegraph Rd, Alexandria, VA 22315',
      'phone': '703-924-7400',
      'principal': 'Mr. David Tremaine',
      'grades': '7-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Haysi High',
      'address': '196 Tiger Circle, Haysi, VA 24256-0147',
      'phone': '276-865-5126',
      'principal': 'Mr. John Randall Whitner',
      'grades': '8-12',
      'division': 'Dickenson County Public Schools'},
     {'name': 'HB Woodlawn Secondary Program',
      'address': '4100 Vacation Lane, Arlington, VA 22207',
      'phone': '703-228-6363',
      'principal': 'Mr. Frank Haltiwanger',
      'grades': '',
      'division': 'Arlington County Public Schools'},
     {'name': 'Henderson Middle',
      'address': '4319 Old Brook Rd, Richmond, VA 23227-3896',
      'phone': '804-780-8288',
      'principal': 'Mr. Jonathan Mitchum',
      'grades': '6-8',
      'division': 'Richmond Public Schools'},
     {'name': 'Henrico High',
      'address': '302 Azalea Ave, Richmond, VA 23227',
      'phone': '804-228-2700',
      'principal': 'Dr. Herbert T. Monroe',
      'grades': '9-12',
      'division': 'Henrico County Public Schools'},
     {'name': 'Henry Clay Elementary',
      'address': '310 S James St, Ashland, VA 23005',
      'phone': '804-365-8120',
      'principal': 'Ms. Teresa M. Keck',
      'grades': 'PK-2',
      'division': 'Hanover County Public Schools'},
     {'name': 'Henry D. Ward Elementary',
      'address': '3400 Darbytown Road, Richmond, VA 23231',
      'phone': '804-795-7030',
      'principal': 'Mr. Bryan Almasian',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Henry Elementary',
      'address': '701 S Highland St, Arlington, VA 22204',
      'phone': '703-228-5820',
      'principal': 'Dr. Lisa Piehota',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Henry Elementary',
      'address': '200 Henry School Rd, Henry, VA 24102',
      'phone': '540-483-5676',
      'principal': 'Mrs. Robin Whitmer',
      'grades': 'PK-5',
      'division': 'Franklin County Public Schools'},
     {'name': 'Herbert J. Saunders Middle',
      'address': '14800 Darbydale Av, Woodbridge, VA 22193',
      'phone': '703-670-9188',
      'principal': 'Ms. Myca Gray',
      'grades': '6-8',
      'division': 'Prince William County Public Schools'},
     {'name': 'Heritage Elementary',
      'address': '501 Leesville Rd, Lynchburg, VA 24502-2392',
      'phone': '434-582-1130',
      'principal': 'Mrs. Sharon S. Anderson',
      'grades': 'PK-5',
      'division': 'Lynchburg Public Schools'},
     {'name': 'Heritage High',
      'address': '520 Evergreen Mill Rd. SE, Leesburg, VA 20175',
      'phone': '571-252-2800',
      'principal': 'Jeffrey Adam',
      'grades': 'PK-12',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Heritage High',
      'address': '3020 Wards Ferry Rd, Lynchburg, VA 24502-2499',
      'phone': '434-582-1147',
      'principal': 'Mr. Timothy T. Beatty',
      'grades': '9-12',
      'division': 'Lynchburg Public Schools'},
     {'name': 'Heritage High',
      'address': '5800 Marshall Ave, Newport News, VA 23605',
      'phone': '757-928-6100',
      'principal': 'Mr. Michael Nichols',
      'grades': '9-12',
      'division': 'Newport News Public Schools'},
     {'name': 'Herman L. Horn Elementary',
      'address': '1002 Ruddell Rd, Vinton, VA 24179',
      'phone': '540-857-5007',
      'principal': 'Ms. Susan Brown',
      'grades': 'PK-5',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Hermitage Elementary',
      'address': '1701 Pleasure House Road, Virginia Beach, VA 23455-2226',
      'phone': '757-648-2600',
      'principal': 'Mrs. Holly J. Coggin',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Hermitage High',
      'address': '8301 Hungary Spring Rd, Richmond, VA 23228',
      'phone': '804-756-3000',
      'principal': 'Mr. Andrew R. Armstrong',
      'grades': '9-12',
      'division': 'Henrico County Public Schools'},
     {'name': 'Hermitage Tech. Ctr.',
      'address': '8301 Hungary Spring Rd, Richmond, VA 23228',
      'phone': '804-756-3020',
      'principal': 'Ms. Terrie W. Allsbrooks',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'Herndon Elementary',
      'address': '630 Dranesville Rd, Herndon, VA 20170-3307',
      'phone': '703-326-3100',
      'principal': 'Ms. Ann M Gwynn',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Herndon High',
      'address': '700 Bennett St, Herndon, VA 20170-3199',
      'phone': '703-810-2200',
      'principal': 'Mr. Willliam L. Bates',
      'grades': '9-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Herndon Middle',
      'address': '901 Locust St, Herndon, VA 20170-4999',
      'phone': '703-904-4800',
      'principal': 'Ms. Justine Klena',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Hickory Elementary',
      'address': '109 Benefit Road, Chesapeake, VA 23322',
      'phone': '757-421-7080',
      'principal': 'Mrs. Kimberly C. Pinello',
      'grades': 'PK-5',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Hickory High',
      'address': '1996 Hawk Blvd, Chesapeake, VA 23322',
      'phone': '757-421-4295',
      'principal': 'Mrs. Alfredia C. Turner',
      'grades': '9-12',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Hickory Middle',
      'address': '1997 Hawk Blvd, Chesapeake, VA 23322',
      'phone': '757-421-0468',
      'principal': 'Dr. Deborah T. Hutchens',
      'grades': '6-8',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Hidden Valley High',
      'address': '5000 Titan Trail, Roanoke, VA 24018',
      'phone': '540-776-7320',
      'principal': 'Ms. Rhonda Stegall',
      'grades': '9-12',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Hidden Valley Middle',
      'address': '4902 Hidden Valley School Rd, Roanoke, VA 24018',
      'phone': '540-772-7570',
      'principal': 'Mr. Mike Riley',
      'grades': '6-8',
      'division': 'Roanoke County Public Schools'},
     {'name': 'Hidenwood Elementary',
      'address': '501 Blount Point Rd, Newport News, VA 23606',
      'phone': '757-591-4766',
      'principal': 'Mr. Jonathan Hochman',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'High Point Elementary',
      'address': '14091 Sinking Creek Rd, Bristol, VA 24202',
      'phone': '276-642-5600',
      'principal': 'Mrs. Sherry King',
      'grades': 'PK-5',
      'division': 'Washington County Public Schools'},
     {'name': 'Highland Elementary',
      'address': '252 Myers/Moon Rd, Monterey, VA 24465',
      'phone': '540-468-6360',
      'principal': 'Ms. Teresa Kay Blum',
      'grades': 'PK-5',
      'division': 'Highland County Public Schools'},
     {'name': 'Highland High',
      'address': '244 Myers/Moon Rd, Monterey, VA 24465',
      'phone': '540-468-6320',
      'principal': 'April Goff',
      'grades': '6-12',
      'division': 'Highland County Public Schools'},
     {'name': 'Highland Park Elementary',
      'address': '1212 5th St SW, Roanoke, VA 24016',
      'phone': '540-853-2963',
      'principal': 'Dr. Mark Crummey',
      'grades': 'PK-5',
      'division': 'Roanoke Public Schools'},
     {'name': 'Highland Springs Elementary',
      'address': '600 W Pleasant St, Highland Springs, VA 23075',
      'phone': '804-328-4045',
      'principal': 'Ms. Shawnya S. Tolliver',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Highland Springs High',
      'address': '15 S Oak Ave, Highland Springs, VA 23075',
      'phone': '804-328-4000',
      'principal': 'Ms. Tinkhani U. Hargrove',
      'grades': '9-12',
      'division': 'Henrico County Public Schools'},
     {'name': 'Highland Springs Technical Center',
      'address': '100 Tech Drive, Highland Springs, VA 23075',
      'phone': '804-328-4075',
      'principal': 'Mr. William J. Crowder Jr.',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'Highland View Elementary',
      'address': '1405 Eads St, Bristol, VA 24201',
      'phone': '276-821-5710',
      'principal': 'Mrs. Pam Smith',
      'grades': 'PK-5',
      'division': 'Bristol Public Schools'},
     {'name': 'Hilda J. Barbour Elementary',
      'address': '290 Westminster Drive, Front Royal, VA 22630',
      'phone': '540-622-8090',
      'principal': 'Ms. Joanne B. Waters',
      'grades': 'KG-5',
      'division': 'Warren County Public Schools'},
     {'name': 'Hillpoint Elementary',
      'address': '1101 Hillpoint Rd, Suffolk, VA 23434',
      'phone': '757-925-6750',
      'principal': 'Mr. Ronald Leigh',
      'grades': 'PK-5',
      'division': 'Suffolk Public Schools'},
     {'name': 'Hillsboro Elementary',
      'address': '37110 Charles Town Pike, Purcellville, VA 20132',
      'phone': '540-751-2560',
      'principal': 'Mr. David Michener',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Hillside Elementary',
      'address': '43000 Ellzey Dr, Ashburn, VA 20148',
      'phone': '571-252-2170',
      'principal': 'Garett Brazina',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Hillsville Elementary School',
      'address': '90 Patriot Lane, Hillsville, VA 24343',
      'phone': '276-728-7312',
      'principal': 'Mrs. Elizabeth S. Motley',
      'grades': 'PK-5',
      'division': 'Carroll County Public Schools'},
     {'name': 'Hilton Elementary',
      'address': '225 River Rd, Newport News, VA 23601',
      'phone': '757-591-4772',
      'principal': 'Ms. Barbara Nagel',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'Hilton Elementary',
      'address': '303 Academy Rd., Highway 58, Hiltons, VA 24258',
      'phone': '276-386-7430',
      'principal': 'Mrs. Kelsey K. Taylor',
      'grades': 'KG-6',
      'division': 'Scott County Public Schools'},
     {'name': 'Hodges Manor Elementary',
      'address': '1201 Cherokee Rd, Portsmouth, VA 23701-1707',
      'phone': '757-465-2921',
      'principal': 'Ms. Faye S. Felton',
      'grades': 'KG-6',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Hoffman-Boston Elementary',
      'address': '1415 S Queen St, Arlington, VA 22204',
      'phone': '703-228-5845',
      'principal': 'Ms. Kimberley Graves',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Holland Elementary',
      'address': '3340 Holland Rd, Virginia Beach, VA 23452-4826',
      'phone': '757-648-2460',
      'principal': 'Dr. Callie M. Richardson',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools<a/>td>'},
     {'name': 'Hollin Meadows Elementary',
      'address': '2310 Nordok Place, Alexandria, VA 22306',
      'phone': '703-718-8300',
      'principal': 'Mr. Jon Gates',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Hollymead Elementary',
      'address': '2775 Powell Creek Drive, Charlottesville, VA 22911-7540',
      'phone': '434-973-8301',
      'principal': 'Ms. Nancy Teel',
      'grades': 'PK-5',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Holman Middle',
      'address': '600 Concourse Blvd., Glen Allen, VA 23059',
      'phone': '804-346-1300',
      'principal': 'Dr. Brian P. Fellows',
      'grades': '6-8',
      'division': 'Henrico County Public Schools'},
     {'name': 'Holmes Middle',
      'address': '6525 Montrose St, Alexandria, VA 22312',
      'phone': '703-658-5900',
      'principal': 'Mr. Roberto Pamas',
      'grades': '6-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Holston High',
      'address': '21308 Monroe Rd, Damascus, VA 24236',
      'phone': '276-739-4000',
      'principal': 'Mrs. Kendra Honaker',
      'grades': '9-12',
      'division': 'Washington County Public Schools'},
     {'name': 'Home-Based Speced School</strong>, ',
      'address': '540-389-0130',
      'phone': ' ',
      'principal': '',
      'grades': 'Salem Public Schools',
      'division': ''},
     {'name': 'Homebound Speced School</strong>, ',
      'address': '540-389-0130',
      'phone': ' ',
      'principal': '',
      'grades': 'Salem Public Schools',
      'division': ''},
     {'name': 'Homer L. Hines Middle',
      'address': '561 McLawhorne Dr, Newport News, VA 23601',
      'phone': '757-591-4878',
      'principal': 'Dr. Amanda Corbin-Staton',
      'grades': '6-8',
      'division': 'Newport News Public Schools'},
     {'name': 'Honaker Elementary',
      'address': '50 Honaker Elementary Dr., Honaker, VA 24260',
      'phone': '276-873-6301',
      'principal': 'Mr. Gary E. Hess',
      'grades': 'PK-7',
      'division': 'Russell County Public Schools'},
     {'name': 'Honaker High',
      'address': '1795 Thompson Creek Rd., Honaker, VA 24266',
      'phone': '276-873-6363',
      'principal': 'Mr. Anthony L Bush',
      'grades': '8-12',
      'division': 'Russell County Public Schools'},
     {'name': 'Hopewell High',
      'address': '400 S Mesa Dr, Hopewell, VA 23860',
      'phone': '804-541-6402',
      'principal': 'Dr. Rodney L. Berry',
      'grades': '9-12',
      'division': 'Hopewell Public Schools'},
     {'name': 'Hopewell ISAEP Center',
      'address': '400 S. Mesa Dr., Hopewell, VA 23860',
      'phone': '804-541-6402',
      'principal': ' ',
      'grades': '',
      'division': 'Hopewell Public Schools'},
     {'name': 'Hopkins Road Elementary',
      'address': '6000 Hopkins Rd., Richmond, VA 23234-5438',
      'phone': '804-743-3665',
      'principal': 'Dr. Lisa Hill',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Horace H. Epes Elementary',
      'address': '855 Lucas Creek Rd, Newport News, VA 23608',
      'phone': '757-886-7755',
      'principal': 'Ms. Camisha Davis',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'Horizon Elementary',
      'address': '46665 Broadmore Dr, Sterling, VA 20165',
      'phone': '571-434-3260',
      'principal': 'Jennifer Ewing',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Huddleston Elementary',
      'address': '1027 Huddleston Drive, Huddleston, VA 24104',
      'phone': '540-297-5144',
      'principal': 'Aprille A Monroe',
      'grades': 'PK-5',
      'division': 'Bedford County Public Schools'},
     {'name': 'Hugh Mercer Elementary',
      'address': '2100 Cowan Blvd, Fredericksburg, VA 22401-1002',
      'phone': '540-372-1115',
      'principal': 'Mrs. Marjorie R. Tankersley',
      'grades': 'KG-2',
      'division': 'Fredericksburg Public Schools'},
     {'name': 'Hughes Middle',
      'address': '11401 Ridge Heights Rd, Reston, VA 20191-1398',
      'phone': '703-715-3600',
      'principal': 'Ms. Aimee Monticchio',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Hugo A. Owens Middle',
      'address': '1997 Horseback Run, Chesapeake, VA 23323',
      'phone': '757-558-5382',
      'principal': 'Mrs. Amber N. Dortch',
      'grades': '6-8',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Huguenot High',
      'address': '7945 Forest Hill Ave, Richmond, VA 23225-1998',
      'phone': '804-320-7967',
      'principal': 'Jafar Barakat',
      'grades': '9-12',
      'division': 'Richmond Public Schools'},
     {'name': 'Hungary Creek Middle',
      'address': '4909 Francistown Rd., Glen Allen, VA 23060',
      'phone': '804-527-2640',
      'principal': 'Mr. Robert J. Moose',
      'grades': '6-8',
      'division': 'Henrico County Public Schools'},
     {'name': 'Hunt Valley Elementary',
      'address': '7107 Sydenstricker Rd, Springfield, VA 22152',
      'phone': '703-913-8800',
      'principal': 'Mr. David M. Fee',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Hunter B. Andrews',
      'address': '3120 Victoria Boulevard, Hampton, VA 23661',
      'phone': '757-268-3333',
      'principal': 'Mr. Jeffery A. Blowe',
      'grades': 'PK-8',
      'division': 'Hampton Public Schools'},
     {'name': 'Hunters Woods Elementary School for the Arts and Sciences',
      'address': '2401 Colts Neck Rd, Reston, VA 20191-2608',
      'phone': '703-262-7400',
      'principal': 'Ms. Emily S Cope',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Huntington Middle',
      'address': '3401 Orcutt Avenue, Newport News, VA 23607',
      'phone': '757-928-6846',
      'principal': 'Ms. Cleo Holloway',
      'grades': '6-8',
      'division': 'Newport News Public Schools'},
     {'name': 'Hurley Elementary/Middle',
      'address': '6911 Hurley Road, Hurley, VA 24620',
      'phone': '276-566-8523',
      'principal': 'Ms. Della Tester',
      'grades': 'PK-7',
      'division': 'Buchanan County Public Schools'},
     {'name': 'Hurley High',
      'address': '6339 Hurley Road, Hurley, VA 24620',
      'phone': '276-566-7642',
      'principal': 'Pam Dotson',
      'grades': '8-12',
      'division': 'Buchanan County Public Schools'},
     {'name': 'Hurt Park Elementary',
      'address': '1525 Salem Ave SW, Roanoke, VA 24016',
      'phone': '540-853-2986',
      'principal': 'Ms. Theresa Kabath',
      'grades': 'PK-5',
      'division': 'Roanoke Public Schools'},
     {'name': 'Hutchison Elementary',
      'address': '13209 Parcher Ave, Herndon, VA 20170-4399',
      'phone': '703-925-8300',
      'principal': 'Ms. Judy Baldwin',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Hutchison Farm Elementary',
      'address': '42819 Center St., South Riding, VA 20152',
      'phone': '703-957-4350',
      'principal': 'Mrs. Heidi E. Smith',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Hybla Valley Elementary',
      'address': '3415 Lockheed Blvd, Alexandria, VA 22306',
      'phone': '703-718-7000',
      'principal': 'Ms. Lauren Sheehy',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'I.C. Norcom High',
      'address': '1801 London Blvd, Portsmouth, VA 23704-2135',
      'phone': '757-393-5442',
      'principal': 'Dr. Rosalynn L Sanderlin',
      'grades': '9-12',
      'division': 'Portsmouth Public Schools'},
     {'name': 'Independence Elementary',
      'address': '915 E Main St, Independence, VA 24348-0429',
      'phone': '276-773-2722',
      'principal': 'Mrs. Susan Mitchell',
      'grades': 'KG-5',
      'division': 'Grayson County Public Schools'},
     {'name': 'Independence Middle',
      'address': '100 Blue Devil Drive, Independence, VA 24348-0155',
      'phone': '276-773-3020',
      'principal': 'Mr. Jamey Hale',
      'grades': '6-7',
      'division': 'Grayson County Public Schools'},
     {'name': 'Independence Middle',
      'address': '1370 Dunstan Ln, Virginia Beach, VA 23455-4960',
      'phone': '757-648-4600',
      'principal': 'Mr. Carey Manugo',
      'grades': '6-8',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Independence Secondary',
      'address': '412 Roanoke St., Christiansburg, VA 24073',
      'phone': '540-381-6100',
      'principal': 'Mr. Larry Lowe',
      'grades': '',
      'division': 'Montgomery County Public Schools'},
     {'name': 'Independent Hill',
      'address': '14780 Joplin Rd, Manassas, VA 20112',
      'phone': '703-791-8150',
      'principal': 'Ms. Jodi Pankowski',
      'grades': '',
      'division': 'Prince William County Public Schools'},
     {'name': 'Indian Hollow Elementary',
      'address': '1548 North Hayfield Rd, Winchester, VA 22603',
      'phone': '540-877-2283',
      'principal': 'Ms. Deanna M. Lock',
      'grades': 'KG-5',
      'division': 'Frederick County Public Schools'},
     {'name': 'Indian Lakes Elementary',
      'address': '1240 Homestead Dr, Virginia Beach, VA 23464',
      'phone': '757-648-2680',
      'principal': 'Jennifer Born',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Indian River High',
      'address': '1969 Braves Trl, Chesapeake, VA 23325',
      'phone': '757-578-7000',
      'principal': 'Mr. James L. Frye',
      'grades': '9-12',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Indian River Middle',
      'address': '2300 Old Greenbrier Rd, Chesapeake, VA 23325',
      'phone': '757-578-7030',
      'principal': 'Mrs. Naomi R. Dunbar',
      'grades': '6-8',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Indian Valley Elementary',
      'address': '4130 Indian Valley Rd NW, Radford, VA 24141',
      'phone': '540-745-9420',
      'principal': 'Mr. Chris D Hewitt',
      'grades': 'PK-7',
      'division': 'Floyd County Public Schools'},
     {'name': 'Ingleside Elementary',
      'address': '976 Ingleside Rd, Norfolk, VA 23502',
      'phone': '757-892-3270',
      'principal': 'Ms. Dwana White',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'Interagency Alternative Secondary Center',
      'address': '3877 Fairfax Ridge Rd, Fairfax, VA 22030',
      'phone': '571-423-3360',
      'principal': 'Ms. Shannon Matheny',
      'grades': '',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Irving Middle',
      'address': '8100 Old Keene Mill Rd, Springfield, VA 22152',
      'phone': '703-912-4500',
      'principal': 'Mr. Danny Little',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'ISEAP Program',
      'address': '201 E. Nine Mile Road, Highland Springs, VA 23075',
      'phone': '804-652-3717',
      'principal': ' ',
      'grades': '',
      'division': 'Henrico County Public Schools'},
     {'name': 'Island Creek Elementary',
      'address': '7855 Morning View Ln., Alexandria, VA 22315',
      'phone': '571-642-6300',
      'principal': 'Mr. Michael G. Macrina',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'J. Blaine Blayton Elementary',
      'address': '800 Jolly Pond Road, Williamsburg, VA 23188',
      'phone': '757-565-9300',
      'principal': 'Paula Huffman',
      'grades': 'PK-5',
      'division': 'Williamsburg-James City County Public Schools'},
     {'name': 'J. Frank Hillyard Middle',
      'address': '226 Hawks Hill Dr, Broadway, VA 22815',
      'phone': '540-896-8961',
      'principal': 'Mr. David Baker',
      'grades': '6-8',
      'division': 'Rockingham County Public Schools'},
     {'name': 'J. Lupton Simpson Middle',
      'address': '490 Evergreen Mill Rd SE, Leesburg, VA 20175',
      'phone': '571-252-2840',
      'principal': 'Mr. Chad A. Runfola',
      'grades': '6-8',
      'division': 'Loudoun County Public Schools'},
     {'name': 'J. Michael Lunsford Middle',
      'address': '26020 Ticonderoga Road, Chantilly, VA 20152',
      'phone': '703-722-2660',
      'principal': 'Neil Slevin',
      'grades': '6-8',
      'division': 'Loudoun County Public Schools'},
     {'name': 'J.A. Chalkley Elementary',
      'address': '8800 Jacobs Rd, Chesterfield, VA 23832-7517',
      'phone': '804-674-1300',
      'principal': 'Myla Burgess',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'J.B. Fisher Elementary',
      'address': '3701 Garden Rd, Richmond, VA 23235-1299',
      'phone': '804-327-5612',
      'principal': 'Mrs. Charlene S. Brooks',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'J.B. Watkins Elementary',
      'address': '501 Coalfield Rd., Midlothian, VA 23114-4406',
      'phone': '804-378-2530',
      'principal': 'Dr. Marlene Scott',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'J.E.B. Stuart Elementary',
      'address': '100 Pleasants Lane, Petersburg, VA 23803',
      'phone': '804-862-7013',
      'principal': 'Ms. Dominique Bourgeios',
      'grades': 'PK-5',
      'division': 'Petersburg Public Schools'},
     {'name': 'J.E.B. Stuart Elementary',
      'address': '3101 Fendall Ave, Richmond, VA 23222-2699',
      'phone': '804-780-4879',
      'principal': 'Mrs. Jennifer K. Moore',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'J.E.J. Moore Middle',
      'address': '11455 Prince George Dr, Disputanta, VA 23842',
      'phone': '804-733-2740',
      'principal': 'Mr. Willie Elliott',
      'grades': '6-7',
      'division': 'Prince George County Public Schools'},
     {'name': 'J.G. Hening Elementary',
      'address': '5230 Chicora Dr., Richmond, VA 23234-4608',
      'phone': '804-743-3655',
      'principal': 'Deia Champ',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'J.I. Burton High',
      'address': '109 11th St, Norton, VA 24273',
      'phone': '276-679-2554',
      'principal': 'Mr. Aaron Williams',
      'grades': '8-12',
      'division': 'Norton Public Schools'},
     {'name': 'J.L. Francis Elementary',
      'address': '5146 Snead Rd, Richmond, VA 23224-6092',
      'phone': '804-745-3702',
      'principal': 'Mrs. Daisy D. Greene',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'J.M. Bevins Elementary',
      'address': '8668 Slate Creek Road, Grundy, VA 24614',
      'phone': '276-259-7202',
      'principal': 'Mr. Jeremy Ratliff',
      'grades': 'PK-5',
      'division': 'Buchanan County Public Schools'},
     {'name': 'J.M. Dozier Middle',
      'address': '432 Industrial Park Dr, Newport News, VA 23608',
      'phone': '757-888-3300',
      'principal': 'Ms. Lisa Gatz',
      'grades': '6-8',
      'division': 'Newport News Public Schools'},
     {'name': 'J.W. Adams Combined',
      'address': '10824 Orby Cantrell Hwy, Pound, VA 24279',
      'phone': '276-796-5419',
      'principal': 'Rick Bolling',
      'grades': 'PK-8',
      'division': 'Wise County Public Schools'},
     {'name': 'J.W. Alvey Elementary',
      'address': '5300 Waverly Farm Dr., Haymarket, VA 20169',
      'phone': '571-261-2556',
      'principal': 'Candace Ann Rotruck',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Jack Jouett Middle',
      'address': '210 Lambs Lane, Charlottesville, VA 22901-8979',
      'phone': '434-975-9320',
      'principal': 'Ms. Kathryn Baylor',
      'grades': '6-8',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Jackson Davis Elementary',
      'address': '8801 Nesslewood Dr, Richmond, VA 23229',
      'phone': '804-527-4620',
      'principal': 'Ms. Christine H. Stallings',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Jackson Memorial Elementary',
      'address': '4424 Fort Chiswell Road, Austinville, VA 24312',
      'phone': '276-699-0160',
      'principal': 'Mrs. Tammy J. Watson',
      'grades': 'PK-5',
      'division': 'Wythe County Public Schools'},
     {'name': 'Jackson Middle',
      'address': '3020 Gallows Rd, Falls Church, VA 22042',
      'phone': '703-204-8100',
      'principal': ' ',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Jackson P. Burley Middle',
      'address': '901 Rose Hill Drive, Charlottesville, VA 22903-5255',
      'phone': '434-295-5101',
      'principal': 'Jim Asher',
      'grades': '6-8',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Jackson-Via Elementary',
      'address': '508 Harris Road, Charlottesville, VA 22903-4322',
      'phone': '434-245-2416',
      'principal': 'Dr. Tracie A. Daniels',
      'grades': 'PK-4',
      'division': 'Charlottesville Public Schools'},
     {'name': 'Jacob L. Adams Elementary',
      'address': '600 S Laburnum Ave, Richmond, VA 23223',
      'phone': '804-226-8745',
      'principal': 'Dr. William R. Hall',
      'grades': 'PK-5',
      'division': 'Henrico County Public Schools'},
     {'name': 'Jacobs Road Elementary',
      'address': '8800 Jacobs Rd., Chesterfield, VA 23832-7517',
      'phone': '804-674-1320',
      'principal': 'Eileen Traveline',
      'grades': 'PK-5',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'Jacox Elementary School',
      'address': '1300 Marshall Ave, Norfolk, VA 23504',
      'phone': '757-628-2433',
      'principal': 'Dr. Sherri Archer',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'James G. Brumfield Elementary',
      'address': '550 Alwington Blvd, Warrenton, VA 20186',
      'phone': '540-347-6180',
      'principal': 'Julie Gagnon',
      'grades': 'PK-5',
      'division': 'Fauquier County Public Schools'},
     {'name': 'James Hurst Elementary',
      'address': '18 Dahlgren Ave, Portsmouth, VA 23702-2820',
      'phone': '757-558-2811',
      'principal': 'Mrs. Evelyn L. Whitley',
      'grades': 'KG-6',
      'division': 'Portsmouth Public Schools'},
     {'name': 'James K. Polk Elementary',
      'address': '5000 Polk Ave, Alexandria, VA 22304',
      'phone': '703-461-4180',
      'principal': 'Mrs. PreAnn Johnson',
      'grades': 'KG-5',
      'division': 'Alexandria Public Schools'},
     {'name': 'James Madison Middle',
      'address': '1160 Overland Rd SW, Roanoke, VA 24015',
      'phone': '540-853-2351',
      'principal': 'Ms. Stephanie Hogan',
      'grades': '6-8',
      'division': 'Roanoke Public Schools'},
     {'name': 'James Monroe Elementary',
      'address': '520 W 29th St, Norfolk, VA 23508',
      'phone': '757-628-3500',
      'principal': 'Ms. Celeste Jones',
      'grades': 'PK-5',
      'division': 'Norfolk Public Schools'},
     {'name': 'James Monroe High',
      'address': '2300 Washington Ave, Fredericksburg, VA 22401-3340',
      'phone': '540-372-1100',
      'principal': 'Dr. John B. Gordon III',
      'grades': '9-12',
      'division': 'Fredericksburg Public Schools'},
     {'name': 'James River Elementary',
      'address': '8901 Pocahontas Trail, Williamsburg, VA 23185',
      'phone': '757-887-1768',
      'principal': 'Stacia Barreau',
      'grades': 'KG-5',
      'division': 'Williamsburg-James City County Public Schools'},
     {'name': 'James River High',
      'address': '9906 Springwood Rd, Buchanan, VA 24066',
      'phone': '540-254-1121',
      'principal': 'Mr. James M. Talbott Jr.',
      'grades': '9-12',
      'division': 'Botetourt County Public Schools'},
     {'name': 'James River High',
      'address': '3700 James River Rd., Midlothian, VA 23113',
      'phone': '804-378-2420',
      'principal': 'Jeffery Ellick',
      'grades': '9-12',
      'division': 'Chesterfield County Public Schools'},
     {'name': 'James S. Russell Middle',
      'address': '19400 Christanna Hwy, Lawrenceville, VA 23868',
      'phone': '434-848-2132',
      'principal': 'Dr. Mark A. Harrison Sr.',
      'grades': '6-8',
      'division': 'Brunswick County Public Schools'},
     {'name': 'James Wood High',
      'address': '161 Apple Pie Ridge Rd, Winchester, VA 22603',
      'phone': '540-667-5226',
      'principal': 'Mr. Joseph M. Salyer',
      'grades': '9-12',
      'division': 'Frederick County Public Schools'},
     {'name': 'James Wood Middle',
      'address': '1313 Amherst Street, Winchester, VA 22601',
      'phone': '540-667-7500',
      'principal': 'Mr. Grant C. Javersak',
      'grades': '6-8',
      'division': 'Frederick County Public Schools'},
     {'name': 'Jamestown Elementary',
      'address': '3700 N Delaware St, Arlington, VA 22207',
      'phone': '703-228-5275',
      'principal': 'Ms. Kenwyn Schaffner',
      'grades': 'PK-5',
      'division': 'Arlington County Public Schools'},
     {'name': 'Jamestown High',
      'address': '3751 John Tyler Hwy, Williamsburg, VA 23135',
      'phone': '757-259-3600',
      'principal': 'Cathy Worley',
      'grades': '9-12',
      'division': 'Williamsburg-James City County Public Schools'},
     {'name': 'Jane H. Bryan Elementary',
      'address': '1021 N Mallory St, Hampton, VA 23663',
      'phone': '757-727-1056',
      'principal': 'Mr. Michael W. Stutt',
      'grades': 'PK-5',
      'division': 'Hampton Public Schools'},
     {'name': 'Jefferson Davis Middle',
      'address': '1435 Todds Ln, Hampton, VA 23666',
      'phone': '757-825-4520',
      'principal': 'Ms. Elizabeth A. Winebarger',
      'grades': '6-8',
      'division': 'Hampton Public Schools'},
     {'name': 'Jefferson Forest High',
      'address': '1 Cavalier Circle, Forest, VA 24551',
      'phone': '434-525-2674',
      'principal': 'Mr. Anthony H. Francis',
      'grades': '9-12',
      'division': 'Bedford County Public Schools'},
     {'name': 'Jefferson Middle',
      'address': '125 S Old Glebe Rd, Arlington, VA 22204',
      'phone': '703-228-5900',
      'principal': 'Ms. Keisha Boggan',
      'grades': '6-8',
      'division': 'Arlington County Public Schools'},
     {'name': 'Jefferson-Houston Elementary',
      'address': '1501 Cameron St, Alexandria, VA 22314',
      'phone': '703-706-4400',
      'principal': 'Rosalyn Rice-Harris',
      'grades': 'PK-8',
      'division': 'Alexandria Public Schools'},
     {'name': 'Jennie Dean Elementary',
      'address': '9601 Prince William St, Manassas, VA 20110-4195',
      'phone': '571-377-6300',
      'principal': 'Dr. Robin Toogood II',
      'grades': 'PK-4',
      'division': 'Manassas Public Schools'},
     {'name': 'Jeter-Watson Intermediate',
      'address': '560 West Indian Valley Road, Covington, VA 24426',
      'phone': '540-965-1430',
      'principal': 'Mr. Marc W. Smith',
      'grades': '4-7',
      'division': 'Covington Public Schools'},
     {'name': 'JM Langston Focus School',
      'address': '228 Cleveland Street, Danville, VA 24541',
      'phone': '434-799-5249',
      'principal': 'Ms. Jocelyn Fitzgerald',
      'grades': '9-12',
      'division': 'Danville Public Schools'},
     {'name': 'John Adams Elementary',
      'address': '5651 Rayburn Ave, Alexandria, VA 22311',
      'phone': '703-824-6970',
      'principal': 'Lakisha Covert',
      'grades': 'PK-5',
      'division': 'Alexandria Public Schools'},
     {'name': 'John B. Cary Elementary',
      'address': '2009 Andrews Blvd, Hampton, VA 23663',
      'phone': '757-850-5092',
      'principal': 'Ms. Heidi R. Brezinski',
      'grades': 'PK-5',
      'division': 'Hampton Public Schools'},
     {'name': 'John B. Cary Elementary',
      'address': '3021 Maplewood Ave, Richmond, VA 23221-3587',
      'phone': '804-780-6252',
      'principal': 'Ms. Brenda Phillips',
      'grades': 'PK-5',
      'division': 'Richmond Public Schools'},
     {'name': 'John B. Dey Elementary',
      'address': '1900 N Great Neck Road, Virginia Beach, VA 23454',
      'phone': '757-648-2440',
      'principal': 'Elizabeth Bianchi',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'John C. Myers Elementary',
      'address': '290 Raider Rd, Broadway, VA 22815',
      'phone': '540-896-2297',
      'principal': 'Mrs. Rebecca Roadcap',
      'grades': 'PK-5',
      'division': 'Rockingham County Public Schools'},
     {'name': 'John Champe High School',
      'address': '41535 Sacred Mountain Street, Aldie, VA 20105',
      'phone': '703-722-2680',
      'principal': 'John Gabriel',
      'grades': '9-12',
      'division': 'Loudoun County Public Schools'},
     {'name': 'John F. Kennedy Middle',
      'address': '2325 E Washington St, Suffolk, VA 23434',
      'phone': '757-934-6212',
      'principal': 'Ms. Vivian P. Covington',
      'grades': '6-8',
      'division': 'Suffolk Public Schools'},
     {'name': 'John F. Pattie Sr. Elementary',
      'address': '16125 Dumfries Road, Dumfries, VA 22025',
      'phone': '703-670-3173',
      'principal': 'Ms. Margaret Otterblad',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'John Handley High',
      'address': '425 Handley Blvd, Winchester, VA 22601',
      'phone': '540-662-3471',
      'principal': 'Dr. Jesse Dingle',
      'grades': '9-12',
      'division': 'Winchester Public Schools'},
     {'name': 'John J. Wright Educational And Cultural Center',
      'address': '7565 Courthouse Road, Spotsylvania, VA 22553',
      'phone': '540-834-2556',
      'principal': 'Terecia R. Gill',
      'grades': '',
      'division': 'Spotsylvania County Public Schools'},
     {'name': 'John Kerr Elementary',
      'address': '536 Jefferson Street, Winchester, VA 22601',
      'phone': '540-662-3945',
      'principal': 'Dr. Nan Bryant',
      'grades': 'KG-4',
      'division': 'Winchester Public Schools'},
     {'name': 'John L. Hurt Elementary',
      'address': '315 Prospect Rd, Hurt, VA 24563',
      'phone': '434-324-7231',
      'principal': 'Mrs. Vickie S. Murphy',
      'grades': 'PK-5',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'John M. Gandy Elementary',
      'address': '201 Archie Cannon Drive, Ashland, VA 23005',
      'phone': '804-365-4640',
      'principal': 'Ms. Leigh D. Finch',
      'grades': '3-5',
      'division': 'Hanover County Public Schools'},
     {'name': 'John Marshall Early Childhood Center',
      'address': '743 24th Street, Newport News, VA 23607',
      'phone': '757-928-6832',
      'principal': 'Ms. Vanessa Keller',
      'grades': 'PK',
      'division': 'Newport News Public Schools'},
     {'name': 'John Marshall High',
      'address': '4225 Old Brook Rd, Richmond, VA 23227-3898',
      'phone': '804-780-6052',
      'principal': 'Mrs. Beverly Britt',
      'grades': '9-12',
      'division': 'Richmond Public Schools'},
     {'name': 'John N. Dalton Intermediate',
      'address': '60 Dalton Dr, Radford, VA 24141',
      'phone': '540-731-3651',
      'principal': 'Mr. Gregory Payne',
      'grades': '7-8',
      'division': 'Radford Public Schools'},
     {'name': 'John Randolph Tucker High',
      'address': '2910 Parham Rd, Richmond, VA 23294',
      'phone': '804-527-4600',
      'principal': 'Dr. Robert C. Lowerre',
      'grades': '9-12',
      'division': 'Henrico County Public Schools'},
     {'name': 'John Redd Smith Elementary',
      'address': '40 School Dr, Collinsville, VA 24078',
      'phone': '276-647-7676',
      'principal': 'Mr. Benjamin D Boone',
      'grades': '3-5',
      'division': 'Henry County Public Schools'},
     {'name': 'John Rolfe Middle',
      'address': '6901 Messer Rd, Richmond, VA 23231',
      'phone': '804-226-8730',
      'principal': 'Mr. Michael A. Jackson',
      'grades': '6-8',
      'division': 'Henrico County Public Schools'},
     {'name': 'John S. Battle High',
      'address': '21264 Battle Hill Dr, Bristol, VA 24202',
      'phone': '276-642-5300',
      'principal': 'Mr. Jeff Hawkins',
      'grades': '9-12',
      'division': 'Washington County Public Schools'},
     {'name': 'John Tyler Elementary',
      'address': '57 Salina St, Hampton, VA 23669',
      'phone': '757-727-1075',
      'principal': 'Ms. Adriane V Bradley-Gray',
      'grades': 'PK-5',
      'division': 'Hampton Public Schools'},
     {'name': 'John Tyler Elementary',
      'address': '3649 Hartford St, Portsmouth, VA 23707-1205',
      'phone': '757-393-8879',
      'principal': 'Dr. Jamill Jones',
      'grades': 'KG-6',
      'division': 'Portsmouth Public Schools'},
     {'name': 'John W. Tolbert Jr. Elementary',
      'address': '691 Potomac Station Dr NE, Leesburg, VA 20176',
      'phone': '571-252-2870',
      'principal': 'Ms. Elaine Layman',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'John W. Wayland Elementary',
      'address': '801 North Main St, Bridgewater, VA 22812',
      'phone': '540-828-6081',
      'principal': 'Dr. David W. Burchfield',
      'grades': 'PK-5',
      'division': 'Rockingham County Public Schools'},
     {'name': 'John Yeates Middle',
      'address': '4901 Bennetts Pasture Rd, Suffolk, VA 23435',
      'phone': '757-923-4105',
      'principal': "Mr. Daniel O'Leary",
      'grades': '6-8',
      'division': 'Suffolk Public Schools'},
     {'name': 'Johnson Elementary',
      'address': '1645 Cherry Avenue, Charlottesville, VA 22903-3704',
      'phone': '434-245-2417',
      'principal': 'Mr. Peter Stern',
      'grades': 'PK-4',
      'division': 'Charlottesville Public Schools'},
     {'name': 'Johnson-Williams Middle',
      'address': '200 Swan Ave, Berryville, VA 22611',
      'phone': '540-955-6160',
      'principal': 'Mr. Evan Robb',
      'grades': '6-8',
      'division': 'Clarke County Public Schools'},
     {'name': 'Jolliff Middle',
      'address': '1021 Jolliff Rd., Chesapeake, VA 23321',
      'phone': '757-465-5246',
      'principal': 'Quentin E. Hicks',
      'grades': '6-8',
      'division': 'Chesapeake Public Schools'},
     {'name': 'Jonesville Middle',
      'address': '160 Bulldog Circle, Jonesville, VA 24263',
      'phone': '276-346-1011',
      'principal': 'Dr. Lynn B. Metcalfe',
      'grades': '6-8',
      'division': 'Lee County Public Schools'},
     {'name': 'Joseph B. Johnson Learning Center',
      'address': '9051 Tudor Ln, Manassas, VA 20110-5724',
      'phone': '571-377-7250',
      'principal': ' ',
      'grades': '',
      'division': 'Manassas Public Schools'},
     {'name': 'Joseph H. Saunders Elementary',
      'address': '853 Harpersville Rd, Newport News, VA 23601',
      'phone': '757-591-4781',
      'principal': 'Mr. Timothy Edwards',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'Joseph P. King Jr. Middle',
      'address': '501 Charles Street, Franklin, VA 23851',
      'phone': '757-562-4631',
      'principal': 'Ms. Lisa Francis',
      'grades': '6-8',
      'division': 'Franklin Public Schools'},
     {'name': 'Joseph T. Henley Middle',
      'address': '5880 Rockfish Gap Turnpike, Crozet, VA 22932-3401',
      'phone': '434-823-4393',
      'principal': 'Mr. Patrick McLaughlin',
      'grades': '6-8',
      'division': 'Albemarle County Public Schools'},
     {'name': 'Joseph Van Pelt Elementary',
      'address': '200 Spring Hill Terrace, Bristol, VA 24201',
      'phone': '276-821-5770',
      'principal': 'Mr. Steven Bonney',
      'grades': 'PK-5',
      'division': 'Bristol Public Schools'},
     {'name': 'Jouett Elementary',
      'address': '315 Jouett School Rd, Mineral, VA 23117',
      'phone': '540-872-3931',
      'principal': 'Mike Pelloni',
      'grades': 'PK-5',
      'division': 'Louisa County Public Schools'},
     {'name': 'Kate Collins Middle',
      'address': '1625 Ivy St, Waynesboro, VA 22980',
      'phone': '540-946-4635',
      'principal': 'Janet Buchheit',
      'grades': '6-8',
      'division': 'Waynesboro Public Schools'},
     {'name': 'Kate Waller Barrett Elementary',
      'address': '150 Duffey Dr., Stafford, VA 22554',
      'phone': '540-658-6464',
      'principal': 'Ms. Kimberly J. Austin',
      'grades': 'PK-5',
      'division': 'Stafford County Public Schools'},
     {'name': 'Kecoughtan High',
      'address': '522 Woodland Rd, Hampton, VA 23669',
      'phone': '757-850-5000',
      'principal': 'Mr. Raymond L. Haynes',
      'grades': '9-12',
      'division': 'Hampton Public Schools'},
     {'name': 'Keene Mill Elementary',
      'address': '6310 Bardu Ave, Springfield, VA 22152',
      'phone': '703-644-4700',
      'principal': 'Ms. Renee C. Miller',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Kegotank Elementary',
      'address': '13300 Lankford Highway, Mappsville, VA 23407',
      'phone': '757-824-4756',
      'principal': 'Mrs. Jennifer Annis',
      'grades': 'PK-5',
      'division': 'Accomack County Public Schools'},
     {'name': 'Keister Elementary',
      'address': '100 Maryland Avenue, Harrisonburg, VA 22801',
      'phone': '540-434-6585',
      'principal': 'Mrs. Anne L. B. Lintner',
      'grades': 'KG-4',
      'division': 'Harrisonburg Public Schools'},
     {'name': 'Kemps Landing Magnet',
      'address': '4722 Jericho Rd, Virginia Beach, VA 23462-2226',
      'phone': '757-648-4650',
      'principal': 'Charles Foster',
      'grades': '6-8',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Kempsville Elementary',
      'address': '570 Kempsville Rd, Virginia Beach, VA 23464',
      'phone': '757-648-2720',
      'principal': 'Lori Hasher',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Kempsville High',
      'address': '5194 Chief Trail, Virginia Beach, VA 23464-2796',
      'phone': '757-648-5450',
      'principal': 'Mr. William W. Harris',
      'grades': '9-12',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Kempsville Meadows Elementary',
      'address': '736 Edwin Dr, Virginia Beach, VA 23462-6410',
      'phone': '757-474-8435',
      'principal': 'Mr. Douglas S. Daughtry',
      'grades': 'PK-5',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Kempsville Middle',
      'address': '860 Churchill Dr, Virginia Beach, VA 23464-2905',
      'phone': '757-648-4700',
      'principal': 'Ms. Patti Jenkins',
      'grades': '6-8',
      'division': 'Virginia Beach Public Schools'},
     {'name': 'Kenbridge Elementary',
      'address': '215 Nottoway Falls Rd, Kenbridge, VA 23944-0907',
      'phone': '434-676-2491',
      'principal': 'Mr. John Long',
      'grades': 'PK-5',
      'division': 'Lunenburg County Public Schools'},
     {'name': 'Kenmore Middle',
      'address': '200 S Carlin Springs Rd, Arlington, VA 22204',
      'phone': '703-228-6800',
      'principal': 'Dr. John A. Word',
      'grades': '6-8',
      'division': 'Arlington County Public Schools'},
     {'name': 'Kenneth W.Culbert Elementary',
      'address': '38180 West Colonial Highway, Hamilton, VA 20158',
      'phone': '540-751-2540',
      'principal': 'Mrs. Jacquelyn L. Brownell',
      'grades': 'PK-5',
      'division': 'Loudoun County Public Schools'},
     {'name': 'Kent Gardens Elementary',
      'address': '1717 Melbourne Dr, Mclean, VA 22101',
      'phone': '703-394-5600',
      'principal': 'Ms. Holly S. McGuigan',
      'grades': 'PK-6',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Kentuck Elementary',
      'address': '100 Kentuck Elementary Cir, Ringgold, VA 24586',
      'phone': '434-822-5944',
      'principal': 'Ms. Pamela J. Fields',
      'grades': 'PK-5',
      'division': 'Pittsylvania County Public Schools'},
     {'name': 'Kerrydale Elementary',
      'address': '13199 Kerrydale Rd, Woodbridge, VA 22193',
      'phone': '703-590-1262',
      'principal': 'Anthony Leonard',
      'grades': 'PK-5',
      'division': 'Prince William County Public Schools'},
     {'name': 'Kersey Creek Elementary',
      'address': '10004 Learning Lane, Mechanicsville, VA 23116',
      'phone': '804-723-3440',
      'principal': 'Dr. Deborah Waters',
      'grades': 'PK-5',
      'division': 'Hanover County Public Schools'},
     {'name': 'Kettle Run High',
      'address': '7403 Academic Avenue, Nokesville, VA 20181',
      'phone': '540-422-7330',
      'principal': 'Mr. Major Warner',
      'grades': '9-12',
      'division': 'Fauquier County Public Schools'},
     {'name': 'Key Center School',
      'address': '6404 Franconia Rd, Springfield, VA 22150',
      'phone': '703-313-4000',
      'principal': 'Ms. Ann M Smith',
      'grades': 'PK-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Key Middle',
      'address': '6402 Franconia Rd, Springfield, VA 22150',
      'phone': '703-313-3900',
      'principal': 'Mr. Christopher S. Larrick',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Kilby Shores Elementary',
      'address': '111 Kilby Shores Dr, Suffolk, VA 23434',
      'phone': '757-934-6214',
      'principal': 'Mrs. Lori Mounie',
      'grades': 'PK-5',
      'division': 'Suffolk Public Schools'},
     {'name': 'Kilmer Center',
      'address': '8102 Wolftrap Rd, Vienna, VA 22182',
      'phone': '571-226-8440',
      'principal': 'Mr. MIchael J. Romanelli',
      'grades': 'PK-12',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Kilmer Middle',
      'address': '8100 Wolftrap Rd, Vienna, VA 22182',
      'phone': '703-846-8800',
      'principal': 'Mr. Ronald James',
      'grades': '7-8',
      'division': 'Fairfax County Public Schools'},
     {'name': 'Kiln Creek Elementary',
      'address': '1501 Kiln Creek Pkwy, Newport News, VA 23602',
      'phone': '757-886-7961',
      'principal': 'Ms. Deborah Pack',
      'grades': 'PK-5',
      'division': 'Newport News Public Schools'},
     {'name': 'King & Queen Elementary',
      'address': '24667 The Trail, Mattaponi, VA 23110',
      'phone': '804-785-5830',
      'principal': 'Dr. Carol B. Carter /td><td>PK-7',
      'grades': 'King and Queen County Public Schools',
      'division': ''},
     {'name': 'King George Elementary',
      'address': '10381 Ridge Road, King George, VA 22485',
      'phone': '540-775-5411',
      'principal': 'Mr. Ronald Monroe',
      'grades': 'KG-6',
      'division': 'King George County Public Schools'},
     {'name': 'King George High',
      'address': '10100 Foxes Way, King George, VA 22485',
      'phone': '540-775-3535',
      'principal': 'Mr. Clifton Conway II',
      'grades': '9-12',
      'division': 'King George County Public Schools'},
     ...]



### importing data from API open dataset


```python
pip install opendatasets
```

    Collecting opendatasets
      Downloading opendatasets-0.1.22-py3-none-any.whl.metadata (9.2 kB)
    Requirement already satisfied: tqdm in c:\users\cyndi\anaconda3\lib\site-packages (from opendatasets) (4.66.5)
    Collecting kaggle (from opendatasets)
      Downloading kaggle-1.7.4.2-py3-none-any.whl.metadata (16 kB)
    Requirement already satisfied: click in c:\users\cyndi\anaconda3\lib\site-packages (from opendatasets) (8.1.7)
    Requirement already satisfied: colorama in c:\users\cyndi\anaconda3\lib\site-packages (from click->opendatasets) (0.4.6)
    Requirement already satisfied: bleach in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (4.1.0)
    Requirement already satisfied: certifi>=14.05.14 in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (2025.4.26)
    Requirement already satisfied: charset-normalizer in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (3.3.2)
    Requirement already satisfied: idna in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (3.7)
    Requirement already satisfied: protobuf in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (4.25.3)
    Requirement already satisfied: python-dateutil>=2.5.3 in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (2.9.0.post0)
    Requirement already satisfied: python-slugify in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (5.0.2)
    Requirement already satisfied: requests in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (2.32.3)
    Requirement already satisfied: setuptools>=21.0.0 in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (75.1.0)
    Requirement already satisfied: six>=1.10 in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (1.16.0)
    Requirement already satisfied: text-unidecode in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (1.3)
    Requirement already satisfied: urllib3>=1.15.1 in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (2.2.3)
    Requirement already satisfied: webencodings in c:\users\cyndi\anaconda3\lib\site-packages (from kaggle->opendatasets) (0.5.1)
    Requirement already satisfied: packaging in c:\users\cyndi\anaconda3\lib\site-packages (from bleach->kaggle->opendatasets) (24.1)
    Downloading opendatasets-0.1.22-py3-none-any.whl (15 kB)
    Downloading kaggle-1.7.4.2-py3-none-any.whl (173 kB)
    Installing collected packages: kaggle, opendatasets
    Successfully installed kaggle-1.7.4.2 opendatasets-0.1.22
    Note: you may need to restart the kernel to use updated packages.
    


```python
#loading data from open dataset with API
import opendatasets as od
opendata = 'https://www.kaggle.com/datasets/aditya0kumar0tiwari/play-badminton'
od.download('https://www.kaggle.com/datasets/aditya0kumar0tiwari/play-badminton', force =True)
```

    Dataset URL: https://www.kaggle.com/datasets/aditya0kumar0tiwari/play-badminton
    Downloading play-badminton.zip to .\play-badminton
    

    100%|██████████| 399/399 [00:00<00:00, 199kB/s]

    
    

    
    

### importing data from HTML webpage


```python
#checking the reponse from the website
import requests
import pandas as pd
from bs4 import BeautifulSoup
url = 'https://afd.calpoly.edu/web/sample-tables'
resp = requests.get(url)
resp
```




    <Response [200]>




```python
tables = pd.io.html.read_html(url)
tables
```




    [                                         Description  \
     0                            Academic Senate Meeting   
     1                               Commencement Meeting   
     2                                     Dean's Council   
     3                            Committee on Committees   
     4  Lorem ipsum dolor sit amet, consectetuer adipi...   
     5                                  Lorem ipsum dolor   
     
                                                     Date  \
     0                                       May 25, 2205   
     1                                  December 15, 2205   
     2                                   February 1, 2206   
     3                                      March 3, 2206   
     4  Lorem ipsum dolor sit amet, consectetuer adipi...   
     5                                  Lorem ipsum dolor   
     
                                                 Location  
     0                                 Building 99 Room 1  
     1                                Building 42 Room 10  
     2                                 Building 35 Room 5  
     3                                Building 1 Room 201  
     4  Lorem ipsum dolor sit amet, consectetuer adipi...  
     5                                  Lorem ipsum dolor  ,
             Name Telephone              Email  Office
     0  Dr. Sally  555-1234  sally@calpoly.edu   12-34
     1  Dr. Steve  555-5678  steve@calpoly.edu   56-78
     2  Dr. Kathy  555-9012  kathy@calpoly.edu  90-123,
       Instructor            Class            Location
     0  Dr. Sally      Surgery 101   Building 2 Room 3
     1  Dr. Steve    Radiology 101   Building 2 Room 5
     2  Dr. Kathy  Orthopedics 101  Building 2 Room 20,
                                             Aligned Left  \
     0                            Academic Senate Meeting   
     1                               Commencement Meeting   
     2  Lorem ipsum dolor sit amet, consectetuer adipi...   
     3                                  Lorem ipsum dolor   
     
                                           Aligned Center  \
     0                                       May 25, 2205   
     1                                  December 15, 2205   
     2  Lorem ipsum dolor sit amet, consectetuer adipi...   
     3                                  Lorem ipsum dolor   
     
                                            Aligned Right  
     0                                 Building 99 Room 1  
     1                                Building 42 Room 10  
     2  Lorem ipsum dolor sit amet, consectetuer adipi...  
     3                                  Lorem ipsum dolor  ,
              Day       Time                               Location
     0  Wednesday     3-6 pm  Cal Poly Campus (follow U-Pick Signs)
     1   Thursday   2:30-5pm              Morro Bay Farmer's Market
     2   Thursday   6:10-9pm           Downtown SLO Farmer's Market
     3   Saturday  8-10:30am     Farmer's Market new Embassy Suites
     4   Saturday   11am-2pm  Cal Poly Campus (follow U-Pick signs),
        NAME OF SYSTEM OR PORTAL CHANNEL  \
     0              Personal Information   
     1              Personal Information   
     2              Personal Information   
     3              Personal Information   
     4               Group Leave Balance   
     5                Leave/CTO Balances   
     6               Faculty Course Info   
     7               Faculty Course Info   
     8               Faculty Course Info   
     9               Faculty Course Info   
     10              Faculty Course Info   
     11              Faculty Course Info   
     12              Enrollment Planning   
     13                      Student Pay   
     14                         PolyData   
     15                         PolyData   
     16                      PolyProfile   
     17                      PolyProfile   
     18                      PolyProfile   
     
                          NAME OF SYSTEM OR ACTIVITY STATUS DURING OUTAGE  \
     0                                     Addresses            View Only   
     1                                         Names            View Only   
     2                                 Phone Numbers            View Only   
     3                            Emergency Contacts            View Only   
     4                          Group Leave Balances            View Only   
     5                        Leave and CTO Balances            View Only   
     6                   Class Search/Browse Catalog                  NaN   
     7                                 Record Grades                  NaN   
     8                           Access Class Roster                  NaN   
     9                                  Student Data                  NaN   
     10                       View My Class Schedule                  NaN   
     11                      View My Weekly Schedule                  NaN   
     12  View Course Catalog and Schedule of Classes                  NaN   
     13                            Timekeeper Access          Unavailable   
     14                                         ????                  NaN   
     15                                          NaN                  NaN   
     16                                          NaN                  NaN   
     17                                          NaN                  NaN   
     18                                          NaN                  NaN   
     
        DATA FROZEN AS OF EXPECTED UP TIME  
     0          1/18/2008     Go live date  
     1          1/18/2008     Go live date  
     2          1/18/2008     Go live date  
     3          1/18/2008     Go live date  
     4         12/31/2007         3/1/2008  
     5         12/31/2007         3/1/2008  
     6                NaN              NaN  
     7                NaN              NaN  
     8                NaN              NaN  
     9                NaN              NaN  
     10               NaN              NaN  
     11               NaN              NaN  
     12               NaN              NaN  
     13         1/18/2008              NaN  
     14               NaN              NaN  
     15               NaN              NaN  
     16               NaN              NaN  
     17               NaN              NaN  
     18               NaN              NaN  ]




```python
tables[0]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Description</th>
      <th>Date</th>
      <th>Location</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Academic Senate Meeting</td>
      <td>May 25, 2205</td>
      <td>Building 99 Room 1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Commencement Meeting</td>
      <td>December 15, 2205</td>
      <td>Building 42 Room 10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Dean's Council</td>
      <td>February 1, 2206</td>
      <td>Building 35 Room 5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Committee on Committees</td>
      <td>March 3, 2206</td>
      <td>Building 1 Room 201</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Lorem ipsum dolor sit amet, consectetuer adipi...</td>
      <td>Lorem ipsum dolor sit amet, consectetuer adipi...</td>
      <td>Lorem ipsum dolor sit amet, consectetuer adipi...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Lorem ipsum dolor</td>
      <td>Lorem ipsum dolor</td>
      <td>Lorem ipsum dolor</td>
    </tr>
  </tbody>
</table>
</div>




```python
tables[1]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Telephone</th>
      <th>Email</th>
      <th>Office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Dr. Sally</td>
      <td>555-1234</td>
      <td>sally@calpoly.edu</td>
      <td>12-34</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Dr. Steve</td>
      <td>555-5678</td>
      <td>steve@calpoly.edu</td>
      <td>56-78</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Dr. Kathy</td>
      <td>555-9012</td>
      <td>kathy@calpoly.edu</td>
      <td>90-123</td>
    </tr>
  </tbody>
</table>
</div>




```python
tables[2]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Instructor</th>
      <th>Class</th>
      <th>Location</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Dr. Sally</td>
      <td>Surgery 101</td>
      <td>Building 2 Room 3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Dr. Steve</td>
      <td>Radiology 101</td>
      <td>Building 2 Room 5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Dr. Kathy</td>
      <td>Orthopedics 101</td>
      <td>Building 2 Room 20</td>
    </tr>
  </tbody>
</table>
</div>




```python
tables[3]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Aligned Left</th>
      <th>Aligned Center</th>
      <th>Aligned Right</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Academic Senate Meeting</td>
      <td>May 25, 2205</td>
      <td>Building 99 Room 1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Commencement Meeting</td>
      <td>December 15, 2205</td>
      <td>Building 42 Room 10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Lorem ipsum dolor sit amet, consectetuer adipi...</td>
      <td>Lorem ipsum dolor sit amet, consectetuer adipi...</td>
      <td>Lorem ipsum dolor sit amet, consectetuer adipi...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Lorem ipsum dolor</td>
      <td>Lorem ipsum dolor</td>
      <td>Lorem ipsum dolor</td>
    </tr>
  </tbody>
</table>
</div>




```python
tables[4]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Day</th>
      <th>Time</th>
      <th>Location</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Wednesday</td>
      <td>3-6 pm</td>
      <td>Cal Poly Campus (follow U-Pick Signs)</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Thursday</td>
      <td>2:30-5pm</td>
      <td>Morro Bay Farmer's Market</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Thursday</td>
      <td>6:10-9pm</td>
      <td>Downtown SLO Farmer's Market</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Saturday</td>
      <td>8-10:30am</td>
      <td>Farmer's Market new Embassy Suites</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Saturday</td>
      <td>11am-2pm</td>
      <td>Cal Poly Campus (follow U-Pick signs)</td>
    </tr>
  </tbody>
</table>
</div>




```python
tables[5]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>NAME OF SYSTEM OR PORTAL CHANNEL</th>
      <th>NAME OF SYSTEM OR ACTIVITY</th>
      <th>STATUS DURING OUTAGE</th>
      <th>DATA FROZEN AS OF</th>
      <th>EXPECTED UP TIME</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Personal Information</td>
      <td>Addresses</td>
      <td>View Only</td>
      <td>1/18/2008</td>
      <td>Go live date</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Personal Information</td>
      <td>Names</td>
      <td>View Only</td>
      <td>1/18/2008</td>
      <td>Go live date</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Personal Information</td>
      <td>Phone Numbers</td>
      <td>View Only</td>
      <td>1/18/2008</td>
      <td>Go live date</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Personal Information</td>
      <td>Emergency Contacts</td>
      <td>View Only</td>
      <td>1/18/2008</td>
      <td>Go live date</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Group Leave Balance</td>
      <td>Group Leave Balances</td>
      <td>View Only</td>
      <td>12/31/2007</td>
      <td>3/1/2008</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Leave/CTO Balances</td>
      <td>Leave and CTO Balances</td>
      <td>View Only</td>
      <td>12/31/2007</td>
      <td>3/1/2008</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Faculty Course Info</td>
      <td>Class Search/Browse Catalog</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Faculty Course Info</td>
      <td>Record Grades</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Faculty Course Info</td>
      <td>Access Class Roster</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Faculty Course Info</td>
      <td>Student Data</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Faculty Course Info</td>
      <td>View My Class Schedule</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Faculty Course Info</td>
      <td>View My Weekly Schedule</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Enrollment Planning</td>
      <td>View Course Catalog and Schedule of Classes</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Student Pay</td>
      <td>Timekeeper Access</td>
      <td>Unavailable</td>
      <td>1/18/2008</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>14</th>
      <td>PolyData</td>
      <td>????</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>15</th>
      <td>PolyData</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>16</th>
      <td>PolyProfile</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>17</th>
      <td>PolyProfile</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>18</th>
      <td>PolyProfile</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
# upload the table from the website to csv file
tables[5].to_csv("webpagetable.csv")
```


```python
# get the raw HTML content as a string
from bs4 import BeautifulSoup
html_text = resp.text
html_text
```




    '<!DOCTYPE html>\r\n<html class="no-js" lang="en" dir="ltr">\r\n\r\n<head>\r\n\t<!--\r\nCal Poly Web Template v2.0.0\r\nCode maintained by\r\nInformation Technology Services\r\nCalifornia Polytechnic State University\r\nSan Luis Obispo, CA 93407\r\n-->\r\n\t<meta charset="UTF-8">\r\n\t<meta http-equiv="X-UA-Compatible" content="IE=Edge">\r\n\t<meta name="viewport" content="width=device-width, initial-scale=1.0"/> \r\n\r\n\t<title>Sample Tables - Web - Cal Poly</title>\n\r\n\t<meta http-equiv="content-language" content="en" />\r\n\t<meta name="language" content="en" />\r\n\t<meta name="msapplication-config" content="none" />\r\n\r\n\t<meta name="codebase" content="AFD-2.0" />\r\n\r\n\r\n\t<meta name="Description" content="As stewards of the University resources, we provide high quality, efficient support and planning services as an integral part of the campus community in support of student learning." />\r\n\t<meta name="Keywords" content="Cal Poly, Administration, AFD, Finance, Police, Budget, Facilities, Fiscal, HR, Risk, Technology, Corporation" />\r\n\t<link rel="stylesheet" href="https://use.typekit.net/asw2aly.css">\r\n\t<link rel="stylesheet" href="/framework/css/app.css">\r\n\t<link rel="stylesheet" href="/framework/fontawesome/v6/css/all.min.css">\r\n\t<link rel="stylesheet" href="/framework/fontawesome/v6/css/v4-shims.css">\r\n\r\n\r\n\t\t<!-- Google Analytics -->\r\n\t<script>\r\n\t(function(i, s, o, g, r, a, m) {\r\n\t\ti[\'GoogleAnalyticsObject\'] = r;\r\n\t\ti[r] = i[r] || function() {\r\n\t\t\t(i[r].q = i[r].q || []).push(arguments)\r\n\t\t}, i[r].l = 1 * new Date();\r\n\t\ta = s.createElement(o),\r\n\t\t\tm = s.getElementsByTagName(o)[0];\r\n\t\ta.async = 1;\r\n\t\ta.src = g;\r\n\t\tm.parentNode.insertBefore(a, m)\r\n\t})(window, document, \'script\', \'https://www.google-analytics.com/analytics.js\', \'ga\');\r\n\r\n\tga(\'create\', \'UA-102181678-1\', \'auto\', \'CP\');\r\n\tga(\'create\', \'UA-31323973-1\', \'auto\', \'AFD\');\r\n\tga(\'require\', \'linkid\', \'linkid.js\');\r\n\tga(\'CP.send\', \'pageview\');\r\n\tga(\'AFD.send\', \'pageview\');\r\n\t</script>\r\n\t<!-- End Google Analytics -->\r\n\r\n\t<!-- Google Tag Manager 1 -->\r\n\t<script>\r\n\t(function(w, d, s, l, i) {\r\n\t\tw[l] = w[l] || [];\r\n\t\tw[l].push({\r\n\t\t\t\'gtm.start\': new Date().getTime(),\r\n\t\t\tevent: \'gtm.js\'\r\n\t\t});\r\n\t\tvar f = d.getElementsByTagName(s)[0],\r\n\t\t\tj = d.createElement(s),\r\n\t\t\tdl = l != \'dataLayer\' ? \'&l=\' + l : \'\';\r\n\t\tj.async = true;\r\n\t\tj.src =\r\n\t\t\t\'https://www.googletagmanager.com/gtm.js?id=\' + i + dl;\r\n\t\tf.parentNode.insertBefore(j, f);\r\n\t})(window, document, \'script\', \'dataLayer1\', \'GTM-P4F3XD3\');\r\n\t</script>\r\n\t<!-- End Google Tag Manager 1 -->\r\n\r\n\t<!-- Google Tag Manager 2 marketing -->\r\n\t<script>\r\n\t(function(w, d, s, l, i) {\r\n\t\tw[l] = w[l] || [];\r\n\t\tw[l].push({\r\n\t\t\t\'gtm.start\': new Date().getTime(),\r\n\t\t\tevent: \'gtm.js\'\r\n\t\t});\r\n\t\tvar f = d.getElementsByTagName(s)[0],\r\n\t\t\tj = d.createElement(s),\r\n\t\t\tdl = l != \'dataLayer\' ? \'&l=\' + l : \'\';\r\n\t\tj.async = true;\r\n\t\tj.src =\r\n\t\t\t\'https://www.googletagmanager.com/gtm.js?id=\' + i + dl;\r\n\t\tf.parentNode.insertBefore(j, f);\r\n\t})(window, document, \'script\', \'dataLayer2\', \'GTM-TKZNRR2\');\r\n\t</script>\r\n\t<!-- End Google Tag Manager 2 marketing -->\r\n\r\n\t\r\n\t<!-- Hotjar Tracking Code for https://afd.calpoly.edu/ -->\r\n\t<script>\r\n\t(function(h, o, t, j, a, r) {\r\n\t\th.hj = h.hj || function() {\r\n\t\t\t(h.hj.q = h.hj.q || []).push(arguments)\r\n\t\t};\r\n\t\th._hjSettings = {\r\n\t\t\thjid: 1763767,\r\n\t\t\thjsv: 6\r\n\t\t};\r\n\t\ta = o.getElementsByTagName(\'head\')[0];\r\n\t\tr = o.createElement(\'script\');\r\n\t\tr.async = 1;\r\n\t\tr.src = t + h._hjSettings.hjid + j + h._hjSettings.hjsv;\r\n\t\ta.appendChild(r);\r\n\t})(window, document, \'https://static.hotjar.com/c/hotjar-\', \'.js?sv=\');\r\n\t</script>\r\n\r\n\t<link rel="apple-touch-icon" sizes="180x180" href="/images/favicon/apple-touch-icon.png">\r\n\t<link rel="icon" type="image/png" sizes="32x32" href="/images/favicon/favicon-32x32.png">\r\n\t<link rel="icon" type="image/png" sizes="16x16" href="/images/favicon/favicon-16x16.png">\r\n\t<link rel="mask-icon" href="/images/favicon/safari-pinned-tab.svg" color="#154734">\r\n\t<meta name="msapplication-TileColor" content="#da532c">\r\n\t<meta name="theme-color" content="#ffffff">\r\n</head>\r\n\r\n<body class="subsite_ants page_default">\r\n\t<!-- Start Facebook -->\r\n\t<div id="fb-root"></div>\r\n\t<script>\r\n\t(function(d, s, id) {\r\n\t\tvar js, fjs = d.getElementsByTagName(s)[0];\r\n\t\tif (d.getElementById(id)) return;\r\n\t\tjs = d.createElement(s);\r\n\t\tjs.id = id;\r\n\t\tjs.src = "//connect.facebook.net/en_US/sdk.js#xfbml=1&version=v2.8&appId=131592030268312";\r\n\t\tfjs.parentNode.insertBefore(js, fjs);\r\n\t}(document, \'script\', \'facebook-jssdk\'));\r\n\t</script>\r\n\t<!-- End Facebook -->\r\n\t<!-- Google Tag Manager (noscript) -->\r\n\t<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P4F3XD3" height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>\r\n\t<!-- End Google Tag Manager (noscript) -->\r\n\t<!-- Google Tag Manager (noscript) Marketing -->\r\n\t<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-TKZNRR2" height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>\r\n\t<!-- End Google Tag Manager (noscript) -->\r\n\t<header>\r\n\t\t<!-- <section class="sitewide-banner" data-closable>\r\n  \t\t\t<button class="close-button" data-close>&times;</button>\r\n\t\t\t<div class="row align-middle">\r\n\t\t\t\t<div class="column small-12 medium-7 ">\r\n\t\t\t\t\t<h3>Coronavirus Information from Administration & Finance</h3>\r\n\t\t\t\t</div>\r\n\t\t\t\t<div class="column small-12 medium-3 medium-offset-2">\r\n\t\t\t\t\t<a href="/coronavirus/" class="button expanded small">Learn More</a>\r\n\t\t\t\t</div>\r\n\t\t\t</div>\r\n\t\t</section> -->\r\n\t\t<section class="cp_header">\r\n\t\t\t<a href="#content" class="skip">Skip to content</a>\r\n\t\t\t<div class="row align-middle align-justify">\r\n\t\t\t\t<div class="columns flex-container">\r\n\t\t\t\t\t<a href="http://www.calpoly.edu/" class="logo">\r\n\t\t\t\t\t\t<img srcset="/framework/images/calpoly-logo-1x.png,\r\n\t\t\t\t\t\t             /framework/images/calpoly-logo-2x.png 2x" src="/framework/images/calpoly-logo-1x.png" alt="Cal Poly Logo and Shield">\r\n\t\t\t\t\t</a>\r\n\t\t\t\t\t<h2 id="sitename" class="sitename align-self-middle"><a href="/">Administration &amp; Finance</a></h2>\r\n\r\n\t\t\t\t</div>\r\n\t\t\t\t<div class="flex-container" data-responsive-toggle="subsite-menu" data-hide-for="medium" style="margin-right:1rem;">\r\n\t\t\t\t\t<a class="" type="button" data-toggle><span class="show-for-sr">menu</span><i class="fas fa-bars"></i></a>\r\n\t\t\t\t\t<!-- <button class="menu-icon" type="button" data-toggle><span class="show-for-sr">menu</span></button> -->\r\n\t\t\t\t</div>\r\n\t\t\t\t<div class="columns search small-12 medium-5">\r\n\t\t\t\t\t<div class="row align-middle align-right">\r\n\t\t\t\t\t\t<div class="shrink column cp-menu small-order-2 medium-order-1">\r\n\t\t\t\t\t\t\t<a href="/services">A&amp;F Services</a>&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://myportal.calpoly.edu">my CalPoly login</a>\r\n\t\t\t\t\t\t</div>\r\n\t\t\t\t\t\t<div class="column small-order-1 medium-order-2">\r\n\t\t\t\t\t\t\t<form method="get" title="Search Form" action="https://www.calpoly.edu/search/?q=">\r\n\t\t\t\t\t\t\t\t<div class="input-group">\r\n\t\t\t\t\t\t\t\t\t<input class="input-group-field" type="text" placeholder="Search Cal Poly" title="Search Cal Poly" name="q">\r\n\t\t\t\t\t\t\t\t\t<div class="input-group-button">\r\n\t\t\t\t\t\t\t\t\t\t<button class="button" type="submit" name="btnG">\r\n\t\t\t\t\t\t\t\t\t\t\t<!-- Screen readers will see "Search" -->\r\n\t\t\t\t\t\t\t\t\t\t\t<span class="show-for-sr">Search</span>\r\n\t\t\t\t\t\t\t\t\t\t\t<!-- Visual users will see the mag glass, but not the "Search" text -->\r\n\t\t\t\t\t\t\t\t\t\t\t<span aria-hidden="true"><i class="fa fa-search"></i></span>\r\n\t\t\t\t\t\t\t\t\t\t</button>\r\n\t\t\t\t\t\t\t\t\t</div>\r\n\t\t\t\t\t\t\t\t</div>\r\n\t\t\t\t\t\t\t</form>\r\n\t\t\t\t\t\t</div>\r\n\t\t\t\t\t</div>\r\n\t\t\t\t</div>\r\n\t\t\t</div>\r\n\t\t</section>\r\n\t\t\t\t\t\t<section class="hero">\r\n\t\t\t<div class="row">\r\n\t\t\t\t<div class="large-12 column">\r\n\t\t\t\t\t<h3>\r\n\t\t\t\t\t\t<div class="mobile-nav-action" data-responsive-toggle="subsite-menu" data-hide-for="medium">\r\n\t\t\t\t\t\t\t<button class="menu-icon" type="button" data-toggle><span class="show-for-sr">menu</span></button>\r\n\t\t\t\t\t\t</div>\r\n\t\t\t\t\t\t<a href="/web/">A&F Web Support</a>\r\n\t\t\t\t\t</h3>\r\n\t\t\t\t</div>\r\n\t\t\t</div>\r\n\t\t</section>\r\n\t\t\t\t\t</header>\r\n\t\t\r\n\t<section class="site-nav">\r\n\t\t<div class="row collapse" id="subsite-menu">\r\n\t\t\t<div class="column">\r\n\t\t\t\t<ul class="vertical medium-horizontal menu">\r\n\t\t\t\t\t<li><a href="https://wiki.calpoly.edu/display/usr/Web+Editing+-+Accessible+Documents">Accessibility</a></li>\r\n\t\t\t\t\t<li><a href="/web/style-guide">Style Guide</a></li>\r\n\t\t\t\t\t<li><a href="mailto:afd-web@calpoly.edu?subject=%5Bwebsite name%5D - %5Bdescriptor%5D">Request Website Changes</a></li>\r\n\t\t\t\t</ul>\r\n\t\t\t</div>\r\n\t\t</div>\r\n\t</section>\r\n\r\n\t\r\n\r\n\t<section class="bread">\n<div class="row">\n<div class="columns">\n<ul class="breadcrumbs">\n<li><a href="/">A&amp;F Home</a></li>\n<li><a href="/web/">Web</a></li>\n<li><span class="show-for-sr">Current: </span>Sample Tables</li>\n</ul>\n</div>\n</div>\n</section>\n<div class="row align-justify">\r\n\t<div class="small-12 medium-8 columns" id="content">\r\n\t\t<a name="topH1"></a>\r\n<!--BEGIN MAIN CONTENT AREA-->\r\n<h1>Sample Page - Data Tables</h1>\r\n      <p><a href="http://warc.calpoly.edu/accessibility/508indepth/rowcolumn.html">For more information on creating accessible data tables see the Accessibility &gt; Row and Column section of the Web Authoring Resource Center</a>.</p>\r\n      <h2>Examples of Accessible Data Tables</h2>\r\n      <p>These example tables contain captions and summaries. When you copy any of these tables into your page you must edit the  caption and summary. The caption can be edited in the Design view but the summary text must be edited in Code view. Click inside the table, then select the table tag on the tag selector, then switch to Code view and edit the text in the summary attribute.      </p>\r\n      <h3><a name="basic" id="basic"></a>Basic Data Table with Column Headings</h3>\r\n      <table border="1" summary="Provide table summary here">\r\n        <caption>\r\n        <strong>Table caption (name and description of table)</strong><br />\r\n        You can describe your table here or in the context of your page.  \r\n        This table is read using the first row as the header for each column.\r\n        (Replace this caption with your own description of the table)\r\n        </caption>\r\n        <tr>\r\n          <th scope="col">Description</th>\r\n          <th scope="col">Date</th>\r\n          <th scope="col"><a href="#">Location</a></th>\r\n        </tr>\r\n        <tr>\r\n          <td> Academic Senate Meeting</td>\r\n          <td>May 25, 2205</td>\r\n          <td>Building 99 Room 1</td>\r\n        </tr>\r\n        <tr class="shade-row">\r\n          <td>Commencement Meeting</td>\r\n          <td>December 15, 2205</td>\r\n          <td>Building 42 Room 10</td>\r\n        </tr>\r\n        <tr>\r\n          <td>Dean\'s Council</td>\r\n          <td>February 1, 2206</td>\r\n          <td>Building 35 Room 5</td>\r\n        </tr>\r\n        <tr class="shade-row">\r\n          <td>Committee on Committees</td>\r\n          <td>March 3, 2206</td>\r\n          <td>Building 1 Room 201</td>\r\n        </tr>\r\n        <tr>\r\n          <td> Lorem ipsum dolor sit amet, <a href="#">consectetuer adipiscing elit</a>. Sed lacus arcu, porta posuere, varius et.</td>\r\n          <td>Lorem <a href="#">ipsum dolor</a> sit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et.</td>\r\n          <td>Lorem <a href="#">ipsum dolor</a> sit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et.</td>\r\n        </tr>\r\n        <tr class="shade-row">\r\n          <td><a href="#">Lorem ipsum dolor</a></td>\r\n          <td><a href="#">Lorem ipsum dolor</a></td>\r\n          <td><a href="#">Lorem ipsum dolor</a></td>\r\n        </tr>\r\n      </table>\r\n      <h3><a name="directory" id="directory"></a>Directory Listing Table - Roll Cursor Over an Item\r\n      </h3>\r\n      <table  border="1" class="table_directory" summary="Provide table summary here" >\r\n        <caption>\r\n        <strong>Directory Listing   (Table caption - name and description of table)</strong><br />\r\n          Apply the &quot;directory&quot; style to the <code>&lt;table&gt;</code> tag to remove the borders and add roll-over styling to rows.\r\n          You can describe  your table here or in the context of your page.\xa0 This table is read using the  first row as the header for each column. (Replace this caption with your  own description of the table)\r\n        </caption>\r\n          <tr>\r\n            <th scope="col">Name</th>\r\n            <th scope="col">Telephone</th>\r\n            <th scope="col">Email</th>\r\n            <th scope="col">Office</th>\r\n          </tr>\r\n          <tr>\r\n            <td>Dr. Sally</td>\r\n            <td>555-1234</td>\r\n            <td>sally@calpoly.edu</td>\r\n            <td>12-34</td>\r\n          </tr>\r\n          <tr>\r\n            <td>Dr. Steve</td>\r\n            <td>555-5678</td>\r\n            <td>steve@calpoly.edu</td>\r\n            <td>56-78</td>\r\n          </tr>\r\n          <tr>\r\n            <td>Dr. Kathy</td>\r\n            <td>555-9012</td>\r\n            <td>kathy@calpoly.edu</td>\r\n            <td>90-123</td>\r\n          </tr>\r\n      </table>\r\n      <h3><a name="columnrow" id="columnrow"></a>Column and Row Headings Example</h3>\r\n      <table border="1"  summary="Provide table summary here">\r\n        <caption>\r\n        <strong>Table caption (name and description of table)</strong><br />\r\n        This table is read using the first row as a column header and then the first item of the first column as a row header.\r\n        (Replace this caption with your own description of the table)\r\n        </caption>\r\n        <tr>\r\n          <th scope="col">Instructor</th>\r\n          <th scope="col">Class</th>\r\n          <th scope="col">Location</th>\r\n        </tr>\r\n        <tr>\r\n          <th scope="row">Dr. Sally</th>\r\n          <td>Surgery 101</td>\r\n          <td>Building 2 Room 3</td>\r\n        </tr>\r\n        <tr>\r\n          <th scope="row">Dr. Steve</th>\r\n          <td><a href="#">Radiology 101</a></td>\r\n          <td><a href="#">Building 2 Room 5</a></td>\r\n        </tr>\r\n        <tr>\r\n          <th scope="row">Dr. Kathy</th>\r\n          <td>Orthopedics 101</td>\r\n          <td>Building 2 Room 20</td>\r\n        </tr>\r\n      </table>\r\n      <h3><a name="aligndata" id="aligndata"></a>Table Data Alignment Styles - Left, Middle, Right </h3>\r\n      <table border="1" summary="Provide table summary here">\r\n        <caption>\r\n          <strong>Table caption (name and description of table)</strong><br />\r\n          This table uses classes center and right to align text or images within a table cell. Default alignment is left. You can describe your table here or in the context of your page.  \r\n          This table is read using the first row as the header for each column.\r\n          (Replace this caption with your own description of the table)\r\n        </caption>\r\n        <tr>\r\n          <th scope="col">Aligned Left</th>\r\n          <th class="table_text_center" scope="col">Aligned Center</th>\r\n          <th class="table_text_right" scope="col">Aligned Right</th>\r\n        </tr>\r\n        <tr>\r\n          <td> Academic Senate Meeting</td>\r\n          <td class="table_text_center">May 25, 2205</td>\r\n          <td class="table_text_right">Building 99 Room 1</td>\r\n        </tr>\r\n        <tr class="shade-row">\r\n          <td>Commencement Meeting</td>\r\n          <td class="table_text_center">December 15, 2205</td>\r\n          <td class="table_text_right">Building 42 Room 10</td>\r\n        </tr>\r\n        <tr>\r\n          <td> Lorem ipsum dolor sit amet, <a href="#">consectetuer adipiscing elit</a>. Sed lacus arcu, porta posuere, varius et.</td>\r\n          <td class="table_text_center">Lorem <a href="#">ipsum dolor</a> sit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et.</td>\r\n          <td class="table_text_right">Lorem <a href="#">ipsum dolor</a> sit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et.</td>\r\n        </tr>\r\n        <tr class="shade-row">\r\n          <td><a href="#">Lorem ipsum dolor</a></td>\r\n          <td class="table_text_center"><a href="#">Lorem ipsum dolor</a></td>\r\n          <td class="table_text_right"><a href="#">Lorem ipsum dolor</a></td>\r\n        </tr>\r\n      </table>\r\n      <h3>Table No Outline - H2</h3>\r\n      <table border="1" class="table_noStyle" summary="Outline Table style">\r\n        <caption>\r\n        <strong>No Style Table Listing    (Table caption - name and description of table)</strong><br />\r\nApply the &quot;table_noStyle&quot; style to the <code>&lt;table&gt;</code> tag to remove the borders\r\n        . You can describe  your table here or in the context of your page.\xa0 This table is read using the  first row as the header for each column. (Replace this caption with your  own description of the table)\r\n        </caption>\r\n        <tbody>\r\n          <tr class="table_greenText">\r\n            <th scope="col" width="30%">Day</th>\r\n            <th scope="col" width="20%">Time</th>\r\n            <th scope="col" width="50%">Location</th>\r\n          </tr>\r\n          <tr>\r\n            <td>Wednesday</td>\r\n            <td>3-6 pm</td>\r\n            <td>Cal Poly Campus (<a href="#">follow U-Pick Signs</a>)</td>\r\n          </tr>\r\n          <tr>\r\n            <td>Thursday</td>\r\n            <td>2:30-5pm</td>\r\n            <td>Morro Bay Farmer\'s Market</td>\r\n          </tr>\r\n          <tr>\r\n            <td>Thursday</td>\r\n            <td>6:10-9pm</td>\r\n            <td>Downtown SLO Farmer\'s Market</td>\r\n          </tr>\r\n          <tr>\r\n            <td>Saturday</td>\r\n            <td>8-10:30am</td>\r\n            <td>Farmer\'s Market new Embassy Suites</td>\r\n          </tr>\r\n          <tr>\r\n            <td>Saturday</td>\r\n            <td>11am-2pm</td>\r\n            <td>Cal Poly Campus (<a href="#">follow U-Pick signs</a>)</td>\r\n          </tr>\r\n        </tbody>\r\n      </table>\r\n      <h3><a name="complex" id="complex"></a>Complex Data Table</h3>\r\n      <table border="1">\r\n        <caption>\r\n        <strong>Table caption (name and description of table)</strong><br />\r\n        This is an example of a <strong>Complex Data table</strong> that associates column headers with <strong>row headers that span multiple rows</strong>. The underlying HTML code of this table belies the necessary associations that make the table readable using a screen reading technology (Replace this caption with your own description of the table)\r\n        </caption>\r\n        <tbody>\r\n          <tr>\r\n            <th id="sname" scope="col"><p>NAME OF SYSTEM OR PORTAL CHANNEL</p></th>\r\n            <th id="activity" scope="col"><p>NAME OF SYSTEM OR ACTIVITY</p></th>\r\n            <th id="status" scope="col"><p>STATUS DURING OUTAGE</p></th>\r\n            <th id="frozen" scope="col"><p>DATA FROZEN AS OF</p></th>\r\n            <th id="exp" scope="col"><p>EXPECTED UP TIME</p></th>\r\n          </tr>\r\n          <tr>\r\n            <th id="pi" headers="sname" rowspan="4" scope="row"><p>Personal Information</p></th>\r\n            <td headers="pi activity"><p>Addresses</p></td>\r\n            <td headers="pi status"><p>View Only</p></td>\r\n            <td headers="pi frozen"><p>1/18/2008</p></td>\r\n            <td headers="pi exp"><p>Go live date</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="pi activity"><p>Names</p></td>\r\n            <td headers="pi status"><p>View Only</p></td>\r\n            <td headers="pi frozen"><p>1/18/2008</p></td>\r\n            <td headers="pi exp"><p>Go live date</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="pi activity"><p>Phone Numbers</p></td>\r\n            <td headers="pi status"><p>View Only</p></td>\r\n            <td headers="pi frozen"><p>1/18/2008</p></td>\r\n            <td headers="pi exp"><p>Go live date</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="pi activity"><p>Emergency Contacts</p></td>\r\n            <td headers="pi status"><p>View Only</p></td>\r\n            <td headers="pi frozen"><p>1/18/2008</p></td>\r\n            <td headers="pi exp"><p>Go live date</p></td>\r\n          </tr>\r\n          <tr>\r\n            <th headers="sname" id="glb" scope="row"><p>Group Leave Balance</p></th>\r\n            <td headers="glb activity"><p>Group Leave Balances</p></td>\r\n            <td headers="glb status"><p>View Only</p></td>\r\n            <td headers="glb frozen"><p>12/31/2007</p></td>\r\n            <td headers="glb exp"><p>3/1/2008</p></td>\r\n          </tr>\r\n          <tr>\r\n            <th headers="sname" id="lcb" scope="row"><p>Leave/CTO Balances</p></th>\r\n            <td headers="lcb activity"><p>Leave and CTO Balances</p></td>\r\n            <td headers="lcb status"><p>View Only</p></td>\r\n            <td headers="lcb frozen"><p>12/31/2007</p></td>\r\n            <td headers="lcb exp"><p>3/1/2008</p></td>\r\n          </tr>\r\n          <tr>\r\n            <th headers="sname" id="fci" rowspan="6" scope="row"><p><a href="#">Faculty Course Info</a></p></th>\r\n            <td headers="fci activity"><p>Class Search/Browse Catalog</p></td>\r\n            <td headers="fci status"><p>&nbsp;</p></td>\r\n            <td headers="fci frozen"><p>&nbsp;</p></td>\r\n            <td headers="fci exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="fci activity"><p>Record Grades</p></td>\r\n            <td headers="fci status"><p>&nbsp;</p></td>\r\n            <td headers="fci frozen"><p>&nbsp;</p></td>\r\n            <td headers="fci exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="fci activity"><p>Access Class Roster</p></td>\r\n            <td headers="fci status"><p>&nbsp;</p></td>\r\n            <td headers="fci frozen"><p>&nbsp;</p></td>\r\n            <td headers="fci exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="fci activity"><p>Student Data</p></td>\r\n            <td headers="fci status"><p>&nbsp;</p></td>\r\n            <td headers="fci frozen"><p>&nbsp;</p></td>\r\n            <td headers="fci exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="fci activity"><p>View My Class Schedule</p></td>\r\n            <td headers="fci status"><p>&nbsp;</p></td>\r\n            <td headers="fci frozen"><p>&nbsp;</p></td>\r\n            <td headers="fci exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="fci activity"><p>View My Weekly Schedule</p></td>\r\n            <td headers="fci status"><p>&nbsp;</p></td>\r\n            <td headers="fci frozen"><p>&nbsp;</p></td>\r\n            <td headers="fci exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <th headers="sname" id="ep" scope="row"><p>Enrollment Planning</p></th>\r\n            <td headers="ep activity"><p>View Course <a href="#">Catalog</a> and Schedule of Classes</p></td>\r\n            <td headers="ep status"><p>&nbsp;</p></td>\r\n            <td headers="ep frozen"><p>&nbsp;</p></td>\r\n            <td headers="ep exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <th headers="sname" id="sp" scope="row"><p>Student Pay</p></th>\r\n            <td headers="sp activity"><p><a href="#">Timekeeper Access</a></p></td>\r\n            <td headers="sp status"><p>Unavailable</p></td>\r\n            <td headers="sp frozen"><p>1/18/2008 </p></td>\r\n            <td headers="sp exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <th headers="sname" id="pd" rowspan="2" scope="row"><p>PolyData</p></th>\r\n            <td headers="pd activity"><p>????</p></td>\r\n            <td headers="pd status"><p>&nbsp;</p></td>\r\n            <td headers="pd frozen"><p>&nbsp;</p></td>\r\n            <td headers="pd exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="pd activity"><p>&nbsp;</p></td>\r\n            <td headers="pd status"><p>&nbsp;</p></td>\r\n            <td headers="pd frozen"><p>&nbsp;</p></td>\r\n            <td headers="pd exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <th headers="sname" id="pp" rowspan="3" scope="row"><p>PolyProfile</p></th>\r\n            <td headers="pp activity"><p>&nbsp;</p></td>\r\n            <td headers="pp status"><p>&nbsp;</p></td>\r\n            <td headers="pp frozen"><p>&nbsp;</p></td>\r\n            <td headers="pp exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="pp activity"><p>&nbsp;</p></td>\r\n            <td headers="pp status"><p>&nbsp;</p></td>\r\n            <td headers="pp frozen"><p>&nbsp;</p></td>\r\n            <td headers="pp exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n          <tr>\r\n            <td headers="pp activity"><p>&nbsp;</p></td>\r\n            <td headers="pp status"><p>&nbsp;</p></td>\r\n            <td headers="pp frozen"><p>&nbsp;</p></td>\r\n            <td headers="pp exp"><p>&nbsp;</p></td>\r\n          </tr>\r\n        </tbody>\r\n      </table>\r\n\r\n</div><!--mainLeft-->\r\n\r\n\t<div id="mainLeftFull">\r\n        <!--END MAIN CONTENT AREA: DO NOT EDIT BELOW-->\r\n\r\n        </div>\r\n        <div class="small-12 medium-4 large-3 columns">\r\n            <div class="side-callout">\t\r\n\r\n\t</div>        </div>\r\n    </div>\r\n    \t<footer>\r\n\t\t<div class="row footer-foot ">\r\n\t\t\t<div class="column small-12 medium-expand">\r\n\t\t\t\t<div class="row">\r\n\t\t\t\t\t<div class="column small-12 footer-content">\r\n\t\t\t\t\t\t<div class="row">\r\n\t\t\t\t\t\t\t<div class="column show-for-medium medium-3 text-center align-self-top">\r\n\t\t\t\t\t\t\t\t<img src="/framework/images/calpoly-logo-vertical-rev-400.png" alt="" width="80%">\r\n\t\t\t\t\t\t\t</div>\r\n\t\t\t\t\t\t\t<div class="column small-12 medium-8 medium-offset-1">\r\n\t\t\t\t\t\t\t\t<h4>AFD Web</h4>\r\n\t\t\t\t\t\t\t\t<p>1 Grand Ave, <a href="http://maps.calpoly.edu/?vlist=058-0">Building 58</a>: Room 107, San Luis Obispo, CA 93407</p>\r\n\t\t\t\t\t\t\t\t<div class="row">\r\n\t\t\t\t\t\t\t\t\t<div class="column small-expand">\r\n\t\t\t\t\t\t\t\t\t\t<ul class="no-bullet">\r\n\t\t\t\t\t\t\t\t\t\t\t<li><strong>Phone:</strong> 805-756-6475</li>\r\n\t\t\t\t\t\t\t\t\t\t\t<li><a href="mailto:afd-web@calpoly.edu">afd-web@calpoly.edu</a></li>\r\n\t\t\t\t\t\t\t\t\t\t</ul>\r\n\t\t\t\t\t\t\t\t\t</div>\r\n\t\t\t\t\t\t\t\t\t<div class="column small-expand">\r\n\t\t\t\t\t\t\t\t\t\t<h5>Office Hours</h5>\r\n\t\t\t\t\t\t\t\t\t\t<ul class="no-bullet">\r\n\t\t\t\t\t\t\t\t\t\t\t<li>Monday — Friday</li>\r\n\t\t\t\t\t\t\t\t\t\t\t<li>7:30 a.m. - 5:00 p.m.</li>\r\n\t\t\t\t\t\t\t\t\t\t</ul>\r\n\t\t\t\t\t\t\t\t\t\t<!-- <h5>Window Hours</h5>\r\n\t\t\t\t\t\t\t\t\t\t<ul class="no-bullet">\r\n\t\t\t\t\t\t\t\t\t\t\t<li>Monday — Friday</li>\r\n\t\t\t\t\t\t\t\t\t\t\t<li>9:00 a.m. - 4:00 p.m.</li>\r\n\t\t\t\t\t\t\t\t\t\t</ul> -->\r\n\t\t\t\t\t\t\t\t\t</div>\r\n\t\t\t\t\t\t\t\t</div>\r\n\t\t\t\t\t\t\t</div>\r\n\t\t\t\t\t\t</div>\r\n\t\t\t\t\t</div>\r\n\t\t\t\t</div>\r\n\t\t\t\t<div class="row align-bottom inside-cp">\r\n\t\t\t\t\t<div class="column small-12 align-self-bottom">\r\n\t\t\t\t\t\t<img src="/framework/images/logo-inside-calpoly.png" alt="Follow A&F at">\r\n\t\t\t\t\t\t<a href="https://www.instagram.com/insidecalpoly/">\r\n\t\t\t\t\t\t\t<span class="show-for-sr">Visit Instagram</span>\r\n\t\t\t\t\t\t\t<span aria-hidden="true"><i class="fab fa-instagram fa-lg"></i></span>\r\n\t\t\t\t\t\t</a>\r\n\t\t\t\t\t\t<a href="https://www.facebook.com/insidecalpoly/">\r\n\t\t\t\t\t\t\t<span class="show-for-sr">Visit Facebook</span>\r\n\t\t\t\t\t\t\t<span aria-hidden="true"><i class="fab fa-facebook fa-lg"></i></span>\r\n\t\t\t\t\t\t</a>\r\n\t\t\t\t\t</div>\r\n\t\t\t\t</div>\r\n\t\t\t</div>\r\n\t\t\t<div class="pop-links">\r\n\t\t\t\t<h5>Popular Links</h5>\r\n\t\t\t\t<ul class="no-bullet">\r\n\t\t\t\t\t<li><a href="https://security.calpoly.edu">Information Security</a></li>\r\n\t\t\t\t\t<li><a href="https://security.calpoly.edu/content/policies/standards/classification/index">Information Classification and Handling Standard</a></li>\r\n\t\t\t\t\t<li><a href="https://wiki.calpoly.edu/x/DouFDw">Password Changes</a></li>\r\n\t\t\t\t\t<li><a href="https://tech.calpoly.edu/services">ITS Service Desk</a></li>\r\n\t\t\t\t</ul>\r\n\t\t\t</div>\r\n\t\t</div>\r\n\t</footer>\t\r\n\r\n\t\r\n\r\n\t<footer class="cp-footer">\r\n\t\t<div class="row align-middle">\r\n\t\t\t<div class="column small-12 medium-2 small-text-center">\r\n\t\t\t\t<a href="http://www.calpoly.edu/">\r\n\t\t\t\t\t<img srcset="/framework/images/calpoly-logo-rev-1x.png,\r\n\t\t\t\t\t\t             /framework/images/calpoly-logo-rev-2x.png 2x" src="/framework/images/calpoly-logo-rev-1x.png" alt="Cal Poly Logo and Shield">\r\n\r\n\r\n\t\t\t\t\t<!-- <img id="logo" title="Go to Cal Poly Home" alt="Cal Poly logo" src="/framework/images/CP_logo_cmyk_rev.svg" width="100%" /> -->\r\n\t\t\t\t</a>\r\n\t\t\t</div>\r\n\r\n\t\t\t<div class="column small-12 medium-8 medium-offset-2">\r\n\t\t\t\t<p>\r\n\t\t\t\t\t&#169; <script>\r\n\t\t\t\t\tdocument.write(new Date().getFullYear())\r\n\t\t\t\t\t</script>\r\n\t\t\t\t\tCalifornia Polytechnic State University — San Luis Obispo, California 93407 — Phone: 805-756-1111\r\n\t\t\t\t</p>\r\n\t\t\t</div>\r\n\t\t</div>\r\n\t\t<div class="row">\r\n\t\t\t<div class="getPlugins column">\r\n\t\t\t\t<ul class="menu simple align-right">\r\n\t\t\t\t\t<li><a href="https://www.calpoly.edu/privacy/">Privacy Notice</a></li>\r\n\t\t\t\t\t<li><a href="https://accessibility.calpoly.edu/website-accessibility-statement">Web Accessibility Statement</a></li>\r\n\t\t\t\t\t<li><a href="https://crco.calpoly.edu/Notice_of_Non-Discrimination">Non-Discrimination</a></li>\r\n\t\t\t\t</ul>\r\n\t\t\t</div>\r\n\t\t</div>\r\n\t</footer><!-- END FOOTER -->\r\n\r\n\r\n\t\t<script src="/framework/js/jquery.min.js"></script>\r\n\t<script src="/framework/js/what-input.min.js"></script>\r\n\t<script src="/framework/js/foundation.min.js"></script>\r\n\t<script src="/framework/js/clipboard.min.js"></script>\r\n\t<script src="/framework/js/app.js"></script>\r\n\t<script defer src="/framework/fontawesome/v6/js/all.min.js"></script>\r\n\t\t\r\n</body>\r\n<!-- InstanceEnd -->\r\n\r\n</html>'




```python
# get a structured HTML content
BeautifulSoup(html_text)
```




    <!DOCTYPE html>
    <html class="no-js" dir="ltr" lang="en">
    <head>
    <!--
    Cal Poly Web Template v2.0.0
    Code maintained by
    Information Technology Services
    California Polytechnic State University
    San Luis Obispo, CA 93407
    -->
    <meta charset="utf-8"/>
    <meta content="IE=Edge" http-equiv="X-UA-Compatible"/>
    <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
    <title>Sample Tables - Web - Cal Poly</title>
    <meta content="en" http-equiv="content-language"/>
    <meta content="en" name="language"/>
    <meta content="none" name="msapplication-config"/>
    <meta content="AFD-2.0" name="codebase"/>
    <meta content="As stewards of the University resources, we provide high quality, efficient support and planning services as an integral part of the campus community in support of student learning." name="Description"/>
    <meta content="Cal Poly, Administration, AFD, Finance, Police, Budget, Facilities, Fiscal, HR, Risk, Technology, Corporation" name="Keywords"/>
    <link href="https://use.typekit.net/asw2aly.css" rel="stylesheet"/>
    <link href="/framework/css/app.css" rel="stylesheet"/>
    <link href="/framework/fontawesome/v6/css/all.min.css" rel="stylesheet"/>
    <link href="/framework/fontawesome/v6/css/v4-shims.css" rel="stylesheet"/>
    <!-- Google Analytics -->
    <script>
    	(function(i, s, o, g, r, a, m) {
    		i['GoogleAnalyticsObject'] = r;
    		i[r] = i[r] || function() {
    			(i[r].q = i[r].q || []).push(arguments)
    		}, i[r].l = 1 * new Date();
    		a = s.createElement(o),
    			m = s.getElementsByTagName(o)[0];
    		a.async = 1;
    		a.src = g;
    		m.parentNode.insertBefore(a, m)
    	})(window, document, 'script', 'https://www.google-analytics.com/analytics.js', 'ga');
    
    	ga('create', 'UA-102181678-1', 'auto', 'CP');
    	ga('create', 'UA-31323973-1', 'auto', 'AFD');
    	ga('require', 'linkid', 'linkid.js');
    	ga('CP.send', 'pageview');
    	ga('AFD.send', 'pageview');
    	</script>
    <!-- End Google Analytics -->
    <!-- Google Tag Manager 1 -->
    <script>
    	(function(w, d, s, l, i) {
    		w[l] = w[l] || [];
    		w[l].push({
    			'gtm.start': new Date().getTime(),
    			event: 'gtm.js'
    		});
    		var f = d.getElementsByTagName(s)[0],
    			j = d.createElement(s),
    			dl = l != 'dataLayer' ? '&l=' + l : '';
    		j.async = true;
    		j.src =
    			'https://www.googletagmanager.com/gtm.js?id=' + i + dl;
    		f.parentNode.insertBefore(j, f);
    	})(window, document, 'script', 'dataLayer1', 'GTM-P4F3XD3');
    	</script>
    <!-- End Google Tag Manager 1 -->
    <!-- Google Tag Manager 2 marketing -->
    <script>
    	(function(w, d, s, l, i) {
    		w[l] = w[l] || [];
    		w[l].push({
    			'gtm.start': new Date().getTime(),
    			event: 'gtm.js'
    		});
    		var f = d.getElementsByTagName(s)[0],
    			j = d.createElement(s),
    			dl = l != 'dataLayer' ? '&l=' + l : '';
    		j.async = true;
    		j.src =
    			'https://www.googletagmanager.com/gtm.js?id=' + i + dl;
    		f.parentNode.insertBefore(j, f);
    	})(window, document, 'script', 'dataLayer2', 'GTM-TKZNRR2');
    	</script>
    <!-- End Google Tag Manager 2 marketing -->
    <!-- Hotjar Tracking Code for https://afd.calpoly.edu/ -->
    <script>
    	(function(h, o, t, j, a, r) {
    		h.hj = h.hj || function() {
    			(h.hj.q = h.hj.q || []).push(arguments)
    		};
    		h._hjSettings = {
    			hjid: 1763767,
    			hjsv: 6
    		};
    		a = o.getElementsByTagName('head')[0];
    		r = o.createElement('script');
    		r.async = 1;
    		r.src = t + h._hjSettings.hjid + j + h._hjSettings.hjsv;
    		a.appendChild(r);
    	})(window, document, 'https://static.hotjar.com/c/hotjar-', '.js?sv=');
    	</script>
    <link href="/images/favicon/apple-touch-icon.png" rel="apple-touch-icon" sizes="180x180"/>
    <link href="/images/favicon/favicon-32x32.png" rel="icon" sizes="32x32" type="image/png"/>
    <link href="/images/favicon/favicon-16x16.png" rel="icon" sizes="16x16" type="image/png"/>
    <link color="#154734" href="/images/favicon/safari-pinned-tab.svg" rel="mask-icon"/>
    <meta content="#da532c" name="msapplication-TileColor"/>
    <meta content="#ffffff" name="theme-color"/>
    </head>
    <body class="subsite_ants page_default">
    <!-- Start Facebook -->
    <div id="fb-root"></div>
    <script>
    	(function(d, s, id) {
    		var js, fjs = d.getElementsByTagName(s)[0];
    		if (d.getElementById(id)) return;
    		js = d.createElement(s);
    		js.id = id;
    		js.src = "//connect.facebook.net/en_US/sdk.js#xfbml=1&version=v2.8&appId=131592030268312";
    		fjs.parentNode.insertBefore(js, fjs);
    	}(document, 'script', 'facebook-jssdk'));
    	</script>
    <!-- End Facebook -->
    <!-- Google Tag Manager (noscript) -->
    <noscript><iframe height="0" src="https://www.googletagmanager.com/ns.html?id=GTM-P4F3XD3" style="display:none;visibility:hidden" width="0"></iframe></noscript>
    <!-- End Google Tag Manager (noscript) -->
    <!-- Google Tag Manager (noscript) Marketing -->
    <noscript><iframe height="0" src="https://www.googletagmanager.com/ns.html?id=GTM-TKZNRR2" style="display:none;visibility:hidden" width="0"></iframe></noscript>
    <!-- End Google Tag Manager (noscript) -->
    <header>
    <!-- <section class="sitewide-banner" data-closable>
      			<button class="close-button" data-close>&times;</button>
    			<div class="row align-middle">
    				<div class="column small-12 medium-7 ">
    					<h3>Coronavirus Information from Administration & Finance</h3>
    				</div>
    				<div class="column small-12 medium-3 medium-offset-2">
    					<a href="/coronavirus/" class="button expanded small">Learn More</a>
    				</div>
    			</div>
    		</section> -->
    <section class="cp_header">
    <a class="skip" href="#content">Skip to content</a>
    <div class="row align-middle align-justify">
    <div class="columns flex-container">
    <a class="logo" href="http://www.calpoly.edu/">
    <img alt="Cal Poly Logo and Shield" src="/framework/images/calpoly-logo-1x.png" srcset="/framework/images/calpoly-logo-1x.png,
    						             /framework/images/calpoly-logo-2x.png 2x"/>
    </a>
    <h2 class="sitename align-self-middle" id="sitename"><a href="/">Administration &amp; Finance</a></h2>
    </div>
    <div class="flex-container" data-hide-for="medium" data-responsive-toggle="subsite-menu" style="margin-right:1rem;">
    <a class="" data-toggle="" type="button"><span class="show-for-sr">menu</span><i class="fas fa-bars"></i></a>
    <!-- <button class="menu-icon" type="button" data-toggle><span class="show-for-sr">menu</span></button> -->
    </div>
    <div class="columns search small-12 medium-5">
    <div class="row align-middle align-right">
    <div class="shrink column cp-menu small-order-2 medium-order-1">
    <a href="/services">A&amp;F Services</a>    <a href="https://myportal.calpoly.edu">my CalPoly login</a>
    </div>
    <div class="column small-order-1 medium-order-2">
    <form action="https://www.calpoly.edu/search/?q=" method="get" title="Search Form">
    <div class="input-group">
    <input class="input-group-field" name="q" placeholder="Search Cal Poly" title="Search Cal Poly" type="text"/>
    <div class="input-group-button">
    <button class="button" name="btnG" type="submit">
    <!-- Screen readers will see "Search" -->
    <span class="show-for-sr">Search</span>
    <!-- Visual users will see the mag glass, but not the "Search" text -->
    <span aria-hidden="true"><i class="fa fa-search"></i></span>
    </button>
    </div>
    </div>
    </form>
    </div>
    </div>
    </div>
    </div>
    </section>
    <section class="hero">
    <div class="row">
    <div class="large-12 column">
    <h3>
    <div class="mobile-nav-action" data-hide-for="medium" data-responsive-toggle="subsite-menu">
    <button class="menu-icon" data-toggle="" type="button"><span class="show-for-sr">menu</span></button>
    </div>
    <a href="/web/">A&amp;F Web Support</a>
    </h3>
    </div>
    </div>
    </section>
    </header>
    <section class="site-nav">
    <div class="row collapse" id="subsite-menu">
    <div class="column">
    <ul class="vertical medium-horizontal menu">
    <li><a href="https://wiki.calpoly.edu/display/usr/Web+Editing+-+Accessible+Documents">Accessibility</a></li>
    <li><a href="/web/style-guide">Style Guide</a></li>
    <li><a href="mailto:afd-web@calpoly.edu?subject=%5Bwebsite name%5D - %5Bdescriptor%5D">Request Website Changes</a></li>
    </ul>
    </div>
    </div>
    </section>
    <section class="bread">
    <div class="row">
    <div class="columns">
    <ul class="breadcrumbs">
    <li><a href="/">A&amp;F Home</a></li>
    <li><a href="/web/">Web</a></li>
    <li><span class="show-for-sr">Current: </span>Sample Tables</li>
    </ul>
    </div>
    </div>
    </section>
    <div class="row align-justify">
    <div class="small-12 medium-8 columns" id="content">
    <a name="topH1"></a>
    <!--BEGIN MAIN CONTENT AREA-->
    <h1>Sample Page - Data Tables</h1>
    <p><a href="http://warc.calpoly.edu/accessibility/508indepth/rowcolumn.html">For more information on creating accessible data tables see the Accessibility &gt; Row and Column section of the Web Authoring Resource Center</a>.</p>
    <h2>Examples of Accessible Data Tables</h2>
    <p>These example tables contain captions and summaries. When you copy any of these tables into your page you must edit the  caption and summary. The caption can be edited in the Design view but the summary text must be edited in Code view. Click inside the table, then select the table tag on the tag selector, then switch to Code view and edit the text in the summary attribute.      </p>
    <h3><a id="basic" name="basic"></a>Basic Data Table with Column Headings</h3>
    <table border="1" summary="Provide table summary here">
    <caption>
    <strong>Table caption (name and description of table)</strong><br/>
            You can describe your table here or in the context of your page.  
            This table is read using the first row as the header for each column.
            (Replace this caption with your own description of the table)
            </caption>
    <tr>
    <th scope="col">Description</th>
    <th scope="col">Date</th>
    <th scope="col"><a href="#">Location</a></th>
    </tr>
    <tr>
    <td> Academic Senate Meeting</td>
    <td>May 25, 2205</td>
    <td>Building 99 Room 1</td>
    </tr>
    <tr class="shade-row">
    <td>Commencement Meeting</td>
    <td>December 15, 2205</td>
    <td>Building 42 Room 10</td>
    </tr>
    <tr>
    <td>Dean's Council</td>
    <td>February 1, 2206</td>
    <td>Building 35 Room 5</td>
    </tr>
    <tr class="shade-row">
    <td>Committee on Committees</td>
    <td>March 3, 2206</td>
    <td>Building 1 Room 201</td>
    </tr>
    <tr>
    <td> Lorem ipsum dolor sit amet, <a href="#">consectetuer adipiscing elit</a>. Sed lacus arcu, porta posuere, varius et.</td>
    <td>Lorem <a href="#">ipsum dolor</a> sit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et.</td>
    <td>Lorem <a href="#">ipsum dolor</a> sit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et.</td>
    </tr>
    <tr class="shade-row">
    <td><a href="#">Lorem ipsum dolor</a></td>
    <td><a href="#">Lorem ipsum dolor</a></td>
    <td><a href="#">Lorem ipsum dolor</a></td>
    </tr>
    </table>
    <h3><a id="directory" name="directory"></a>Directory Listing Table - Roll Cursor Over an Item
          </h3>
    <table border="1" class="table_directory" summary="Provide table summary here">
    <caption>
    <strong>Directory Listing   (Table caption - name and description of table)</strong><br/>
              Apply the "directory" style to the <code>&lt;table&gt;</code> tag to remove the borders and add roll-over styling to rows.
              You can describe  your table here or in the context of your page.  This table is read using the  first row as the header for each column. (Replace this caption with your  own description of the table)
            </caption>
    <tr>
    <th scope="col">Name</th>
    <th scope="col">Telephone</th>
    <th scope="col">Email</th>
    <th scope="col">Office</th>
    </tr>
    <tr>
    <td>Dr. Sally</td>
    <td>555-1234</td>
    <td>sally@calpoly.edu</td>
    <td>12-34</td>
    </tr>
    <tr>
    <td>Dr. Steve</td>
    <td>555-5678</td>
    <td>steve@calpoly.edu</td>
    <td>56-78</td>
    </tr>
    <tr>
    <td>Dr. Kathy</td>
    <td>555-9012</td>
    <td>kathy@calpoly.edu</td>
    <td>90-123</td>
    </tr>
    </table>
    <h3><a id="columnrow" name="columnrow"></a>Column and Row Headings Example</h3>
    <table border="1" summary="Provide table summary here">
    <caption>
    <strong>Table caption (name and description of table)</strong><br/>
            This table is read using the first row as a column header and then the first item of the first column as a row header.
            (Replace this caption with your own description of the table)
            </caption>
    <tr>
    <th scope="col">Instructor</th>
    <th scope="col">Class</th>
    <th scope="col">Location</th>
    </tr>
    <tr>
    <th scope="row">Dr. Sally</th>
    <td>Surgery 101</td>
    <td>Building 2 Room 3</td>
    </tr>
    <tr>
    <th scope="row">Dr. Steve</th>
    <td><a href="#">Radiology 101</a></td>
    <td><a href="#">Building 2 Room 5</a></td>
    </tr>
    <tr>
    <th scope="row">Dr. Kathy</th>
    <td>Orthopedics 101</td>
    <td>Building 2 Room 20</td>
    </tr>
    </table>
    <h3><a id="aligndata" name="aligndata"></a>Table Data Alignment Styles - Left, Middle, Right </h3>
    <table border="1" summary="Provide table summary here">
    <caption>
    <strong>Table caption (name and description of table)</strong><br/>
              This table uses classes center and right to align text or images within a table cell. Default alignment is left. You can describe your table here or in the context of your page.  
              This table is read using the first row as the header for each column.
              (Replace this caption with your own description of the table)
            </caption>
    <tr>
    <th scope="col">Aligned Left</th>
    <th class="table_text_center" scope="col">Aligned Center</th>
    <th class="table_text_right" scope="col">Aligned Right</th>
    </tr>
    <tr>
    <td> Academic Senate Meeting</td>
    <td class="table_text_center">May 25, 2205</td>
    <td class="table_text_right">Building 99 Room 1</td>
    </tr>
    <tr class="shade-row">
    <td>Commencement Meeting</td>
    <td class="table_text_center">December 15, 2205</td>
    <td class="table_text_right">Building 42 Room 10</td>
    </tr>
    <tr>
    <td> Lorem ipsum dolor sit amet, <a href="#">consectetuer adipiscing elit</a>. Sed lacus arcu, porta posuere, varius et.</td>
    <td class="table_text_center">Lorem <a href="#">ipsum dolor</a> sit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et.</td>
    <td class="table_text_right">Lorem <a href="#">ipsum dolor</a> sit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et.</td>
    </tr>
    <tr class="shade-row">
    <td><a href="#">Lorem ipsum dolor</a></td>
    <td class="table_text_center"><a href="#">Lorem ipsum dolor</a></td>
    <td class="table_text_right"><a href="#">Lorem ipsum dolor</a></td>
    </tr>
    </table>
    <h3>Table No Outline - H2</h3>
    <table border="1" class="table_noStyle" summary="Outline Table style">
    <caption>
    <strong>No Style Table Listing    (Table caption - name and description of table)</strong><br/>
    Apply the "table_noStyle" style to the <code>&lt;table&gt;</code> tag to remove the borders
            . You can describe  your table here or in the context of your page.  This table is read using the  first row as the header for each column. (Replace this caption with your  own description of the table)
            </caption>
    <tbody>
    <tr class="table_greenText">
    <th scope="col" width="30%">Day</th>
    <th scope="col" width="20%">Time</th>
    <th scope="col" width="50%">Location</th>
    </tr>
    <tr>
    <td>Wednesday</td>
    <td>3-6 pm</td>
    <td>Cal Poly Campus (<a href="#">follow U-Pick Signs</a>)</td>
    </tr>
    <tr>
    <td>Thursday</td>
    <td>2:30-5pm</td>
    <td>Morro Bay Farmer's Market</td>
    </tr>
    <tr>
    <td>Thursday</td>
    <td>6:10-9pm</td>
    <td>Downtown SLO Farmer's Market</td>
    </tr>
    <tr>
    <td>Saturday</td>
    <td>8-10:30am</td>
    <td>Farmer's Market new Embassy Suites</td>
    </tr>
    <tr>
    <td>Saturday</td>
    <td>11am-2pm</td>
    <td>Cal Poly Campus (<a href="#">follow U-Pick signs</a>)</td>
    </tr>
    </tbody>
    </table>
    <h3><a id="complex" name="complex"></a>Complex Data Table</h3>
    <table border="1">
    <caption>
    <strong>Table caption (name and description of table)</strong><br/>
            This is an example of a <strong>Complex Data table</strong> that associates column headers with <strong>row headers that span multiple rows</strong>. The underlying HTML code of this table belies the necessary associations that make the table readable using a screen reading technology (Replace this caption with your own description of the table)
            </caption>
    <tbody>
    <tr>
    <th id="sname" scope="col"><p>NAME OF SYSTEM OR PORTAL CHANNEL</p></th>
    <th id="activity" scope="col"><p>NAME OF SYSTEM OR ACTIVITY</p></th>
    <th id="status" scope="col"><p>STATUS DURING OUTAGE</p></th>
    <th id="frozen" scope="col"><p>DATA FROZEN AS OF</p></th>
    <th id="exp" scope="col"><p>EXPECTED UP TIME</p></th>
    </tr>
    <tr>
    <th headers="sname" id="pi" rowspan="4" scope="row"><p>Personal Information</p></th>
    <td headers="pi activity"><p>Addresses</p></td>
    <td headers="pi status"><p>View Only</p></td>
    <td headers="pi frozen"><p>1/18/2008</p></td>
    <td headers="pi exp"><p>Go live date</p></td>
    </tr>
    <tr>
    <td headers="pi activity"><p>Names</p></td>
    <td headers="pi status"><p>View Only</p></td>
    <td headers="pi frozen"><p>1/18/2008</p></td>
    <td headers="pi exp"><p>Go live date</p></td>
    </tr>
    <tr>
    <td headers="pi activity"><p>Phone Numbers</p></td>
    <td headers="pi status"><p>View Only</p></td>
    <td headers="pi frozen"><p>1/18/2008</p></td>
    <td headers="pi exp"><p>Go live date</p></td>
    </tr>
    <tr>
    <td headers="pi activity"><p>Emergency Contacts</p></td>
    <td headers="pi status"><p>View Only</p></td>
    <td headers="pi frozen"><p>1/18/2008</p></td>
    <td headers="pi exp"><p>Go live date</p></td>
    </tr>
    <tr>
    <th headers="sname" id="glb" scope="row"><p>Group Leave Balance</p></th>
    <td headers="glb activity"><p>Group Leave Balances</p></td>
    <td headers="glb status"><p>View Only</p></td>
    <td headers="glb frozen"><p>12/31/2007</p></td>
    <td headers="glb exp"><p>3/1/2008</p></td>
    </tr>
    <tr>
    <th headers="sname" id="lcb" scope="row"><p>Leave/CTO Balances</p></th>
    <td headers="lcb activity"><p>Leave and CTO Balances</p></td>
    <td headers="lcb status"><p>View Only</p></td>
    <td headers="lcb frozen"><p>12/31/2007</p></td>
    <td headers="lcb exp"><p>3/1/2008</p></td>
    </tr>
    <tr>
    <th headers="sname" id="fci" rowspan="6" scope="row"><p><a href="#">Faculty Course Info</a></p></th>
    <td headers="fci activity"><p>Class Search/Browse Catalog</p></td>
    <td headers="fci status"><p> </p></td>
    <td headers="fci frozen"><p> </p></td>
    <td headers="fci exp"><p> </p></td>
    </tr>
    <tr>
    <td headers="fci activity"><p>Record Grades</p></td>
    <td headers="fci status"><p> </p></td>
    <td headers="fci frozen"><p> </p></td>
    <td headers="fci exp"><p> </p></td>
    </tr>
    <tr>
    <td headers="fci activity"><p>Access Class Roster</p></td>
    <td headers="fci status"><p> </p></td>
    <td headers="fci frozen"><p> </p></td>
    <td headers="fci exp"><p> </p></td>
    </tr>
    <tr>
    <td headers="fci activity"><p>Student Data</p></td>
    <td headers="fci status"><p> </p></td>
    <td headers="fci frozen"><p> </p></td>
    <td headers="fci exp"><p> </p></td>
    </tr>
    <tr>
    <td headers="fci activity"><p>View My Class Schedule</p></td>
    <td headers="fci status"><p> </p></td>
    <td headers="fci frozen"><p> </p></td>
    <td headers="fci exp"><p> </p></td>
    </tr>
    <tr>
    <td headers="fci activity"><p>View My Weekly Schedule</p></td>
    <td headers="fci status"><p> </p></td>
    <td headers="fci frozen"><p> </p></td>
    <td headers="fci exp"><p> </p></td>
    </tr>
    <tr>
    <th headers="sname" id="ep" scope="row"><p>Enrollment Planning</p></th>
    <td headers="ep activity"><p>View Course <a href="#">Catalog</a> and Schedule of Classes</p></td>
    <td headers="ep status"><p> </p></td>
    <td headers="ep frozen"><p> </p></td>
    <td headers="ep exp"><p> </p></td>
    </tr>
    <tr>
    <th headers="sname" id="sp" scope="row"><p>Student Pay</p></th>
    <td headers="sp activity"><p><a href="#">Timekeeper Access</a></p></td>
    <td headers="sp status"><p>Unavailable</p></td>
    <td headers="sp frozen"><p>1/18/2008 </p></td>
    <td headers="sp exp"><p> </p></td>
    </tr>
    <tr>
    <th headers="sname" id="pd" rowspan="2" scope="row"><p>PolyData</p></th>
    <td headers="pd activity"><p>????</p></td>
    <td headers="pd status"><p> </p></td>
    <td headers="pd frozen"><p> </p></td>
    <td headers="pd exp"><p> </p></td>
    </tr>
    <tr>
    <td headers="pd activity"><p> </p></td>
    <td headers="pd status"><p> </p></td>
    <td headers="pd frozen"><p> </p></td>
    <td headers="pd exp"><p> </p></td>
    </tr>
    <tr>
    <th headers="sname" id="pp" rowspan="3" scope="row"><p>PolyProfile</p></th>
    <td headers="pp activity"><p> </p></td>
    <td headers="pp status"><p> </p></td>
    <td headers="pp frozen"><p> </p></td>
    <td headers="pp exp"><p> </p></td>
    </tr>
    <tr>
    <td headers="pp activity"><p> </p></td>
    <td headers="pp status"><p> </p></td>
    <td headers="pp frozen"><p> </p></td>
    <td headers="pp exp"><p> </p></td>
    </tr>
    <tr>
    <td headers="pp activity"><p> </p></td>
    <td headers="pp status"><p> </p></td>
    <td headers="pp frozen"><p> </p></td>
    <td headers="pp exp"><p> </p></td>
    </tr>
    </tbody>
    </table>
    </div><!--mainLeft-->
    <div id="mainLeftFull">
    <!--END MAIN CONTENT AREA: DO NOT EDIT BELOW-->
    </div>
    <div class="small-12 medium-4 large-3 columns">
    <div class="side-callout">
    </div> </div>
    </div>
    <footer>
    <div class="row footer-foot">
    <div class="column small-12 medium-expand">
    <div class="row">
    <div class="column small-12 footer-content">
    <div class="row">
    <div class="column show-for-medium medium-3 text-center align-self-top">
    <img alt="" src="/framework/images/calpoly-logo-vertical-rev-400.png" width="80%"/>
    </div>
    <div class="column small-12 medium-8 medium-offset-1">
    <h4>AFD Web</h4>
    <p>1 Grand Ave, <a href="http://maps.calpoly.edu/?vlist=058-0">Building 58</a>: Room 107, San Luis Obispo, CA 93407</p>
    <div class="row">
    <div class="column small-expand">
    <ul class="no-bullet">
    <li><strong>Phone:</strong> 805-756-6475</li>
    <li><a href="mailto:afd-web@calpoly.edu">afd-web@calpoly.edu</a></li>
    </ul>
    </div>
    <div class="column small-expand">
    <h5>Office Hours</h5>
    <ul class="no-bullet">
    <li>Monday — Friday</li>
    <li>7:30 a.m. - 5:00 p.m.</li>
    </ul>
    <!-- <h5>Window Hours</h5>
    										<ul class="no-bullet">
    											<li>Monday — Friday</li>
    											<li>9:00 a.m. - 4:00 p.m.</li>
    										</ul> -->
    </div>
    </div>
    </div>
    </div>
    </div>
    </div>
    <div class="row align-bottom inside-cp">
    <div class="column small-12 align-self-bottom">
    <img alt="Follow A&amp;F at" src="/framework/images/logo-inside-calpoly.png"/>
    <a href="https://www.instagram.com/insidecalpoly/">
    <span class="show-for-sr">Visit Instagram</span>
    <span aria-hidden="true"><i class="fab fa-instagram fa-lg"></i></span>
    </a>
    <a href="https://www.facebook.com/insidecalpoly/">
    <span class="show-for-sr">Visit Facebook</span>
    <span aria-hidden="true"><i class="fab fa-facebook fa-lg"></i></span>
    </a>
    </div>
    </div>
    </div>
    <div class="pop-links">
    <h5>Popular Links</h5>
    <ul class="no-bullet">
    <li><a href="https://security.calpoly.edu">Information Security</a></li>
    <li><a href="https://security.calpoly.edu/content/policies/standards/classification/index">Information Classification and Handling Standard</a></li>
    <li><a href="https://wiki.calpoly.edu/x/DouFDw">Password Changes</a></li>
    <li><a href="https://tech.calpoly.edu/services">ITS Service Desk</a></li>
    </ul>
    </div>
    </div>
    </footer>
    <footer class="cp-footer">
    <div class="row align-middle">
    <div class="column small-12 medium-2 small-text-center">
    <a href="http://www.calpoly.edu/">
    <img alt="Cal Poly Logo and Shield" src="/framework/images/calpoly-logo-rev-1x.png" srcset="/framework/images/calpoly-logo-rev-1x.png,
    						             /framework/images/calpoly-logo-rev-2x.png 2x"/>
    <!-- <img id="logo" title="Go to Cal Poly Home" alt="Cal Poly logo" src="/framework/images/CP_logo_cmyk_rev.svg" width="100%" /> -->
    </a>
    </div>
    <div class="column small-12 medium-8 medium-offset-2">
    <p>
    					© <script>
    					document.write(new Date().getFullYear())
    					</script>
    					California Polytechnic State University — San Luis Obispo, California 93407 — Phone: 805-756-1111
    				</p>
    </div>
    </div>
    <div class="row">
    <div class="getPlugins column">
    <ul class="menu simple align-right">
    <li><a href="https://www.calpoly.edu/privacy/">Privacy Notice</a></li>
    <li><a href="https://accessibility.calpoly.edu/website-accessibility-statement">Web Accessibility Statement</a></li>
    <li><a href="https://crco.calpoly.edu/Notice_of_Non-Discrimination">Non-Discrimination</a></li>
    </ul>
    </div>
    </div>
    </footer><!-- END FOOTER -->
    <script src="/framework/js/jquery.min.js"></script>
    <script src="/framework/js/what-input.min.js"></script>
    <script src="/framework/js/foundation.min.js"></script>
    <script src="/framework/js/clipboard.min.js"></script>
    <script src="/framework/js/app.js"></script>
    <script defer="" src="/framework/fontawesome/v6/js/all.min.js"></script>
    </body>
    <!-- InstanceEnd -->
    </html>








