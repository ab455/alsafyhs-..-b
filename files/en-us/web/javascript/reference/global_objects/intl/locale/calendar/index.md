---
title: Intl.Locale.prototype.calendar
slug: Web/JavaScript/Reference/Global_Objects/Intl/Locale/calendar
tags:
  - Internationalization
  - Intl
  - JavaScript
  - Property
  - Locale
  - Localization
  - Prototype
  - Reference
browser-compat: javascript.builtins.Intl.Locale.calendar
---
{{JSRef}}

The **`Intl.Locale.prototype.calendar`** property is an accessor property which returns the type of calendar used in the `Locale`.

## Description

The `calendar` property returns the part of the `Locale` that indicates the `Locale`'s calendar era. While most of the world uses the Gregorian calendar, there are several regional calendar eras used around the world. The following table shows all the valid Unicode calendar key strings, along with a description of the calendar era they represent.

### Unicode calendar keys

<table class="standard-table">
  <caption>
    Unicode calendar keys
  </caption>
  <thead>
    <tr>
      <th scope="col">Calendar key (name)</th>
      <th scope="col">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>buddhist</code></td>
      <td>Thai Buddhist calendar</td>
    </tr>
    <tr>
      <td><code>chinese</code></td>
      <td>Traditional Chinese calendar</td>
    </tr>
    <tr>
      <td><code>coptic</code></td>
      <td>Coptic calendar</td>
    </tr>
    <tr>
      <td><code>dangi</code></td>
      <td>Traditional Korean calendar</td>
    </tr>
    <tr>
      <td><code>ethioaa</code></td>
      <td>Ethiopic calendar, Amete Alem (epoch approx. 5493 B.C.E)</td>
    </tr>
    <tr>
      <td><code>ethiopic</code></td>
      <td>Ethiopic calendar, Amete Mihret (epoch approx, 8 C.E.)</td>
    </tr>
    <tr>
      <td><code>gregory</code></td>
      <td>Gregorian calendar</td>
    </tr>
    <tr>
      <td><code>hebrew</code></td>
      <td>Traditional Hebrew calendar</td>
    </tr>
    <tr>
      <td><code>indian</code></td>
      <td>Indian calendar</td>
    </tr>
    <tr>
      <td><code>islamic</code></td>
      <td>Islamic calendar</td>
    </tr>
    <tr>
      <td><code>islamic-umalqura</code></td>
      <td>Islamic calendar, Umm al-Qura</td>
    </tr>
    <tr>
      <td><code>islamic-tbla</code></td>
      <td>
        Islamic calendar, tabular (intercalary years
        [2,5,7,10,13,16,18,21,24,26,29] - astronomical epoch)
      </td>
    </tr>
    <tr>
      <td><code>islamic-civil</code></td>
      <td>
        Islamic calendar, tabular (intercalary years
        [2,5,7,10,13,16,18,21,24,26,29] - civil epoch)
      </td>
    </tr>
    <tr>
      <td><code>islamic-rgsa</code></td>
      <td>Islamic calendar, Saudi Arabia sighting</td>
    </tr>
    <tr>
      <td><code>iso8601</code></td>
      <td>
        ISO calendar (Gregorian calendar using the ISO 8601 calendar week rules)
      </td>
    </tr>
    <tr>
      <td><code>japanese</code></td>
      <td>Japanese Imperial calendar</td>
    </tr>
    <tr>
      <td><code>persian</code></td>
      <td>Persian calendar</td>
    </tr>
    <tr>
      <td><code>roc</code></td>
      <td>Republic of China calendar</td>
    </tr>
    <tr>
      <td>
        <div class="notecard warning">
          <p>
            <strong>Warning:</strong> The <code>islamicc</code> calendar key has
            been deprecated. Please use <code>islamic-civil</code>.
          </p>
        </div>
        <p><code>islamicc</code></p>
      </td>
      <td>Civil (algorithmic) Arabic calendar</td>
    </tr>
  </tbody>
</table>

## Examples

### Adding a calendar in the Locale string

Calendar eras fall under the category of locale key "extension keys". These keys add additional data about the locale, and are added to locale identifiers by using the `-u` extension. Thus, the calendar era type can be added to the initial locale identifier string that is passed into the {{jsxref("Intl/Locale/Locale", "Intl.Locale")}} constructor. To add the calendar type, first add the `-u` extension to the string. Next, add the `-ca` extension to indicate that you are adding a calendar type. Finally, add the calendar era to the string.

```js
let locale = new Intl.Locale("fr-FR-u-ca-buddhist");
console.log(locale.calendar); // Prints "buddhist"
```

### Adding a calendar with a configuration object

The {{jsxref("Intl/Locale/Locale", "Intl.Locale")}} constructor has an optional configuration object argument, which can contain any of several extension types, including calendars. Set the `calendar` property of the configuration object to your desired calendar era, and then pass it into the constructor.

```js
let locale = new Intl.Locale("fr-FR", { calendar: "buddhist" });
console.log(locale.calendar); // Prints "buddhist"
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{jsxref("Intl/Locale", "Intl.Locale")}}
- [Unicode Calendar Identifiers](https://www.unicode.org/reports/tr35/#UnicodeCalendarIdentifier)
