# Budget

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.6.

 As applications grow in functionality, they also grow in size. Budgets is a feature in the Angular CLI which allows you to set budget thresholds in your configuration to ensure parts of your application stay within boundaries which you set

 ```json
 {
  ...
  "configurations": {
    "production": {
      ...
      budgets: []
    }
  }
}
```

[See more](https://github.com/angular/angular-cli/blob/master/docs/documentation/stories/budgets.md)


Check for each file, use type `bundle`:
```
  "budgets": [
          {
            "type": "bundle",
            "name": "polyfills",
            "baseline": "150kb",
            "maximumWarning": "50kb",
            "maximumError": "150kb"
          },
          {
            "type": "bundle",
            "name": "vendor",
            "baseline": "900kb",
            "maximumWarning": "100kb",
            "maximumError": "200kb"
          },
          {
            "type": "bundle",
            "name": "styles",
            "baseline": "280kb",
            "maximumWarning": "50kb",
            "maximumError": "100kb"
          },
          {
            "type": "bundle",
            "name": "main",
            "baseline": "200kb",
            "maximumWarning": "100kb",
            "maximumError": "150kb"
          },

        ]
```


Check the size for all file ( without stats.json), , use type `initial`:
```
{
  "type": "initial",
  "maximumWarning": "600kb",
  "maximumError": "5mb"
},

```

A new budget, `anyComponentStyle`, has been added in version 8.2, allowing to check your component CSS sizes. This is a very nice feature because I’ve audited quite a few projects where there was no problem in the JS bundles, but where bad practices with CSS imports resulted in bloated CSS files. As component CSS are self-contained, it’s quite easy to make a mistake and import the whole Material or Bootstrap CSS into each component…

```
{
  "type": "anyComponentStyle",
  "maximumWarning": "6kb",
  "maximumError": "10kb"
}
```
