# custom-validators
Custom validators are great to add additional validation to your pages. They alert the supporter that a field hasn't been input in the correct format. 

You can create new validators by going to **Pages > Alerts & validators > Validators**. When you create a new one, choose the Validator Type of "Custom". The custom code uses a language called "regex". You can learn about regex on sites like https://regexone.com and test your regex code before applying it to your pages at sites like https://regex101.com.

Below we'll include some example custom validators which you can use to modify your own use

## Examples to understand regex in Engaging Networks
### Must be between 1 and 100 characters (any character) long
```regex
^.{1,100}$
```
### Must be up to 10 digits long
```regex
^\d{0,10}$
```

### Should start with 0 followed by 9 digits
```regex
^(0[0-9]{9})?$
```

### Must contain the letter a at least once
```regex
[a]+
```

### Must not contain characters < > ~ or % anywhere (but must contain something)
```regex
^[^<>~%]+$
```

### Can be blank OR not contain characters < > ~ or % anywhere
```regex
^$|^[^<>~%]+$
```

### Must only contain letters - nothing else (not even spaces) ###
```regex
^[a-zA-Z]*$
```

## Address validators
### Address field - Can be blank OR contain letters, numbers, commas, spaces, dots, slashes, dashes, apostophes
```regex
^$|^[A-Za-z0-9\s\-\\\/.,—'’]+$
```

### UK Postcode validator (based on one supplied by UK government). Will also allow blank postcodes which can be picked up by the mandatory option instead
```regex
^$|([Gg][Ii][Rr] 0[Aa]{2})|((([A-Za-z][0-9]{1,2})|(([A-Za-z][A-Ha-hJ-Yj-y][0-9]{1,2})|(([A-Za-z][0-9][A-Za-z])|([A-Za-z][A-Ha-hJ-Yj-y][0-9]?[A-Za-z]))))\s?[0-9][A-Za-z]{2})
```

## Email validators
### Email validator but exclude qq.com, 163.com, pp.com
```regex
^\w+[-\.\w]*@(?!(?:qq|163|pp)\.com$)\w+[-\.\w]*?\.\w{2,4}$
```
### Email checker for commonly misspelt domains - must not contain @hotmial or @gmial
```regex
^((?!@hotmial|@gmial).)*$
```

## Fundraising validators
### Must be six digits long (sort codes)
```regex
^\d{6}$
```

### Must be eight digits long (account numbers)
```regex
^\d{8}$
```

### Must be 16 digits long (most card numbers)
```regex
^\d{16}$
```

## Anti-spam validators
### Must not contain any characters at all (i.e. be blank) - good for a spam trap since bots usually auto-fill all fields
```regex
^$
```
