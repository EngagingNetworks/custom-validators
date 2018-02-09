# custom-validators
Custom validators are great to add additional validation to your pages. They alert the supporter that a field hasn't been input in the correct format. 

You can create new validators by going to **Pages > Alerts & validators > Validators**. When you create a new one, choose the Validator Type of "Custom". The custom code uses a language called "regex". You can learn about regex on sites like https://regexone.com and test your regex code before applying it to your pages at sites like https://regex101.com.

Below we'll include some example custom validators

### Must be six digits long
```regex
^\d{6}$
```

## Must contain the letter a at least once
```regex
[a]+
```

## Must not contain any characters at all (i.e. be blank) - good for a spam trap
```regex
^$
```

## Must not contain characters < > ~ or % anywhere (but must contain something)
```regex
^[^<>~%]+$
```

## Can be blank or not contain characters < > ~ or % anywhere
```regex
^$|^[^<>~%]+$
```

## Should start with 0 followed by 9 digits
```regex
^(0[0-9]{9})?$
```

## UK postcode validator
```regex
(^\s?[A-Z][A-Z]?[0-9]{1,2}[A-Z]?\s?[0-9][A-Z]{2}?$)
```
