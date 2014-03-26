If you ever have need for [Fiscal](http://en.wikipedia.org/wiki/Fiscal_year), Calendar or Academic quarters, you can use the [moment-fquarter](https://github.com/robgallen/moment-fquarter) plugin by [@robgallen](https://github.com/robgallen).

At it's simplest, just call the fquarter method on any moment object. This returns an object with the details of that quarter. You can also return a formatted string using the .toString() method. April is the starting month of the first quarter, by default.

```javascript
moment("2013-04-01").fquarter();
// {quarter:1, year:2013, nextYear:2014}
moment("2013-04-01").fquarter().toString();
// Q1 2013/14
```

You can pass in any month as the starting quarter, e.g. July

```javascript
moment("2013-01-01").fquarter(7);
// {quarter:3, year:2012, nextYear:2013}
moment("2013-01-01").fquarter(7).toString();
// Q3 2012/13
```

If you want calendar quarters, start in January

```javascript
moment("2013-01-01").fquarter(1);
// {quarter:1, year:2013, nextYear:null}
moment("2013-01-01").fquarter(1).toString();
// Q1 2013
```
