# 1
---

### **Code**:  
```python
df = pd.read_csv(r"C:\Users\sachi\python\projects\amazon.csv")
```

---

### 1. **`df`**
   - **Type**: **Variable**
   - **Explanation**: `df` ek variable hai jisme hum data store karenge. Yahan pe `df` ka use **DataFrame** ko represent karne ke liye kiya gaya hai. DataFrame ek 2D data structure hota hai jo tabular data ko represent karta hai (like a table with rows and columns).
   - **In Simple Terms**: `df` me jo data hoga, wo tabular form (rows aur columns) me store hoga.

---

### 2. **`pd`**
   - **Type**: **Alias (Short Name)**
   - **Explanation**: `pd` ek alias hai jo **pandas** library ke liye use ho raha hai. Aap pandas ko full name se bhi use kar sakte ho, lekin **`pd`** ek commonly used shorthand hai jo readability ko improve karta hai.
   - **In Simple Terms**: `pd` ek short form hai, jo hum pandas ko call karne ke liye use karte hain. 
   - **Example**: 
     ```python
     import pandas as pd
     ```

---

### 3. **`read_csv`**
   - **Type**: **Function**
   - **Explanation**: `read_csv` pandas ka ek function hai jo **CSV (Comma Separated Values)** file ko read (load) karne ke liye use hota hai. Yeh function CSV file ko read karne ke baad **DataFrame** ke form me data ko return karta hai.
   - **In Simple Terms**: `read_csv` ka kaam hai ek CSV file ko read karna aur us data ko tabular form me convert karna.

---

