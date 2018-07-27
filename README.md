# custom-validators
Custom validators are great to add additional validation to your pages. They alert the supporter that a field hasn't been input in the correct format. 

You can create new validators by going to **Pages > Alerts & validators > Validators**. When you create a new one, choose the Validator Type of "Custom". The custom code uses a language called "regex". You can learn about regex on sites like https://regexone.com and test your regex code before applying it to your pages at sites like https://regex101.com.

Below we'll include some example custom validators which you can use to modify your own use

### Must be between 1 and 100 characters (any character) long
```regex
^.{1,100}$
```

### Must be six digits long
```regex
^\d{6}$
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

### Must not contain any characters at all (i.e. be blank) - good for a spam trap
```regex
^$
```

### Address field - Can be blank OR contain letters, numbers, commas, spaces, dots, slashes, dashes, apostophes
```regex
^$|^[A-Za-z0-9\s\-\\\/.,—'’]+$
```

### Must not contain characters < > ~ or % anywhere (but must contain something)
```regex
^[^<>~%]+$
```

### Can be blank OR not contain characters < > ~ or % anywhere
```regex
^$|^[^<>~%]+$
```

### UK postcode validator
```regex
(^\s?[A-Z][A-Z]?[0-9]{1,2}[A-Z]?\s?[0-9][A-Z]{2}?$)
```
### Email checker for commonly misspelt domains - must not contain @hotmial or @gmial
```regex
^((?!@hotmial|@gmial).)*$
```
