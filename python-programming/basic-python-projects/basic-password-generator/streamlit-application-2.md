# 💎 Streamlit Application #2

## Our Application Preview

{% embed url="https://www.youtube.com/watch?v=W0rpxld3UCU" %}



<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Screenshot of our app</p></figcaption></figure>

### Explanation

#### External Dependencies

```python
import streamlit as st
import random
```

AI-generated code. Review and use carefully. [More info on FAQ](https://www.bing.com/new#faq).

* **Streamlit** is imported to create the web interface.
* **Random** is imported to generate random characters for the password.

#### Initializations

```python
lowercase = list(range(97, 123))
uppercase = list(range(65, 91))
digits = list(range(48, 58))
special = list(range(33, 48)) + list(range(58,65)) + list(range(91,97)) + list(range(123,127))
```

* These lists represent ASCII values for different character sets:
  * `lowercase`: ASCII values for ‘a’ to ‘z’.
  * `uppercase`: ASCII values for ‘A’ to ‘Z’.
  * `digits`: ASCII values for ‘0’ to ‘9’.
  * `special`: ASCII values for special characters like `!`, `@`, `#`, etc.

#### Streamlit App

```python
st.header("Password Maker")
st.write("This application will generate a password based on the desired criteria.")
```

* Sets up the header and description for the app.

#### User Inputs

```python
size = st.number_input(label="Enter the length of the password. (Minimum 8)", min_value=8, step=1, key="pwd_size")
has_upper = st.toggle(label="Contain Uppercase letters?", key="pwd_upper")
has_digit = st.toggle(label="Contain numbers?", key="pwd_digit")
has_special = st.toggle(label="Contain Special Characters?", key="pwd_special")
make_pwd = st.button("Generate Password")
```

* **size**: Input for the length of the password (minimum 8 characters).
* **has\_upper**: Toggle for including uppercase letters.
* **has\_digit**: Toggle for including digits.
* **has\_special**: Toggle for including special characters.
* **make\_pwd**: Button to generate the password.

#### Password Generation

```python
if make_pwd and size >= 8:
    if has_upper:
        options.extend(uppercase)
    if has_digit:
        options.extend(digits)
    if has_special:
        options.extend(special)
    
    while len(password) <= size:
        password += chr(random.choice(options))
    
    st.write(f"The generated password is: {password}")
    options = lowercase.copy()
```

* **Condition**: Checks if the button is clicked and the size is at least 8.
* **Options Update**: Adds selected character sets to the options list.
* **Password Loop**: Generates a password by randomly selecting characters from the options list until it reaches the desired length.
* **Display**: Shows the generated password.
* **Reset**: Resets the options list for reuse.

### Code

```python
# Password Creator in Streamlit

# External Dependencies
import streamlit as st

# Internal Imports
import random

# Initializations
# ASCII Table Decimal to Characters
lowercase = list(range(97, 123))
uppercase = list(range(65, 91))
digits = list(range(48, 58))
special = list(range(33, 48)) + list(range(58,65)) + list(range(91,97)) + list(range(123,127))

# initialize empty password
password = "" # Empty String
options = lowercase.copy()

# Streamlit App starts here
st.header("Password Maker")
st.write("This application will generate a password based on the desired criteria.")

size = st.number_input(
    label="Enter the length of the password. (Minimum 8)",
    min_value=8,
    step=1,
    key="pwd_size"
)

has_upper = st.toggle(
    label="Contain Uppercase letters?",
    key="pwd_upper"
)

has_digit = st.toggle(
    label="Contain numbers?",
    key="pwd_digit"
)

has_special = st.toggle(
    label="Contain Special Characters?",
    key="pwd_special"
)

make_pwd = st.button("Generate Password")

if make_pwd and size >= 8:
    # This means the the button has been clicked.

    # Step 1: Based on the criteria, add in the options
    if has_upper:
        options.extend(uppercase)
    
    if has_digit:
        options.extend(digits)
    
    if has_special:
        options.extend(special)
    
    # Step 2: Loop until the password variable is long as the given length
    while len(password) <= size:
        password += chr(random.choice(options))
    
    # Step 3: Display Password
    st.write(f"The generated password is: {password}")

    # Step 4: Reset options list back to just lowercase for reusability
    options = lowercase.copy()

```