### 4. **`r"C:\Users\sachi\python\projects\amazon.csv"`**
   - **Type**: **Raw String (String with Path)**
   - **Explanation**: Yeh ek **string** hai jisme file ka path diya gaya hai. `r` ka matlab hai **raw string**, jiska use **escape characters** ko ignore karne ke liye hota hai. Matlab, agar aap path likh rahe hain, toh aapko backslashes (`\`) ko escape karne ki zarurat nahi hoti.
   - **In Simple Terms**: `r` ka matlab hai **raw string**, aur yeh path ke beech jo backslash hai unko special characters ke tarah treat nahi karega.

   **Example**:
   ```python
   path = r"C:\Users\sachi\python\projects\amazon.csv"
   ```

---

### Complete Explanation:
1. **`pd.read_csv(r"C:\Users\sachi\python\projects\amazon.csv")`**:
   - Yeh **pandas** ka function **`read_csv`** hai jo file path `r"C:\Users\sachi\python\projects\amazon.csv"` se **CSV file** ko read karega.
   - File ke andar jo data hai usko **DataFrame** ke format me convert karega (rows and columns).
   
2. **`df =`**:
   - Yeh DataFrame ko **`df`** variable me store kar raha hai. Matlab, jo data aapne CSV file se read kiya hai, wo `df` me store ho jayega.

### Example Process:
1. `pd.read_csv(r"C:\Users\sachi\python\projects\amazon.csv")` CSV file ko load karega aur data ko pandas ke **DataFrame** me convert karega.
2. **`df`** me yeh data store ho jayega.

---

### Final Example:

```python
import pandas as pd

# File path
df = pd.read_csv(r"C:\Users\sachi\python\projects\amazon.csv")

# DataFrame ka preview
print(df.head())  # This will print the first 5 rows of the DataFrame
```

Is code ka output hoga: `df` me stored Amazon sales data ke first 5 rows.

---

### Elements Breakdown:

- **`df`**: Variable (to store the data)
- **`pd`**: Alias for pandas library
- **`read_csv`**: Function to read the CSV file
- **File Path**: Location of the CSV file on your system

---

# 2
---
Code:  
```python
pd.set_option('display.max_columns', None)
```

---

### **Explanation:**

#### 1. **What is it doing?**
   - **`pd.set_option`**:
     Pandas ka ek function hai jo **display settings** ko customize karne ke liye use hota hai. Iska matlab hai ki Pandas ke DataFrame ko kaise display kiya jayega, usko hum control kar sakte hain.
   - **`'display.max_columns'`**:
     Yeh ek setting hai jo specify karti hai ki DataFrame me maximum kitne columns display honge. Default setting me agar columns bohot zyada ho jayein, toh Pandas sirf limited columns hi dikhata hai aur baaki ko truncate kar deta hai.
   - **`None`**:
     Iska matlab hai **"Unlimited"**. Agar aap `None` set karte hain, toh Pandas DataFrame ke **saare columns** display karega, chahe wo kitne bhi zyada ho.

---

#### 2. **Why is it useful?**
   Jab DataFrame ke columns bohot zyada ho jaate hain (e.g., 50, 100, ya usse zyada), toh Pandas kuch columns ko hide kar deta hai aur middle columns ko aise show karta hai:
   ```
   Column1  Column2  ...  Column99  Column100
   ```
   Agar aap **saare columns dekhna chahte hain** bina truncate kiye, toh yeh command useful hai.

---

#### 3. **Other Useful Settings:**
   Pandas me `pd.set_option` ke through aur bhi settings customize kar sakte hain:
   - **`'display.max_rows'`**:
     DataFrame me dikhne wale maximum rows set karta hai.
     ```python
     pd.set_option('display.max_rows', 50)
     ```
   - **`'precision'`**:
     Numbers ke decimal places control karta hai.
     ```python
     pd.set_option('precision', 2)
     ```
   - **`'expand_frame_repr'`**:
     DataFrame ko vertically (scrollable) ya horizontally wrap karne ke liye.
     ```python
     pd.set_option('display.expand_frame_repr', False)
     ```

---

### **In Short:**
- **Command:** `pd.set_option('display.max_columns', None)`
- **Purpose:** DataFrame ke **saare columns dikhane** ke liye, truncate na ho.
----
# 3 
---
### **Code**:  
```python
df.head(5)
```

---

### **Explanation:**

#### 1. **What does it do?**
- `df.head(5)` ek Pandas function hai jo DataFrame (`df`) ke **top 5 rows** ko display karta hai.  
- Iska matlab hai ki DataFrame ka **starting ka sample data** dikhana.  

---

#### 2. **How does it work?**
- **`head(n)`**:
  - **`n`**: Number of rows to display (default value is `5`).
  - Agar aap `head()` me kuch specify nahi karte, toh by default yeh **top 5 rows** return karta hai.
  - Example:
    ```python
    df.head()  # Same as df.head(5)
    ```

---

#### 3. **Why is it useful?**
- **Quick Overview**: DataFrame ke starting ke kuch rows dekhne ke liye useful hai, taaki aapko data structure aur contents ka **overview** mil sake.
- **Debugging**: Jab aap kisi file ya query se data load karte ho, toh `head()` use karke aap verify kar sakte ho ki data sahi se load hua ya nahi.
- **Sample Data**: Large datasets me puri table ko print karne ki zarurat nahi hoti, `head()` se ek chhota part dekhke kaam chal jata hai.

---

#### 4. **Example:**
Agar DataFrame `df` ka data kuch aisa hai:
| Name  | Age | Salary  |
|-------|-----|---------|
| Alice | 25  | 50000   |
| Bob   | 30  | 60000   |
| Eve   | 35  | 70000   |
| John  | 40  | 80000   |
| Jane  | 45  | 90000   |
| Mike  | 50  | 100000  |

Toh:
```python
df.head(5)
```
Output hoga:
| Name  | Age | Salary  |
|-------|-----|---------|
| Alice | 25  | 50000   |
| Bob   | 30  | 60000   |
| Eve   | 35  | 70000   |
| John  | 40  | 80000   |
| Jane  | 45  | 90000   |

---

#### 5. **Other Variants of `head`**:
- **Specify number of rows**:
  ```python
  df.head(10)  # Top 10 rows
  ```
- **Default behavior**:
  ```python
  df.head()  # Top 5 rows by default
  ```

---

### **Reverse of `head`: `tail()`**
Agar aap **last rows** dekhna chahte hain, toh `tail()` use karte hain:
```python
df.tail(5)  # Last 5 rows of the DataFrame
```

---

### In Short:
- **`df.head(5)`**: DataFrame ke **starting ke 5 rows** dekhne ke liye.  
- Useful for **quick preview** of the data.  
---
# 4

### **Code**:
```python
df.columns
```

---

### **Explanation:**

#### 1. **What does it do?**
- `df.columns` Pandas DataFrame (`df`) ke **saare column names** ko return karta hai.  
- Yeh ek **attribute** hai (function nahi hai), isiliye iske baad parentheses `()` lagane ki zarurat nahi hoti.

---

#### 2. **How does it work?**
- **Attribute**:  
  - `df.columns` ek **Index object** return karta hai, jo DataFrame ke **columns ke names (labels)** ko represent karta hai.
  - Output me column names ek iterable object (Index) ke form me milta hai.

---

#### 3. **Why is it useful?**
- **Understanding the Data**: Agar aapko DataFrame me kaun-kaun se columns hain yeh samajhna ho, toh yeh quick overview deta hai.
- **Debugging**: Agar data load karte waqt column names galat aaye ho (e.g., spaces ya special characters), toh `df.columns` se unhe verify kar sakte hain.
- **Renaming Columns**: Column names ko change ya clean karne se pehle unhe check karna zaruri hota hai.

---

#### 4. **Example**:
Agar DataFrame `df` ka structure kuch aisa hai:
| Name  | Age | Salary  |
|-------|-----|---------|
| Alice | 25  | 50000   |
| Bob   | 30  | 60000   |

Toh:
```python
df.columns
```

Output hoga:
```
Index(['Name', 'Age', 'Salary'], dtype='object')
```

Yahaan:
- **`Index`**: Pandas ka special object jo column names ko represent karta hai.
- **`dtype='object'`**: Yeh batata hai ki column names strings hain (object type).

---

#### 5. **Practical Use Cases**:

- **List of Column Names**:
  ```python
  columns_list = list(df.columns)  # Convert to a Python list
  print(columns_list)  # Output: ['Name', 'Age', 'Salary']
  ```

- **Renaming Columns**:
  ```python
  df.columns = ['Employee Name', 'Employee Age', 'Employee Salary']
  ```

- **Checking Column Name Presence**:
  ```python
  if 'Age' in df.columns:
      print("Column 'Age' exists!")
  ```

---

### **In Short**:
- **`df.columns`**: DataFrame ke column names ko retrieve karne ka quick and efficient way.
- Output: **Index object** containing all column labels.

---
# 5

---
`df.info()` ek method hai jo **pandas DataFrame** ki basic summary information display karta hai. Iska use aap **data exploration** me kar sakte hain taaki aapko quickly pata chal sake ki aapke DataFrame me kaunse columns hain, unka data type kya hai, aur missing values kitni hain.

### Working of `df.info()`:

1. **Basic Information**:
   - **Number of entries** (rows) in the DataFrame.
   - **Columns**: List of column names.
   - **Data type** of each column (e.g., `int64`, `float64`, `object`, etc.).
   - **Non-null count**: Each column me kitni non-null (non-missing) values hain.
   - **Memory usage**: DataFrame ko kitni memory use ho rahi hai.

### Example:

Assume `df` ka content kuch is tarah hai:

| Name  | Age | City      |
|-------|-----|-----------|
| Alice | 30  | New York  |
| Bob   | 25  | Chicago   |
| Charlie | 28  | San Francisco |

Agar aap `df.info()` run karte hain, toh output kuch is tarah dikh sakta hai:

```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 3 entries, 0 to 2
Data columns (total 3 columns):
 #   Column   Non-Null Count  Dtype  
 ---  ------   --------------  -----  
 0   Name     3 non-null      object 
 1   Age      3 non-null      int64  
 2   City     3 non-null      object 
dtypes: int64(1), object(2)
memory usage: 111.0+ bytes
```

### Breakdown of the Output:
- **`<class 'pandas.core.frame.DataFrame'>`**: Yeh show karta hai ki object ek pandas DataFrame hai.
- **`RangeIndex: 3 entries, 0 to 2`**: DataFrame me 3 rows hain, jo index 0 se 2 tak hai.
- **`Data columns (total 3 columns)`**: Total 3 columns hain.
- **Columns' Details**:
  - **Name**: Column name hai.
  - **Non-Null Count**: Har column me kitni non-null (non-missing) values hain.
  - **Dtype**: Data type of the column (e.g., `int64`, `object`).
- **`memory usage: 111.0+ bytes`**: DataFrame ko kitni memory use ho rahi hai.

### Use Case:
- Jab aapko DataFrame ke structure, types, aur missing data ke baare me quickly info chahiye hota hai.
  
---
# 6
---
`df.isnull().sum()` ek commonly used pandas method hai jo aapko **missing (null)** values ki count de deta hai, har column ke liye. Yeh method **NaN (Not a Number)** ya **None** values ko count karta hai jo data me missing hote hain.

### Code Breakdown:

1. **`df.isnull()`**:
   - **Purpose**: Yeh method DataFrame me har cell ko check karta hai ki woh **missing (null)** hai ya nahi.
   - **Working**: 
     - Agar value **missing** hai, toh `True` return hota hai.
     - Agar value **not missing** hai, toh `False` return hota hai.

   **Example**:
   Maan lijiye, yeh aapka DataFrame hai:

   | Name  | Age | City      |
   |-------|-----|-----------|
   | Alice | 30  | New York  |
   | Bob   | NaN | Chicago   |
   | Charlie | 28  | San Francisco |

   Agar aap `df.isnull()` run karenge, toh output kuch is tarah ka hoga:

   ```
      Name    Age   City
   0  False  False  False
   1  False   True  False
   2  False  False  False
   ```

   - Yahan pe **Age** column me second row mein `NaN` hai, isliye uska value `True` hoga, baaki cells me `False` hai.

---

2. **`sum()`**:
   - **Purpose**: `sum()` method `True` values ko count karta hai (because `True` ko internally 1 treat kiya jata hai, aur `False` ko 0 treat kiya jata hai).
   - **Working**: Yeh har column ke liye **missing values** ka count return karta hai.

   Agar aap `df.isnull().sum()` run karenge, toh yeh aapko **missing values ki count** har column ke liye batayega:

   **Example**:
   Given the previous DataFrame:

   ```
      Name    Age   City
   0  False  False  False
   1  False   True  False
   2  False  False  False
   ```

   Output of `df.isnull().sum()` would be:

   ```
   Name    0
   Age     1
   City    0
   dtype: int64
   ```

   - **Name**: 0 missing values
   - **Age**: 1 missing value
   - **City**: 0 missing values

---

### Final Summary:

- **`df.isnull()`**: Har column me missing values ko `True` se mark karta hai.
- **`sum()`**: `True` (missing) values ko count karta hai, jo **NaN** ya **None** hain.

Iska use aap **missing data handling** ke liye karte hain, jahan aapko yeh pata chal sakta hai ki kaunse columns me missing values hain aur unhe kaise handle karna hai (like filling with a default value, removing rows, etc.).

---

# 7 
---

Yeh code `pandas` ka use karke ek DataFrame ke **`discounted_price`** column me string-based data ko **numeric format** me convert kar raha hai. Aapko step-by-step samjhata hoon ki yeh code kya kar raha hai:

---

### 1. **Initial Problem**:
   - Column **`discounted_price`** me jo data hai wo string format me hai, aur usme unwanted characters (like `"₹"` aur `","`) hain.
   - Data analysis aur calculations ke liye, aapko is column ko numeric format me convert karna hoga.

---

### Code Breakdown:

#### 1st Line:
```python
df['discounted_price'] = df['discounted_price'].str.replace("₹",'')
```
   - **Purpose**: Is step me, column **`discounted_price`** ke andar jo `"₹"` (Indian Rupee Symbol) hai, usse remove kiya ja raha hai.
   - **How it works**:
     - `.str.replace()` function ka use karke `"₹"` ko empty string (`''`) se replace karte hain.
   - **Example**:
     - Input: `"₹1,200"`
     - Output: `"1,200"`

---

#### 2nd Line:
```python
df['discounted_price'] = df['discounted_price'].str.replace(",",'')
```
   - **Purpose**: Is step me, column **`discounted_price`** ke andar jo commas `","` hain, unhe remove kiya ja raha hai.
   - **How it works**:
     - `.str.replace()` function ka use karke `","` ko empty string (`''`) se replace karte hain.
   - **Example**:
     - Input: `"1,200"`
     - Output: `"1200"`

---

#### 3rd Line:
```python
df['discounted_price'] = df['discounted_price'].astype('float64')
```
   - **Purpose**: Is step me, **`discounted_price`** column ko string se **numeric format (`float64`)** me convert kiya ja raha hai.
   - **How it works**:
     - `.astype('float64')` method ka use karke string values ko **float type** me convert karte hain.
   - **Example**:
     - Input: `"1200"`
     - Output: `1200.0` (float value)

---

### Full Process Example:

Maan lijiye **`discounted_price`** column ka data kuch aisa hai:

| discounted_price |
|------------------|
| ₹1,200           |
| ₹2,500           |
| ₹999             |

1. **1st Line** (`str.replace("₹",'')`):
   - Removes `"₹"`.
   - Result:
     | discounted_price |
     |------------------|
     | 1,200            |
     | 2,500            |
     | 999              |

2. **2nd Line** (`str.replace(",",'')`):
   - Removes commas `","`.
   - Result:
     | discounted_price |
     |------------------|
     | 1200             |
     | 2500             |
     | 999              |

3. **3rd Line** (`astype('float64')`):
   - Converts strings to **float64** type.
   - Result:
     | discounted_price |
     |------------------|
     | 1200.0           |
     | 2500.0           |
     | 999.0            |

---

### Why It’s Important for Data Analysis:
1. **Numeric Format**:
   - Data ko numeric format me convert karna zaroori hai taaki calculations, aggregations, aur visualizations (e.g., mean, sum, plot) kar sakein.
   
2. **Cleaning Unnecessary Characters**:
   - Strings me `"₹"` aur `","` jaisi extra cheezein calculations ko block karengi. Unko remove karna zaroori hai.

---
# 8
---
