
# <a id="i18n"></a>i18n

Some utilities for working with i18n and finding the correct formats based on the configured language.

## Contents

**Module Members**

- [- unknown -](#- unknown -)
- [- unknown -](#- unknown -)

## Module Members

#### <a id="- unknown -"></a>- unknown - `undefined`

Contains formats for usage with Moment.js indexed by a `languageTag`. The stored values are objects having
the properties `date` and `time`, each with an according format string.

Example:
```js
i18n.update( 'de' ).then( () => {
   axI18n.localize( ui.i18n.momentFormats ); // => { date: 'DD.MM.YYYY', time: 'HH:mm' }
} );
i18n.update( 'en-gb' ).then( () => {
   axI18n.localize( ui.i18n.momentFormats ); // => { date: 'DD/MM/YYYY', time: 'HH:mm' }
} );
i18n.update( 'xy' ).then( () => {
  axI18n.localize( ui.i18n.momentFormats ); // => undefined
} );
```

#### <a id="- unknown -"></a>- unknown - `undefined`

Contains number formatting characters indexed by a `languageTag`. The stored values are objects having
the properties `g` (grouping separator) and `d` (decimal separator), each with the according character
to use for that language tag.

Example:
```js
i18n.update( 'de' ).then( () => {
   axI18n.localize( ui.i18n.numberFormats ); // => { g: '.', d: ',' }
} );
i18n.update( 'en-gb' ).then( () => {
   axI18n.localize( ui.i18n.numberFormats ); // => { g: ',', d: '.' }
} );
i18n.update( 'xy' ).then( () => {
   axI18n.localize( ui.i18n.numberFormats ); // => undefined
} );
```