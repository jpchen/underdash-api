---
title: API Reference

language_tabs:
  - javascript

toc_footers:
  - <a href='https://github.com/jpchen/underdash-api'>Contribute on Github</a>

includes:

search: true
---

# Introduction

 This is a cross documentation of [lodash](https://lodash.com/) and [underscore.js](http://underscorejs.org/).  This arose from my need to translate some underscore.js code, and I noticed that there was no place that aggregated the APIs together.  This does not attempt to prescribe one nor the other as the library of choice, as there is plenty of [discussion](http://stackoverflow.com/questions/13789618/differences-between-lodash-and-underscore) of that already.  As of the date of writing, this uses lodash [4.17.2](https://www.npmjs.com/package/lodash) and underscore [1.8.3](https://www.npmjs.com/package/underscore).  Freely use for your own benefit (risk).

# Table of Contents

<!-- div class="toc-container" -->



## Array
* [`_.chunk`](#_chunkarray-size1)
* [`_.compact`](#_compactarray)
* [`_.concat`](#_concatarray-values)
* [`_.difference`](#_differencearray-values)
* [`_.differenceBy`](#_differencebyarray-values-iteratee_identity)
* [`_.differenceWith`](#_differencewitharray-values-comparator)
* [`_.drop`](#_droparray-n1)
* [`_.dropRight`](#_droprightarray-n1)
* [`_.dropRightWhile`](#_droprightwhilearray-predicate_identity)
* [`_.dropWhile`](#_dropwhilearray-predicate_identity)
* [`_.fill`](#_fillarray-value-start0-endarraylength)
* [`_.findIndex`](#_findindexarray-predicate_identity-fromindex0)
* [`_.findLastIndex`](#_findlastindexarray-predicate_identity-fromindexarraylength-1)
* [`_.first` -> `head`](#_headarray" class="alias)
* [`_.flatten`](#_flattenarray)
* [`_.flattenDeep`](#_flattendeeparray)
* [`_.flattenDepth`](#_flattendeptharray-depth1)
* [`_.fromPairs`](#_frompairspairs)
* [`_.head`](#_headarray)
* [`_.indexOf`](#_indexofarray-value-fromindex0)
* [`_.initial`](#_initialarray)
* [`_.intersection`](#_intersectionarrays)
* [`_.intersectionBy`](#_intersectionbyarrays-iteratee_identity)
* [`_.intersectionWith`](#_intersectionwitharrays-comparator)
* [`_.join`](#_joinarray-separator-)
* [`_.last`](#_lastarray)
* [`_.lastIndexOf`](#_lastindexofarray-value-fromindexarraylength-1)
* [`_.nth`](#_ntharray-n0)
* [`_.pull`](#_pullarray-values)
* [`_.pullAll`](#_pullallarray-values)
* [`_.pullAllBy`](#_pullallbyarray-values-iteratee_identity)
* [`_.pullAllWith`](#_pullallwitharray-values-comparator)
* [`_.pullAt`](#_pullatarray-indexes)
* [`_.remove`](#_removearray-predicate_identity)
* [`_.reverse`](#_reversearray)
* [`_.slice`](#_slicearray-start0-endarraylength)
* [`_.sortedIndex`](#_sortedindexarray-value)
* [`_.sortedIndexBy`](#_sortedindexbyarray-value-iteratee_identity)
* [`_.sortedIndexOf`](#_sortedindexofarray-value)
* [`_.sortedLastIndex`](#_sortedlastindexarray-value)
* [`_.sortedLastIndexBy`](#_sortedlastindexbyarray-value-iteratee_identity)
* [`_.sortedLastIndexOf`](#_sortedlastindexofarray-value)
* [`_.sortedUniq`](#_sorteduniqarray)
* [`_.sortedUniqBy`](#_sorteduniqbyarray-iteratee)
* [`_.tail`](#_tailarray)
* [`_.take`](#_takearray-n1)
* [`_.takeRight`](#_takerightarray-n1)
* [`_.takeRightWhile`](#_takerightwhilearray-predicate_identity)
* [`_.takeWhile`](#_takewhilearray-predicate_identity)
* [`_.union`](#_unionarrays)
* [`_.unionBy`](#_unionbyarrays-iteratee_identity)
* [`_.unionWith`](#_unionwitharrays-comparator)
* [`_.uniq`](#_uniqarray)
* [`_.uniqBy`](#_uniqbyarray-iteratee_identity)
* [`_.uniqWith`](#_uniqwitharray-comparator)
* [`_.unzip`](#_unziparray)
* [`_.unzipWith`](#_unzipwitharray-iteratee_identity)
* [`_.without`](#_withoutarray-values)
* [`_.xor`](#_xorarrays)
* [`_.xorBy`](#_xorbyarrays-iteratee_identity)
* [`_.xorWith`](#_xorwitharrays-comparator)
* [`_.zip`](#_ziparrays)
* [`_.zipObject`](#_zipobjectprops-values)
* [`_.zipObjectDeep`](#_zipobjectdeepprops-values)
* [`_.zipWith`](#_zipwitharrays-iteratee_identity)





## Collection
* [`_.countBy`](#_countbycollection-iteratee_identity)
* [`_.each` -> `forEach`](#_foreachcollection-iteratee_identity" class="alias)
* [`_.eachRight` -> `forEachRight`](#_foreachrightcollection-iteratee_identity" class="alias)
* [`_.every`](#_everycollection-predicate_identity)
* [`_.filter`](#_filtercollection-predicate_identity)
* [`_.find`](#_findcollection-predicate_identity-fromindex0)
* [`_.findLast`](#_findlastcollection-predicate_identity-fromindexcollectionlength-1)
* [`_.flatMap`](#_flatmapcollection-iteratee_identity)
* [`_.flatMapDeep`](#_flatmapdeepcollection-iteratee_identity)
* [`_.flatMapDepth`](#_flatmapdepthcollection-iteratee_identity-depth1)
* [`_.forEach`](#_foreachcollection-iteratee_identity)
* [`_.forEachRight`](#_foreachrightcollection-iteratee_identity)
* [`_.groupBy`](#_groupbycollection-iteratee_identity)
* [`_.includes`](#_includescollection-value-fromindex0)
* [`_.invokeMap`](#_invokemapcollection-path-args)
* [`_.keyBy`](#_keybycollection-iteratee_identity)
* [`_.map`](#_mapcollection-iteratee_identity)
* [`_.orderBy`](#_orderbycollection-iteratees_identity-orders)
* [`_.partition`](#_partitioncollection-predicate_identity)
* [`_.reduce`](#_reducecollection-iteratee_identity-accumulator)
* [`_.reduceRight`](#_reducerightcollection-iteratee_identity-accumulator)
* [`_.reject`](#_rejectcollection-predicate_identity)
* [`_.sample`](#_samplecollection)
* [`_.sampleSize`](#_samplesizecollection-n1)
* [`_.shuffle`](#_shufflecollection)
* [`_.size`](#_sizecollection)
* [`_.some`](#_somecollection-predicate_identity)
* [`_.sortBy`](#_sortbycollection-iteratees_identity)





## Date
* [`_.now`](#_now)





## Function
* [`_.after`](#_aftern-func)
* [`_.ary`](#_aryfunc-nfunclength)
* [`_.before`](#_beforen-func)
* [`_.bind`](#_bindfunc-thisarg-partials)
* [`_.bindKey`](#_bindkeyobject-key-partials)
* [`_.curry`](#_curryfunc-arityfunclength)
* [`_.curryRight`](#_curryrightfunc-arityfunclength)
* [`_.debounce`](#_debouncefunc-wait0-options)
* [`_.defer`](#_deferfunc-args)
* [`_.delay`](#_delayfunc-wait-args)
* [`_.flip`](#_flipfunc)
* [`_.memoize`](#_memoizefunc-resolver)
* [`_.negate`](#_negatepredicate)
* [`_.once`](#_oncefunc)
* [`_.overArgs`](#_overargsfunc-transforms_identity)
* [`_.partial`](#_partialfunc-partials)
* [`_.partialRight`](#_partialrightfunc-partials)
* [`_.rearg`](#_reargfunc-indexes)
* [`_.rest`](#_restfunc-startfunclength-1)
* [`_.spread`](#_spreadfunc-start0)
* [`_.throttle`](#_throttlefunc-wait0-options)
* [`_.unary`](#_unaryfunc)
* [`_.wrap`](#_wrapvalue-wrapperidentity)





## Lang
* [`_.castArray`](#_castarrayvalue)
* [`_.clone`](#_clonevalue)
* [`_.cloneDeep`](#_clonedeepvalue)
* [`_.cloneDeepWith`](#_clonedeepwithvalue-customizer)
* [`_.cloneWith`](#_clonewithvalue-customizer)
* [`_.conformsTo`](#_conformstoobject-source)
* [`_.eq`](#_eqvalue-other)
* [`_.gt`](#_gtvalue-other)
* [`_.gte`](#_gtevalue-other)
* [`_.isArguments`](#_isargumentsvalue)
* [`_.isArray`](#_isarrayvalue)
* [`_.isArrayBuffer`](#_isarraybuffervalue)
* [`_.isArrayLike`](#_isarraylikevalue)
* [`_.isArrayLikeObject`](#_isarraylikeobjectvalue)
* [`_.isBoolean`](#_isbooleanvalue)
* [`_.isBuffer`](#_isbuffervalue)
* [`_.isDate`](#_isdatevalue)
* [`_.isElement`](#_iselementvalue)
* [`_.isEmpty`](#_isemptyvalue)
* [`_.isEqual`](#_isequalvalue-other)
* [`_.isEqualWith`](#_isequalwithvalue-other-customizer)
* [`_.isError`](#_iserrorvalue)
* [`_.isFinite`](#_isfinitevalue)
* [`_.isFunction`](#_isfunctionvalue)
* [`_.isInteger`](#_isintegervalue)
* [`_.isLength`](#_islengthvalue)
* [`_.isMap`](#_ismapvalue)
* [`_.isMatch`](#_ismatchobject-source)
* [`_.isMatchWith`](#_ismatchwithobject-source-customizer)
* [`_.isNaN`](#_isnanvalue)
* [`_.isNative`](#_isnativevalue)
* [`_.isNil`](#_isnilvalue)
* [`_.isNull`](#_isnullvalue)
* [`_.isNumber`](#_isnumbervalue)
* [`_.isObject`](#_isobjectvalue)
* [`_.isObjectLike`](#_isobjectlikevalue)
* [`_.isPlainObject`](#_isplainobjectvalue)
* [`_.isRegExp`](#_isregexpvalue)
* [`_.isSafeInteger`](#_issafeintegervalue)
* [`_.isSet`](#_issetvalue)
* [`_.isString`](#_isstringvalue)
* [`_.isSymbol`](#_issymbolvalue)
* [`_.isTypedArray`](#_istypedarrayvalue)
* [`_.isUndefined`](#_isundefinedvalue)
* [`_.isWeakMap`](#_isweakmapvalue)
* [`_.isWeakSet`](#_isweaksetvalue)
* [`_.lt`](#_ltvalue-other)
* [`_.lte`](#_ltevalue-other)
* [`_.toArray`](#_toarrayvalue)
* [`_.toFinite`](#_tofinitevalue)
* [`_.toInteger`](#_tointegervalue)
* [`_.toLength`](#_tolengthvalue)
* [`_.toNumber`](#_tonumbervalue)
* [`_.toPlainObject`](#_toplainobjectvalue)
* [`_.toSafeInteger`](#_tosafeintegervalue)
* [`_.toString`](#_tostringvalue)





## Math
* [`_.add`](#_addaugend-addend)
* [`_.ceil`](#_ceilnumber-precision0)
* [`_.divide`](#_dividedividend-divisor)
* [`_.floor`](#_floornumber-precision0)
* [`_.max`](#_maxarray)
* [`_.maxBy`](#_maxbyarray-iteratee_identity)
* [`_.mean`](#_meanarray)
* [`_.meanBy`](#_meanbyarray-iteratee_identity)
* [`_.min`](#_minarray)
* [`_.minBy`](#_minbyarray-iteratee_identity)
* [`_.multiply`](#_multiplymultiplier-multiplicand)
* [`_.round`](#_roundnumber-precision0)
* [`_.subtract`](#_subtractminuend-subtrahend)
* [`_.sum`](#_sumarray)
* [`_.sumBy`](#_sumbyarray-iteratee_identity)





## Number
* [`_.clamp`](#_clampnumber-lower-upper)
* [`_.inRange`](#_inrangenumber-start0-end)
* [`_.random`](#_randomlower0-upper1-floating)





## Object
* [`_.assign`](#_assignobject-sources)
* [`_.assignIn`](#_assigninobject-sources)
* [`_.assignInWith`](#_assigninwithobject-sources-customizer)
* [`_.assignWith`](#_assignwithobject-sources-customizer)
* [`_.at`](#_atobject-paths)
* [`_.create`](#_createprototype-properties)
* [`_.defaults`](#_defaultsobject-sources)
* [`_.defaultsDeep`](#_defaultsdeepobject-sources)
* [`_.entries` -> `toPairs`](#_topairsobject" class="alias)
* [`_.entriesIn` -> `toPairsIn`](#_topairsinobject" class="alias)
* [`_.extend` -> `assignIn`](#_assigninobject-sources" class="alias)
* [`_.extendWith` -> `assignInWith`](#_assigninwithobject-sources-customizer" class="alias)
* [`_.findKey`](#_findkeyobject-predicate_identity)
* [`_.findLastKey`](#_findlastkeyobject-predicate_identity)
* [`_.forIn`](#_forinobject-iteratee_identity)
* [`_.forInRight`](#_forinrightobject-iteratee_identity)
* [`_.forOwn`](#_forownobject-iteratee_identity)
* [`_.forOwnRight`](#_forownrightobject-iteratee_identity)
* [`_.functions`](#_functionsobject)
* [`_.functionsIn`](#_functionsinobject)
* [`_.get`](#_getobject-path-defaultvalue)
* [`_.has`](#_hasobject-path)
* [`_.hasIn`](#_hasinobject-path)
* [`_.invert`](#_invertobject)
* [`_.invertBy`](#_invertbyobject-iteratee_identity)
* [`_.invoke`](#_invokeobject-path-args)
* [`_.keys`](#_keysobject)
* [`_.keysIn`](#_keysinobject)
* [`_.mapKeys`](#_mapkeysobject-iteratee_identity)
* [`_.mapValues`](#_mapvaluesobject-iteratee_identity)
* [`_.merge`](#_mergeobject-sources)
* [`_.mergeWith`](#_mergewithobject-sources-customizer)
* [`_.omit`](#_omitobject-paths)
* [`_.omitBy`](#_omitbyobject-predicate_identity)
* [`_.pick`](#_pickobject-paths)
* [`_.pickBy`](#_pickbyobject-predicate_identity)
* [`_.result`](#_resultobject-path-defaultvalue)
* [`_.set`](#_setobject-path-value)
* [`_.setWith`](#_setwithobject-path-value-customizer)
* [`_.toPairs`](#_topairsobject)
* [`_.toPairsIn`](#_topairsinobject)
* [`_.transform`](#_transformobject-iteratee_identity-accumulator)
* [`_.unset`](#_unsetobject-path)
* [`_.update`](#_updateobject-path-updater)
* [`_.updateWith`](#_updatewithobject-path-updater-customizer)
* [`_.values`](#_valuesobject)
* [`_.valuesIn`](#_valuesinobject)


## Seq
* [`_`](#_value)
* [`_.chain`](#_chainvalue)
* [`_.tap`](#_tapvalue-interceptor)
* [`_.thru`](#_thruvalue-interceptor)
* [`_.prototype[Symbol.iterator]`](#_prototypesymboliterator)
* [`_.prototype.at`](#_prototypeatpaths)
* [`_.prototype.chain`](#_prototypechain)
* [`_.prototype.commit`](#_prototypecommit)
* [`_.prototype.next`](#_prototypenext)
* [`_.prototype.plant`](#_prototypeplantvalue)
* [`_.prototype.reverse`](#_prototypereverse)
* [`_.prototype.toJSON` -> `value`](#_prototypevalue" class="alias)
* [`_.prototype.value`](#_prototypevalue)
* [`_.prototype.valueOf` -> `value`](#_prototypevalue" class="alias)



## String
* [`_.camelCase`](#_camelcasestring)
* [`_.capitalize`](#_capitalizestring)
* [`_.deburr`](#_deburrstring)
* [`_.endsWith`](#_endswithstring-target-positionstringlength)
* [`_.escape`](#_escapestring)
* [`_.escapeRegExp`](#_escaperegexpstring)
* [`_.kebabCase`](#_kebabcasestring)
* [`_.lowerCase`](#_lowercasestring)
* [`_.lowerFirst`](#_lowerfirststring)
* [`_.pad`](#_padstring-length0-chars)
* [`_.padEnd`](#_padendstring-length0-chars)
* [`_.padStart`](#_padstartstring-length0-chars)
* [`_.parseInt`](#_parseintstring-radix10)
* [`_.repeat`](#_repeatstring-n1)
* [`_.replace`](#_replacestring-pattern-replacement)
* [`_.snakeCase`](#_snakecasestring)
* [`_.split`](#_splitstring-separator-limit)
* [`_.startCase`](#_startcasestring)
* [`_.startsWith`](#_startswithstring-target-position0)
* [`_.template`](#_templatestring-options)
* [`_.toLower`](#_tolowerstring)
* [`_.toUpper`](#_toupperstring)
* [`_.trim`](#_trimstring-charswhitespace)
* [`_.trimEnd`](#_trimendstring-charswhitespace)
* [`_.trimStart`](#_trimstartstring-charswhitespace)
* [`_.truncate`](#_truncatestring-options)
* [`_.unescape`](#_unescapestring)
* [`_.upperCase`](#_uppercasestring)
* [`_.upperFirst`](#_upperfirststring)
* [`_.words`](#_wordsstring-pattern)





## Util
* [`_.attempt`](#_attemptfunc-args)
* [`_.bindAll`](#_bindallobject-methodnames)
* [`_.cond`](#_condpairs)
* [`_.conforms`](#_conformssource)
* [`_.constant`](#_constantvalue)
* [`_.defaultTo`](#_defaulttovalue-defaultvalue)
* [`_.flow`](#_flowfuncs)
* [`_.flowRight`](#_flowrightfuncs)
* [`_.identity`](#_identityvalue)
* [`_.iteratee`](#_iterateefunc_identity)
* [`_.matches`](#_matchessource)
* [`_.matchesProperty`](#_matchespropertypath-srcvalue)
* [`_.method`](#_methodpath-args)
* [`_.methodOf`](#_methodofobject-args)
* [`_.mixin`](#_mixinobjectlodash-source-options)
* [`_.noConflict`](#_noconflict)
* [`_.noop`](#_noop)
* [`_.nthArg`](#_nthargn0)
* [`_.over`](#_overiteratees_identity)
* [`_.overEvery`](#_overeverypredicates_identity)
* [`_.overSome`](#_oversomepredicates_identity)
* [`_.property`](#_propertypath)
* [`_.propertyOf`](#_propertyofobject)
* [`_.range`](#_rangestart0-end-step1)
* [`_.rangeRight`](#_rangerightstart0-end-step1)
* [`_.runInContext`](#_runincontextcontextroot)
* [`_.stubArray`](#_stubarray)
* [`_.stubFalse`](#_stubfalse)
* [`_.stubObject`](#_stubobject)
* [`_.stubString`](#_stubstring)
* [`_.stubTrue`](#_stubtrue)
* [`_.times`](#_timesn-iteratee_identity)
* [`_.toPath`](#_topathvalue)
* [`_.uniqueId`](#_uniqueidprefix)





## Properties
* [`_.VERSION`](#_version)
* [`_.templateSettings`](#_templatesettings)
* [`_.templateSettings.escape`](#_templatesettingsescape)
* [`_.templateSettings.evaluate`](#_templatesettingsevaluate)
* [`_.templateSettings.imports`](#_templatesettingsimports)
* [`_.templateSettings.interpolate`](#_templatesettingsinterpolate)
* [`_.templateSettings.variable`](#_templatesettingsvariable)





## Methods
* [`_.templateSettings.imports._`](#_templatesettingsimports_)

# Array

## <a name="_chunkarray-size1"></a><code>_.chunk(array, [size=1])</code>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L6856 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.chunk "See the npm package") [&#x24C9;][1]

Creates an array of elements split into groups the length of `size`.
If `array` can't be split evenly, the final chunk will be the remaining
elements.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to process.
2. `[size=1]` *(number)*: The length of each chunk

#### Returns
*(Array)*: Returns the new array of chunks.


```javascript
_.chunk(['a', 'b', 'c', 'd'], 2);
// => [['a', 'b'], ['c', 'd']]

_.chunk(['a', 'b', 'c', 'd'], 3);
// => [['a', 'b', 'c'], ['d']]
```
------
## <a name="_compactarray"><code>_.compact(array)</code></a>
```javascript
_.compact([0, 1, false, 2, '', 3]);
// => [1, 2, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L6891 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.compact "See the npm package") [&#x24C9;][1]

Creates an array with all falsey values removed. The values `false`, `null`,
`0`, `""`, `undefined`, and `NaN` are falsey.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to compact.

#### Returns
*(Array)*: Returns the new array of filtered values.



------

## <a name="_concatarray-values"><code>_.concat(array, [values])</code></a>
```javascript
var array = [1];
var other = _.concat(array, 2, [3], [[4]]);

console.log(other);
// => [1, 2, 3, [4]]

console.log(array);
// => [1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L6928 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.concat "See the npm package") [&#x24C9;][1]

Creates a new array concatenating `array` with any additional arrays
and/or values.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to concatenate.
2. `[values]` *(...&#42;)*: The values to concatenate.

#### Returns
*(Array)*: Returns the new concatenated array.



------





## <a name="_differencearray-values"><code>_.difference(array, [values])</code></a>
```javascript
_.difference([2, 1], [2, 3]);
// => [1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L6964 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.difference "See the npm package") [&#x24C9;][1]

Creates an array of `array` values not included in the other given arrays
using [`SameValueZero`](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)
for equality comparisons. The order and references of result values are
determined by the first array.
<br>
<br>
**Note:** Unlike `_.pullAll`, this method returns a new array.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `[values]` *(...Array)*: The values to exclude.

#### Returns
*(Array)*: Returns the new array of filtered values.



---





## <a name="_differencebyarray-values-iteratee_identity"><code>_.differenceBy(array, [values], [iteratee=_.identity])</code></a>
```javascript
_.differenceBy([2.1, 1.2], [2.3, 3.4], Math.floor);
// => [1.2]

// The `_.property` iteratee shorthand.
_.differenceBy([{ 'x': 2 }, { 'x': 1 }], [{ 'x': 1 }], 'x');
// => [{ 'x': 2 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L6996 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.differenceby "See the npm package") [&#x24C9;][1]

This method is like `_.difference` except that it accepts `iteratee` which
is invoked for each element of `array` and `values` to generate the criterion
by which they're compared. The order and references of result values are
determined by the first array. The iteratee is invoked with one argument:
*(value)*.
<br>
<br>
**Note:** Unlike `_.pullAllBy`, this method returns a new array.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `[values]` *(...Array)*: The values to exclude.
3. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(Array)*: Returns the new array of filtered values.



---





## <a name="_differencewitharray-values-comparator"><code>_.differenceWith(array, [values], [comparator])</code></a>
```javascript
var objects = [{ 'x': 1, 'y': 2 }, { 'x': 2, 'y': 1 }];

_.differenceWith(objects, [{ 'x': 1, 'y': 2 }], _.isEqual);
// => [{ 'x': 2, 'y': 1 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7029 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.differencewith "See the npm package") [&#x24C9;][1]

This method is like `_.difference` except that it accepts `comparator`
which is invoked to compare elements of `array` to `values`. The order and
references of result values are determined by the first array. The comparator
is invoked with two arguments: *(arrVal, othVal)*.
<br>
<br>
**Note:** Unlike `_.pullAllWith`, this method returns a new array.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `[values]` *(...Array)*: The values to exclude.
3. `[comparator]` *(Function)*: The comparator invoked per element.

#### Returns
*(Array)*: Returns the new array of filtered values.



---





## <a name="_droparray-n1"><code>_.drop(array, [n=1])</code></a>
```javascript
_.drop([1, 2, 3]);
// => [2, 3]

_.drop([1, 2, 3], 2);
// => [3]

_.drop([1, 2, 3], 5);
// => []

_.drop([1, 2, 3], 0);
// => [1, 2, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7064 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.drop "See the npm package") [&#x24C9;][1]

Creates a slice of `array` with `n` elements dropped from the beginning.

#### Since
0.5.0

#### Arguments
1. `array` *(Array)*: The array to query.
2. `[n=1]` *(number)*: The number of elements to drop.

#### Returns
*(Array)*: Returns the slice of `array`.



---





## <a name="_droprightarray-n1"><code>_.dropRight(array, [n=1])</code></a>
```javascript
_.dropRight([1, 2, 3]);
// => [1, 2]

_.dropRight([1, 2, 3], 2);
// => [1]

_.dropRight([1, 2, 3], 5);
// => []

_.dropRight([1, 2, 3], 0);
// => [1, 2, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7098 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.dropright "See the npm package") [&#x24C9;][1]

Creates a slice of `array` with `n` elements dropped from the end.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to query.
2. `[n=1]` *(number)*: The number of elements to drop.

#### Returns
*(Array)*: Returns the slice of `array`.



---





## <a name="_droprightwhilearray-predicate_identity"><code>_.dropRightWhile(array, [predicate=_.identity])</code></a>
```javascript
var users = [
  { 'user': 'barney',  'active': true },
  { 'user': 'fred',    'active': false },
  { 'user': 'pebbles', 'active': false }
];

_.dropRightWhile(users, function(o) { return !o.active; });
// => objects for ['barney']

// The `_.matches` iteratee shorthand.
_.dropRightWhile(users, { 'user': 'pebbles', 'active': false });
// => objects for ['barney', 'fred']

// The `_.matchesProperty` iteratee shorthand.
_.dropRightWhile(users, ['active', false]);
// => objects for ['barney']

// The `_.property` iteratee shorthand.
_.dropRightWhile(users, 'active');
// => objects for ['barney', 'fred', 'pebbles']
```

[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7143 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.droprightwhile "See the npm package") [&#x24C9;][1]

Creates a slice of `array` excluding elements dropped from the end.
Elements are dropped until `predicate` returns falsey. The predicate is
invoked with three arguments: *(value, index, array)*.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to query.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the slice of `array`.

---





## <a name="_dropwhilearray-predicate_identity"><code>_.dropWhile(array, [predicate=_.identity])</code></a>
```javascript
var users = [
  { 'user': 'barney',  'active': false },
  { 'user': 'fred',    'active': false },
  { 'user': 'pebbles', 'active': true }
];

_.dropWhile(users, function(o) { return !o.active; });
// => objects for ['pebbles']

// The `_.matches` iteratee shorthand.
_.dropWhile(users, { 'user': 'barney', 'active': false });
// => objects for ['fred', 'pebbles']

// The `_.matchesProperty` iteratee shorthand.
_.dropWhile(users, ['active', false]);
// => objects for ['pebbles']

// The `_.property` iteratee shorthand.
_.dropWhile(users, 'active');
// => objects for ['barney', 'fred', 'pebbles']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7184 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.dropwhile "See the npm package") [&#x24C9;][1]

Creates a slice of `array` excluding elements dropped from the beginning.
Elements are dropped until `predicate` returns falsey. The predicate is
invoked with three arguments: *(value, index, array)*.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to query.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the slice of `array`.



---





## <a name="_fillarray-value-start0-endarraylength"><code>_.fill(array, value, [start=0], [end=array.length])</code></a>
```javascript
var array = [1, 2, 3];

_.fill(array, 'a');
console.log(array);
// => ['a', 'a', 'a']

_.fill(Array(3), 2);
// => [2, 2, 2]

_.fill([4, 6, 8, 10], '*', 1, 3);
// => [4, '*', '*', 10]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7219 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.fill "See the npm package") [&#x24C9;][1]

Fills elements of `array` with `value` from `start` up to, but not
including, `end`.
<br>
<br>
**Note:** This method mutates `array`.

#### Since
3.2.0

#### Arguments
1. `array` *(Array)*: The array to fill.
2. `value` *(&#42;)*: The value to fill `array` with.
3. `[start=0]` *(number)*: The start position.
4. `[end=array.length]` *(number)*: The end position.

#### Returns
*(Array)*: Returns `array`.



---





## <a name="_findindexarray-predicate_identity-fromindex0"><code>_.findIndex(array, [predicate=_.identity], [fromIndex=0])</code></a>
```javascript
var users = [
  { 'user': 'barney',  'active': false },
  { 'user': 'fred',    'active': false },
  { 'user': 'pebbles', 'active': true }
];

_.findIndex(users, function(o) { return o.user == 'barney'; });
// => 0

// The `_.matches` iteratee shorthand.
_.findIndex(users, { 'user': 'fred', 'active': false });
// => 1

// The `_.matchesProperty` iteratee shorthand.
_.findIndex(users, ['active', false]);
// => 0

// The `_.property` iteratee shorthand.
_.findIndex(users, 'active');
// => 2
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7266 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.findindex "See the npm package") [&#x24C9;][1]

This method is like `_.find` except that it returns the index of the first
element `predicate` returns truthy for instead of the element itself.

#### Since
1.1.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.
3. `[fromIndex=0]` *(number)*: The index to search from.

#### Returns
*(number)*: Returns the index of the found element, else `-1`.



---





## <a name="_findlastindexarray-predicate_identity-fromindexarraylength-1"><code>_.findLastIndex(array, [predicate=_.identity], [fromIndex=array.length-1])</code></a>
```javascript
var users = [
  { 'user': 'barney',  'active': true },
  { 'user': 'fred',    'active': false },
  { 'user': 'pebbles', 'active': false }
];

_.findLastIndex(users, function(o) { return o.user == 'pebbles'; });
// => 2

// The `_.matches` iteratee shorthand.
_.findLastIndex(users, { 'user': 'barney', 'active': true });
// => 0

// The `_.matchesProperty` iteratee shorthand.
_.findLastIndex(users, ['active', false]);
// => 2

// The `_.property` iteratee shorthand.
_.findLastIndex(users, 'active');
// => 0
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7313 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.findlastindex "See the npm package") [&#x24C9;][1]

This method is like `_.findIndex` except that it iterates over elements
of `collection` from right to left.

#### Since
2.0.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.
3. `[fromIndex=array.length-1]` *(number)*: The index to search from.

#### Returns
*(number)*: Returns the index of the found element, else `-1`.



---





## <a name="_flattenarray"><code>_.flatten(array)</code></a>
```javascript
_.flatten([1, [2, [3, [4]], 5]]);
// => [1, 2, [3, [4]], 5]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7342 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.flatten "See the npm package") [&#x24C9;][1]

Flattens `array` a single level deep.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to flatten.

#### Returns
*(Array)*: Returns the new flattened array.



---





## <a name="_flattendeeparray"><code>_.flattenDeep(array)</code></a>
```javascript
_.flattenDeep([1, [2, [3, [4]], 5]]);
// => [1, 2, 3, 4, 5]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7361 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.flattendeep "See the npm package") [&#x24C9;][1]

Recursively flattens `array`.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to flatten.

#### Returns
*(Array)*: Returns the new flattened array.



---





## <a name="_flattendeptharray-depth1"><code>_.flattenDepth(array, [depth=1])</code></a>
```javascript
var array = [1, [2, [3, [4]], 5]];

_.flattenDepth(array, 1);
// => [1, 2, [3, [4]], 5]

_.flattenDepth(array, 2);
// => [1, 2, 3, [4], 5]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7386 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.flattendepth "See the npm package") [&#x24C9;][1]

Recursively flatten `array` up to `depth` times.

#### Since
4.4.0

#### Arguments
1. `array` *(Array)*: The array to flatten.
2. `[depth=1]` *(number)*: The maximum recursion depth.

#### Returns
*(Array)*: Returns the new flattened array.



---





## <a name="_frompairspairs"><code>_.fromPairs(pairs)</code></a>
```javascript
_.fromPairs([['a', 1], ['b', 2]]);
// => { 'a': 1, 'b': 2 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7410 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.frompairs "See the npm package") [&#x24C9;][1]

The inverse of `_.toPairs`; this method returns an object composed
from key-value `pairs`.

#### Since
4.0.0

#### Arguments
1. `pairs` *(Array)*: The key-value pairs.

#### Returns
*(Object)*: Returns the new object.



---





## <a name="_headarray"><code>_.head(array)</code></a>
```javascript
_.head([1, 2, 3]);
// => 1

_.head([]);
// => undefined
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7440 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.head "See the npm package") [&#x24C9;][1]

Gets the first element of `array`.

#### Since
0.1.0

#### Aliases
*_.first*

#### Arguments
1. `array` *(Array)*: The array to query.

#### Returns
*(&#42;)*: Returns the first element of `array`.



---





## <a name="_indexofarray-value-fromindex0"><code>_.indexOf(array, value, [fromIndex=0])</code></a>
```javascript
_.indexOf([1, 2, 1, 2], 2);
// => 1

// Search from the `fromIndex`.
_.indexOf([1, 2, 1, 2], 2, 2);
// => 3
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7467 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.indexof "See the npm package") [&#x24C9;][1]

Gets the index at which the first occurrence of `value` is found in `array`
using [`SameValueZero`](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)
for equality comparisons. If `fromIndex` is negative, it's used as the
offset from the end of `array`.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `value` *(&#42;)*: The value to search for.
3. `[fromIndex=0]` *(number)*: The index to search from.

#### Returns
*(number)*: Returns the index of the matched value, else `-1`.



---





## <a name="_initialarray"><code>_.initial(array)</code></a>
```javascript
_.initial([1, 2, 3]);
// => [1, 2]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7493 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.initial "See the npm package") [&#x24C9;][1]

Gets all but the last element of `array`.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to query.

#### Returns
*(Array)*: Returns the slice of `array`.



---





## <a name="_intersectionarrays"><code>_.intersection([arrays])</code></a>
```javascript
_.intersection([2, 1], [2, 3]);
// => [2]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7515 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.intersection "See the npm package") [&#x24C9;][1]

Creates an array of unique values that are included in all given arrays
using [`SameValueZero`](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)
for equality comparisons. The order and references of result values are
determined by the first array.

#### Since
0.1.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to inspect.

#### Returns
*(Array)*: Returns the new array of intersecting values.



---





## <a name="_intersectionbyarrays-iteratee_identity"><code>_.intersectionBy([arrays], [iteratee=_.identity])</code></a>
```javascript
_.intersectionBy([2.1, 1.2], [2.3, 3.4], Math.floor);
// => [2.1]

// The `_.property` iteratee shorthand.
_.intersectionBy([{ 'x': 1 }], [{ 'x': 2 }, { 'x': 1 }], 'x');
// => [{ 'x': 1 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7545 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.intersectionby "See the npm package") [&#x24C9;][1]

This method is like `_.intersection` except that it accepts `iteratee`
which is invoked for each element of each `arrays` to generate the criterion
by which they're compared. The order and references of result values are
determined by the first array. The iteratee is invoked with one argument:<br>
*(value)*.

#### Since
4.0.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to inspect.
2. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(Array)*: Returns the new array of intersecting values.



---





## <a name="_intersectionwitharrays-comparator"><code>_.intersectionWith([arrays], [comparator])</code></a>
```javascript
var objects = [{ 'x': 1, 'y': 2 }, { 'x': 2, 'y': 1 }];
var others = [{ 'x': 1, 'y': 1 }, { 'x': 1, 'y': 2 }];

_.intersectionWith(objects, others, _.isEqual);
// => [{ 'x': 1, 'y': 2 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7580 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.intersectionwith "See the npm package") [&#x24C9;][1]

This method is like `_.intersection` except that it accepts `comparator`
which is invoked to compare elements of `arrays`. The order and references
of result values are determined by the first array. The comparator is
invoked with two arguments: *(arrVal, othVal)*.

#### Since
4.0.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to inspect.
2. `[comparator]` *(Function)*: The comparator invoked per element.

#### Returns
*(Array)*: Returns the new array of intersecting values.



---





## <a name="_joinarray-separator-"><code>_.join(array, [separator=','])</code></a>
```javascript
_.join(['a', 'b', 'c'], '~');
// => 'a~b~c'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7608 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.join "See the npm package") [&#x24C9;][1]

Converts all elements in `array` into a string separated by `separator`.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to convert.
2. `[separator=',']` *(string)*: The element separator.

#### Returns
*(string)*: Returns the joined string.



---





## <a name="_lastarray"><code>_.last(array)</code></a>
```javascript
_.last([1, 2, 3]);
// => 3
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7626 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.last "See the npm package") [&#x24C9;][1]

Gets the last element of `array`.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to query.

#### Returns
*(&#42;)*: Returns the last element of `array`.



---





## <a name="_lastindexofarray-value-fromindexarraylength-1"><code>_.lastIndexOf(array, value, [fromIndex=array.length-1])</code></a>
```javascript
_.lastIndexOf([1, 2, 1, 2], 2);
// => 3

// Search from the `fromIndex`.
_.lastIndexOf([1, 2, 1, 2], 2, 2);
// => 1
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7652 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.lastindexof "See the npm package") [&#x24C9;][1]

This method is like `_.indexOf` except that it iterates over elements of
`array` from right to left.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `value` *(&#42;)*: The value to search for.
3. `[fromIndex=array.length-1]` *(number)*: The index to search from.

#### Returns
*(number)*: Returns the index of the matched value, else `-1`.



---





## <a name="_ntharray-n0"><code>_.nth(array, [n=0])</code></a>
```javascript
var array = ['a', 'b', 'c', 'd'];

_.nth(array, 1);
// => 'b'

_.nth(array, -2);
// => 'c';
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7688 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.nth "See the npm package") [&#x24C9;][1]

Gets the element at index `n` of `array`. If `n` is negative, the nth
element from the end is returned.

#### Since
4.11.0

#### Arguments
1. `array` *(Array)*: The array to query.
2. `[n=0]` *(number)*: The index of the element to return.

#### Returns
*(&#42;)*: Returns the nth element of `array`.



---





## <a name="_pullarray-values"><code>_.pull(array, [values])</code></a>
```javascript
var array = ['a', 'b', 'c', 'a', 'b', 'c'];

_.pull(array, 'a', 'c');
console.log(array);
// => ['b', 'b']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7715 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.pull "See the npm package") [&#x24C9;][1]

Removes all given values from `array` using
[`SameValueZero`](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)
for equality comparisons.
<br>
<br>
**Note:** Unlike `_.without`, this method mutates `array`. Use `_.remove`
to remove elements from an array by predicate.

#### Since
2.0.0

#### Arguments
1. `array` *(Array)*: The array to modify.
2. `[values]` *(...&#42;)*: The values to remove.

#### Returns
*(Array)*: Returns `array`.



---





## <a name="_pullallarray-values"><code>_.pullAll(array, values)</code></a>
```javascript
var array = ['a', 'b', 'c', 'a', 'b', 'c'];

_.pullAll(array, ['a', 'c']);
console.log(array);
// => ['b', 'b']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7737 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.pullall "See the npm package") [&#x24C9;][1]

This method is like `_.pull` except that it accepts an array of values to remove.
<br>
<br>
**Note:** Unlike `_.difference`, this method mutates `array`.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to modify.
2. `values` *(Array)*: The values to remove.

#### Returns
*(Array)*: Returns `array`.



---





## <a name="_pullallbyarray-values-iteratee_identity"><code>_.pullAllBy(array, values, [iteratee=_.identity])</code></a>
```javascript
var array = [{ 'x': 1 }, { 'x': 2 }, { 'x': 3 }, { 'x': 1 }];

_.pullAllBy(array, [{ 'x': 1 }, { 'x': 3 }], 'x');
console.log(array);
// => [{ 'x': 2 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7766 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.pullallby "See the npm package") [&#x24C9;][1]

This method is like `_.pullAll` except that it accepts `iteratee` which is
invoked for each element of `array` and `values` to generate the criterion
by which they're compared. The iteratee is invoked with one argument: *(value)*.
<br>
<br>
**Note:** Unlike `_.differenceBy`, this method mutates `array`.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to modify.
2. `values` *(Array)*: The values to remove.
3. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(Array)*: Returns `array`.



---





## <a name="_pullallwitharray-values-comparator"><code>_.pullAllWith(array, values, [comparator])</code></a>
```javascript
var array = [{ 'x': 1, 'y': 2 }, { 'x': 3, 'y': 4 }, { 'x': 5, 'y': 6 }];

_.pullAllWith(array, [{ 'x': 3, 'y': 4 }], _.isEqual);
console.log(array);
// => [{ 'x': 1, 'y': 2 }, { 'x': 5, 'y': 6 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7795 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.pullallwith "See the npm package") [&#x24C9;][1]

This method is like `_.pullAll` except that it accepts `comparator` which
is invoked to compare elements of `array` to `values`. The comparator is
invoked with two arguments: *(arrVal, othVal)*.
<br>
<br>
**Note:** Unlike `_.differenceWith`, this method mutates `array`.

#### Since
4.6.0

#### Arguments
1. `array` *(Array)*: The array to modify.
2. `values` *(Array)*: The values to remove.
3. `[comparator]` *(Function)*: The comparator invoked per element.

#### Returns
*(Array)*: Returns `array`.



---





## <a name="_pullatarray-indexes"><code>_.pullAt(array, [indexes])</code></a>
```javascript
var array = ['a', 'b', 'c', 'd'];
var pulled = _.pullAt(array, [1, 3]);

console.log(array);
// => ['a', 'c']

console.log(pulled);
// => ['b', 'd']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7825 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.pullat "See the npm package") [&#x24C9;][1]

Removes elements from `array` corresponding to `indexes` and returns an
array of removed elements.
<br>
<br>
**Note:** Unlike `_.at`, this method mutates `array`.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to modify.
2. `[indexes]` *(...(number|number&#91;&#93;))*: The indexes of elements to remove.

#### Returns
*(Array)*: Returns the new array of removed elements.



---





## <a name="_removearray-predicate_identity"><code>_.remove(array, [predicate=_.identity])</code></a>
```javascript
var array = [1, 2, 3, 4];
var evens = _.remove(array, function(n) {
  return n % 2 == 0;
});

console.log(array);
// => [1, 3]

console.log(evens);
// => [2, 4]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7864 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.remove "See the npm package") [&#x24C9;][1]

Removes all elements from `array` that `predicate` returns truthy for
and returns an array of the removed elements. The predicate is invoked
with three arguments: *(value, index, array)*.
<br>
<br>
**Note:** Unlike `_.filter`, this method mutates `array`. Use `_.pull`
to pull elements from an array by value.

#### Since
2.0.0

#### Arguments
1. `array` *(Array)*: The array to modify.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the new array of removed elements.



---





## <a name="_reversearray"><code>_.reverse(array)</code></a>
```javascript
var array = [1, 2, 3];

_.reverse(array);
// => [3, 2, 1]

console.log(array);
// => [3, 2, 1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7908 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.reverse "See the npm package") [&#x24C9;][1]

Reverses `array` so that the first element becomes the last, the second
element becomes the second to last, and so on.
<br>
<br>
**Note:** This method mutates `array` and is based on
[`Array#reverse`](https://mdn.io/Array/reverse).

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to modify.

#### Returns
*(Array)*: Returns `array`.



---





## <a name="_slicearray-start0-endarraylength"><code>_.slice(array, [start=0], [end=array.length])</code></a>
```javascript
_.sortedIndex([30, 50], 40);
// => 1
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7928 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.slice "See the npm package") [&#x24C9;][1]

Creates a slice of `array` from `start` up to, but not including, `end`.
<br>
<br>
**Note:** This method is used instead of
[`Array#slice`](https://mdn.io/Array/slice) to ensure dense arrays are
returned.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to slice.
2. `[start=0]` *(number)*: The start position.
3. `[end=array.length]` *(number)*: The end position.

#### Returns
*(Array)*: Returns the slice of `array`.







## <a name="_sortedindexarray-value"><code>_.sortedIndex(array, value)</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7961 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sortedindex "See the npm package") [&#x24C9;][1]

Uses a binary search to determine the lowest index at which `value`
should be inserted into `array` in order to maintain its sort order.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The sorted array to inspect.
2. `value` *(&#42;)*: The value to evaluate.

#### Returns
*(number)*: Returns the index at which `value` should be inserted into `array`.



---





## <a name="_sortedindexbyarray-value-iteratee_identity"><code>_.sortedIndexBy(array, value, [iteratee=_.identity])</code></a>
```javascript
var objects = [{ 'x': 4 }, { 'x': 5 }];

_.sortedIndexBy(objects, { 'x': 4 }, function(o) { return o.x; });
// => 0

// The `_.property` iteratee shorthand.
_.sortedIndexBy(objects, { 'x': 4 }, 'x');
// => 0
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L7990 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sortedindexby "See the npm package") [&#x24C9;][1]

This method is like `_.sortedIndex` except that it accepts `iteratee`
which is invoked for `value` and each element of `array` to compute their
sort ranking. The iteratee is invoked with one argument: *(value)*.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The sorted array to inspect.
2. `value` *(&#42;)*: The value to evaluate.
3. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(number)*: Returns the index at which `value` should be inserted into `array`.



---





## <a name="_sortedindexofarray-value"><code>_.sortedIndexOf(array, value)</code></a>
```javascript
_.sortedIndexOf([4, 5, 5, 5, 6], 5);
// => 1
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8010 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sortedindexof "See the npm package") [&#x24C9;][1]

This method is like `_.indexOf` except that it performs a binary
search on a sorted `array`.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `value` *(&#42;)*: The value to search for.

#### Returns
*(number)*: Returns the index of the matched value, else `-1`.



---





## <a name="_sortedlastindexarray-value"><code>_.sortedLastIndex(array, value)</code></a>
```javascript
_.sortedLastIndex([4, 5, 5, 5, 6], 5);
// => 4
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8039 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sortedlastindex "See the npm package") [&#x24C9;][1]

This method is like `_.sortedIndex` except that it returns the highest
index at which `value` should be inserted into `array` in order to
maintain its sort order.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The sorted array to inspect.
2. `value` *(&#42;)*: The value to evaluate.

#### Returns
*(number)*: Returns the index at which `value` should be inserted into `array`.



---





## <a name="_sortedlastindexbyarray-value-iteratee_identity"><code>_.sortedLastIndexBy(array, value, [iteratee=_.identity])</code></a>
```javascript
var objects = [{ 'x': 4 }, { 'x': 5 }];

_.sortedLastIndexBy(objects, { 'x': 4 }, function(o) { return o.x; });
// => 1

// The `_.property` iteratee shorthand.
_.sortedLastIndexBy(objects, { 'x': 4 }, 'x');
// => 1
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8068 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sortedlastindexby "See the npm package") [&#x24C9;][1]

This method is like `_.sortedLastIndex` except that it accepts `iteratee`
which is invoked for `value` and each element of `array` to compute their
sort ranking. The iteratee is invoked with one argument: *(value)*.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The sorted array to inspect.
2. `value` *(&#42;)*: The value to evaluate.
3. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(number)*: Returns the index at which `value` should be inserted into `array`.



---





## <a name="_sortedlastindexofarray-value"><code>_.sortedLastIndexOf(array, value)</code></a>
```javascript
_.sortedLastIndexOf([4, 5, 5, 5, 6], 5);
// => 3
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8088 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sortedlastindexof "See the npm package") [&#x24C9;][1]

This method is like `_.lastIndexOf` except that it performs a binary
search on a sorted `array`.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `value` *(&#42;)*: The value to search for.

#### Returns
*(number)*: Returns the index of the matched value, else `-1`.



---





## <a name="_sorteduniqarray"><code>_.sortedUniq(array)</code></a>
```javascript
_.sortedUniq([1, 1, 2]);
// => [1, 2]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8114 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sorteduniq "See the npm package") [&#x24C9;][1]

This method is like `_.uniq` except that it's designed and optimized
for sorted arrays.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to inspect.

#### Returns
*(Array)*: Returns the new duplicate free array.



---





## <a name="_sorteduniqbyarray-iteratee"><code>_.sortedUniqBy(array, [iteratee])</code></a>
```javascript
_.sortedUniqBy([1.1, 1.2, 2.3, 2.4], Math.floor);
// => [1.1, 2.3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8136 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sorteduniqby "See the npm package") [&#x24C9;][1]

This method is like `_.uniqBy` except that it's designed and optimized
for sorted arrays.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `[iteratee]` *(Function)*: The iteratee invoked per element.

#### Returns
*(Array)*: Returns the new duplicate free array.



---





## <a name="_tailarray"><code>_.tail(array)</code></a>
```javascript
_.tail([1, 2, 3]);
// => [2, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8156 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.tail "See the npm package") [&#x24C9;][1]

Gets all but the first element of `array`.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to query.

#### Returns
*(Array)*: Returns the slice of `array`.



---





## <a name="_takearray-n1"><code>_.take(array, [n=1])</code></a>
```javascript
_.take([1, 2, 3]);
// => [1]

_.take([1, 2, 3], 2);
// => [1, 2]

_.take([1, 2, 3], 5);
// => [1, 2, 3]

_.take([1, 2, 3], 0);
// => []
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8186 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.take "See the npm package") [&#x24C9;][1]

Creates a slice of `array` with `n` elements taken from the beginning.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to query.
2. `[n=1]` *(number)*: The number of elements to take.

#### Returns
*(Array)*: Returns the slice of `array`.



---





## <a name="_takerightarray-n1"><code>_.takeRight(array, [n=1])</code></a>
```javascript
_.takeRight([1, 2, 3]);
// => [3]

_.takeRight([1, 2, 3], 2);
// => [2, 3]

_.takeRight([1, 2, 3], 5);
// => [1, 2, 3]

_.takeRight([1, 2, 3], 0);
// => []
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8219 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.takeright "See the npm package") [&#x24C9;][1]

Creates a slice of `array` with `n` elements taken from the end.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to query.
2. `[n=1]` *(number)*: The number of elements to take.

#### Returns
*(Array)*: Returns the slice of `array`.



---





## <a name="_takerightwhilearray-predicate_identity"><code>_.takeRightWhile(array, [predicate=_.identity])</code></a>
```javascript
var users = [
  { 'user': 'barney',  'active': true },
  { 'user': 'fred',    'active': false },
  { 'user': 'pebbles', 'active': false }
];

_.takeRightWhile(users, function(o) { return !o.active; });
// => objects for ['fred', 'pebbles']

// The `_.matches` iteratee shorthand.
_.takeRightWhile(users, { 'user': 'pebbles', 'active': false });
// => objects for ['pebbles']

// The `_.matchesProperty` iteratee shorthand.
_.takeRightWhile(users, ['active', false]);
// => objects for ['fred', 'pebbles']

// The `_.property` iteratee shorthand.
_.takeRightWhile(users, 'active');
// => []
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8264 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.takerightwhile "See the npm package") [&#x24C9;][1]

Creates a slice of `array` with elements taken from the end. Elements are
taken until `predicate` returns falsey. The predicate is invoked with
three arguments: *(value, index, array)*.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to query.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the slice of `array`.



---





## <a name="_takewhilearray-predicate_identity"><code>_.takeWhile(array, [predicate=_.identity])</code></a>
```javascript
var users = [
  { 'user': 'barney',  'active': false },
  { 'user': 'fred',    'active': false },
  { 'user': 'pebbles', 'active': true }
];

_.takeWhile(users, function(o) { return !o.active; });
// => objects for ['barney', 'fred']

// The `_.matches` iteratee shorthand.
_.takeWhile(users, { 'user': 'barney', 'active': false });
// => objects for ['barney']

// The `_.matchesProperty` iteratee shorthand.
_.takeWhile(users, ['active', false]);
// => objects for ['barney', 'fred']

// The `_.property` iteratee shorthand.
_.takeWhile(users, 'active');
// => []
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8305 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.takewhile "See the npm package") [&#x24C9;][1]

Creates a slice of `array` with elements taken from the beginning. Elements
are taken until `predicate` returns falsey. The predicate is invoked with
three arguments: *(value, index, array)*.

#### Since
3.0.0

#### Arguments
1. `array` *(Array)*: The array to query.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the slice of `array`.



---





## <a name="_unionarrays"><code>_.union([arrays])</code></a>
```javascript
_.union([2], [1, 2]);
// => [2, 1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8327 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.union "See the npm package") [&#x24C9;][1]

Creates an array of unique values, in order, from all given arrays using
[`SameValueZero`](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)
for equality comparisons.

#### Since
0.1.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to inspect.

#### Returns
*(Array)*: Returns the new array of combined values.



---





## <a name="_unionbyarrays-iteratee_identity"><code>_.unionBy([arrays], [iteratee=_.identity])</code></a>
```javascript
_.unionBy([2.1], [1.2, 2.3], Math.floor);
// => [2.1, 1.2]

// The `_.property` iteratee shorthand.
_.unionBy([{ 'x': 1 }], [{ 'x': 2 }, { 'x': 1 }], 'x');
// => [{ 'x': 1 }, { 'x': 2 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8354 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.unionby "See the npm package") [&#x24C9;][1]

This method is like `_.union` except that it accepts `iteratee` which is
invoked for each element of each `arrays` to generate the criterion by
which uniqueness is computed. Result values are chosen from the first
array in which the value occurs. The iteratee is invoked with one argument:<br>
*(value)*.

#### Since
4.0.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to inspect.
2. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(Array)*: Returns the new array of combined values.



---





## <a name="_unionwitharrays-comparator"><code>_.unionWith([arrays], [comparator])</code></a>
```javascript
var objects = [{ 'x': 1, 'y': 2 }, { 'x': 2, 'y': 1 }];
var others = [{ 'x': 1, 'y': 1 }, { 'x': 1, 'y': 2 }];

_.unionWith(objects, others, _.isEqual);
// => [{ 'x': 1, 'y': 2 }, { 'x': 2, 'y': 1 }, { 'x': 1, 'y': 1 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8383 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.unionwith "See the npm package") [&#x24C9;][1]

This method is like `_.union` except that it accepts `comparator` which
is invoked to compare elements of `arrays`. Result values are chosen from
the first array in which the value occurs. The comparator is invoked
with two arguments: *(arrVal, othVal)*.

#### Since
4.0.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to inspect.
2. `[comparator]` *(Function)*: The comparator invoked per element.

#### Returns
*(Array)*: Returns the new array of combined values.



---





## <a name="_uniqarray"><code>_.uniq(array)</code></a>
```javascript
_.uniq([2, 1, 2]);
// => [2, 1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8407 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.uniq "See the npm package") [&#x24C9;][1]

Creates a duplicate-free version of an array, using
[`SameValueZero`](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)
for equality comparisons, in which only the first occurrence of each element
is kept. The order of result values is determined by the order they occur
in the array.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to inspect.

#### Returns
*(Array)*: Returns the new duplicate free array.



---





## <a name="_uniqbyarray-iteratee_identity"><code>_.uniqBy(array, [iteratee=_.identity])</code></a>
```javascript
_.uniqBy([2.1, 1.2, 2.3], Math.floor);
// => [2.1, 1.2]

// The `_.property` iteratee shorthand.
_.uniqBy([{ 'x': 1 }, { 'x': 2 }, { 'x': 1 }], 'x');
// => [{ 'x': 1 }, { 'x': 2 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8434 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.uniqby "See the npm package") [&#x24C9;][1]

This method is like `_.uniq` except that it accepts `iteratee` which is
invoked for each element in `array` to generate the criterion by which
uniqueness is computed. The order of result values is determined by the
order they occur in the array. The iteratee is invoked with one argument:<br>
*(value)*.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(Array)*: Returns the new duplicate free array.



---





## <a name="_uniqwitharray-comparator"><code>_.uniqWith(array, [comparator])</code></a>
```javascript
var objects = [{ 'x': 1, 'y': 2 }, { 'x': 2, 'y': 1 }, { 'x': 1, 'y': 2 }];

_.uniqWith(objects, _.isEqual);
// => [{ 'x': 1, 'y': 2 }, { 'x': 2, 'y': 1 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8458 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.uniqwith "See the npm package") [&#x24C9;][1]

This method is like `_.uniq` except that it accepts `comparator` which
is invoked to compare elements of `array`. The order of result values is
determined by the order they occur in the array.The comparator is invoked
with two arguments: *(arrVal, othVal)*.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `[comparator]` *(Function)*: The comparator invoked per element.

#### Returns
*(Array)*: Returns the new duplicate free array.



---





## <a name="_unziparray"><code>_.unzip(array)</code></a>
```javascript
var zipped = _.zip(['a', 'b'], [1, 2], [true, false]);
// => [['a', 1, true], ['b', 2, false]]

_.unzip(zipped);
// => [['a', 'b'], [1, 2], [true, false]]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8482 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.unzip "See the npm package") [&#x24C9;][1]

This method is like `_.zip` except that it accepts an array of grouped
elements and creates an array regrouping the elements to their pre-zip
configuration.

#### Since
1.2.0

#### Arguments
1. `array` *(Array)*: The array of grouped elements to process.

#### Returns
*(Array)*: Returns the new array of regrouped elements.



---





## <a name="_unzipwitharray-iteratee_identity"><code>_.unzipWith(array, [iteratee=_.identity])</code></a>
```javascript
var zipped = _.zip([1, 2], [10, 20], [100, 200]);
// => [[1, 10, 100], [2, 20, 200]]

_.unzipWith(zipped, _.add);
// => [3, 30, 300]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8519 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.unzipwith "See the npm package") [&#x24C9;][1]

This method is like `_.unzip` except that it accepts `iteratee` to specify
how regrouped values should be combined. The iteratee is invoked with the
elements of each group: *(...group)*.

#### Since
3.8.0

#### Arguments
1. `array` *(Array)*: The array of grouped elements to process.
2. `[iteratee=_.identity]` *(Function)*: The function to combine regrouped values.

#### Returns
*(Array)*: Returns the new array of regrouped elements.



---





## <a name="_withoutarray-values"><code>_.without(array, [values])</code></a>
```javascript
_.without([2, 1, 2, 3], 1, 2);
// => [3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8552 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.without "See the npm package") [&#x24C9;][1]

Creates an array excluding all given values using
[`SameValueZero`](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)
for equality comparisons.
<br>
<br>
**Note:** Unlike `_.pull`, this method returns a new array.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to inspect.
2. `[values]` *(...&#42;)*: The values to exclude.

#### Returns
*(Array)*: Returns the new array of filtered values.



---





## <a name="_xorarrays"><code>_.xor([arrays])</code></a>
```javascript
_.xor([2, 1], [2, 3]);
// => [1, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8576 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.xor "See the npm package") [&#x24C9;][1]

Creates an array of unique values that is the
[symmetric difference](https://en.wikipedia.org/wiki/Symmetric_difference)
of the given arrays. The order of result values is determined by the order
they occur in the arrays.

#### Since
2.4.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to inspect.

#### Returns
*(Array)*: Returns the new array of filtered values.



---





## <a name="_xorbyarrays-iteratee_identity"><code>_.xorBy([arrays], [iteratee=_.identity])</code></a>
```javascript
_.xorBy([2.1, 1.2], [2.3, 3.4], Math.floor);
// => [1.2, 3.4]

// The `_.property` iteratee shorthand.
_.xorBy([{ 'x': 1 }], [{ 'x': 2 }, { 'x': 1 }], 'x');
// => [{ 'x': 2 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8603 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.xorby "See the npm package") [&#x24C9;][1]

This method is like `_.xor` except that it accepts `iteratee` which is
invoked for each element of each `arrays` to generate the criterion by
which by which they're compared. The order of result values is determined
by the order they occur in the arrays. The iteratee is invoked with one
argument: *(value)*.

#### Since
4.0.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to inspect.
2. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(Array)*: Returns the new array of filtered values.



---





## <a name="_xorwitharrays-comparator"><code>_.xorWith([arrays], [comparator])</code></a>
```javascript
var objects = [{ 'x': 1, 'y': 2 }, { 'x': 2, 'y': 1 }];
var others = [{ 'x': 1, 'y': 1 }, { 'x': 1, 'y': 2 }];

_.xorWith(objects, others, _.isEqual);
// => [{ 'x': 2, 'y': 1 }, { 'x': 1, 'y': 1 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8632 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.xorwith "See the npm package") [&#x24C9;][1]

This method is like `_.xor` except that it accepts `comparator` which is
invoked to compare elements of `arrays`. The order of result values is
determined by the order they occur in the arrays. The comparator is invoked
with two arguments: *(arrVal, othVal)*.

#### Since
4.0.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to inspect.
2. `[comparator]` *(Function)*: The comparator invoked per element.

#### Returns
*(Array)*: Returns the new array of filtered values.



---





## <a name="_ziparrays"><code>_.zip([arrays])</code></a>
```javascript
_.zip(['a', 'b'], [1, 2], [true, false]);
// => [['a', 1, true], ['b', 2, false]]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8654 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.zip "See the npm package") [&#x24C9;][1]

Creates an array of grouped elements, the first of which contains the
first elements of the given arrays, the second of which contains the
second elements of the given arrays, and so on.

#### Since
0.1.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to process.

#### Returns
*(Array)*: Returns the new array of grouped elements.



---





## <a name="_zipobjectprops-values"><code>_.zipObject([props=[]], [values=[]])</code></a>
```javascript
_.zipObject(['a', 'b'], [1, 2]);
// => { 'a': 1, 'b': 2 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8672 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.zipobject "See the npm package") [&#x24C9;][1]

This method is like `_.fromPairs` except that it accepts two arrays,
one of property identifiers and one of corresponding values.

#### Since
0.4.0

#### Arguments
1. `[props=[]]` *(Array)*: The property identifiers.
2. `[values=[]]` *(Array)*: The property values.

#### Returns
*(Object)*: Returns the new object.



---





## <a name="_zipobjectdeepprops-values"><code>_.zipObjectDeep([props=[]], [values=[]])</code></a>
```javascript
_.zipObjectDeep(['a.b[0].c', 'a.b[1].d'], [1, 2]);
// => { 'a': { 'b': [{ 'c': 1 }, { 'd': 2 }] } }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8691 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.zipobjectdeep "See the npm package") [&#x24C9;][1]

This method is like `_.zipObject` except that it supports property paths.

#### Since
4.1.0

#### Arguments
1. `[props=[]]` *(Array)*: The property identifiers.
2. `[values=[]]` *(Array)*: The property values.

#### Returns
*(Object)*: Returns the new object.



---





## <a name="_zipwitharrays-iteratee_identity"><code>_.zipWith([arrays], [iteratee=_.identity])</code></a>
```javascript
_.zipWith([1, 2], [10, 20], [100, 200], function(a, b, c) {
  return a + b + c;
});
// => [111, 222]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8715 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.zipwith "See the npm package") [&#x24C9;][1]

This method is like `_.zip` except that it accepts `iteratee` to specify
how grouped values should be combined. The iteratee is invoked with the
elements of each group: *(...group)*.

#### Since
3.8.0

#### Arguments
1. `[arrays]` *(...Array)*: The arrays to process.
2. `[iteratee=_.identity]` *(Function)*: The function to combine grouped values.

#### Returns
*(Array)*: Returns the new array of grouped elements.



---







# Collections



## <a name="_countbycollection-iteratee_identity"><code>_.countBy(collection, [iteratee=_.identity])</code></a>
```javascript
_.countBy([6.1, 4.2, 6.3], Math.floor);
// => { '4': 1, '6': 2 }

// The `_.property` iteratee shorthand.
_.countBy(['one', 'two', 'three'], 'length');
// => { '3': 2, '5': 1 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9094 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.countby "See the npm package") [&#x24C9;][1]

Creates an object composed of keys generated from the results of running
each element of `collection` thru `iteratee`. The corresponding value of
each key is the number of times the key was returned by `iteratee`. The
iteratee is invoked with one argument: *(value)*.

#### Since
0.5.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The iteratee to transform keys.

#### Returns
*(Object)*: Returns the composed aggregate object.



---





## <a name="_everycollection-predicate_identity"><code>_.every(collection, [predicate=_.identity])</code></a>
```javascript
_.every([true, 1, null, 'yes'], Boolean);
// => false

var users = [
  { 'user': 'barney', 'age': 36, 'active': false },
  { 'user': 'fred',   'age': 40, 'active': false }
];

// The `_.matches` iteratee shorthand.
_.every(users, { 'user': 'barney', 'active': false });
// => false

// The `_.matchesProperty` iteratee shorthand.
_.every(users, ['active', false]);
// => true

// The `_.property` iteratee shorthand.
_.every(users, 'active');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9143 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.every "See the npm package") [&#x24C9;][1]

Checks if `predicate` returns truthy for **all** elements of `collection`.
Iteration is stopped once `predicate` returns falsey. The predicate is
invoked with three arguments: *(value, index|key, collection)*.
<br>
<br>
**Note:** This method returns `true` for
[empty collections](https://en.wikipedia.org/wiki/Empty_set) because
[everything is true](https://en.wikipedia.org/wiki/Vacuous_truth) of
elements of empty collections.

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(boolean)*: Returns `true` if all elements pass the predicate check, else `false`.



---





## <a name="_filtercollection-predicate_identity"><code>_.filter(collection, [predicate=_.identity])</code></a>
```javascript
var users = [
  { 'user': 'barney', 'age': 36, 'active': true },
  { 'user': 'fred',   'age': 40, 'active': false }
];

_.filter(users, function(o) { return !o.active; });
// => objects for ['fred']

// The `_.matches` iteratee shorthand.
_.filter(users, { 'age': 36, 'active': true });
// => objects for ['barney']

// The `_.matchesProperty` iteratee shorthand.
_.filter(users, ['active', false]);
// => objects for ['fred']

// The `_.property` iteratee shorthand.
_.filter(users, 'active');
// => objects for ['barney']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9188 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.filter "See the npm package") [&#x24C9;][1]

Iterates over elements of `collection`, returning an array of all elements
`predicate` returns truthy for. The predicate is invoked with three
arguments: *(value, index|key, collection)*.
<br>
<br>
**Note:** Unlike `_.remove`, this method returns a new array.

### Underscore
<code>_.filter(list, predicate, [context])</code> Alias: select <br> <br>
<code>_.where(list, properties)</code> <br> 
* Looks through each value in the list, returning an array of all the values that contain all of the key-value pairs listed in properties.<br> <br>
<code>_.findWhere(list, properties)</code> <br>
* Looks through the list and returns the first value that matches all of the key-value pairs listed in properties.  If no match is found, or if list is empty, undefined will be returned. <br>

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the new filtered array.



---





## <a name="_findcollection-predicate_identity-fromindex0"><code>_.find(collection, [predicate=_.identity], [fromIndex=0])</code></a>
```javascript
var users = [
  { 'user': 'barney',  'age': 36, 'active': true },
  { 'user': 'fred',    'age': 40, 'active': false },
  { 'user': 'pebbles', 'age': 1,  'active': true }
];

_.find(users, function(o) { return o.age < 40; });
// => object for 'barney'

// The `_.matches` iteratee shorthand.
_.find(users, { 'age': 1, 'active': true });
// => object for 'pebbles'

// The `_.matchesProperty` iteratee shorthand.
_.find(users, ['active', false]);
// => object for 'fred'

// The `_.property` iteratee shorthand.
_.find(users, 'active');
// => object for 'barney'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9229 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.find "See the npm package") [&#x24C9;][1]

Iterates over elements of `collection`, returning the first element
`predicate` returns truthy for. The predicate is invoked with three
arguments: *(value, index|key, collection)*.

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to inspect.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.
3. `[fromIndex=0]` *(number)*: The index to search from.

#### Returns
*(&#42;)*: Returns the matched element, else `undefined`.



---





## <a name="_findlastcollection-predicate_identity-fromindexcollectionlength-1"><code>_.findLast(collection, [predicate=_.identity], [fromIndex=collection.length-1])</code></a>
```javascript
_.findLast([1, 2, 3, 4], function(n) {
  return n % 2 == 1;
});
// => 3
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9250 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.findlast "See the npm package") [&#x24C9;][1]

This method is like `_.find` except that it iterates over elements of
`collection` from right to left.

#### Since
2.0.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to inspect.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.
3. `[fromIndex=collection.length-1]` *(number)*: The index to search from.

#### Returns
*(&#42;)*: Returns the matched element, else `undefined`.



---





## <a name="_flatmapcollection-iteratee_identity"><code>_.flatMap(collection, [iteratee=_.identity])</code></a>
```javascript
function duplicate(n) {
  return [n, n];
}

_.flatMap([1, 2], duplicate);
// => [1, 1, 2, 2]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9273 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.flatmap "See the npm package") [&#x24C9;][1]

Creates a flattened array of values by running each element in `collection`
thru `iteratee` and flattening the mapped results. The iteratee is invoked
with three arguments: *(value, index|key, collection)*.

#### Since
4.0.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the new flattened array.



---





## <a name="_flatmapdeepcollection-iteratee_identity"><code>_.flatMapDeep(collection, [iteratee=_.identity])</code></a>
```javascript
function duplicate(n) {
  return [[[n, n]]];
}

_.flatMapDeep([1, 2], duplicate);
// => [1, 1, 2, 2]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9297 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.flatmapdeep "See the npm package") [&#x24C9;][1]

This method is like `_.flatMap` except that it recursively flattens the
mapped results.

#### Since
4.7.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the new flattened array.



---





## <a name="_flatmapdepthcollection-iteratee_identity-depth1"><code>_.flatMapDepth(collection, [iteratee=_.identity], [depth=1])</code></a>
```javascript
function duplicate(n) {
  return [[[n, n]]];
}

_.flatMapDepth([1, 2], duplicate, 2);
// => [[1, 1], [2, 2]]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9322 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.flatmapdepth "See the npm package") [&#x24C9;][1]

This method is like `_.flatMap` except that it recursively flattens the
mapped results up to `depth` times.

#### Since
4.7.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.
3. `[depth=1]` *(number)*: The maximum recursion depth.

#### Returns
*(Array)*: Returns the new flattened array.



---





## <a name="_foreachcollection-iteratee_identity"><code>_.forEach(collection, [iteratee=_.identity])</code></a>
```javascript
_.forEach([1, 2], function(value) {
  console.log(value);
});
// => Logs `1` then `2`.

_.forEach({ 'a': 1, 'b': 2 }, function(value, key) {
  console.log(key);
});
// => Logs 'a' then 'b' (iteration order is not guaranteed).
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9357 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.foreach "See the npm package") [&#x24C9;][1]

Iterates over elements of `collection` and invokes `iteratee` for each element.
The iteratee is invoked with three arguments: *(value, index|key, collection)*.
Iteratee functions may exit iteration early by explicitly returning `false`.
<br>
<br>
**Note:** As with other "Collections" methods, objects with a "length"
property are iterated like arrays. To avoid this behavior use `_.forIn`
or `_.forOwn` for object iteration.

#### Underscore
<code>_.each(list, iteratee, [context])</code> Alias: forEach 

#### Since
0.1.0

#### Aliases
*_.each*

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(&#42;)*: Returns `collection`.



---





## <a name="_foreachrightcollection-iteratee_identity"><code>_.forEachRight(collection, [iteratee=_.identity])</code></a>
```javascript
_.forEachRight([1, 2], function(value) {
  console.log(value);
});
// => Logs `2` then `1`.
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9382 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.foreachright "See the npm package") [&#x24C9;][1]

This method is like `_.forEach` except that it iterates over elements of
`collection` from right to left.

#### Since
2.0.0

#### Aliases
*_.eachRight*

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(&#42;)*: Returns `collection`.



---





## <a name="_groupbycollection-iteratee_identity"><code>_.groupBy(collection, [iteratee=_.identity])</code></a>
```javascript
_.groupBy([6.1, 4.2, 6.3], Math.floor);
// => { '4': [4.2], '6': [6.1, 6.3] }

// The `_.property` iteratee shorthand.
_.groupBy(['one', 'two', 'three'], 'length');
// => { '3': ['one', 'two'], '5': ['three'] }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9410 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.groupby "See the npm package") [&#x24C9;][1]

Creates an object composed of keys generated from the results of running
each element of `collection` thru `iteratee`. The order of grouped values
is determined by the order they occur in `collection`. The corresponding
value of each key is an array of elements responsible for generating the
key. The iteratee is invoked with one argument: *(value)*.

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The iteratee to transform keys.

#### Returns
*(Object)*: Returns the composed aggregate object.



---





## <a name="_includescollection-value-fromindex0"><code>_.includes(collection, value, [fromIndex=0])</code></a>
```javascript
_.includes([1, 2, 3], 1);
// => true

_.includes([1, 2, 3], 1, 2);
// => false

_.includes({ 'a': 1, 'b': 2 }, 1);
// => true

_.includes('abcd', 'bc');
// => true

//Underscore
_.contains([1, 2, 3], 3);
=> true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9448 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.includes "See the npm package") [&#x24C9;][1]

Checks if `value` is in `collection`. If `collection` is a string, it's
checked for a substring of `value`, otherwise
[`SameValueZero`](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)
is used for equality comparisons. If `fromIndex` is negative, it's used as
the offset from the end of `collection`.

#### Underscore
<code>.contains(list, value, [fromIndex])</code> Alias: includes 

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object|string)*: The collection to inspect.
2. `value` *(&#42;)*: The value to search for.
3. `[fromIndex=0]` *(number)*: The index to search from.

#### Returns
*(boolean)*: Returns `true` if `value` is found, else `false`.



---





## <a name="_invokemapcollection-path-args"><code>_.invokeMap(collection, path, [args])</code></a>
```javascript
_.invokeMap([[5, 1, 7], [3, 2, 1]], 'sort');
// => [[1, 5, 7], [1, 2, 3]]

_.invokeMap([123, 456], String.prototype.split, '');
// => [['1', '2', '3'], ['4', '5', '6']]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9484 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.invokemap "See the npm package") [&#x24C9;][1]

Invokes the method at `path` of each element in `collection`, returning
an array of the results of each invoked method. Any additional arguments
are provided to each invoked method. If `path` is a function, it's invoked
for, and `this` bound to, each element in `collection`.

#### Since
4.0.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `path` *(Array|Function|string)*: The path of the method to invoke or the function invoked per iteration.
3. `[args]` *(...&#42;)*: The arguments to invoke each method with.

#### Returns
*(Array)*: Returns the array of results.



---





## <a name="_keybycollection-iteratee_identity"><code>_.keyBy(collection, [iteratee=_.identity])</code></a>
```javascript
var array = [
  { 'dir': 'left', 'code': 97 },
  { 'dir': 'right', 'code': 100 }
];

_.keyBy(array, function(o) {
  return String.fromCharCode(o.code);
});
// => { 'a': { 'dir': 'left', 'code': 97 }, 'd': { 'dir': 'right', 'code': 100 } }

_.keyBy(array, 'dir');
// => { 'left': { 'dir': 'left', 'code': 97 }, 'right': { 'dir': 'right', 'code': 100 } }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9523 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.keyby "See the npm package") [&#x24C9;][1]

Creates an object composed of keys generated from the results of running
each element of `collection` thru `iteratee`. The corresponding value of
each key is the last element responsible for generating the key. The
iteratee is invoked with one argument: *(value)*.

#### Since
4.0.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The iteratee to transform keys.

#### Returns
*(Object)*: Returns the composed aggregate object.



---





## <a name="_mapcollection-iteratee_identity"><code>_.map(collection, [iteratee=_.identity])</code></a>
```javascript
function square(n) {
  return n * n;
}

_.map([4, 8], square);
// => [16, 64]

_.map({ 'a': 4, 'b': 8 }, square);
// => [16, 64] (iteration order is not guaranteed)

var users = [
  { 'user': 'barney' },
  { 'user': 'fred' }
];

// The `_.property` iteratee shorthand.
_.map(users, 'user');
// => ['barney', 'fred']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9569 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.map "See the npm package") [&#x24C9;][1]

Creates an array of values by running each element in `collection` thru
`iteratee`. The iteratee is invoked with three arguments:<br>
*(value, index|key, collection)*.
<br>
<br>
Many lodash methods are guarded to work as iteratees for methods like
`_.every`, `_.filter`, `_.map`, `_.mapValues`, `_.reject`, and `_.some`.
<br>
<br>
The guarded methods are:<br>
`ary`, `chunk`, `curry`, `curryRight`, `drop`, `dropRight`, `every`,
`fill`, `invert`, `parseInt`, `random`, `range`, `rangeRight`, `repeat`,
`sampleSize`, `slice`, `some`, `sortBy`, `split`, `take`, `takeRight`,
`template`, `trim`, `trimEnd`, `trimStart`, and `words`

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the new mapped array.



---





## <a name="_orderbycollection-iteratees_identity-orders"><code>_.orderBy(collection, [iteratees=[_.identity]], [orders])</code></a>
```javascript
var users = [
  { 'user': 'fred',   'age': 48 },
  { 'user': 'barney', 'age': 34 },
  { 'user': 'fred',   'age': 40 },
  { 'user': 'barney', 'age': 36 }
];

// Sort by `user` in ascending order and by `age` in descending order.
_.orderBy(users, ['user', 'age'], ['asc', 'desc']);
// => objects for [['barney', 36], ['barney', 34], ['fred', 48], ['fred', 40]]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9603 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.orderby "See the npm package") [&#x24C9;][1]

This method is like `_.sortBy` except that it allows specifying the sort
orders of the iteratees to sort by. If `orders` is unspecified, all values
are sorted in ascending order. Otherwise, specify an order of "desc" for
descending or "asc" for ascending sort order of corresponding values.

#### Since
4.0.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratees=[_.identity]]` *(Array&#91;&#93;|Function&#91;&#93;|Object&#91;&#93;|string&#91;&#93;)*: The iteratees to sort by.
3. `[orders]` *(string&#91;&#93;)*: The sort orders of `iteratees`.

#### Returns
*(Array)*: Returns the new sorted array.



---





## <a name="_partitioncollection-predicate_identity"><code>_.partition(collection, [predicate=_.identity])</code></a>
```javascript
var users = [
  { 'user': 'barney',  'age': 36, 'active': false },
  { 'user': 'fred',    'age': 40, 'active': true },
  { 'user': 'pebbles', 'age': 1,  'active': false }
];

_.partition(users, function(o) { return o.active; });
// => objects for [['fred'], ['barney', 'pebbles']]

// The `_.matches` iteratee shorthand.
_.partition(users, { 'age': 1, 'active': false });
// => objects for [['pebbles'], ['barney', 'fred']]

// The `_.matchesProperty` iteratee shorthand.
_.partition(users, ['active', false]);
// => objects for [['barney', 'pebbles'], ['fred']]

// The `_.property` iteratee shorthand.
_.partition(users, 'active');
// => objects for [['fred'], ['barney', 'pebbles']]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9653 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.partition "See the npm package") [&#x24C9;][1]

Creates an array of elements split into two groups, the first of which
contains elements `predicate` returns truthy for, the second of which
contains elements `predicate` returns falsey for. The predicate is
invoked with one argument: *(value)*.

#### Since
3.0.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the array of grouped elements.



---





## <a name="_reducecollection-iteratee_identity-accumulator"><code>_.reduce(collection, [iteratee=_.identity], [accumulator])</code></a>
```javascript
_.reduce([1, 2], function(sum, n) {
  return sum + n;
}, 0);
// => 3

_.reduce({ 'a': 1, 'b': 2, 'c': 1 }, function(result, value, key) {
  (result[value] || (result[value] = [])).push(key);
  return result;
}, {});
// => { '1': ['a', 'c'], '2': ['b'] } (iteration order is not guaranteed)
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9694 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.reduce "See the npm package") [&#x24C9;][1]

Reduces `collection` to a value which is the accumulated result of running
each element in `collection` thru `iteratee`, where each successive
invocation is supplied the return value of the previous. If `accumulator`
is not given, the first element of `collection` is used as the initial
value. The iteratee is invoked with four arguments:<br>
*(accumulator, value, index|key, collection)*.
<br>
<br>
Many lodash methods are guarded to work as iteratees for methods like
`_.reduce`, `_.reduceRight`, and `_.transform`.
<br>
<br>
The guarded methods are:<br>
`assign`, `defaults`, `defaultsDeep`, `includes`, `merge`, `orderBy`,
and `sortBy`

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.
3. `[accumulator]` *(&#42;)*: The initial value.

#### Returns
*(&#42;)*: Returns the accumulated value.



---





## <a name="_reducerightcollection-iteratee_identity-accumulator"><code>_.reduceRight(collection, [iteratee=_.identity], [accumulator])</code></a>
```javascript
var array = [[0, 1], [2, 3], [4, 5]];

_.reduceRight(array, function(flattened, other) {
  return flattened.concat(other);
}, []);
// => [4, 5, 2, 3, 0, 1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9723 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.reduceright "See the npm package") [&#x24C9;][1]

This method is like `_.reduce` except that it iterates over elements of
`collection` from right to left.

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.
3. `[accumulator]` *(&#42;)*: The initial value.

#### Returns
*(&#42;)*: Returns the accumulated value.



---





## <a name="_rejectcollection-predicate_identity"><code>_.reject(collection, [predicate=_.identity])</code></a>
```javascript
var users = [
  { 'user': 'barney', 'age': 36, 'active': false },
  { 'user': 'fred',   'age': 40, 'active': true }
];

_.reject(users, function(o) { return !o.active; });
// => objects for ['fred']

// The `_.matches` iteratee shorthand.
_.reject(users, { 'age': 40, 'active': true });
// => objects for ['barney']

// The `_.matchesProperty` iteratee shorthand.
_.reject(users, ['active', false]);
// => objects for ['fred']

// The `_.property` iteratee shorthand.
_.reject(users, 'active');
// => objects for ['barney']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9764 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.reject "See the npm package") [&#x24C9;][1]

The opposite of `_.filter`; this method returns the elements of `collection`
that `predicate` does **not** return truthy for.

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the new filtered array.



---





## <a name="_samplecollection"><code>_.sample(collection)</code></a>
```javascript
_.sample([1, 2, 3, 4]);
// => 2
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9783 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sample "See the npm package") [&#x24C9;][1]

Gets a random element from `collection`.

#### Since
2.0.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to sample.

#### Returns
*(&#42;)*: Returns the random element.



---





## <a name="_samplesizecollection-n1"><code>_.sampleSize(collection, [n=1])</code></a>
```javascript
_.sampleSize([1, 2, 3], 2);
// => [3, 1]

_.sampleSize([1, 2, 3], 4);
// => [2, 3, 1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9808 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.samplesize "See the npm package") [&#x24C9;][1]

Gets `n` random elements at unique keys from `collection` up to the
size of `collection`.

#### Since
4.0.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to sample.
2. `[n=1]` *(number)*: The number of elements to sample.

#### Returns
*(Array)*: Returns the random elements.



---





## <a name="_shufflecollection"><code>_.shuffle(collection)</code></a>
```javascript
_.shuffle([1, 2, 3, 4]);
// => [4, 1, 3, 2]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9833 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.shuffle "See the npm package") [&#x24C9;][1]

Creates an array of shuffled values, using a version of the
[Fisher-Yates shuffle](https://en.wikipedia.org/wiki/Fisher-Yates_shuffle).

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to shuffle.

#### Returns
*(Array)*: Returns the new shuffled array.



---





## <a name="_sizecollection"><code>_.size(collection)</code></a>
```javascript
_.size([1, 2, 3]);
// => 3

_.size({ 'a': 1, 'b': 2 });
// => 2

_.size('pebbles');
// => 7
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9859 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.size "See the npm package") [&#x24C9;][1]

Gets the size of `collection` by returning its length for array-like
values or the number of own enumerable string keyed properties for objects.

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object|string)*: The collection to inspect.

#### Returns
*(number)*: Returns the collection size.



---





## <a name="_somecollection-predicate_identity"><code>_.some(collection, [predicate=_.identity])</code></a>
```javascript
_.some([null, 0, 'yes', false], Boolean);
// => true

var users = [
  { 'user': 'barney', 'active': true },
  { 'user': 'fred',   'active': false }
];

// The `_.matches` iteratee shorthand.
_.some(users, { 'user': 'barney', 'active': false });
// => false

// The `_.matchesProperty` iteratee shorthand.
_.some(users, ['active', false]);
// => true

// The `_.property` iteratee shorthand.
_.some(users, 'active');
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9909 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.some "See the npm package") [&#x24C9;][1]

Checks if `predicate` returns truthy for **any** element of `collection`.
Iteration is stopped once `predicate` returns truthy. The predicate is
invoked with three arguments: *(value, index|key, collection)*.

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(boolean)*: Returns `true` if any element passes the predicate check, else `false`.



---





## <a name="_sortbycollection-iteratees_identity"><code>_.sortBy(collection, [iteratees=[_.identity]])</code></a>
```javascript
var users = [
  { 'user': 'fred',   'age': 48 },
  { 'user': 'barney', 'age': 36 },
  { 'user': 'fred',   'age': 40 },
  { 'user': 'barney', 'age': 34 }
];

_.sortBy(users, [function(o) { return o.user; }]);
// => objects for [['barney', 36], ['barney', 34], ['fred', 48], ['fred', 40]]

_.sortBy(users, ['user', 'age']);
// => objects for [['barney', 34], ['barney', 36], ['fred', 40], ['fred', 48]]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9946 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sortby "See the npm package") [&#x24C9;][1]

Creates an array of elements, sorted in ascending order by the results of
running each element in a collection thru each iteratee. This method
performs a stable sort, that is, it preserves the original sort order of
equal elements. The iteratees are invoked with one argument: *(value)*.

#### Since
0.1.0

#### Arguments
1. `collection` *(Array|Object)*: The collection to iterate over.
2. `[iteratees=[_.identity]]` *(...(Function|Function&#91;&#93;))*: The iteratees to sort by.

#### Returns
*(Array)*: Returns the new sorted array.



---







# Date



## <a name="_now"><code>_.now()</code></a>
```javascript
_.defer(function(stamp) {
  console.log(_.now() - stamp);
}, _.now());
// => Logs the number of milliseconds it took for the deferred invocation.
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9977 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.now "See the npm package") [&#x24C9;][1]

Gets the timestamp of the number of milliseconds that have elapsed since
the Unix epoch *(1 January `1970 00`:00:00 UTC)*.

#### Since
2.4.0

#### Returns
*(number)*: Returns the timestamp.



---







# Function



## <a name="_aftern-func"><code>_.after(n, func)</code></a>
```javascript
var saves = ['profile', 'settings'];

var done = _.after(saves.length, function() {
  console.log('done saving!');
});

_.forEach(saves, function(type) {
  asyncSave({ 'type': type, 'complete': done });
});
// => Logs 'done saving!' after the two async saves have completed.
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10007 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.after "See the npm package") [&#x24C9;][1]

The opposite of `_.before`; this method creates a function that invokes
`func` once it's called `n` or more times.

#### Since
0.1.0

#### Arguments
1. `n` *(number)*: The number of calls before `func` is invoked.
2. `func` *(Function)*: The function to restrict.

#### Returns
*(Function)*: Returns the new restricted function.



---





## <a name="_aryfunc-nfunclength"><code>_.ary(func, [n=func.length])</code></a>
```javascript
_.map(['6', '8', '10'], _.ary(parseInt, 1));
// => [6, 8, 10]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10036 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.ary "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func`, with up to `n` arguments,
ignoring any additional arguments.

#### Since
3.0.0

#### Arguments
1. `func` *(Function)*: The function to cap arguments for.
2. `[n=func.length]` *(number)*: The arity cap.

#### Returns
*(Function)*: Returns the new capped function.



---





## <a name="_beforen-func"><code>_.before(n, func)</code></a>
```javascript
jQuery(element).on('click', _.before(5, addContactToList));
// => Allows adding up to 4 contacts to the list.
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10059 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.before "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func`, with the `this` binding and arguments
of the created function, while it's called less than `n` times. Subsequent
calls to the created function return the result of the last `func` invocation.

#### Since
3.0.0

#### Arguments
1. `n` *(number)*: The number of calls at which `func` is no longer invoked.
2. `func` *(Function)*: The function to restrict.

#### Returns
*(Function)*: Returns the new restricted function.



---





## <a name="_bindfunc-thisarg-partials"><code>_.bind(func, thisArg, [partials])</code></a>
```javascript
function greet(greeting, punctuation) {
  return greeting + ' ' + this.user + punctuation;
}

var object = { 'user': 'fred' };

var bound = _.bind(greet, object, 'hi');
bound('!');
// => 'hi fred!'

// Bound with placeholders.
var bound = _.bind(greet, object, _, '!');
bound('hi');
// => 'hi fred!'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10111 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.bind "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func` with the `this` binding of `thisArg`
and `partials` prepended to the arguments it receives.
<br>
<br>
The `_.bind.placeholder` value, which defaults to `_` in monolithic builds,
may be used as a placeholder for partially applied arguments.
<br>
<br>
**Note:** Unlike native `Function#bind`, this method doesn't set the "length"
property of bound functions.

#### Since
0.1.0

#### Arguments
1. `func` *(Function)*: The function to bind.
2. `thisArg` *(&#42;)*: The `this` binding of `func`.
3. `[partials]` *(...&#42;)*: The arguments to be partially applied.

#### Returns
*(Function)*: Returns the new bound function.



---





## <a name="_bindkeyobject-key-partials"><code>_.bindKey(object, key, [partials])</code></a>
```javascript
var object = {
  'user': 'fred',
  'greet': function(greeting, punctuation) {
    return greeting + ' ' + this.user + punctuation;
  }
};

var bound = _.bindKey(object, 'greet', 'hi');
bound('!');
// => 'hi fred!'

object.greet = function(greeting, punctuation) {
  return greeting + 'ya ' + this.user + punctuation;
};

bound('!');
// => 'hiya fred!'

// Bound with placeholders.
var bound = _.bindKey(object, 'greet', _, '!');
bound('hi');
// => 'hiya fred!'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10165 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.bindkey "See the npm package") [&#x24C9;][1]

Creates a function that invokes the method at `object[key]` with `partials`
prepended to the arguments it receives.
<br>
<br>
This method differs from `_.bind` by allowing bound functions to reference
methods that may be redefined or don't yet exist. See
[Peter Michaux's article](http://peter.michaux.ca/articles/lazy-function-definition-pattern)
for more details.
<br>
<br>
The `_.bindKey.placeholder` value, which defaults to `_` in monolithic
builds, may be used as a placeholder for partially applied arguments.

#### Since
0.10.0

#### Arguments
1. `object` *(Object)*: The object to invoke the method on.
2. `key` *(string)*: The key of the method.
3. `[partials]` *(...&#42;)*: The arguments to be partially applied.

#### Returns
*(Function)*: Returns the new bound function.



---





## <a name="_curryfunc-arityfunclength"><code>_.curry(func, [arity=func.length])</code></a>
```javascript
var abc = function(a, b, c) {
  return [a, b, c];
};

var curried = _.curry(abc);

curried(1)(2)(3);
// => [1, 2, 3]

curried(1, 2)(3);
// => [1, 2, 3]

curried(1, 2, 3);
// => [1, 2, 3]

// Curried with placeholders.
curried(1)(_, 3)(2);
// => [1, 2, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10215 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.curry "See the npm package") [&#x24C9;][1]

Creates a function that accepts arguments of `func` and either invokes
`func` returning its result, if at least `arity` number of arguments have
been provided, or returns a function that accepts the remaining `func`
arguments, and so on. The arity of `func` may be specified if `func.length`
is not sufficient.
<br>
<br>
The `_.curry.placeholder` value, which defaults to `_` in monolithic builds,
may be used as a placeholder for provided arguments.
<br>
<br>
**Note:** This method doesn't set the "length" property of curried functions.

#### Since
2.0.0

#### Arguments
1. `func` *(Function)*: The function to curry.
2. `[arity=func.length]` *(number)*: The arity of `func`.

#### Returns
*(Function)*: Returns the new curried function.



---





## <a name="_curryrightfunc-arityfunclength"><code>_.curryRight(func, [arity=func.length])</code></a>
```javascript
var abc = function(a, b, c) {
  return [a, b, c];
};

var curried = _.curryRight(abc);

curried(3)(2)(1);
// => [1, 2, 3]

curried(2, 3)(1);
// => [1, 2, 3]

curried(1, 2, 3);
// => [1, 2, 3]

// Curried with placeholders.
curried(3)(1, _)(2);
// => [1, 2, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10260 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.curryright "See the npm package") [&#x24C9;][1]

This method is like `_.curry` except that arguments are applied to `func`
in the manner of `_.partialRight` instead of `_.partial`.
<br>
<br>
The `_.curryRight.placeholder` value, which defaults to `_` in monolithic
builds, may be used as a placeholder for provided arguments.
<br>
<br>
**Note:** This method doesn't set the "length" property of curried functions.

#### Since
3.0.0

#### Arguments
1. `func` *(Function)*: The function to curry.
2. `[arity=func.length]` *(number)*: The arity of `func`.

#### Returns
*(Function)*: Returns the new curried function.



---





## <a name="_debouncefunc-wait0-options"><code>_.debounce(func, [wait=0], [options={}])</code></a>
```javascript
// Avoid costly calculations while the window size is in flux.
jQuery(window).on('resize', _.debounce(calculateLayout, 150));

// Invoke `sendMail` when clicked, debouncing subsequent calls.
jQuery(element).on('click', _.debounce(sendMail, 300, {
  'leading': true,
  'trailing': false
}));

// Ensure `batchLog` is invoked once after 1 second of debounced calls.
var debounced = _.debounce(batchLog, 250, { 'maxWait': 1000 });
var source = new EventSource('/stream');
jQuery(source).on('message', debounced);

// Cancel the trailing debounced invocation.
jQuery(window).on('popstate', debounced.cancel);
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10321 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.debounce "See the npm package") [&#x24C9;][1]

Creates a debounced function that delays invoking `func` until after `wait`
milliseconds have elapsed since the last time the debounced function was
invoked. The debounced function comes with a `cancel` method to cancel
delayed `func` invocations and a `flush` method to immediately invoke them.
Provide `options` to indicate whether `func` should be invoked on the
leading and/or trailing edge of the `wait` timeout. The `func` is invoked
with the last arguments provided to the debounced function. Subsequent
calls to the debounced function return the result of the last `func`
invocation.
<br>
<br>
**Note:** If `leading` and `trailing` options are `true`, `func` is
invoked on the trailing edge of the timeout only if the debounced function
is invoked more than once during the `wait` timeout.
<br>
<br>
If `wait` is `0` and `leading` is `false`, `func` invocation is deferred
until to the next tick, similar to `setTimeout` with a timeout of `0`.
<br>
<br>
See [David Corbacho's article](https://css-tricks.com/debouncing-throttling-explained-examples/)
for details over the differences between `_.debounce` and `_.throttle`.

#### Since
0.1.0

#### Arguments
1. `func` *(Function)*: The function to debounce.
2. `[wait=0]` *(number)*: The number of milliseconds to delay.
3. `[options={}]` *(Object)*: The options object.
4. `[options.leading=false]` *(boolean)*: Specify invoking on the leading edge of the timeout.
5. `[options.maxWait]` *(number)*: The maximum time `func` is allowed to be delayed before it's invoked.
6. `[options.trailing=true]` *(boolean)*: Specify invoking on the trailing edge of the timeout.

#### Returns
*(Function)*: Returns the new debounced function.



---





## <a name="_deferfunc-args"><code>_.defer(func, [args])</code></a>
```javascript
_.defer(function(text) {
  console.log(text);
}, 'deferred');
// => Logs 'deferred' after one millisecond.
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10461 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.defer "See the npm package") [&#x24C9;][1]

Defers invoking the `func` until the current call stack has cleared. Any
additional arguments are provided to `func` when it's invoked.

#### Since
0.1.0

#### Arguments
1. `func` *(Function)*: The function to defer.
2. `[args]` *(...&#42;)*: The arguments to invoke `func` with.

#### Returns
*(number)*: Returns the timer id.



---





## <a name="_delayfunc-wait-args"><code>_.delay(func, wait, [args])</code></a>
```javascript
_.delay(function(text) {
  console.log(text);
}, 1000, 'later');
// => Logs 'later' after one second.
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10484 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.delay "See the npm package") [&#x24C9;][1]

Invokes `func` after `wait` milliseconds. Any additional arguments are
provided to `func` when it's invoked.

#### Since
0.1.0

#### Arguments
1. `func` *(Function)*: The function to delay.
2. `wait` *(number)*: The number of milliseconds to delay invocation.
3. `[args]` *(...&#42;)*: The arguments to invoke `func` with.

#### Returns
*(number)*: Returns the timer id.



---





## <a name="_flipfunc"><code>_.flip(func)</code></a>
```javascript
var flipped = _.flip(function() {
  return _.toArray(arguments);
});

flipped('a', 'b', 'c', 'd');
// => ['d', 'c', 'b', 'a']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10506 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.flip "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func` with arguments reversed.

#### Since
4.0.0

#### Arguments
1. `func` *(Function)*: The function to flip arguments for.

#### Returns
*(Function)*: Returns the new flipped function.



---





## <a name="_memoizefunc-resolver"><code>_.memoize(func, [resolver])</code></a>
```javascript
var object = { 'a': 1, 'b': 2 };
var other = { 'c': 3, 'd': 4 };

var values = _.memoize(_.values);
values(object);
// => [1, 2]

values(other);
// => [3, 4]

object.a = 2;
values(object);
// => [1, 2]

// Modify the result cache.
values.cache.set(object, ['a', 'b']);
values(object);
// => ['a', 'b']

// Replace `_.memoize.Cache`.
_.memoize.Cache = WeakMap;
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10554 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.memoize "See the npm package") [&#x24C9;][1]

Creates a function that memoizes the result of `func`. If `resolver` is
provided, it determines the cache key for storing the result based on the
arguments provided to the memoized function. By default, the first argument
provided to the memoized function is used as the map cache key. The `func`
is invoked with the `this` binding of the memoized function.
<br>
<br>
**Note:** The cache is exposed as the `cache` property on the memoized
function. Its creation may be customized by replacing the `_.memoize.Cache`
constructor with one whose instances implement the
[`Map`](http://ecma-international.org/ecma-262/7.0/#sec-properties-of-the-map-prototype-object)
method interface of `clear`, `delete`, `get`, `has`, and `set`.

#### Since
0.1.0

#### Arguments
1. `func` *(Function)*: The function to have its output memoized.
2. `[resolver]` *(Function)*: The function to resolve the cache key.

#### Returns
*(Function)*: Returns the new memoized function.



---





## <a name="_negatepredicate"><code>_.negate(predicate)</code></a>
```javascript
function isEven(n) {
  return n % 2 == 0;
}

_.filter([1, 2, 3, 4, 5, 6], _.negate(isEven));
// => [1, 3, 5]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10597 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.negate "See the npm package") [&#x24C9;][1]

Creates a function that negates the result of the predicate `func`. The
`func` predicate is invoked with the `this` binding and arguments of the
created function.

#### Since
3.0.0

#### Arguments
1. `predicate` *(Function)*: The predicate to negate.

#### Returns
*(Function)*: Returns the new negated function.



---





## <a name="_oncefunc"><code>_.once(func)</code></a>
```javascript
var initialize = _.once(createApplication);
initialize();
initialize();
// => `createApplication` is invoked once
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10631 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.once "See the npm package") [&#x24C9;][1]

Creates a function that is restricted to invoking `func` once. Repeat calls
to the function return the value of the first invocation. The `func` is
invoked with the `this` binding and arguments of the created function.

#### Since
0.1.0

#### Arguments
1. `func` *(Function)*: The function to restrict.

#### Returns
*(Function)*: Returns the new restricted function.



---





## <a name="_overargsfunc-transforms_identity"><code>_.overArgs(func, [transforms=[_.identity]])</code></a>
```javascript
function doubled(n) {
  return n * 2;
}

function square(n) {
  return n * n;
}

var func = _.overArgs(function(x, y) {
  return [x, y];
}, [square, doubled]);

func(9, 3);
// => [81, 6]

func(10, 5);
// => [100, 10]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10666 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.overargs "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func` with its arguments transformed.

#### Since
4.0.0

#### Arguments
1. `func` *(Function)*: The function to wrap.
2. `[transforms=[_.identity]]` *(...(Function|Function&#91;&#93;))*: The argument transforms.

#### Returns
*(Function)*: Returns the new function.



---





## <a name="_partialfunc-partials"><code>_.partial(func, [partials])</code></a>
```javascript
function greet(greeting, name) {
  return greeting + ' ' + name;
}

var sayHelloTo = _.partial(greet, 'hello');
sayHelloTo('fred');
// => 'hello fred'

// Partially applied with placeholders.
var greetFred = _.partial(greet, _, 'fred');
greetFred('hi');
// => 'hi fred'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10716 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.partial "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func` with `partials` prepended to the
arguments it receives. This method is like `_.bind` except it does **not**
alter the `this` binding.
<br>
<br>
The `_.partial.placeholder` value, which defaults to `_` in monolithic
builds, may be used as a placeholder for partially applied arguments.
<br>
<br>
**Note:** This method doesn't set the "length" property of partially
applied functions.

#### Since
0.2.0

#### Arguments
1. `func` *(Function)*: The function to partially apply arguments to.
2. `[partials]` *(...&#42;)*: The arguments to be partially applied.

#### Returns
*(Function)*: Returns the new partially applied function.



---





## <a name="_partialrightfunc-partials"><code>_.partialRight(func, [partials])</code></a>
```javascript
function greet(greeting, name) {
  return greeting + ' ' + name;
}

var greetFred = _.partialRight(greet, 'fred');
greetFred('hi');
// => 'hi fred'

// Partially applied with placeholders.
var sayHelloTo = _.partialRight(greet, 'hello', _);
sayHelloTo('fred');
// => 'hello fred'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10753 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.partialright "See the npm package") [&#x24C9;][1]

This method is like `_.partial` except that partially applied arguments
are appended to the arguments it receives.
<br>
<br>
The `_.partialRight.placeholder` value, which defaults to `_` in monolithic
builds, may be used as a placeholder for partially applied arguments.
<br>
<br>
**Note:** This method doesn't set the "length" property of partially
applied functions.

#### Since
1.0.0

#### Arguments
1. `func` *(Function)*: The function to partially apply arguments to.
2. `[partials]` *(...&#42;)*: The arguments to be partially applied.

#### Returns
*(Function)*: Returns the new partially applied function.



---





## <a name="_reargfunc-indexes"><code>_.rearg(func, indexes)</code></a>
```javascript
var rearged = _.rearg(function(a, b, c) {
  return [a, b, c];
}, [2, 0, 1]);

rearged('b', 'c', 'a')
// => ['a', 'b', 'c']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10780 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.rearg "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func` with arguments arranged according
to the specified `indexes` where the argument value at the first index is
provided as the first argument, the argument value at the second index is
provided as the second argument, and so on.

#### Since
3.0.0

#### Arguments
1. `func` *(Function)*: The function to rearrange arguments for.
2. `indexes` *(...(number|number&#91;&#93;))*: The arranged argument indexes.

#### Returns
*(Function)*: Returns the new function.



---





## <a name="_restfunc-startfunclength-1"><code>_.rest(func, [start=func.length-1])</code></a>
```javascript
var say = _.rest(function(what, names) {
  return what + ' ' + _.initial(names).join(', ') +
    (_.size(names) > 1 ? ', & ' : '') + _.last(names);
});

say('hello', 'fred', 'barney', 'pebbles');
// => 'hello fred, barney, & pebbles'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10809 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.rest "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func` with the `this` binding of the
created function and arguments from `start` and beyond provided as
an array.
<br>
<br>
**Note:** This method is based on the
[rest parameter](https://mdn.io/rest_parameters).

#### Since
4.0.0

#### Arguments
1. `func` *(Function)*: The function to apply a rest parameter to.
2. `[start=func.length-1]` *(number)*: The start position of the rest parameter.

#### Returns
*(Function)*: Returns the new function.



---





## <a name="_spreadfunc-start0"><code>_.spread(func, [start=0])</code></a>
```javascript
var say = _.spread(function(who, what) {
  return who + ' says ' + what;
});

say(['fred', 'hello']);
// => 'fred says hello'

var numbers = Promise.all([
  Promise.resolve(40),
  Promise.resolve(36)
]);

numbers.then(_.spread(function(x, y) {
  return x + y;
}));
// => a Promise of 76
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10851 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.spread "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func` with the `this` binding of the
create function and an array of arguments much like
[`Function#apply`](http://www.ecma-international.org/ecma-262/7.0/#sec-function.prototype.apply).
<br>
<br>
**Note:** This method is based on the
[spread operator](https://mdn.io/spread_operator).

#### Since
3.2.0

#### Arguments
1. `func` *(Function)*: The function to spread arguments over.
2. `[start=0]` *(number)*: The start position of the spread.

#### Returns
*(Function)*: Returns the new function.



---





## <a name="_throttlefunc-wait0-options"><code>_.throttle(func, [wait=0], [options={}])</code></a>
```javascript
// Avoid excessively updating the position while scrolling.
jQuery(window).on('scroll', _.throttle(updatePosition, 100));

// Invoke `renewToken` when the click event is fired, but not more than once every 5 minutes.
var throttled = _.throttle(renewToken, 300000, { 'trailing': false });
jQuery(element).on('click', throttled);

// Cancel the trailing throttled invocation.
jQuery(window).on('popstate', throttled.cancel);
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10911 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.throttle "See the npm package") [&#x24C9;][1]

Creates a throttled function that only invokes `func` at most once per
every `wait` milliseconds. The throttled function comes with a `cancel`
method to cancel delayed `func` invocations and a `flush` method to
immediately invoke them. Provide `options` to indicate whether `func`
should be invoked on the leading and/or trailing edge of the `wait`
timeout. The `func` is invoked with the last arguments provided to the
throttled function. Subsequent calls to the throttled function return the
result of the last `func` invocation.
<br>
<br>
**Note:** If `leading` and `trailing` options are `true`, `func` is
invoked on the trailing edge of the timeout only if the throttled function
is invoked more than once during the `wait` timeout.
<br>
<br>
If `wait` is `0` and `leading` is `false`, `func` invocation is deferred
until to the next tick, similar to `setTimeout` with a timeout of `0`.
<br>
<br>
See [David Corbacho's article](https://css-tricks.com/debouncing-throttling-explained-examples/)
for details over the differences between `_.throttle` and `_.debounce`.

#### Since
0.1.0

#### Arguments
1. `func` *(Function)*: The function to throttle.
2. `[wait=0]` *(number)*: The number of milliseconds to throttle invocations to.
3. `[options={}]` *(Object)*: The options object.
4. `[options.leading=true]` *(boolean)*: Specify invoking on the leading edge of the timeout.
5. `[options.trailing=true]` *(boolean)*: Specify invoking on the trailing edge of the timeout.

#### Returns
*(Function)*: Returns the new throttled function.



---





## <a name="_unaryfunc"><code>_.unary(func)</code></a>
```javascript
_.map(['6', '8', '10'], _.unary(parseInt));
// => [6, 8, 10]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10944 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.unary "See the npm package") [&#x24C9;][1]

Creates a function that accepts up to one argument, ignoring any
additional arguments.

#### Since
4.0.0

#### Arguments
1. `func` *(Function)*: The function to cap arguments for.

#### Returns
*(Function)*: Returns the new capped function.



---





## <a name="_wrapvalue-wrapperidentity"><code>_.wrap(value, [wrapper=identity])</code></a>
```javascript
var p = _.wrap(_.escape, function(func, text) {
  return '<p>' + func(text) + '</p>';
});

p('fred, barney, & pebbles');
// => '<p>fred, barney, &amp; pebbles</p>'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L10970 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.wrap "See the npm package") [&#x24C9;][1]

Creates a function that provides `value` to `wrapper` as its first
argument. Any additional arguments provided to the function are appended
to those provided to the `wrapper`. The wrapper is invoked with the `this`
binding of the created function.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to wrap.
2. `[wrapper=identity]` *(Function)*: The wrapper function.

#### Returns
*(Function)*: Returns the new function.



---







# Lang



## <a name="_castarrayvalue"><code>_.castArray(value)</code></a>
```javascript
_.castArray(1);
// => [1]

_.castArray({ 'a': 1 });
// => [{ 'a': 1 }]

_.castArray('abc');
// => ['abc']

_.castArray(null);
// => [null]

_.castArray(undefined);
// => [undefined]

_.castArray();
// => []

var array = [1, 2, 3];
console.log(_.castArray(array) === array);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11009 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.castarray "See the npm package") [&#x24C9;][1]

Casts `value` as an array if it's not one.

#### Since
4.4.0

#### Arguments
1. `value` *(&#42;)*: The value to inspect.

#### Returns
*(Array)*: Returns the cast array.



---





## <a name="_clonevalue"><code>_.clone(value)</code></a>
```javascript
var objects = [{ 'a': 1 }, { 'b': 2 }];

var shallow = _.clone(objects);
console.log(shallow[0] === objects[0]);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11043 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.clone "See the npm package") [&#x24C9;][1]

Creates a shallow clone of `value`.
<br>
<br>
**Note:** This method is loosely based on the
[structured clone algorithm](https://mdn.io/Structured_clone_algorithm)
and supports cloning arrays, array buffers, booleans, date objects, maps,
numbers, `Object` objects, regexes, sets, strings, symbols, and typed
arrays. The own enumerable properties of `arguments` objects are cloned
as plain objects. An empty object is returned for uncloneable values such
as error objects, functions, DOM nodes, and WeakMaps.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to clone.

#### Returns
*(&#42;)*: Returns the cloned value.



---





## <a name="_clonedeepvalue"><code>_.cloneDeep(value)</code></a>
```javascript
function customizer(value) {
  if (_.isElement(value)) {
    return value.cloneNode(true);
  }
}

var el = _.cloneDeepWith(document.body, customizer);

console.log(el === document.body);
// => false
console.log(el.nodeName);
// => 'BODY'
console.log(el.childNodes.length);
// => 20
```
```javascript
var objects = [{ 'a': 1 }, { 'b': 2 }];

var deep = _.cloneDeep(objects);
console.log(deep[0] === objects[0]);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11101 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.clonedeep "See the npm package") [&#x24C9;][1]

This method is like `_.clone` except that it recursively clones `value`.

#### Since
1.0.0

#### Arguments
1. `value` *(&#42;)*: The value to recursively clone.

#### Returns
*(&#42;)*: Returns the deep cloned value.



---





## <a name="_clonedeepwithvalue-customizer"><code>_.cloneDeepWith(value, [customizer])</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11133 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.clonedeepwith "See the npm package") [&#x24C9;][1]

This method is like `_.cloneWith` except that it recursively clones `value`.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to recursively clone.
2. `[customizer]` *(Function)*: The function to customize cloning.

#### Returns
*(&#42;)*: Returns the deep cloned value.



---





## <a name="_clonewithvalue-customizer"><code>_.cloneWith(value, [customizer])</code></a>
```javascript
function customizer(value) {
  if (_.isElement(value)) {
    return value.cloneNode(false);
  }
}

var el = _.cloneWith(document.body, customizer);

console.log(el === document.body);
// => false
console.log(el.nodeName);
// => 'BODY'
console.log(el.childNodes.length);
// => 0
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11078 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.clonewith "See the npm package") [&#x24C9;][1]

This method is like `_.clone` except that it accepts `customizer` which
is invoked to produce the cloned value. If `customizer` returns `undefined`,
cloning is handled by the method instead. The `customizer` is invoked with
up to four arguments; *(value [, index|key, object, stack])*.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to clone.
2. `[customizer]` *(Function)*: The function to customize cloning.

#### Returns
*(&#42;)*: Returns the cloned value.



---





## <a name="_conformstoobject-source"><code>_.conformsTo(object, source)</code></a>
```javascript
var object = { 'a': 1, 'b': 2 };

_.conformsTo(object, { 'b': function(n) { return n > 1; } });
// => true

_.conformsTo(object, { 'b': function(n) { return n > 2; } });
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11162 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.conformsto "See the npm package") [&#x24C9;][1]

Checks if `object` conforms to `source` by invoking the predicate
properties of `source` with the corresponding property values of `object`.
<br>
<br>
**Note:** This method is equivalent to `_.conforms` when `source` is
partially applied.

#### Since
4.14.0

#### Arguments
1. `object` *(Object)*: The object to inspect.
2. `source` *(Object)*: The object of property predicates to conform to.

#### Returns
*(boolean)*: Returns `true` if `object` conforms, else `false`.



---





## <a name="_eqvalue-other"><code>_.eq(value, other)</code></a>
```javascript
var object = { 'a': 1 };
var other = { 'a': 1 };

_.eq(object, object);
// => true

_.eq(object, other);
// => false

_.eq('a', 'a');
// => true

_.eq('a', Object('a'));
// => false

_.eq(NaN, NaN);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11198 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.eq "See the npm package") [&#x24C9;][1]

Performs a
[`SameValueZero`](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)
comparison between two values to determine if they are equivalent.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to compare.
2. `other` *(&#42;)*: The other value to compare.

#### Returns
*(boolean)*: Returns `true` if the values are equivalent, else `false`.



---





## <a name="_gtvalue-other"><code>_.gt(value, other)</code></a>
```javascript
_.gt(3, 1);
// => true

_.gt(3, 3);
// => false

_.gt(1, 3);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11225 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.gt "See the npm package") [&#x24C9;][1]

Checks if `value` is greater than `other`.

#### Since
3.9.0

#### Arguments
1. `value` *(&#42;)*: The value to compare.
2. `other` *(&#42;)*: The other value to compare.

#### Returns
*(boolean)*: Returns `true` if `value` is greater than `other`, else `false`.



---





## <a name="_gtevalue-other"><code>_.gte(value, other)</code></a>
```javascript
_.gte(3, 1);
// => true

_.gte(3, 3);
// => true

_.gte(1, 3);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11250 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.gte "See the npm package") [&#x24C9;][1]

Checks if `value` is greater than or equal to `other`.

#### Since
3.9.0

#### Arguments
1. `value` *(&#42;)*: The value to compare.
2. `other` *(&#42;)*: The other value to compare.

#### Returns
*(boolean)*: Returns `true` if `value` is greater than or equal to `other`, else `false`.



---





## <a name="_isargumentsvalue"><code>_.isArguments(value)</code></a>
```javascript
_.isArguments(function() { return arguments; }());
// => true

_.isArguments([1, 2, 3]);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11272 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isarguments "See the npm package") [&#x24C9;][1]

Checks if `value` is likely an `arguments` object.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is an `arguments` object, else `false`.



---





## <a name="_isarrayvalue"><code>_.isArray(value)</code></a>
```javascript
_.isArray([1, 2, 3]);
// => true

_.isArray(document.body.children);
// => false

_.isArray('abc');
// => false

_.isArray(_.noop);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11300 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isarray "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as an `Array` object.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is an array, else `false`.



---





## <a name="_isarraybuffervalue"><code>_.isArrayBuffer(value)</code></a>
```javascript
_.isArrayBuffer(new ArrayBuffer(2));
// => true

_.isArrayBuffer(new Array(2));
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11319 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isarraybuffer "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as an `ArrayBuffer` object.

#### Since
4.3.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is an array buffer, else `false`.



---





## <a name="_isarraylikevalue"><code>_.isArrayLike(value)</code></a>
```javascript
_.isArrayLike([1, 2, 3]);
// => true

_.isArrayLike(document.body.children);
// => true

_.isArrayLike('abc');
// => true

_.isArrayLike(_.noop);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11346 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isarraylike "See the npm package") [&#x24C9;][1]

Checks if `value` is array-like. A value is considered array-like if it's
not a function and has a `value.length` that's an integer greater than or
equal to `0` and less than or equal to `Number.MAX_SAFE_INTEGER`.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is array-like, else `false`.



---





## <a name="_isarraylikeobjectvalue"><code>_.isArrayLikeObject(value)</code></a>
```javascript
_.isArrayLikeObject([1, 2, 3]);
// => true

_.isArrayLikeObject(document.body.children);
// => true

_.isArrayLikeObject('abc');
// => false

_.isArrayLikeObject(_.noop);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11375 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isarraylikeobject "See the npm package") [&#x24C9;][1]

This method is like `_.isArrayLike` except that it also checks if `value`
is an object.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is an array-like object, else `false`.



---





## <a name="_isbooleanvalue"><code>_.isBoolean(value)</code></a>
```javascript
_.isBoolean(false);
// => true

_.isBoolean(null);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11396 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isboolean "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a boolean primitive or object.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a boolean, else `false`.



---





## <a name="_isbuffervalue"><code>_.isBuffer(value)</code></a>
```javascript
_.isBuffer(new Buffer(2));
// => true

_.isBuffer(new Uint8Array(2));
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11418 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isbuffer "See the npm package") [&#x24C9;][1]

Checks if `value` is a buffer.

#### Since
4.3.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a buffer, else `false`.



---





## <a name="_isdatevalue"><code>_.isDate(value)</code></a>
```javascript
_.isDate(new Date);
// => true

_.isDate('Mon April 23 2012');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11437 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isdate "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `Date` object.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a date object, else `false`.



---





## <a name="_iselementvalue"><code>_.isElement(value)</code></a>
```javascript
_.isElement(document.body);
// => true

_.isElement('<body>');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11456 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.iselement "See the npm package") [&#x24C9;][1]

Checks if `value` is likely a DOM element.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a DOM element, else `false`.



---





## <a name="_isemptyvalue"><code>_.isEmpty(value)</code></a>
```javascript
_.isEmpty(null);
// => true

_.isEmpty(true);
// => true

_.isEmpty(1);
// => true

_.isEmpty([1, 2, 3]);
// => false

_.isEmpty({ 'a': 1 });
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11493 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isempty "See the npm package") [&#x24C9;][1]

Checks if `value` is an empty object, collection, map, or set.
<br>
<br>
Objects are considered empty if they have no own enumerable string keyed
properties.
<br>
<br>
Array-like values such as `arguments` objects, arrays, buffers, strings, or
jQuery-like collections are considered empty if they have a `length` of `0`.
Similarly, maps and sets are considered empty if they have a `size` of `0`.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is empty, else `false`.



---





## <a name="_isequalvalue-other"><code>_.isEqual(value, other)</code></a>
```javascript
var object = { 'a': 1 };
var other = { 'a': 1 };

_.isEqual(object, other);
// => true

object === other;
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11545 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isequal "See the npm package") [&#x24C9;][1]

Performs a deep comparison between two values to determine if they are
equivalent.
<br>
<br>
**Note:** This method supports comparing arrays, array buffers, booleans,
date objects, error objects, maps, numbers, `Object` objects, regexes,
sets, strings, symbols, and typed arrays. `Object` objects are compared
by their own, not inherited, enumerable properties. Functions and DOM
nodes are compared by strict equality, i.e. `===`.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to compare.
2. `other` *(&#42;)*: The other value to compare.

#### Returns
*(boolean)*: Returns `true` if the values are equivalent, else `false`.



---





## <a name="_isequalwithvalue-other-customizer"><code>_.isEqualWith(value, other, [customizer])</code></a>
```javascript
function isGreeting(value) {
  return /^h(?:i|ello)$/.test(value);
}

function customizer(objValue, othValue) {
  if (isGreeting(objValue) && isGreeting(othValue)) {
    return true;
  }
}

var array = ['hello', 'goodbye'];
var other = ['hi', 'goodbye'];

_.isEqualWith(array, other, customizer);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11581 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isequalwith "See the npm package") [&#x24C9;][1]

This method is like `_.isEqual` except that it accepts `customizer` which
is invoked to compare values. If `customizer` returns `undefined`, comparisons
are handled by the method instead. The `customizer` is invoked with up to
six arguments: *(objValue, othValue [, index|key, object, other, stack])*.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to compare.
2. `other` *(&#42;)*: The other value to compare.
3. `[customizer]` *(Function)*: The function to customize comparisons.

#### Returns
*(boolean)*: Returns `true` if the values are equivalent, else `false`.



---





## <a name="_iserrorvalue"><code>_.isError(value)</code></a>
```javascript
_.isError(new Error);
// => true

_.isError(Error);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11605 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.iserror "See the npm package") [&#x24C9;][1]

Checks if `value` is an `Error`, `EvalError`, `RangeError`, `ReferenceError`,
`SyntaxError`, `TypeError`, or `URIError` object.

#### Since
3.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is an error object, else `false`.



---





## <a name="_isfinitevalue"><code>_.isFinite(value)</code></a>
```javascript
_.isFinite(3);
// => true

_.isFinite(Number.MIN_VALUE);
// => true

_.isFinite(Infinity);
// => false

_.isFinite('3');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11640 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isfinite "See the npm package") [&#x24C9;][1]

Checks if `value` is a finite primitive number.
<br>
<br>
**Note:** This method is based on
[`Number.isFinite`](https://mdn.io/Number/isFinite).

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a finite number, else `false`.



---





## <a name="_isfunctionvalue"><code>_.isFunction(value)</code></a>
```javascript
_.isFunction(_);
// => true

_.isFunction(/abc/);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11661 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isfunction "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `Function` object.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a function, else `false`.



---





## <a name="_isintegervalue"><code>_.isInteger(value)</code></a>
```javascript
_.isInteger(3);
// => true

_.isInteger(Number.MIN_VALUE);
// => false

_.isInteger(Infinity);
// => false

_.isInteger('3');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11697 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isinteger "See the npm package") [&#x24C9;][1]

Checks if `value` is an integer.
<br>
<br>
**Note:** This method is based on
[`Number.isInteger`](https://mdn.io/Number/isInteger).

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is an integer, else `false`.



---





## <a name="_islengthvalue"><code>_.isLength(value)</code></a>
```javascript
_.isLength(3);
// => true

_.isLength(Number.MIN_VALUE);
// => false

_.isLength(Infinity);
// => false

_.isLength('3');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11727 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.islength "See the npm package") [&#x24C9;][1]

Checks if `value` is a valid array-like length.
<br>
<br>
**Note:** This method is loosely based on
[`ToLength`](http://ecma-international.org/ecma-262/7.0/#sec-tolength).

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a valid length, else `false`.



---





## <a name="_ismapvalue"><code>_.isMap(value)</code></a>
```javascript
_.isMap(new Map);
// => true

_.isMap(new WeakMap);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11807 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.ismap "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `Map` object.

#### Since
4.3.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a map, else `false`.



---





## <a name="_ismatchobject-source"><code>_.isMatch(object, source)</code></a>
```javascript
var object = { 'a': 1, 'b': 2 };

_.isMatch(object, { 'b': 2 });
// => true

_.isMatch(object, { 'b': 1 });
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11837 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.ismatch "See the npm package") [&#x24C9;][1]

Performs a partial deep comparison between `object` and `source` to
determine if `object` contains equivalent property values.
<br>
<br>
**Note:** This method is equivalent to `_.matches` when `source` is
partially applied.
<br>
<br>
Partial comparisons will match empty array and empty object `source`
values against any array or object value, respectively. See `_.isEqual`
for a list of supported value comparisons.

#### Since
3.0.0

#### Arguments
1. `object` *(Object)*: The object to inspect.
2. `source` *(Object)*: The object of property values to match.

#### Returns
*(boolean)*: Returns `true` if `object` is a match, else `false`.



---





## <a name="_ismatchwithobject-source-customizer"><code>_.isMatchWith(object, source, [customizer])</code></a>
```javascript
function isGreeting(value) {
  return /^h(?:i|ello)$/.test(value);
}

function customizer(objValue, srcValue) {
  if (isGreeting(objValue) && isGreeting(srcValue)) {
    return true;
  }
}

var object = { 'greeting': 'hello' };
var source = { 'greeting': 'hi' };

_.isMatchWith(object, source, customizer);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11873 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.ismatchwith "See the npm package") [&#x24C9;][1]

This method is like `_.isMatch` except that it accepts `customizer` which
is invoked to compare values. If `customizer` returns `undefined`, comparisons
are handled by the method instead. The `customizer` is invoked with five
arguments: *(objValue, srcValue, index|key, object, source)*.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The object to inspect.
2. `source` *(Object)*: The object of property values to match.
3. `[customizer]` *(Function)*: The function to customize comparisons.

#### Returns
*(boolean)*: Returns `true` if `object` is a match, else `false`.



---





## <a name="_isnanvalue"><code>_.isNaN(value)</code></a>
```javascript
_.isNaN(NaN);
// => true

_.isNaN(new Number(NaN));
// => true

isNaN(undefined);
// => true

_.isNaN(undefined);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11906 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isnan "See the npm package") [&#x24C9;][1]

Checks if `value` is `NaN`.
<br>
<br>
**Note:** This method is based on
[`Number.isNaN`](https://mdn.io/Number/isNaN) and is not the same as
global [`isNaN`](https://mdn.io/isNaN) which returns `true` for
`undefined` and other non-number values.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is `NaN`, else `false`.



---





## <a name="_isnativevalue"><code>_.isNative(value)</code></a>
```javascript
_.isNative(Array.prototype.push);
// => true

_.isNative(_);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11939 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isnative "See the npm package") [&#x24C9;][1]

Checks if `value` is a pristine native function.
<br>
<br>
**Note:** This method can't reliably detect native functions in the presence
of the core-js package because core-js circumvents this kind of detection.
Despite multiple requests, the core-js maintainer has made it clear: any
attempt to fix the detection will be obstructed. As a result, we're left
with little choice but to throw an error. Unfortunately, this also affects
packages, like [babel-polyfill](https://www.npmjs.com/package/babel-polyfill),
which rely on core-js.

#### Since
3.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a native function, else `false`.



---





## <a name="_isnilvalue"><code>_.isNil(value)</code></a>
```javascript
_.isNil(null);
// => true

_.isNil(void 0);
// => true

_.isNil(NaN);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11987 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isnil "See the npm package") [&#x24C9;][1]

Checks if `value` is `null` or `undefined`.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is nullish, else `false`.



---





## <a name="_isnullvalue"><code>_.isNull(value)</code></a>
```javascript
_.isNull(null);
// => true

_.isNull(void 0);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11963 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isnull "See the npm package") [&#x24C9;][1]

Checks if `value` is `null`.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is `null`, else `false`.



---





## <a name="_isnumbervalue"><code>_.isNumber(value)</code></a>
```javascript
_.isNumber(3);
// => true

_.isNumber(Number.MIN_VALUE);
// => true

_.isNumber(Infinity);
// => true

_.isNumber('3');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12017 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isnumber "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `Number` primitive or object.
<br>
<br>
**Note:** To exclude `Infinity`, `-Infinity`, and `NaN`, which are
classified as numbers, use the `_.isFinite` method.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a number, else `false`.



---





## <a name="_isobjectvalue"><code>_.isObject(value)</code></a>
```javascript
_.isObject({});
// => true

_.isObject([1, 2, 3]);
// => true

_.isObject(_.noop);
// => true

_.isObject(null);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11757 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isobject "See the npm package") [&#x24C9;][1]

Checks if `value` is the
[language type](http://www.ecma-international.org/ecma-262/7.0/#sec-ecmascript-language-types)
of `Object`. *(e.g. arrays, functions, objects, regexes, `new Number(0)`, and `new String('')`)*

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is an object, else `false`.



---





## <a name="_isobjectlikevalue"><code>_.isObjectLike(value)</code></a>
```javascript
_.isObjectLike({});
// => true

_.isObjectLike([1, 2, 3]);
// => true

_.isObjectLike(_.noop);
// => false

_.isObjectLike(null);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L11786 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isobjectlike "See the npm package") [&#x24C9;][1]

Checks if `value` is object-like. A value is object-like if it's not `null`
and has a `typeof` result of "object".

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is object-like, else `false`.



---





## <a name="_isplainobjectvalue"><code>_.isPlainObject(value)</code></a>
```javascript
function Foo() {
  this.a = 1;
}

_.isPlainObject(new Foo);
// => false

_.isPlainObject([1, 2, 3]);
// => false

_.isPlainObject({ 'x': 0, 'y': 0 });
// => true

_.isPlainObject(Object.create(null));
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12050 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isplainobject "See the npm package") [&#x24C9;][1]

Checks if `value` is a plain object, that is, an object created by the
`Object` constructor or one with a `[[Prototype]]` of `null`.

#### Since
0.8.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a plain object, else `false`.



---





## <a name="_isregexpvalue"><code>_.isRegExp(value)</code></a>
```javascript
_.isRegExp(/abc/);
// => true

_.isRegExp('/abc/');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12080 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isregexp "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `RegExp` object.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a regexp, else `false`.



---





## <a name="_issafeintegervalue"><code>_.isSafeInteger(value)</code></a>
```javascript
_.isSafeInteger(3);
// => true

_.isSafeInteger(Number.MIN_VALUE);
// => false

_.isSafeInteger(Infinity);
// => false

_.isSafeInteger('3');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12109 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.issafeinteger "See the npm package") [&#x24C9;][1]

Checks if `value` is a safe integer. An integer is safe if it's an IEEE-754
double precision number which isn't the result of a rounded unsafe integer.
<br>
<br>
**Note:** This method is based on
[`Number.isSafeInteger`](https://mdn.io/Number/isSafeInteger).

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a safe integer, else `false`.



---





## <a name="_issetvalue"><code>_.isSet(value)</code></a>
```javascript
_.isSet(new Set);
// => true

_.isSet(new WeakSet);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12130 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isset "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `Set` object.

#### Since
4.3.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a set, else `false`.



---





## <a name="_isstringvalue"><code>_.isString(value)</code></a>
```javascript
_.isString('abc');
// => true

_.isString(1);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12149 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isstring "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `String` primitive or object.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a string, else `false`.



---





## <a name="_issymbolvalue"><code>_.isSymbol(value)</code></a>
```javascript
_.isSymbol(Symbol.iterator);
// => true

_.isSymbol('abc');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12171 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.issymbol "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `Symbol` primitive or object.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a symbol, else `false`.



---





## <a name="_istypedarrayvalue"><code>_.isTypedArray(value)</code></a>
```javascript
_.isTypedArray(new Uint8Array);
// => true

_.isTypedArray([]);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12193 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.istypedarray "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a typed array.

#### Since
3.0.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a typed array, else `false`.



---





## <a name="_isundefinedvalue"><code>_.isUndefined(value)</code></a>
```javascript
_.isUndefined(void 0);
// => true

_.isUndefined(null);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12212 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isundefined "See the npm package") [&#x24C9;][1]

Checks if `value` is `undefined`.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is `undefined`, else `false`.



---





## <a name="_isweakmapvalue"><code>_.isWeakMap(value)</code></a>
```javascript
_.isWeakMap(new WeakMap);
// => true

_.isWeakMap(new Map);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12233 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isweakmap "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `WeakMap` object.

#### Since
4.3.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a weak map, else `false`.



---





## <a name="_isweaksetvalue"><code>_.isWeakSet(value)</code></a>
```javascript
_.isWeakSet(new WeakSet);
// => true

_.isWeakSet(new Set);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12254 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.isweakset "See the npm package") [&#x24C9;][1]

Checks if `value` is classified as a `WeakSet` object.

#### Since
4.3.0

#### Arguments
1. `value` *(&#42;)*: The value to check.

#### Returns
*(boolean)*: Returns `true` if `value` is a weak set, else `false`.



---





## <a name="_ltvalue-other"><code>_.lt(value, other)</code></a>
```javascript
_.lt(1, 3);
// => true

_.lt(3, 3);
// => false

_.lt(3, 1);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12281 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.lt "See the npm package") [&#x24C9;][1]

Checks if `value` is less than `other`.

#### Since
3.9.0

#### Arguments
1. `value` *(&#42;)*: The value to compare.
2. `other` *(&#42;)*: The other value to compare.

#### Returns
*(boolean)*: Returns `true` if `value` is less than `other`, else `false`.



---





## <a name="_ltevalue-other"><code>_.lte(value, other)</code></a>
```javascript
_.lte(1, 3);
// => true

_.lte(3, 3);
// => true

_.lte(3, 1);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12306 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.lte "See the npm package") [&#x24C9;][1]

Checks if `value` is less than or equal to `other`.

#### Since
3.9.0

#### Arguments
1. `value` *(&#42;)*: The value to compare.
2. `other` *(&#42;)*: The other value to compare.

#### Returns
*(boolean)*: Returns `true` if `value` is less than or equal to `other`, else `false`.



---





## <a name="_toarrayvalue"><code>_.toArray(value)</code></a>
```javascript
_.toArray({ 'a': 1, 'b': 2 });
// => [1, 2]

_.toArray('abc');
// => ['a', 'b', 'c']

_.toArray(1);
// => []

_.toArray(null);
// => []
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12333 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.toarray "See the npm package") [&#x24C9;][1]

Converts `value` to an array.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to convert.

#### Returns
*(Array)*: Returns the converted array.



---





## <a name="_tofinitevalue"><code>_.toFinite(value)</code></a>
```javascript
_.toFinite(3.2);
// => 3.2

_.toFinite(Number.MIN_VALUE);
// => 5e-324

_.toFinite(Infinity);
// => 1.7976931348623157e+308

_.toFinite('3.2');
// => 3.2
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12372 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.tofinite "See the npm package") [&#x24C9;][1]

Converts `value` to a finite number.

#### Since
4.12.0

#### Arguments
1. `value` *(&#42;)*: The value to convert.

#### Returns
*(number)*: Returns the converted number.



---





## <a name="_tointegervalue"><code>_.toInteger(value)</code></a>
```javascript
_.toInteger(3.2);
// => 3

_.toInteger(Number.MIN_VALUE);
// => 0

_.toInteger(Infinity);
// => 1.7976931348623157e+308

_.toInteger('3.2');
// => 3
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12410 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.tointeger "See the npm package") [&#x24C9;][1]

Converts `value` to an integer.
<br>
<br>
**Note:** This method is loosely based on
[`ToInteger`](http://www.ecma-international.org/ecma-262/7.0/#sec-tointeger).

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to convert.

#### Returns
*(number)*: Returns the converted integer.



---





## <a name="_tolengthvalue"><code>_.toLength(value)</code></a>
```javascript
_.toLength(3.2);
// => 3

_.toLength(Number.MIN_VALUE);
// => 0

_.toLength(Infinity);
// => 4294967295

_.toLength('3.2');
// => 3
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12444 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.tolength "See the npm package") [&#x24C9;][1]

Converts `value` to an integer suitable for use as the length of an
array-like object.
<br>
<br>
**Note:** This method is based on
[`ToLength`](http://ecma-international.org/ecma-262/7.0/#sec-tolength).

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to convert.

#### Returns
*(number)*: Returns the converted integer.



---





## <a name="_tonumbervalue"><code>_.toNumber(value)</code></a>
```javascript
_.toNumber(3.2);
// => 3.2

_.toNumber(Number.MIN_VALUE);
// => 5e-324

_.toNumber(Infinity);
// => Infinity

_.toNumber('3.2');
// => 3.2
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12471 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.tonumber "See the npm package") [&#x24C9;][1]

Converts `value` to a number.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to process.

#### Returns
*(number)*: Returns the number.



---





## <a name="_toplainobjectvalue"><code>_.toPlainObject(value)</code></a>
```javascript
function Foo() {
  this.b = 2;
}

Foo.prototype.c = 3;

_.assign({ 'a': 1 }, new Foo);
// => { 'a': 1, 'b': 2 }

_.assign({ 'a': 1 }, _.toPlainObject(new Foo));
// => { 'a': 1, 'b': 2, 'c': 3 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12516 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.toplainobject "See the npm package") [&#x24C9;][1]

Converts `value` to a plain object flattening inherited enumerable string
keyed properties of `value` to own properties of the plain object.

#### Since
3.0.0

#### Arguments
1. `value` *(&#42;)*: The value to convert.

#### Returns
*(Object)*: Returns the converted plain object.



---





## <a name="_tosafeintegervalue"><code>_.toSafeInteger(value)</code></a>
```javascript
_.toSafeInteger(3.2);
// => 3

_.toSafeInteger(Number.MIN_VALUE);
// => 0

_.toSafeInteger(Infinity);
// => 9007199254740991

_.toSafeInteger('3.2');
// => 3
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12544 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.tosafeinteger "See the npm package") [&#x24C9;][1]

Converts `value` to a safe integer. A safe integer can be compared and
represented correctly.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to convert.

#### Returns
*(number)*: Returns the converted integer.



---





## <a name="_tostringvalue"><code>_.toString(value)</code></a>
```javascript
_.toString(null);
// => ''

_.toString(-0);
// => '-0'

_.toString([1, 2, 3]);
// => '1,2,3'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12569 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.tostring "See the npm package") [&#x24C9;][1]

Converts `value` to a string. An empty string is returned for `null`
and `undefined` values. The sign of `-0` is preserved.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to convert.

#### Returns
*(string)*: Returns the converted string.



---







# Math



## <a name="_addaugend-addend"><code>_.add(augend, addend)</code></a>
```javascript
_.add(6, 4);
// => 10
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16160 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.add "See the npm package") [&#x24C9;][1]

Adds two numbers.

#### Since
3.4.0

#### Arguments
1. `augend` *(number)*: The first number in an addition.
2. `addend` *(number)*: The second number in an addition.

#### Returns
*(number)*: Returns the total.



---





## <a name="_ceilnumber-precision0"><code>_.ceil(number, [precision=0])</code></a>
```javascript
_.ceil(4.006);
// => 5

_.ceil(6.004, 2);
// => 6.01

_.ceil(6040, -2);
// => 6100
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16185 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.ceil "See the npm package") [&#x24C9;][1]

Computes `number` rounded up to `precision`.

#### Since
3.10.0

#### Arguments
1. `number` *(number)*: The number to round up.
2. `[precision=0]` *(number)*: The precision to round up to.

#### Returns
*(number)*: Returns the rounded up number.



---





## <a name="_dividedividend-divisor"><code>_.divide(dividend, divisor)</code></a>
```javascript
_.divide(6, 4);
// => 1.5
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16202 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.divide "See the npm package") [&#x24C9;][1]

Divide two numbers.

#### Since
4.7.0

#### Arguments
1. `dividend` *(number)*: The first number in a division.
2. `divisor` *(number)*: The second number in a division.

#### Returns
*(number)*: Returns the quotient.



---





## <a name="_floornumber-precision0"><code>_.floor(number, [precision=0])</code></a>
```javascript
_.floor(4.006);
// => 4

_.floor(0.046, 2);
// => 0.04

_.floor(4060, -2);
// => 4000
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16227 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.floor "See the npm package") [&#x24C9;][1]

Computes `number` rounded down to `precision`.

#### Since
3.10.0

#### Arguments
1. `number` *(number)*: The number to round down.
2. `[precision=0]` *(number)*: The precision to round down to.

#### Returns
*(number)*: Returns the rounded down number.



---





## <a name="_maxarray"><code>_.max(array)</code></a>
```javascript
_.max([4, 2, 8, 6]);
// => 8

_.max([]);
// => undefined
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16247 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.max "See the npm package") [&#x24C9;][1]

Computes the maximum value of `array`. If `array` is empty or falsey,
`undefined` is returned.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to iterate over.

#### Returns
*(&#42;)*: Returns the maximum value.



---





## <a name="_maxbyarray-iteratee_identity"><code>_.maxBy(array, [iteratee=_.identity])</code></a>
```javascript
var objects = [{ 'n': 1 }, { 'n': 2 }];

_.maxBy(objects, function(o) { return o.n; });
// => { 'n': 2 }

// The `_.property` iteratee shorthand.
_.maxBy(objects, 'n');
// => { 'n': 2 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16276 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.maxby "See the npm package") [&#x24C9;][1]

This method is like `_.max` except that it accepts `iteratee` which is
invoked for each element in `array` to generate the criterion by which
the value is ranked. The iteratee is invoked with one argument: *(value)*.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(&#42;)*: Returns the maximum value.



---





## <a name="_meanarray"><code>_.mean(array)</code></a>
```javascript
_.mean([4, 2, 8, 6]);
// => 5
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16296 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.mean "See the npm package") [&#x24C9;][1]

Computes the mean of the values in `array`.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to iterate over.

#### Returns
*(number)*: Returns the mean.



---





## <a name="_meanbyarray-iteratee_identity"><code>_.meanBy(array, [iteratee=_.identity])</code></a>
```javascript
var objects = [{ 'n': 4 }, { 'n': 2 }, { 'n': 8 }, { 'n': 6 }];

_.meanBy(objects, function(o) { return o.n; });
// => 5

// The `_.property` iteratee shorthand.
_.meanBy(objects, 'n');
// => 5
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16323 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.meanby "See the npm package") [&#x24C9;][1]

This method is like `_.mean` except that it accepts `iteratee` which is
invoked for each element in `array` to generate the value to be averaged.
The iteratee is invoked with one argument: *(value)*.

#### Since
4.7.0

#### Arguments
1. `array` *(Array)*: The array to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(number)*: Returns the mean.



---





## <a name="_minarray"><code>_.min(array)</code></a>
```javascript
_.min([4, 2, 8, 6]);
// => 2

_.min([]);
// => undefined
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16345 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.min "See the npm package") [&#x24C9;][1]

Computes the minimum value of `array`. If `array` is empty or falsey,
`undefined` is returned.

#### Since
0.1.0

#### Arguments
1. `array` *(Array)*: The array to iterate over.

#### Returns
*(&#42;)*: Returns the minimum value.



---





## <a name="_minbyarray-iteratee_identity"><code>_.minBy(array, [iteratee=_.identity])</code></a>
```javascript
var objects = [{ 'n': 1 }, { 'n': 2 }];

_.minBy(objects, function(o) { return o.n; });
// => { 'n': 1 }

// The `_.property` iteratee shorthand.
_.minBy(objects, 'n');
// => { 'n': 1 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16374 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.minby "See the npm package") [&#x24C9;][1]

This method is like `_.min` except that it accepts `iteratee` which is
invoked for each element in `array` to generate the criterion by which
the value is ranked. The iteratee is invoked with one argument: *(value)*.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(&#42;)*: Returns the minimum value.



---





## <a name="_multiplymultiplier-multiplicand"><code>_.multiply(multiplier, multiplicand)</code></a>
```javascript
_.multiply(6, 4);
// => 24
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16395 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.multiply "See the npm package") [&#x24C9;][1]

Multiply two numbers.

#### Since
4.7.0

#### Arguments
1. `multiplier` *(number)*: The first number in a multiplication.
2. `multiplicand` *(number)*: The second number in a multiplication.

#### Returns
*(number)*: Returns the product.



---





## <a name="_roundnumber-precision0"><code>_.round(number, [precision=0])</code></a>
```javascript
_.round(4.006);
// => 4

_.round(4.006, 2);
// => 4.01

_.round(4060, -2);
// => 4100
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16420 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.round "See the npm package") [&#x24C9;][1]

Computes `number` rounded to `precision`.

#### Since
3.10.0

#### Arguments
1. `number` *(number)*: The number to round.
2. `[precision=0]` *(number)*: The precision to round to.

#### Returns
*(number)*: Returns the rounded number.



---





## <a name="_subtractminuend-subtrahend"><code>_.subtract(minuend, subtrahend)</code></a>
```javascript
_.subtract(6, 4);
// => 2
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16437 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.subtract "See the npm package") [&#x24C9;][1]

Subtract two numbers.

#### Since
4.0.0

#### Arguments
1. `minuend` *(number)*: The first number in a subtraction.
2. `subtrahend` *(number)*: The second number in a subtraction.

#### Returns
*(number)*: Returns the difference.



---





## <a name="_sumarray"><code>_.sum(array)</code></a>
```javascript
_.sum([4, 2, 8, 6]);
// => 20
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16455 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sum "See the npm package") [&#x24C9;][1]

Computes the sum of the values in `array`.

#### Since
3.4.0

#### Arguments
1. `array` *(Array)*: The array to iterate over.

#### Returns
*(number)*: Returns the sum.



---





## <a name="_sumbyarray-iteratee_identity"><code>_.sumBy(array, [iteratee=_.identity])</code></a>
```javascript
var objects = [{ 'n': 4 }, { 'n': 2 }, { 'n': 8 }, { 'n': 6 }];

_.sumBy(objects, function(o) { return o.n; });
// => 20

// The `_.property` iteratee shorthand.
_.sumBy(objects, 'n');
// => 20
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16484 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.sumby "See the npm package") [&#x24C9;][1]

This method is like `_.sum` except that it accepts `iteratee` which is
invoked for each element in `array` to generate the value to be summed.
The iteratee is invoked with one argument: *(value)*.

#### Since
4.0.0

#### Arguments
1. `array` *(Array)*: The array to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(number)*: Returns the sum.



---







# Number



## <a name="_clampnumber-lower-upper"><code>_.clamp(number, [lower], upper)</code></a>
```javascript
_.clamp(-10, -5, 5);
// => -5

_.clamp(10, -5, 5);
// => 5
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13957 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.clamp "See the npm package") [&#x24C9;][1]

Clamps `number` within the inclusive `lower` and `upper` bounds.

#### Since
4.0.0

#### Arguments
1. `number` *(number)*: The number to clamp.
2. `[lower]` *(number)*: The lower bound.
3. `upper` *(number)*: The upper bound.

#### Returns
*(number)*: Returns the clamped number.



---





## <a name="_inrangenumber-start0-end"><code>_.inRange(number, [start=0], end)</code></a>
```javascript
_.inRange(3, 2, 4);
// => true

_.inRange(4, 8);
// => true

_.inRange(4, 2);
// => false

_.inRange(2, 2);
// => false

_.inRange(1.2, 2);
// => true

_.inRange(5.2, 4);
// => false

_.inRange(-3, -2, -6);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14011 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.inrange "See the npm package") [&#x24C9;][1]

Checks if `n` is between `start` and up to, but not including, `end`. If
`end` is not specified, it's set to `start` with `start` then set to `0`.
If `start` is greater than `end` the params are swapped to support
negative ranges.

#### Since
3.3.0

#### Arguments
1. `number` *(number)*: The number to check.
2. `[start=0]` *(number)*: The start of the range.
3. `end` *(number)*: The end of the range.

#### Returns
*(boolean)*: Returns `true` if `number` is in the range, else `false`.



---





## <a name="_randomlower0-upper1-floating"><code>_.random([lower=0], [upper=1], [floating])</code></a>
```javascript
_.random(0, 5);
// => an integer between 0 and 5

_.random(5);
// => also an integer between 0 and 5

_.random(5, true);
// => a floating-point number between 0 and 5

_.random(1.2, 5.2);
// => a floating-point number between 1.2 and 5.2
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14054 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.random "See the npm package") [&#x24C9;][1]

Produces a random number between the inclusive `lower` and `upper` bounds.
If only one argument is provided a number between `0` and the given number
is returned. If `floating` is `true`, or either `lower` or `upper` are
floats, a floating-point number is returned instead of an integer.
<br>
<br>
**Note:** JavaScript follows the IEEE-754 standard for resolving
floating-point values which can produce unexpected results.

#### Since
0.7.0

#### Arguments
1. `[lower=0]` *(number)*: The lower bound.
2. `[upper=1]` *(number)*: The upper bound.
3. `[floating]` *(boolean)*: Specify returning a floating-point number.

#### Returns
*(number)*: Returns the random number.



---







# Object



## <a name="_assignobject-sources"><code>_.assign(object, [sources])</code></a>
```javascript
function Foo() {
  this.a = 1;
}

function Bar() {
  this.c = 3;
}

Foo.prototype.b = 2;
Bar.prototype.d = 4;

_.assign({ 'a': 0 }, new Foo, new Bar);
// => { 'a': 1, 'c': 3 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12607 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.assign "See the npm package") [&#x24C9;][1]

Assigns own enumerable string keyed properties of source objects to the
destination object. Source objects are applied from left to right.
Subsequent sources overwrite property assignments of previous sources.
<br>
<br>
**Note:** This method mutates `object` and is loosely based on
[`Object.assign`](https://mdn.io/Object/assign).

### Underscore
_.extendOwn(destination, *sources) Alias: assign <br>
Like extend, but only copies own properties over to the destination object.


#### Since
0.10.0

#### Arguments
1. `object` *(Object)*: The destination object.
2. `[sources]` *(...Object)*: The source objects.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_assigninobject-sources"><code>_.assignIn(object, [sources])</code></a>
```javascript
function Foo() {
  this.a = 1;
}

function Bar() {
  this.c = 3;
}

Foo.prototype.b = 2;
Bar.prototype.d = 4;

_.assignIn({ 'a': 0 }, new Foo, new Bar);
// => { 'a': 1, 'b': 2, 'c': 3, 'd': 4 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12650 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.assignin "See the npm package") [&#x24C9;][1]

This method is like `_.assign` except that it iterates over own and
inherited source properties.
<br>
<br>
**Note:** This method mutates `object`.

#### Underscore
_.extendOwn(destination, *sources) Alias: assign <br>
Like Underscore's extend, but only copies own properties over to the destination object.

#### Since
4.0.0

#### Aliases
*_.extend*

#### Arguments
1. `object` *(Object)*: The destination object.
2. `[sources]` *(...Object)*: The source objects.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_assigninwithobject-sources-customizer"><code>_.assignInWith(object, sources, [customizer])</code></a>
```javascript
function customizer(objValue, srcValue) {
  return _.isUndefined(objValue) ? srcValue : objValue;
}

var defaults = _.partialRight(_.assignInWith, customizer);

defaults({ 'a': 1 }, { 'b': 2 }, { 'a': 3 });
// => { 'a': 1, 'b': 2 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12683 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.assigninwith "See the npm package") [&#x24C9;][1]

This method is like `_.assignIn` except that it accepts `customizer`
which is invoked to produce the assigned values. If `customizer` returns
`undefined`, assignment is handled by the method instead. The `customizer`
is invoked with five arguments: *(objValue, srcValue, key, object, source)*.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
4.0.0

#### Aliases
*_.extendWith*

#### Arguments
1. `object` *(Object)*: The destination object.
2. `sources` *(...Object)*: The source objects.
3. `[customizer]` *(Function)*: The function to customize assigned values.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_assignwithobject-sources-customizer"><code>_.assignWith(object, sources, [customizer])</code></a>
```javascript
function customizer(objValue, srcValue) {
  return _.isUndefined(objValue) ? srcValue : objValue;
}

var defaults = _.partialRight(_.assignWith, customizer);

defaults({ 'a': 1 }, { 'b': 2 }, { 'a': 3 });
// => { 'a': 1, 'b': 2 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12715 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.assignwith "See the npm package") [&#x24C9;][1]

This method is like `_.assign` except that it accepts `customizer`
which is invoked to produce the assigned values. If `customizer` returns
`undefined`, assignment is handled by the method instead. The `customizer`
is invoked with five arguments: *(objValue, srcValue, key, object, source)*.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The destination object.
2. `sources` *(...Object)*: The source objects.
3. `[customizer]` *(Function)*: The function to customize assigned values.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_atobject-paths"><code>_.at(object, [paths])</code></a>
```javascript
var object = { 'a': [{ 'b': { 'c': 3 } }, 4] };

_.at(object, ['a[0].b.c', 'a[1]']);
// => [3, 4]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12736 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.at "See the npm package") [&#x24C9;][1]

Creates an array of values corresponding to `paths` of `object`.

#### Since
1.0.0

#### Arguments
1. `object` *(Object)*: The object to iterate over.
2. `[paths]` *(...(string|string&#91;&#93;))*: The property paths to pick.

#### Returns
*(Array)*: Returns the picked values.



---





## <a name="_createprototype-properties"><code>_.create(prototype, [properties])</code></a>
```javascript
function Shape() {
  this.x = 0;
  this.y = 0;
}

function Circle() {
  Shape.call(this);
}

Circle.prototype = _.create(Shape.prototype, {
  'constructor': Circle
});

var circle = new Circle;
circle instanceof Circle;
// => true

circle instanceof Shape;
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12772 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.create "See the npm package") [&#x24C9;][1]

Creates an object that inherits from the `prototype` object. If a
`properties` object is given, its own enumerable string keyed properties
are assigned to the created object.

#### Since
2.3.0

#### Arguments
1. `prototype` *(Object)*: The object to inherit from.
2. `[properties]` *(Object)*: The properties to assign to the object.

#### Returns
*(Object)*: Returns the new object.



---





## <a name="_defaultsobject-sources"><code>_.defaults(object, [sources])</code></a>
```javascript
_.defaults({ 'a': 1 }, { 'b': 2 }, { 'a': 3 });
// => { 'a': 1, 'b': 2 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12798 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.defaults "See the npm package") [&#x24C9;][1]

Assigns own and inherited enumerable string keyed properties of source
objects to the destination object for all destination properties that
resolve to `undefined`. Source objects are applied from left to right.
Once a property is set, additional values of the same property are ignored.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
0.1.0

#### Arguments
1. `object` *(Object)*: The destination object.
2. `[sources]` *(...Object)*: The source objects.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_defaultsdeepobject-sources"><code>_.defaultsDeep(object, [sources])</code></a>
```javascript
_.defaultsDeep({ 'a': { 'b': 2 } }, { 'a': { 'b': 1, 'c': 3 } });
// => { 'a': { 'b': 2, 'c': 3 } }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12822 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.defaultsdeep "See the npm package") [&#x24C9;][1]

This method is like `_.defaults` except that it recursively assigns
default properties.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
3.10.0

#### Arguments
1. `object` *(Object)*: The destination object.
2. `[sources]` *(...Object)*: The source objects.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_findkeyobject-predicate_identity"><code>_.findKey(object, [predicate=_.identity])</code></a>
```javascript
var users = {
  'barney':  { 'age': 36, 'active': true },
  'fred':    { 'age': 40, 'active': false },
  'pebbles': { 'age': 1,  'active': true }
};

_.findKey(users, function(o) { return o.age < 40; });
// => 'barney' (iteration order is not guaranteed)

// The `_.matches` iteratee shorthand.
_.findKey(users, { 'age': 1, 'active': true });
// => 'pebbles'

// The `_.matchesProperty` iteratee shorthand.
_.findKey(users, ['active', false]);
// => 'fred'

// The `_.property` iteratee shorthand.
_.findKey(users, 'active');
// => 'barney'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12862 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.findkey "See the npm package") [&#x24C9;][1]

This method is like `_.find` except that it returns the key of the first
element `predicate` returns truthy for instead of the element itself.

#### Since
1.1.0

#### Arguments
1. `object` *(Object)*: The object to inspect.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(&#42;)*: Returns the key of the matched element, else `undefined`.



---





## <a name="_findlastkeyobject-predicate_identity"><code>_.findLastKey(object, [predicate=_.identity])</code></a>
```javascript
var users = {
  'barney':  { 'age': 36, 'active': true },
  'fred':    { 'age': 40, 'active': false },
  'pebbles': { 'age': 1,  'active': true }
};

_.findLastKey(users, function(o) { return o.age < 40; });
// => returns 'pebbles' assuming `_.findKey` returns 'barney'

// The `_.matches` iteratee shorthand.
_.findLastKey(users, { 'age': 36, 'active': true });
// => 'barney'

// The `_.matchesProperty` iteratee shorthand.
_.findLastKey(users, ['active', false]);
// => 'fred'

// The `_.property` iteratee shorthand.
_.findLastKey(users, 'active');
// => 'pebbles'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12901 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.findlastkey "See the npm package") [&#x24C9;][1]

This method is like `_.findKey` except that it iterates over elements of
a collection in the opposite order.

#### Since
2.0.0

#### Arguments
1. `object` *(Object)*: The object to inspect.
2. `[predicate=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(&#42;)*: Returns the key of the matched element, else `undefined`.



---





## <a name="_forinobject-iteratee_identity"><code>_.forIn(object, [iteratee=_.identity])</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.forIn(new Foo, function(value, key) {
  console.log(key);
});
// => Logs 'a', 'b', then 'c' (iteration order is not guaranteed).
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12933 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.forin "See the npm package") [&#x24C9;][1]

Iterates over own and inherited enumerable string keyed properties of an
object and invokes `iteratee` for each property. The iteratee is invoked
with three arguments: *(value, key, object)*. Iteratee functions may exit
iteration early by explicitly returning `false`.

#### Since
0.3.0

#### Arguments
1. `object` *(Object)*: The object to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Object)*: Returns `object`.



---


## <a name="_forinrightobject-iteratee_identity"><code>_.forInRight(object, [iteratee=_.identity])</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.forInRight(new Foo, function(value, key) {
  console.log(key);
});
// => Logs 'c', 'b', then 'a' assuming `_.forIn` logs 'a', 'b', then 'c'.
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12965 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.forinright "See the npm package") [&#x24C9;][1]

This method is like `_.forIn` except that it iterates over properties of
`object` in the opposite order.

#### Since
2.0.0

#### Arguments
1. `object` *(Object)*: The object to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_forownobject-iteratee_identity"><code>_.forOwn(object, [iteratee=_.identity])</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.forOwn(new Foo, function(value, key) {
  console.log(key);
});
// => Logs 'a' then 'b' (iteration order is not guaranteed).
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L12999 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.forown "See the npm package") [&#x24C9;][1]

Iterates over own enumerable string keyed properties of an object and
invokes `iteratee` for each property. The iteratee is invoked with three
arguments: *(value, key, object)*. Iteratee functions may exit iteration
early by explicitly returning `false`.

#### Since
0.3.0

#### Arguments
1. `object` *(Object)*: The object to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_forownrightobject-iteratee_identity"><code>_.forOwnRight(object, [iteratee=_.identity])</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.forOwnRight(new Foo, function(value, key) {
  console.log(key);
});
// => Logs 'b' then 'a' assuming `_.forOwn` logs 'a' then 'b'.
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13029 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.forownright "See the npm package") [&#x24C9;][1]

This method is like `_.forOwn` except that it iterates over properties of
`object` in the opposite order.

#### Since
2.0.0

#### Arguments
1. `object` *(Object)*: The object to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_functionsobject"><code>_.functions(object)</code></a>
```javascript
function Foo() {
  this.a = _.constant('a');
  this.b = _.constant('b');
}

Foo.prototype.c = _.constant('c');

_.functions(new Foo);
// => ['a', 'b']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13056 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.functions "See the npm package") [&#x24C9;][1]

Creates an array of function property names from own enumerable properties
of `object`.

#### Since
0.1.0

#### Arguments
1. `object` *(Object)*: The object to inspect.

#### Returns
*(Array)*: Returns the function names.



---





## <a name="_functionsinobject"><code>_.functionsIn(object)</code></a>
```javascript
function Foo() {
  this.a = _.constant('a');
  this.b = _.constant('b');
}

Foo.prototype.c = _.constant('c');

_.functionsIn(new Foo);
// => ['a', 'b', 'c']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13083 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.functionsin "See the npm package") [&#x24C9;][1]

Creates an array of function property names from own and inherited
enumerable properties of `object`.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The object to inspect.

#### Returns
*(Array)*: Returns the function names.



---





## <a name="_getobject-path-defaultvalue"><code>_.get(object, path, [defaultValue])</code></a>
```javascript
var object = { 'a': [{ 'b': { 'c': 3 } }] };

_.get(object, 'a[0].b.c');
// => 3

_.get(object, ['a', '0', 'b', 'c']);
// => 3

_.get(object, 'a.b.c', 'default');
// => 'default'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13112 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.get "See the npm package") [&#x24C9;][1]

Gets the value at `path` of `object`. If the resolved value is
`undefined`, the `defaultValue` is returned in its place.

#### Since
3.7.0

#### Arguments
1. `object` *(Object)*: The object to query.
2. `path` *(Array|string)*: The path of the property to get.
3. `[defaultValue]` *(&#42;)*: The value returned for `undefined` resolved values.

#### Returns
*(&#42;)*: Returns the resolved value.



---





## <a name="_hasobject-path"><code>_.has(object, path)</code></a>
```javascript
var object = { 'a': { 'b': 2 } };
var other = _.create({ 'a': _.create({ 'b': 2 }) });

_.has(object, 'a');
// => true

_.has(object, 'a.b');
// => true

_.has(object, ['a', 'b']);
// => true

_.has(other, 'a');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13144 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.has "See the npm package") [&#x24C9;][1]

Checks if `path` is a direct property of `object`.

### Underscore
<code>_.has(object, key) </code>

#### Since
0.1.0

#### Arguments
1. `object` *(Object)*: The object to query.
2. `path` *(Array|string)*: The path to check.

#### Returns
*(boolean)*: Returns `true` if `path` exists, else `false`.



---





## <a name="_hasinobject-path"><code>_.hasIn(object, path)</code></a>
```javascript
var object = _.create({ 'a': _.create({ 'b': 2 }) });

_.hasIn(object, 'a');
// => true

_.hasIn(object, 'a.b');
// => true

_.hasIn(object, ['a', 'b']);
// => true

_.hasIn(object, 'b');
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13174 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.hasin "See the npm package") [&#x24C9;][1]

Checks if `path` is a direct or inherited property of `object`.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The object to query.
2. `path` *(Array|string)*: The path to check.

#### Returns
*(boolean)*: Returns `true` if `path` exists, else `false`.



---





## <a name="_invertobject"><code>_.invert(object)</code></a>
```javascript
var object = { 'a': 1, 'b': 2, 'c': 1 };

_.invert(object);
// => { '1': 'c', '2': 'b' }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13196 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.invert "See the npm package") [&#x24C9;][1]

Creates an object composed of the inverted keys and values of `object`.
If `object` contains duplicate values, subsequent values overwrite
property assignments of previous values.

#### Since
0.7.0

#### Arguments
1. `object` *(Object)*: The object to invert.

#### Returns
*(Object)*: Returns the new inverted object.



---





## <a name="_invertbyobject-iteratee_identity"><code>_.invertBy(object, [iteratee=_.identity])</code></a>
```javascript
var object = { 'a': 1, 'b': 2, 'c': 1 };

_.invertBy(object);
// => { '1': ['a', 'c'], '2': ['b'] }

_.invertBy(object, function(value) {
  return 'group' + value;
});
// => { 'group1': ['a', 'c'], 'group2': ['b'] }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13226 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.invertby "See the npm package") [&#x24C9;][1]

This method is like `_.invert` except that the inverted object is generated
from the results of running each element of `object` thru `iteratee`. The
corresponding inverted value of each inverted key is an array of keys
responsible for generating the inverted value. The iteratee is invoked
with one argument: *(value)*.

#### Since
4.1.0

#### Arguments
1. `object` *(Object)*: The object to invert.
2. `[iteratee=_.identity]` *(Function)*: The iteratee invoked per element.

#### Returns
*(Object)*: Returns the new inverted object.



---





## <a name="_invokeobject-path-args"><code>_.invoke(object, path, [args])</code></a>
```javascript
var object = { 'a': [{ 'b': { 'c': [1, 2, 3, 4] } }] };

_.invoke(object, 'a[0].b.c.slice', 1, 3);
// => [2, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13252 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.invoke "See the npm package") [&#x24C9;][1]

Invokes the method at `path` of `object`.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The object to query.
2. `path` *(Array|string)*: The path of the method to invoke.
3. `[args]` *(...&#42;)*: The arguments to invoke the method with.

#### Returns
*(&#42;)*: Returns the result of the invoked method.



---





## <a name="_keysobject"><code>_.keys(object)</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.keys(new Foo);
// => ['a', 'b'] (iteration order is not guaranteed)

_.keys('hi');
// => ['0', '1']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13282 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.keys "See the npm package") [&#x24C9;][1]

Creates an array of the own enumerable property names of `object`.
<br>
<br>
**Note:** Non-object values are coerced to objects. See the
[ES spec](http://ecma-international.org/ecma-262/7.0/#sec-object.keys)
for more details.

#### Since
0.1.0

#### Arguments
1. `object` *(Object)*: The object to query.

#### Returns
*(Array)*: Returns the array of property names.



---





## <a name="_keysinobject"><code>_.keysIn(object)</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.keysIn(new Foo);
// => ['a', 'b', 'c'] (iteration order is not guaranteed)
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13309 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.keysin "See the npm package") [&#x24C9;][1]

Creates an array of the own and inherited enumerable property names of `object`.
<br>
<br>
**Note:** Non-object values are coerced to objects.

#### Since
3.0.0

#### Arguments
1. `object` *(Object)*: The object to query.

#### Returns
*(Array)*: Returns the array of property names.



---





## <a name="_mapkeysobject-iteratee_identity"><code>_.mapKeys(object, [iteratee=_.identity])</code></a>
```javascript
_.mapKeys({ 'a': 1, 'b': 2 }, function(value, key) {
  return key + value;
});
// => { 'a1': 1, 'b2': 2 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13334 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.mapkeys "See the npm package") [&#x24C9;][1]

The opposite of `_.mapValues`; this method creates an object with the
same values as `object` and keys generated by running each own enumerable
string keyed property of `object` thru `iteratee`. The iteratee is invoked
with three arguments: *(value, key, object)*.

#### Since
3.8.0

#### Arguments
1. `object` *(Object)*: The object to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Object)*: Returns the new mapped object.



---


## <a name="_mapvaluesobject-iteratee_identity"><code>_.mapValues(object, [iteratee=_.identity])</code></a>
```javascript
var users = {
  'fred':    { 'user': 'fred',    'age': 40 },
  'pebbles': { 'user': 'pebbles', 'age': 1 }
};

_.mapValues(users, function(o) { return o.age; });
// => { 'fred': 40, 'pebbles': 1 } (iteration order is not guaranteed)

// The `_.property` iteratee shorthand.
_.mapValues(users, 'age');
// => { 'fred': 40, 'pebbles': 1 } (iteration order is not guaranteed)

_.mapObject({ one: 1, two: 2, three: 3 }, function (v) { return v * 3; });

// => { one: 3, two: 6, three: 9 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13372 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.mapvalues "See the npm package") [&#x24C9;][1]

Creates an object with the same keys as `object` and values generated
by running each own enumerable string keyed property of `object` thru
`iteratee`. The iteratee is invoked with three arguments:<br>
*(value, key, object)*.

#### Underscore
<code>_.mapObject(object, iteratee, [context]) </code>

#### Since
2.4.0

#### Arguments
1. `object` *(Object)*: The object to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Object)*: Returns the new mapped object.


---





## <a name="_mergeobject-sources"><code>_.merge(object, [sources])</code></a>
```javascript
var object = {
  'a': [{ 'b': 2 }, { 'd': 4 }]
};

var other = {
  'a': [{ 'c': 3 }, { 'e': 5 }]
};

_.merge(object, other);
// => { 'a': [{ 'b': 2, 'c': 3 }, { 'd': 4, 'e': 5 }] }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13413 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.merge "See the npm package") [&#x24C9;][1]

This method is like `_.assign` except that it recursively merges own and
inherited enumerable string keyed properties of source objects into the
destination object. Source properties that resolve to `undefined` are
skipped if a destination value exists. Array and plain object properties
are merged recursively. Other objects and value types are overridden by
assignment. Source objects are applied from left to right. Subsequent
sources overwrite property assignments of previous sources.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
0.5.0

#### Arguments
1. `object` *(Object)*: The destination object.
2. `[sources]` *(...Object)*: The source objects.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_mergewithobject-sources-customizer"><code>_.mergeWith(object, sources, customizer)</code></a>
```javascript
function customizer(objValue, srcValue) {
  if (_.isArray(objValue)) {
    return objValue.concat(srcValue);
  }
}

var object = { 'a': [1], 'b': [2] };
var other = { 'a': [3], 'b': [4] };

_.mergeWith(object, other, customizer);
// => { 'a': [1, 3], 'b': [2, 4] }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13448 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.mergewith "See the npm package") [&#x24C9;][1]

This method is like `_.merge` except that it accepts `customizer` which
is invoked to produce the merged values of the destination and source
properties. If `customizer` returns `undefined`, merging is handled by the
method instead. The `customizer` is invoked with six arguments:<br>
*(objValue, srcValue, key, object, source, stack)*.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The destination object.
2. `sources` *(...Object)*: The source objects.
3. `customizer` *(Function)*: The function to customize assigned values.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_omitobject-paths"><code>_.omit(object, [paths])</code></a>
```javascript
var object = { 'a': 1, 'b': '2', 'c': 3 };

_.omit(object, ['a', 'c']);
// => { 'b': '2' }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13472 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.omit "See the npm package") [&#x24C9;][1]

The opposite of `_.pick`; this method creates an object composed of the
own and inherited enumerable property paths of `object` that are not omitted.
<br>
<br>
**Note:** This method is considerably slower than `_.pick`.

#### Since
0.1.0

#### Arguments
1. `object` *(Object)*: The source object.
2. `[paths]` *(...(string|string&#91;&#93;))*: The property paths to omit.

#### Returns
*(Object)*: Returns the new object.



---





## <a name="_omitbyobject-predicate_identity"><code>_.omitBy(object, [predicate=_.identity])</code></a>
```javascript
var object = { 'a': 1, 'b': '2', 'c': 3 };

_.omitBy(object, _.isNumber);
// => { 'b': '2' }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13514 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.omitby "See the npm package") [&#x24C9;][1]

The opposite of `_.pickBy`; this method creates an object composed of
the own and inherited enumerable string keyed properties of `object` that
`predicate` doesn't return truthy for. The predicate is invoked with two
arguments: *(value, key)*.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The source object.
2. `[predicate=_.identity]` *(Function)*: The function invoked per property.

#### Returns
*(Object)*: Returns the new object.



---





## <a name="_pickobject-paths"><code>_.pick(object, [paths])</code></a>
```javascript
var object = { 'a': 1, 'b': '2', 'c': 3 };

_.pick(object, ['a', 'c']);
// => { 'a': 1, 'c': 3 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13535 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.pick "See the npm package") [&#x24C9;][1]

Creates an object composed of the picked `object` properties.

#### Since
0.1.0

#### Arguments
1. `object` *(Object)*: The source object.
2. `[paths]` *(...(string|string&#91;&#93;))*: The property paths to pick.

#### Returns
*(Object)*: Returns the new object.



---





## <a name="_pickbyobject-predicate_identity"><code>_.pickBy(object, [predicate=_.identity])</code></a>
```javascript
var object = { 'a': 1, 'b': '2', 'c': 3 };

_.pickBy(object, _.isNumber);
// => { 'a': 1, 'c': 3 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13557 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.pickby "See the npm package") [&#x24C9;][1]

Creates an object composed of the `object` properties `predicate` returns
truthy for. The predicate is invoked with two arguments: *(value, key)*.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The source object.
2. `[predicate=_.identity]` *(Function)*: The function invoked per property.

#### Returns
*(Object)*: Returns the new object.



---





## <a name="_resultobject-path-defaultvalue"><code>_.result(object, path, [defaultValue])</code></a>
```javascript
var object = { 'a': [{ 'b': { 'c1': 3, 'c2': _.constant(4) } }] };

_.result(object, 'a[0].b.c1');
// => 3

_.result(object, 'a[0].b.c2');
// => 4

_.result(object, 'a[0].b.c3', 'default');
// => 'default'

_.result(object, 'a[0].b.c3', _.constant('default'));
// => 'default'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13599 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.result "See the npm package") [&#x24C9;][1]

This method is like `_.get` except that if the resolved value is a
function it's invoked with the `this` binding of its parent object and
its result is returned.

#### Since
0.1.0

#### Arguments
1. `object` *(Object)*: The object to query.
2. `path` *(Array|string)*: The path of the property to resolve.
3. `[defaultValue]` *(&#42;)*: The value returned for `undefined` resolved values.

#### Returns
*(&#42;)*: Returns the resolved value.



---





## <a name="_setobject-path-value"><code>_.set(object, path, value)</code></a>
```javascript
var object = { 'a': [{ 'b': { 'c': 3 } }] };

_.set(object, 'a[0].b.c', 4);
console.log(object.a[0].b.c);
// => 4

_.set(object, ['x', '0', 'y', 'z'], 5);
console.log(object.x[0].y.z);
// => 5
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13649 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.set "See the npm package") [&#x24C9;][1]

Sets the value at `path` of `object`. If a portion of `path` doesn't exist,
it's created. Arrays are created for missing index properties while objects
are created for all other missing properties. Use `_.setWith` to customize
`path` creation.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
3.7.0

#### Arguments
1. `object` *(Object)*: The object to modify.
2. `path` *(Array|string)*: The path of the property to set.
3. `value` *(&#42;)*: The value to set.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_setwithobject-path-value-customizer"><code>_.setWith(object, path, value, [customizer])</code></a>
```javascript
var object = {};

_.setWith(object, '[0][1]', 'a', Object);
// => { '0': { '1': 'a' } }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13677 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.setwith "See the npm package") [&#x24C9;][1]

This method is like `_.set` except that it accepts `customizer` which is
invoked to produce the objects of `path`.  If `customizer` returns `undefined`
path creation is handled by the method instead. The `customizer` is invoked
with three arguments: *(nsValue, key, nsObject)*.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The object to modify.
2. `path` *(Array|string)*: The path of the property to set.
3. `value` *(&#42;)*: The value to set.
4. `[customizer]` *(Function)*: The function to customize assigned values.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_topairsobject"><code>_.toPairs(object)</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.toPairs(new Foo);
// => [['a', 1], ['b', 2]] (iteration order is not guaranteed)
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13706 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.topairs "See the npm package") [&#x24C9;][1]

Creates an array of own enumerable string keyed-value pairs for `object`
which can be consumed by `_.fromPairs`. If `object` is a map or set, its
entries are returned.

#### Since
4.0.0

#### Aliases
*_.entries*

#### Arguments
1. `object` *(Object)*: The object to query.

#### Returns
*(Array)*: Returns the key-value pairs.



---





## <a name="_topairsinobject"><code>_.toPairsIn(object)</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.toPairsIn(new Foo);
// => [['a', 1], ['b', 2], ['c', 3]] (iteration order is not guaranteed)
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13732 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.topairsin "See the npm package") [&#x24C9;][1]

Creates an array of own and inherited enumerable string keyed-value pairs
for `object` which can be consumed by `_.fromPairs`. If `object` is a map
or set, its entries are returned.

#### Since
4.0.0

#### Aliases
*_.entriesIn*

#### Arguments
1. `object` *(Object)*: The object to query.

#### Returns
*(Array)*: Returns the key-value pairs.



---





## <a name="_transformobject-iteratee_identity-accumulator"><code>_.transform(object, [iteratee=_.identity], [accumulator])</code></a>
```javascript
_.transform([2, 3, 4], function(result, n) {
  result.push(n *= n);
  return n % 2 == 0;
}, []);
// => [4, 9]

_.transform({ 'a': 1, 'b': 2, 'c': 1 }, function(result, value, key) {
  (result[value] || (result[value] = [])).push(key);
}, {});
// => { '1': ['a', 'c'], '2': ['b'] }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13764 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.transform "See the npm package") [&#x24C9;][1]

An alternative to `_.reduce`; this method transforms `object` to a new
`accumulator` object which is the result of running each of its own
enumerable string keyed properties thru `iteratee`, with each invocation
potentially mutating the `accumulator` object. If `accumulator` is not
provided, a new object with the same `[[Prototype]]` will be used. The
iteratee is invoked with four arguments: *(accumulator, value, key, object)*.
Iteratee functions may exit iteration early by explicitly returning `false`.

#### Since
1.3.0

#### Arguments
1. `object` *(Object)*: The object to iterate over.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.
3. `[accumulator]` *(&#42;)*: The custom accumulator value.

#### Returns
*(&#42;)*: Returns the accumulated value.



---





## <a name="_unsetobject-path"><code>_.unset(object, path)</code></a>
```javascript
var object = { 'a': [{ 'b': { 'c': 7 } }] };
_.unset(object, 'a[0].b.c');
// => true

console.log(object);
// => { 'a': [{ 'b': {} }] };

_.unset(object, ['a', '0', 'b', 'c']);
// => true

console.log(object);
// => { 'a': [{ 'b': {} }] };
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13814 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.unset "See the npm package") [&#x24C9;][1]

Removes the property at `path` of `object`.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
4.0.0

#### Arguments
1. `object` *(Object)*: The object to modify.
2. `path` *(Array|string)*: The path of the property to unset.

#### Returns
*(boolean)*: Returns `true` if the property is deleted, else `false`.



---





## <a name="_updateobject-path-updater"><code>_.update(object, path, updater)</code></a>
```javascript
var object = { 'a': [{ 'b': { 'c': 3 } }] };

_.update(object, 'a[0].b.c', function(n) { return n * n; });
console.log(object.a[0].b.c);
// => 9

_.update(object, 'x[0].y.z', function(n) { return n ? n + 1 : 0; });
console.log(object.x[0].y.z);
// => 0
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13845 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.update "See the npm package") [&#x24C9;][1]

This method is like `_.set` except that accepts `updater` to produce the
value to set. Use `_.updateWith` to customize `path` creation. The `updater`
is invoked with one argument: *(value)*.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
4.6.0

#### Arguments
1. `object` *(Object)*: The object to modify.
2. `path` *(Array|string)*: The path of the property to set.
3. `updater` *(Function)*: The function to produce the updated value.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_updatewithobject-path-updater-customizer"><code>_.updateWith(object, path, updater, [customizer])</code></a>
```javascript
var object = {};

_.updateWith(object, '[0][1]', _.constant('a'), Object);
// => { '0': { '1': 'a' } }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13873 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.updatewith "See the npm package") [&#x24C9;][1]

This method is like `_.update` except that it accepts `customizer` which is
invoked to produce the objects of `path`.  If `customizer` returns `undefined`
path creation is handled by the method instead. The `customizer` is invoked
with three arguments: *(nsValue, key, nsObject)*.
<br>
<br>
**Note:** This method mutates `object`.

#### Since
4.6.0

#### Arguments
1. `object` *(Object)*: The object to modify.
2. `path` *(Array|string)*: The path of the property to set.
3. `updater` *(Function)*: The function to produce the updated value.
4. `[customizer]` *(Function)*: The function to customize assigned values.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_valuesobject"><code>_.values(object)</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.values(new Foo);
// => [1, 2] (iteration order is not guaranteed)

_.values('hi');
// => ['h', 'i']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13904 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.values "See the npm package") [&#x24C9;][1]

Creates an array of the own enumerable string keyed property values of `object`.
<br>
<br>
**Note:** Non-object values are coerced to objects.

#### Since
0.1.0

#### Arguments
1. `object` *(Object)*: The object to query.

#### Returns
*(Array)*: Returns the array of property values.



---





## <a name="_valuesinobject"><code>_.valuesIn(object)</code></a>
```javascript
function Foo() {
  this.a = 1;
  this.b = 2;
}

Foo.prototype.c = 3;

_.valuesIn(new Foo);
// => [1, 2, 3] (iteration order is not guaranteed)
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L13932 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.valuesin "See the npm package") [&#x24C9;][1]

Creates an array of the own and inherited enumerable string keyed property
values of `object`.
<br>
<br>
**Note:** Non-object values are coerced to objects.

#### Since
3.0.0

#### Arguments
1. `object` *(Object)*: The object to query.

#### Returns
*(Array)*: Returns the array of property values.



---







# Seq



## <a name="_value"><code>_(value)</code></a>
```javascript
function square(n) {
  return n * n;
}

var wrapped = _([1, 2, 3]);

// Returns an unwrapped value.
wrapped.reduce(_.add);
// => 6

// Returns a wrapped value.
var squares = wrapped.map(square);

_.isArray(squares);
// => false

_.isArray(squares.value());
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L1669 "View in source") [&#x24C9;][1]

Creates a `lodash` object which wraps `value` to enable implicit method
chain sequences. Methods that operate on and return arrays, collections,
and functions can be chained together. Methods that retrieve a single value
or may return a primitive value will automatically end the chain sequence
and return the unwrapped value. Otherwise, the value must be unwrapped
with `_#value`.
<br>
<br>
Explicit chain sequences, which must be unwrapped with `_#value`, may be
enabled using `_.chain`.
<br>
<br>
The execution of chained methods is lazy, that is, it's deferred until
`_#value` is implicitly or explicitly called.
<br>
<br>
Lazy evaluation allows several methods to support shortcut fusion.
Shortcut fusion is an optimization to merge iteratee calls; this avoids
the creation of intermediate arrays and can greatly reduce the number of
iteratee executions. Sections of a chain sequence qualify for shortcut
fusion if the section is applied to an array and iteratees accept only
one argument. The heuristic for whether a section qualifies for shortcut
fusion is subject to change.
<br>
<br>
Chaining is supported in custom builds as long as the `_#value` method is
directly or indirectly included in the build.
<br>
<br>
In addition to lodash methods, wrappers have `Array` and `String` methods.
<br>
<br>
The wrapper `Array` methods are:<br>
`concat`, `join`, `pop`, `push`, `shift`, `sort`, `splice`, and `unshift`
<br>
<br>
The wrapper `String` methods are:<br>
`replace` and `split`
<br>
<br>
The wrapper methods that support shortcut fusion are:<br>
`at`, `compact`, `drop`, `dropRight`, `dropWhile`, `filter`, `find`,
`findLast`, `head`, `initial`, `last`, `map`, `reject`, `reverse`, `slice`,
`tail`, `take`, `takeRight`, `takeRightWhile`, `takeWhile`, and `toArray`
<br>
<br>
The chainable wrapper methods are:<br>
`after`, `ary`, `assign`, `assignIn`, `assignInWith`, `assignWith`, `at`,
`before`, `bind`, `bindAll`, `bindKey`, `castArray`, `chain`, `chunk`,
`commit`, `compact`, `concat`, `conforms`, `constant`, `countBy`, `create`,
`curry`, `debounce`, `defaults`, `defaultsDeep`, `defer`, `delay`,
`difference`, `differenceBy`, `differenceWith`, `drop`, `dropRight`,
`dropRightWhile`, `dropWhile`, `extend`, `extendWith`, `fill`, `filter`,
`flatMap`, `flatMapDeep`, `flatMapDepth`, `flatten`, `flattenDeep`,
`flattenDepth`, `flip`, `flow`, `flowRight`, `fromPairs`, `functions`,
`functionsIn`, `groupBy`, `initial`, `intersection`, `intersectionBy`,
`intersectionWith`, `invert`, `invertBy`, `invokeMap`, `iteratee`, `keyBy`,
`keys`, `keysIn`, `map`, `mapKeys`, `mapValues`, `matches`, `matchesProperty`,
`memoize`, `merge`, `mergeWith`, `method`, `methodOf`, `mixin`, `negate`,
`nthArg`, `omit`, `omitBy`, `once`, `orderBy`, `over`, `overArgs`,
`overEvery`, `overSome`, `partial`, `partialRight`, `partition`, `pick`,
`pickBy`, `plant`, `property`, `propertyOf`, `pull`, `pullAll`, `pullAllBy`,
`pullAllWith`, `pullAt`, `push`, `range`, `rangeRight`, `rearg`, `reject`,
`remove`, `rest`, `reverse`, `sampleSize`, `set`, `setWith`, `shuffle`,
`slice`, `sort`, `sortBy`, `splice`, `spread`, `tail`, `take`, `takeRight`,
`takeRightWhile`, `takeWhile`, `tap`, `throttle`, `thru`, `toArray`,
`toPairs`, `toPairsIn`, `toPath`, `toPlainObject`, `transform`, `unary`,
`union`, `unionBy`, `unionWith`, `uniq`, `uniqBy`, `uniqWith`, `unset`,
`unshift`, `unzip`, `unzipWith`, `update`, `updateWith`, `values`,
`valuesIn`, `without`, `wrap`, `xor`, `xorBy`, `xorWith`, `zip`,
`zipObject`, `zipObjectDeep`, and `zipWith`
<br>
<br>
The wrapper methods that are **not** chainable by default are:<br>
`add`, `attempt`, `camelCase`, `capitalize`, `ceil`, `clamp`, `clone`,
`cloneDeep`, `cloneDeepWith`, `cloneWith`, `conformsTo`, `deburr`,
`defaultTo`, `divide`, `each`, `eachRight`, `endsWith`, `eq`, `escape`,
`escapeRegExp`, `every`, `find`, `findIndex`, `findKey`, `findLast`,
`findLastIndex`, `findLastKey`, `first`, `floor`, `forEach`, `forEachRight`,
`forIn`, `forInRight`, `forOwn`, `forOwnRight`, `get`, `gt`, `gte`, `has`,
`hasIn`, `head`, `identity`, `includes`, `indexOf`, `inRange`, `invoke`,
`isArguments`, `isArray`, `isArrayBuffer`, `isArrayLike`, `isArrayLikeObject`,
`isBoolean`, `isBuffer`, `isDate`, `isElement`, `isEmpty`, `isEqual`,
`isEqualWith`, `isError`, `isFinite`, `isFunction`, `isInteger`, `isLength`,
`isMap`, `isMatch`, `isMatchWith`, `isNaN`, `isNative`, `isNil`, `isNull`,
`isNumber`, `isObject`, `isObjectLike`, `isPlainObject`, `isRegExp`,
`isSafeInteger`, `isSet`, `isString`, `isUndefined`, `isTypedArray`,
`isWeakMap`, `isWeakSet`, `join`, `kebabCase`, `last`, `lastIndexOf`,
`lowerCase`, `lowerFirst`, `lt`, `lte`, `max`, `maxBy`, `mean`, `meanBy`,
`min`, `minBy`, `multiply`, `noConflict`, `noop`, `now`, `nth`, `pad`,
`padEnd`, `padStart`, `parseInt`, `pop`, `random`, `reduce`, `reduceRight`,
`repeat`, `result`, `round`, `runInContext`, `sample`, `shift`, `size`,
`snakeCase`, `some`, `sortedIndex`, `sortedIndexBy`, `sortedLastIndex`,
`sortedLastIndexBy`, `startCase`, `startsWith`, `stubArray`, `stubFalse`,
`stubObject`, `stubString`, `stubTrue`, `subtract`, `sum`, `sumBy`,
`template`, `times`, `toFinite`, `toInteger`, `toJSON`, `toLength`,
`toLower`, `toNumber`, `toSafeInteger`, `toString`, `toUpper`, `trim`,
`trimEnd`, `trimStart`, `truncate`, `unescape`, `uniqueId`, `upperCase`,
`upperFirst`, `value`, and `words`

#### Arguments
1. `value` *(&#42;)*: The value to wrap in a `lodash` instance.

#### Returns
*(Object)*: Returns the new `lodash` wrapper instance.



---





## <a name="_chainvalue"><code>_.chain(value)</code></a>
```javascript
var users = [
  { 'user': 'barney',  'age': 36 },
  { 'user': 'fred',    'age': 40 },
  { 'user': 'pebbles', 'age': 1 }
];

var youngest = _
  .chain(users)
  .sortBy('age')
  .map(function(o) {
    return o.user + ' is ' + o.age;
  })
  .head()
  .value();
// => 'pebbles is 1'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8754 "View in source") [&#x24C9;][1]

Creates a `lodash` wrapper instance that wraps `value` with explicit method
chain sequences enabled. The result of such sequences must be unwrapped
with `_#value`.

#### Since
1.3.0

#### Arguments
1. `value` *(&#42;)*: The value to wrap.

#### Returns
*(Object)*: Returns the new `lodash` wrapper instance.



---





## <a name="_tapvalue-interceptor"><code>_.tap(value, interceptor)</code></a>
```javascript
_([1, 2, 3])
 .tap(function(array) {
   // Mutate input array.
   array.pop();
 })
 .reverse()
 .value();
// => [2, 1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8783 "View in source") [&#x24C9;][1]

This method invokes `interceptor` and returns `value`. The interceptor
is invoked with one argument; *(value)*. The purpose of this method is to
"tap into" a method chain sequence in order to modify intermediate results.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: The value to provide to `interceptor`.
2. `interceptor` *(Function)*: The function to invoke.

#### Returns
*(&#42;)*: Returns `value`.



---





## <a name="_thruvalue-interceptor"><code>_.thru(value, interceptor)</code></a>
```javascript
_('  abc  ')
 .chain()
 .trim()
 .thru(function(value) {
   return [value];
 })
 .value();
// => ['abc']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8811 "View in source") [&#x24C9;][1]

This method is like `_.tap` except that it returns the result of `interceptor`.
The purpose of this method is to "pass thru" values replacing intermediate
results in a method chain sequence.

#### Since
3.0.0

#### Arguments
1. `value` *(&#42;)*: The value to provide to `interceptor`.
2. `interceptor` *(Function)*: The function to invoke.

#### Returns
*(&#42;)*: Returns the result of `interceptor`.



---





## <a name="_prototypesymboliterator"><code>_.prototype[Symbol.iterator]()</code></a>
```javascript
var wrapped = _([1, 2]);

wrapped[Symbol.iterator]() === wrapped;
// => true

Array.from(wrapped);
// => [1, 2]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8966 "View in source") [&#x24C9;][1]

Enables the wrapper to be iterable.

#### Since
4.0.0

#### Returns
*(Object)*: Returns the wrapper object.



---





## <a name="_prototypeatpaths"><code>_.prototype.at([paths])</code></a>
```javascript
var object = { 'a': [{ 'b': { 'c': 3 } }, 4] };

_(object).at(['a[0].b.c', 'a[1]']).value();
// => [3, 4]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8831 "View in source") [&#x24C9;][1]

This method is the wrapper version of `_.at`.

#### Since
1.0.0

#### Arguments
1. `[paths]` *(...(string|string&#91;&#93;))*: The property paths to pick.

#### Returns
*(Object)*: Returns the new `lodash` wrapper instance.



---





## <a name="_prototypechain"><code>_.prototype.chain()</code></a>
```javascript
var users = [
  { 'user': 'barney', 'age': 36 },
  { 'user': 'fred',   'age': 40 }
];

// A sequence without explicit chaining.
_(users).head();
// => { 'user': 'barney', 'age': 36 }

// A sequence with explicit chaining.
_(users)
  .chain()
  .head()
  .pick('user')
  .value();
// => { 'user': 'barney' }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8882 "View in source") [&#x24C9;][1]

Creates a `lodash` wrapper instance with explicit method chain sequences enabled.

#### Since
0.1.0

#### Returns
*(Object)*: Returns the new `lodash` wrapper instance.



---





## <a name="_prototypecommit"><code>_.prototype.commit()</code></a>
```javascript
var array = [1, 2];
var wrapped = _(array).push(3);

console.log(array);
// => [1, 2]

wrapped = wrapped.commit();
console.log(array);
// => [1, 2, 3]

wrapped.last();
// => 3

console.log(array);
// => [1, 2, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8912 "View in source") [&#x24C9;][1]

Executes the chain sequence and returns the wrapped result.

#### Since
3.2.0

#### Returns
*(Object)*: Returns the new `lodash` wrapper instance.



---





## <a name="_prototypenext"><code>_.prototype.next()</code></a>
```javascript
var wrapped = _([1, 2]);

wrapped.next();
// => { 'done': false, 'value': 1 }

wrapped.next();
// => { 'done': false, 'value': 2 }

wrapped.next();
// => { 'done': true, 'value': undefined }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8938 "View in source") [&#x24C9;][1]

Gets the next value on a wrapped object following the
[iterator protocol](https://mdn.io/iteration_protocols#iterator).

#### Since
4.0.0

#### Returns
*(Object)*: Returns the next iterator value.



---





## <a name="_prototypeplantvalue"><code>_.prototype.plant(value)</code></a>
```javascript
function square(n) {
  return n * n;
}

var wrapped = _([1, 2]).map(square);
var other = wrapped.plant([3, 4]);

other.value();
// => [9, 16]

wrapped.value();
// => [1, 4]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L8994 "View in source") [&#x24C9;][1]

Creates a clone of the chain sequence planting `value` as the wrapped value.

#### Since
3.2.0

#### Arguments
1. `value` *(&#42;)*: The value to plant.

#### Returns
*(Object)*: Returns the new `lodash` wrapper instance.



---





## <a name="_prototypereverse"><code>_.prototype.reverse()</code></a>
```javascript
var array = [1, 2, 3];

_(array).reverse().value()
// => [3, 2, 1]

console.log(array);
// => [3, 2, 1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9034 "View in source") [&#x24C9;][1]

This method is the wrapper version of `_.reverse`.
<br>
<br>
**Note:** This method mutates the wrapped array.

#### Since
0.1.0

#### Returns
*(Object)*: Returns the new `lodash` wrapper instance.



---





## <a name="_prototypevalue"><code>_.prototype.value()</code></a>
```javascript
_([1, 2, 3]).value();
// => [1, 2, 3]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L9066 "View in source") [&#x24C9;][1]

Executes the chain sequence to resolve the unwrapped value.

#### Since
0.1.0

#### Aliases
*_.prototype.toJSON, _.prototype.valueOf*

#### Returns
*(&#42;)*: Returns the resolved unwrapped value.



---







# String



## <a name="_camelcasestring"><code>_.camelCase([string=''])</code></a>
```javascript
_.camelCase('Foo Bar');
// => 'fooBar'

_.camelCase('--foo-bar--');
// => 'fooBar'

_.camelCase('__FOO_BAR__');
// => 'fooBar'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14115 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.camelcase "See the npm package") [&#x24C9;][1]

Converts `string` to [camel case](https://en.wikipedia.org/wiki/CamelCase).

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the camel cased string.



---





## <a name="_capitalizestring"><code>_.capitalize([string=''])</code></a>
```javascript
_.capitalize('FRED');
// => 'Fred'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14135 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.capitalize "See the npm package") [&#x24C9;][1]

Converts the first character of `string` to upper case and the remaining
to lower case.

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to capitalize.

#### Returns
*(string)*: Returns the capitalized string.



---





## <a name="_deburrstring"><code>_.deburr([string=''])</code></a>
```javascript
_.deburr('déjà vu');
// => 'deja vu'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14157 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.deburr "See the npm package") [&#x24C9;][1]

Deburrs `string` by converting
[Latin-1 Supplement](https://en.wikipedia.org/wiki/Latin-1_Supplement_(Unicode_block)#Character_table)
and [Latin Extended-A](https://en.wikipedia.org/wiki/Latin_Extended-A)
letters to basic Latin letters and removing
[combining diacritical marks](https://en.wikipedia.org/wiki/Combining_Diacritical_Marks).

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to deburr.

#### Returns
*(string)*: Returns the deburred string.



---





## <a name="_endswithstring-target-positionstringlength"><code>_.endsWith([string=''], [target], [position=string.length])</code></a>
```javascript
_.endsWith('abc', 'c');
// => true

_.endsWith('abc', 'b');
// => false

_.endsWith('abc', 'b', 2);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14185 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.endswith "See the npm package") [&#x24C9;][1]

Checks if `string` ends with the given target string.

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to inspect.
2. `[target]` *(string)*: The string to search for.
3. `[position=string.length]` *(number)*: The position to search up to.

#### Returns
*(boolean)*: Returns `true` if `string` ends with `target`, else `false`.



---





## <a name="_escapestring"><code>_.escape([string=''])</code></a>
```javascript
_.escape('fred, barney, & pebbles');
// => 'fred, barney, &amp; pebbles'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14227 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.escape "See the npm package") [&#x24C9;][1]

Converts the characters "&", "<", ">", '"', and "'" in `string` to their
corresponding HTML entities.
<br>
<br>
**Note:** No other characters are escaped. To escape additional
characters use a third-party library like [_he_](https://mths.be/he).
<br>
<br>
Though the ">" character is escaped for symmetry, characters like
">" and "/" don't need escaping in HTML and have no special meaning
unless they're part of a tag or unquoted attribute value. See
[Mathias Bynens's article](https://mathiasbynens.be/notes/ambiguous-ampersands)
*(under "semi-related fun fact")* for more details.
<br>
<br>
When working with HTML you should always
[quote attribute values](http://wonko.com/post/html-escaping) to reduce
XSS vectors.

#### Since
0.1.0

#### Arguments
1. `[string='']` *(string)*: The string to escape.

#### Returns
*(string)*: Returns the escaped string.



---





## <a name="_escaperegexpstring"><code>_.escapeRegExp([string=''])</code></a>
```javascript
_.escapeRegExp('[lodash](https://lodash.com/)');
// => '\[lodash\]\(https://lodash\.com/\)'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14249 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.escaperegexp "See the npm package") [&#x24C9;][1]

Escapes the `RegExp` special characters "^", "$", "\", ".", "*", "+",
"?", "(", ")", "[", "]", "{", "}", and "|" in `string`.

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to escape.

#### Returns
*(string)*: Returns the escaped string.



---





## <a name="_kebabcasestring"><code>_.kebabCase([string=''])</code></a>
```javascript
_.kebabCase('Foo Bar');
// => 'foo-bar'

_.kebabCase('fooBar');
// => 'foo-bar'

_.kebabCase('__FOO_BAR__');
// => 'foo-bar'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14277 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.kebabcase "See the npm package") [&#x24C9;][1]

Converts `string` to
[kebab case](https://en.wikipedia.org/wiki/Letter_case#Special_case_styles).

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the kebab cased string.



---





## <a name="_lowercasestring"><code>_.lowerCase([string=''])</code></a>
```javascript
_.lowerCase('--Foo-Bar--');
// => 'foo bar'

_.lowerCase('fooBar');
// => 'foo bar'

_.lowerCase('__FOO_BAR__');
// => 'foo bar'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14301 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.lowercase "See the npm package") [&#x24C9;][1]

Converts `string`, as space separated words, to lower case.

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the lower cased string.



---





## <a name="_lowerfirststring"><code>_.lowerFirst([string=''])</code></a>
```javascript
_.lowerFirst('Fred');
// => 'fred'

_.lowerFirst('FRED');
// => 'fRED'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14322 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.lowerfirst "See the npm package") [&#x24C9;][1]

Converts the first character of `string` to lower case.

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the converted string.



---





## <a name="_padstring-length0-chars"><code>_.pad([string=''], [length=0], [chars=' '])</code></a>
```javascript
_.pad('abc', 8);
// => '  abc   '

_.pad('abc', 8, '_-');
// => '_-abc_-_'

_.pad('abc', 3);
// => 'abc'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14347 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.pad "See the npm package") [&#x24C9;][1]

Pads `string` on the left and right sides if it's shorter than `length`.
Padding characters are truncated if they can't be evenly divided by `length`.

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to pad.
2. `[length=0]` *(number)*: The padding length.
3. `[chars=' ']` *(string)*: The string used as padding.

#### Returns
*(string)*: Returns the padded string.



---





## <a name="_padendstring-length0-chars"><code>_.padEnd([string=''], [length=0], [chars=' '])</code></a>
```javascript
_.padEnd('abc', 6);
// => 'abc   '

_.padEnd('abc', 6, '_-');
// => 'abc_-_'

_.padEnd('abc', 3);
// => 'abc'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14386 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.padend "See the npm package") [&#x24C9;][1]

Pads `string` on the right side if it's shorter than `length`. Padding
characters are truncated if they exceed `length`.

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to pad.
2. `[length=0]` *(number)*: The padding length.
3. `[chars=' ']` *(string)*: The string used as padding.

#### Returns
*(string)*: Returns the padded string.



---





## <a name="_padstartstring-length0-chars"><code>_.padStart([string=''], [length=0], [chars=' '])</code></a>
```javascript
_.padStart('abc', 6);
// => '   abc'

_.padStart('abc', 6, '_-');
// => '_-_abc'

_.padStart('abc', 3);
// => 'abc'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14419 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.padstart "See the npm package") [&#x24C9;][1]

Pads `string` on the left side if it's shorter than `length`. Padding
characters are truncated if they exceed `length`.

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to pad.
2. `[length=0]` *(number)*: The padding length.
3. `[chars=' ']` *(string)*: The string used as padding.

#### Returns
*(string)*: Returns the padded string.



---





## <a name="_parseintstring-radix10"><code>_.parseInt(string, [radix=10])</code></a>
```javascript
_.parseInt('08');
// => 8

_.map(['6', '08', '10'], _.parseInt);
// => [6, 8, 10]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14453 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.parseint "See the npm package") [&#x24C9;][1]

Converts `string` to an integer of the specified radix. If `radix` is
`undefined` or `0`, a `radix` of `10` is used unless `value` is a
hexadecimal, in which case a `radix` of `16` is used.
<br>
<br>
**Note:** This method aligns with the
[ES5 implementation](https://es5.github.io/#x15.1.2.2) of `parseInt`.

#### Since
1.1.0

#### Arguments
1. `string` *(string)*: The string to convert.
2. `[radix=10]` *(number)*: The radix to interpret `value` by.

#### Returns
*(number)*: Returns the converted integer.



---





## <a name="_repeatstring-n1"><code>_.repeat([string=''], [n=1])</code></a>
```javascript
_.repeat('*', 3);
// => '***'

_.repeat('abc', 2);
// => 'abcabc'

_.repeat('abc', 0);
// => ''
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14484 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.repeat "See the npm package") [&#x24C9;][1]

Repeats the given string `n` times.

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to repeat.
2. `[n=1]` *(number)*: The number of times to repeat the string.

#### Returns
*(string)*: Returns the repeated string.



---





## <a name="_replacestring-pattern-replacement"><code>_.replace([string=''], pattern, replacement)</code></a>
```javascript
_.replace('Hi Fred', 'Fred', 'Barney');
// => 'Hi Barney'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14512 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.replace "See the npm package") [&#x24C9;][1]

Replaces matches for `pattern` in `string` with `replacement`.
<br>
<br>
**Note:** This method is based on
[`String#replace`](https://mdn.io/String/replace).

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to modify.
2. `pattern` *(RegExp|string)*: The pattern to replace.
3. `replacement` *(Function|string)*: The match replacement.

#### Returns
*(string)*: Returns the modified string.



---





## <a name="_snakecasestring"><code>_.snakeCase([string=''])</code></a>
```javascript
_.snakeCase('Foo Bar');
// => 'foo_bar'

_.snakeCase('fooBar');
// => 'foo_bar'

_.snakeCase('--FOO-BAR--');
// => 'foo_bar'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14540 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.snakecase "See the npm package") [&#x24C9;][1]

Converts `string` to
[snake case](https://en.wikipedia.org/wiki/Snake_case).

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the snake cased string.



---





## <a name="_splitstring-separator-limit"><code>_.split([string=''], separator, [limit])</code></a>
```javascript
_.split('a-b-c', '-', 2);
// => ['a', 'b']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14563 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.split "See the npm package") [&#x24C9;][1]

Splits `string` by `separator`.
<br>
<br>
**Note:** This method is based on
[`String#split`](https://mdn.io/String/split).

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to split.
2. `separator` *(RegExp|string)*: The separator pattern to split by.
3. `[limit]` *(number)*: The length to truncate results to.

#### Returns
*(Array)*: Returns the string segments.



---





## <a name="_startcasestring"><code>_.startCase([string=''])</code></a>
```javascript
_.startCase('--foo-bar--');
// => 'Foo Bar'

_.startCase('fooBar');
// => 'Foo Bar'

_.startCase('__FOO_BAR__');
// => 'FOO BAR'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14605 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.startcase "See the npm package") [&#x24C9;][1]

Converts `string` to
[start case](https://en.wikipedia.org/wiki/Letter_case#Stylistic_or_specialised_usage).

#### Since
3.1.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the start cased string.



---





## <a name="_startswithstring-target-position0"><code>_.startsWith([string=''], [target], [position=0])</code></a>
```javascript
_.startsWith('abc', 'a');
// => true

_.startsWith('abc', 'b');
// => false

_.startsWith('abc', 'b', 1);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14632 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.startswith "See the npm package") [&#x24C9;][1]

Checks if `string` starts with the given target string.

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to inspect.
2. `[target]` *(string)*: The string to search for.
3. `[position=0]` *(number)*: The position to search from.

#### Returns
*(boolean)*: Returns `true` if `string` starts with `target`, else `false`.



---





## <a name="_templatestring-options"><code>_.template([string=''], [options={}])</code></a>
```javascript
/*UnderScore*/
var compiled = _.template("hello: <%= name %>");
compiled({name: 'moe'});
//=> "hello: moe"


var template = _.template("<b><%- value %></b>");
template({value: '<script>'});
//=> "<b>&lt;script&gt;</b>"

/*Lodash*/
// Use the "interpolate" delimiter to create a compiled template.
var compiled = _.template('hello <%= user %>!');
compiled({ 'user': 'fred' });
// => 'hello fred!'

// Use the HTML "escape" delimiter to escape data property values.
var compiled = _.template('<b><%- value %></b>');
compiled({ 'value': '<script>' });
// => '<b>&lt;script&gt;</b>'

// Use the "evaluate" delimiter to execute JavaScript and generate HTML.
var compiled = _.template('<% _.forEach(users, function(user) { %><li><%- user %></li><% }); %>');
compiled({ 'users': ['fred', 'barney'] });
// => '<li>fred</li><li>barney</li>'

// Use the internal `print` function in "evaluate" delimiters.
var compiled = _.template('<% print("hello " + user); %>!');
compiled({ 'user': 'barney' });
// => 'hello barney!'

// Use the ES template literal delimiter as an "interpolate" delimiter.
// Disable support by replacing the "interpolate" delimiter.
var compiled = _.template('hello ${ user }!');
compiled({ 'user': 'pebbles' });
// => 'hello pebbles!'

// Use backslashes to treat delimiters as plain text.
var compiled = _.template('<%= "\\<%- value %\\>" %>');
compiled({ 'value': 'ignored' });
// => '<%- value %>'

// Use the `imports` option to import `jQuery` as `jq`.
var text = '<% jq.each(users, function(user) { %><li><%- user %></li><% }); %>';
var compiled = _.template(text, { 'imports': { 'jq': jQuery } });
compiled({ 'users': ['fred', 'barney'] });
// => '<li>fred</li><li>barney</li>'

// Use the `sourceURL` option to specify a custom sourceURL for the template.
var compiled = _.template('hello <%= user %>!', { 'sourceURL': '/basic/greeting.jst' });
compiled(data);
// => Find the source of "greeting.jst" under the Sources tab or Resources panel of the web inspector.

// Use the `variable` option to ensure a with-statement isn't used in the compiled template.
var compiled = _.template('hi <%= data.user %>!', { 'variable': 'data' });
compiled.source;
// => function(data) {
//   var __t, __p = '';
//   __p += 'hi ' + ((__t = ( data.user )) == null ? '' : __t) + '!';
//   return __p;
// }

// Use custom template delimiters.
_.templateSettings.interpolate = /{{([\s\S]+?)}}/g;
var compiled = _.template('hello {{ user }}!');
compiled({ 'user': 'mustache' });
// => 'hello mustache!'

// Use the `source` property to inline compiled templates for meaningful
// line numbers in error messages and stack traces.
fs.writeFileSync(path.join(process.cwd(), 'jst.js'), '\
  var JST = {\
    "main": ' + _.template(mainText).source + '\
  };\
');
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14743 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.template "See the npm package") [&#x24C9;][1]

Creates a compiled template function that can interpolate data properties
in "interpolate" delimiters, HTML-escape interpolated data properties in
"escape" delimiters, and execute JavaScript in "evaluate" delimiters. Data
properties may be accessed as free variables in the template. If a setting
object is given, it takes precedence over `_.templateSettings` values.
<br>
<br>
**Note:** In the development build `_.template` utilizes
[sourceURLs](http://www.html5rocks.com/en/tutorials/developertools/sourcemaps/#toc-sourceurl)
for easier debugging.
<br>
<br>
For more information on precompiling templates see
[lodash's custom builds documentation](https://lodash.com/custom-builds).
<br>
<br>
For more information on Chrome extension sandboxes see
[Chrome's extensions documentation](https://developer.chrome.com/extensions/sandboxingEval).

#### Underscore
<code>_.template(templateString, [settings]) </code>

#### Since
0.1.0

#### Arguments
1. `[string='']` *(string)*: The template string.
2. `[options={}]` *(Object)*: The options object.
3. `[options.escape=_.templateSettings.escape]` *(RegExp)*: The HTML "escape" delimiter.
4. `[options.evaluate=_.templateSettings.evaluate]` *(RegExp)*: The "evaluate" delimiter.
5. `[options.imports=_.templateSettings.imports]` *(Object)*: An object to import into the template as free variables.
6. `[options.interpolate=_.templateSettings.interpolate]` *(RegExp)*: The "interpolate" delimiter.
7. `[options.sourceURL='lodash.templateSources[n]']` *(string)*: The sourceURL of the compiled template.
8. `[options.variable='obj']` *(string)*: The data object variable name.

#### Returns
*(Function)*: Returns the compiled template function.



---





## <a name="_tolowerstring"><code>_.toLower([string=''])</code></a>
```javascript
_.toLower('--Foo-Bar--');
// => '--foo-bar--'

_.toLower('fooBar');
// => 'foobar'

_.toLower('__FOO_BAR__');
// => '__foo_bar__'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14872 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.tolower "See the npm package") [&#x24C9;][1]

Converts `string`, as a whole, to lower case just like
[String#toLowerCase](https://mdn.io/toLowerCase).

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the lower cased string.



---





## <a name="_toupperstring"><code>_.toUpper([string=''])</code></a>
```javascript
_.toUpper('--foo-bar--');
// => '--FOO-BAR--'

_.toUpper('fooBar');
// => 'FOOBAR'

_.toUpper('__foo_bar__');
// => '__FOO_BAR__'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14897 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.toupper "See the npm package") [&#x24C9;][1]

Converts `string`, as a whole, to upper case just like
[String#toUpperCase](https://mdn.io/toUpperCase).

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the upper cased string.



---





## <a name="_trimstring-charswhitespace"><code>_.trim([string=''], [chars=whitespace])</code></a>
```javascript
_.trim('  abc  ');
// => 'abc'

_.trim('-_-abc-_-', '_-');
// => 'abc'

_.map(['  foo  ', '  bar  '], _.trim);
// => ['foo', 'bar']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14923 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.trim "See the npm package") [&#x24C9;][1]

Removes leading and trailing whitespace or specified characters from `string`.

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to trim.
2. `[chars=whitespace]` *(string)*: The characters to trim.

#### Returns
*(string)*: Returns the trimmed string.



---





## <a name="_trimendstring-charswhitespace"><code>_.trimEnd([string=''], [chars=whitespace])</code></a>
```javascript
_.trimEnd('  abc  ');
// => '  abc'

_.trimEnd('-_-abc-_-', '_-');
// => '-_-abc'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14958 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.trimend "See the npm package") [&#x24C9;][1]

Removes trailing whitespace or specified characters from `string`.

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to trim.
2. `[chars=whitespace]` *(string)*: The characters to trim.

#### Returns
*(string)*: Returns the trimmed string.



---





## <a name="_trimstartstring-charswhitespace"><code>_.trimStart([string=''], [chars=whitespace])</code></a>
```javascript
_.trimStart('  abc  ');
// => 'abc  '

_.trimStart('-_-abc-_-', '_-');
// => 'abc-_-'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L14991 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.trimstart "See the npm package") [&#x24C9;][1]

Removes leading whitespace or specified characters from `string`.

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to trim.
2. `[chars=whitespace]` *(string)*: The characters to trim.

#### Returns
*(string)*: Returns the trimmed string.



---





## <a name="_truncatestring-options"><code>_.truncate([string=''], [options={}])</code></a>
```javascript
_.truncate('hi-diddly-ho there, neighborino');
// => 'hi-diddly-ho there, neighbo...'

_.truncate('hi-diddly-ho there, neighborino', {
  'length': 24,
  'separator': ' '
});
// => 'hi-diddly-ho there,...'

_.truncate('hi-diddly-ho there, neighborino', {
  'length': 24,
  'separator': /,? +/
});
// => 'hi-diddly-ho there...'

_.truncate('hi-diddly-ho there, neighborino', {
  'omission': ' [...]'
});
// => 'hi-diddly-ho there, neig [...]'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15042 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.truncate "See the npm package") [&#x24C9;][1]

Truncates `string` if it's longer than the given maximum string length.
The last characters of the truncated string are replaced with the omission
string which defaults to "...".

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to truncate.
2. `[options={}]` *(Object)*: The options object.
3. `[options.length=30]` *(number)*: The maximum string length.
4. `[options.omission='...']` *(string)*: The string to indicate text is omitted.
5. `[options.separator]` *(RegExp|string)*: The separator pattern to truncate to.

#### Returns
*(string)*: Returns the truncated string.



---





## <a name="_unescapestring"><code>_.unescape([string=''])</code></a>
```javascript
_.unescape('fred, barney, &amp; pebbles');
// => 'fred, barney, & pebbles'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15117 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.unescape "See the npm package") [&#x24C9;][1]

The inverse of `_.escape`; this method converts the HTML entities
`&amp;`, `&lt;`, `&gt;`, `&quot;`, and `&#39;` in `string` to
their corresponding characters.
<br>
<br>
**Note:** No other HTML entities are unescaped. To unescape additional
HTML entities use a third-party library like [_he_](https://mths.be/he).

#### Since
0.6.0

#### Arguments
1. `[string='']` *(string)*: The string to unescape.

#### Returns
*(string)*: Returns the unescaped string.



---





## <a name="_uppercasestring"><code>_.upperCase([string=''])</code></a>
```javascript
_.upperCase('--foo-bar');
// => 'FOO BAR'

_.upperCase('fooBar');
// => 'FOO BAR'

_.upperCase('__foo_bar__');
// => 'FOO BAR'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15144 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.uppercase "See the npm package") [&#x24C9;][1]

Converts `string`, as space separated words, to upper case.

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the upper cased string.



---





## <a name="_upperfirststring"><code>_.upperFirst([string=''])</code></a>
```javascript
_.upperFirst('fred');
// => 'Fred'

_.upperFirst('FRED');
// => 'FRED'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15165 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.upperfirst "See the npm package") [&#x24C9;][1]

Converts the first character of `string` to upper case.

#### Since
4.0.0

#### Arguments
1. `[string='']` *(string)*: The string to convert.

#### Returns
*(string)*: Returns the converted string.



---





## <a name="_wordsstring-pattern"><code>_.words([string=''], [pattern])</code></a>
```javascript
_.words('fred, barney, & pebbles');
// => ['fred', 'barney', 'pebbles']

_.words('fred, barney, & pebbles', /[^, ]+/g);
// => ['fred', 'barney', '&', 'pebbles']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15186 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.words "See the npm package") [&#x24C9;][1]

Splits `string` into an array of its words.

#### Since
3.0.0

#### Arguments
1. `[string='']` *(string)*: The string to inspect.
2. `[pattern]` *(RegExp|string)*: The pattern to match words.

#### Returns
*(Array)*: Returns the words of `string`.



---







# Util



## <a name="_attemptfunc-args"><code>_.attempt(func, [args])</code></a>
```javascript
// Avoid throwing errors for invalid selectors.
var elements = _.attempt(function(selector) {
  return document.querySelectorAll(selector);
}, '>_>');

if (_.isError(elements)) {
  elements = [];
}
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15220 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.attempt "See the npm package") [&#x24C9;][1]

Attempts to invoke `func`, returning either the result or the caught error
object. Any additional arguments are provided to `func` when it's invoked.

#### Since
3.0.0

#### Arguments
1. `func` *(Function)*: The function to attempt.
2. `[args]` *(...&#42;)*: The arguments to invoke `func` with.

#### Returns
*(&#42;)*: Returns the `func` result or error object.



---





## <a name="_bindallobject-methodnames"><code>_.bindAll(object, methodNames)</code></a>
```javascript
var view = {
  'label': 'docs',
  'click': function() {
    console.log('clicked ' + this.label);
  }
};

_.bindAll(view, ['click']);
jQuery(element).on('click', view.click);
// => Logs 'clicked docs' when clicked.
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15254 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.bindall "See the npm package") [&#x24C9;][1]

Binds methods of an object to the object itself, overwriting the existing
method.
<br>
<br>
**Note:** This method doesn't set the "length" property of bound functions.

#### Since
0.1.0

#### Arguments
1. `object` *(Object)*: The object to bind and assign the bound methods to.
2. `methodNames` *(...(string|string&#91;&#93;))*: The object method names to bind.

#### Returns
*(Object)*: Returns `object`.



---





## <a name="_condpairs"><code>_.cond(pairs)</code></a>
```javascript
var func = _.cond([
  [_.matches({ 'a': 1 }),           _.constant('matches A')],
  [_.conforms({ 'b': _.isNumber }), _.constant('matches B')],
  [_.stubTrue,                      _.constant('no match')]
]);

func({ 'a': 1, 'b': 2 });
// => 'matches A'

func({ 'a': 0, 'b': 1 });
// => 'matches B'

func({ 'a': '1', 'b': '2' });
// => 'no match'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15291 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.cond "See the npm package") [&#x24C9;][1]

Creates a function that iterates over `pairs` and invokes the corresponding
function of the first predicate to return truthy. The predicate-function
pairs are invoked with the `this` binding and arguments of the created
function.

#### Since
4.0.0

#### Arguments
1. `pairs` *(Array)*: The predicate-function pairs.

#### Returns
*(Function)*: Returns the new composite function.



---





## <a name="_conformssource"><code>_.conforms(source)</code></a>
```javascript
var objects = [
  { 'a': 2, 'b': 1 },
  { 'a': 1, 'b': 2 }
];

_.filter(objects, _.conforms({ 'b': function(n) { return n > 1; } }));
// => [{ 'a': 1, 'b': 2 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15337 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.conforms "See the npm package") [&#x24C9;][1]

Creates a function that invokes the predicate properties of `source` with
the corresponding property values of a given object, returning `true` if
all predicates return truthy, else `false`.
<br>
<br>
**Note:** The created function is equivalent to `_.conformsTo` with
`source` partially applied.

#### Since
4.0.0

#### Arguments
1. `source` *(Object)*: The object of property predicates to conform to.

#### Returns
*(Function)*: Returns the new spec function.



---





## <a name="_constantvalue"><code>_.constant(value)</code></a>
```javascript
var objects = _.times(2, _.constant({ 'a': 1 }));

console.log(objects);
// => [{ 'a': 1 }, { 'a': 1 }]

console.log(objects[0] === objects[1]);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15360 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.constant "See the npm package") [&#x24C9;][1]

Creates a function that returns `value`.

#### Since
2.4.0

#### Arguments
1. `value` *(&#42;)*: The value to return from the new function.

#### Returns
*(Function)*: Returns the new constant function.



---





## <a name="_defaulttovalue-defaultvalue"><code>_.defaultTo(value, defaultValue)</code></a>
```javascript
_.defaultTo(1, 10);
// => 1

_.defaultTo(undefined, 10);
// => 10
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15386 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.defaultto "See the npm package") [&#x24C9;][1]

Checks `value` to determine whether a default value should be returned in
its place. The `defaultValue` is returned if `value` is `NaN`, `null`,
or `undefined`.

#### Since
4.14.0

#### Arguments
1. `value` *(&#42;)*: The value to check.
2. `defaultValue` *(&#42;)*: The default value.

#### Returns
*(&#42;)*: Returns the resolved value.



---





## <a name="_flowfuncs"><code>_.flow([funcs])</code></a>
```javascript
function square(n) {
  return n * n;
}

var addSquare = _.flow([_.add, square]);
addSquare(1, 2);
// => 9
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15412 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.flow "See the npm package") [&#x24C9;][1]

Creates a function that returns the result of invoking the given functions
with the `this` binding of the created function, where each successive
invocation is supplied the return value of the previous.

#### Since
3.0.0

#### Arguments
1. `[funcs]` *(...(Function|Function&#91;&#93;))*: The functions to invoke.

#### Returns
*(Function)*: Returns the new composite function.



---





## <a name="_flowrightfuncs"><code>_.flowRight([funcs])</code></a>
```javascript
function square(n) {
  return n * n;
}

var addSquare = _.flowRight([square, _.add]);
addSquare(1, 2);
// => 9
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15435 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.flowright "See the npm package") [&#x24C9;][1]

This method is like `_.flow` except that it creates a function that
invokes the given functions from right to left.

#### Since
3.0.0

#### Arguments
1. `[funcs]` *(...(Function|Function&#91;&#93;))*: The functions to invoke.

#### Returns
*(Function)*: Returns the new composite function.



---





## <a name="_identityvalue"><code>_.identity(value)</code></a>
```javascript
var object = { 'a': 1 };

console.log(_.identity(object) === object);
// => true
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15453 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.identity "See the npm package") [&#x24C9;][1]

This method returns the first argument it receives.

#### Since
0.1.0

#### Arguments
1. `value` *(&#42;)*: Any value.

#### Returns
*(&#42;)*: Returns `value`.



---





## <a name="_iterateefunc_identity"><code>_.iteratee([func=_.identity])</code></a>
```javascript
var users = [
  { 'user': 'barney', 'age': 36, 'active': true },
  { 'user': 'fred',   'age': 40, 'active': false }
];

// The `_.matches` iteratee shorthand.
_.filter(users, _.iteratee({ 'user': 'barney', 'active': true }));
// => [{ 'user': 'barney', 'age': 36, 'active': true }]

// The `_.matchesProperty` iteratee shorthand.
_.filter(users, _.iteratee(['user', 'fred']));
// => [{ 'user': 'fred', 'age': 40 }]

// The `_.property` iteratee shorthand.
_.map(users, _.iteratee('user'));
// => ['barney', 'fred']

// Create custom iteratee shorthands.
_.iteratee = _.wrap(_.iteratee, function(iteratee, func) {
  return !_.isRegExp(func) ? iteratee(func) : function(string) {
    return func.test(string);
  };
});

_.filter(['abc', 'def'], /ef/);
// => ['def']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15499 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.iteratee "See the npm package") [&#x24C9;][1]

Creates a function that invokes `func` with the arguments of the created
function. If `func` is a property name, the created function returns the
property value for a given element. If `func` is an array or object, the
created function returns `true` for elements that contain the equivalent
source properties, otherwise it returns `false`.

#### Since
4.0.0

#### Arguments
1. `[func=_.identity]` *(&#42;)*: The value to convert to a callback.

#### Returns
*(Function)*: Returns the callback.



---





## <a name="_matchessource"><code>_.matches(source)</code></a>
```javascript
var objects = [
  { 'a': 1, 'b': 2, 'c': 3 },
  { 'a': 4, 'b': 5, 'c': 6 }
];

_.filter(objects, _.matches({ 'a': 4, 'c': 6 }));
// => [{ 'a': 4, 'b': 5, 'c': 6 }]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15531 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.matches "See the npm package") [&#x24C9;][1]

Creates a function that performs a partial deep comparison between a given
object and `source`, returning `true` if the given object has equivalent
property values, else `false`.
<br>
<br>
**Note:** The created function is equivalent to `_.isMatch` with `source`
partially applied.
<br>
<br>
Partial comparisons will match empty array and empty object `source`
values against any array or object value, respectively. See `_.isEqual`
for a list of supported value comparisons.

#### Since
3.0.0

#### Arguments
1. `source` *(Object)*: The object of property values to match.

#### Returns
*(Function)*: Returns the new spec function.



---





## <a name="_matchespropertypath-srcvalue"><code>_.matchesProperty(path, srcValue)</code></a>
```javascript
var objects = [
  { 'a': 1, 'b': 2, 'c': 3 },
  { 'a': 4, 'b': 5, 'c': 6 }
];

_.find(objects, _.matchesProperty('a', 4));
// => { 'a': 4, 'b': 5, 'c': 6 }
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15561 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.matchesproperty "See the npm package") [&#x24C9;][1]

Creates a function that performs a partial deep comparison between the
value at `path` of a given object to `srcValue`, returning `true` if the
object value is equivalent, else `false`.
<br>
<br>
**Note:** Partial comparisons will match empty array and empty object
`srcValue` values against any array or object value, respectively. See
`_.isEqual` for a list of supported value comparisons.

#### Since
3.2.0

#### Arguments
1. `path` *(Array|string)*: The path of the property to get.
2. `srcValue` *(&#42;)*: The value to match.

#### Returns
*(Function)*: Returns the new spec function.



---





## <a name="_methodpath-args"><code>_.method(path, [args])</code></a>
```javascript
var objects = [
  { 'a': { 'b': _.constant(2) } },
  { 'a': { 'b': _.constant(1) } }
];

_.map(objects, _.method('a.b'));
// => [2, 1]

_.map(objects, _.method(['a', 'b']));
// => [2, 1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15589 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.method "See the npm package") [&#x24C9;][1]

Creates a function that invokes the method at `path` of a given object.
Any additional arguments are provided to the invoked method.

#### Since
3.7.0

#### Arguments
1. `path` *(Array|string)*: The path of the method to invoke.
2. `[args]` *(...&#42;)*: The arguments to invoke the method with.

#### Returns
*(Function)*: Returns the new invoker function.



---





## <a name="_methodofobject-args"><code>_.methodOf(object, [args])</code></a>
```javascript
var array = _.times(3, _.constant),
    object = { 'a': array, 'b': array, 'c': array };

_.map(['a[2]', 'c[0]'], _.methodOf(object));
// => [2, 0]

_.map([['a', '2'], ['c', '0']], _.methodOf(object));
// => [2, 0]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15618 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.methodof "See the npm package") [&#x24C9;][1]

The opposite of `_.method`; this method creates a function that invokes
the method at a given path of `object`. Any additional arguments are
provided to the invoked method.

#### Since
3.7.0

#### Arguments
1. `object` *(Object)*: The object to query.
2. `[args]` *(...&#42;)*: The arguments to invoke the method with.

#### Returns
*(Function)*: Returns the new invoker function.



---





## <a name="_mixinobjectlodash-source-options"><code>_.mixin([object=lodash], source, [options={}])</code></a>
```javascript
function vowels(string) {
  return _.filter(string, function(v) {
    return /[aeiou]/i.test(v);
  });
}

_.mixin({ 'vowels': vowels });
_.vowels('fred');
// => ['e']

_('fred').vowels().value();
// => ['e']

_.mixin({ 'vowels': vowels }, { 'chain': false });
_('fred').vowels();
// => ['e']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15660 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.mixin "See the npm package") [&#x24C9;][1]

Adds all own enumerable string keyed function properties of a source
object to the destination object. If `object` is a function, then methods
are added to its prototype as well.
<br>
<br>
**Note:** Use `_.runInContext` to create a pristine `lodash` function to
avoid conflicts caused by modifying the original.

#### Since
0.1.0

#### Arguments
1. `[object=lodash]` *(Function|Object)*: The destination object.
2. `source` *(Object)*: The object of functions to add.
3. `[options={}]` *(Object)*: The options object.
4. `[options.chain=true]` *(boolean)*: Specify whether mixins are chainable.

#### Returns
*(&#42;)*: Returns `object`.



---





## <a name="_noconflict"><code>_.noConflict()</code></a>
```javascript
var lodash = _.noConflict();
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15709 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.noconflict "See the npm package") [&#x24C9;][1]

Reverts the `_` variable to its previous value and returns a reference to
the `lodash` function.

#### Since
0.1.0

#### Returns
*(Function)*: Returns the `lodash` function.



---





## <a name="_noop"><code>_.noop()</code></a>
```javascript
_.times(2, _.noop);
// => [undefined, undefined]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15728 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.noop "See the npm package") [&#x24C9;][1]

This method returns `undefined`.

#### Since
2.3.0



---





## <a name="_nthargn0"><code>_.nthArg([n=0])</code></a>
```javascript
var func = _.nthArg(1);
func('a', 'b', 'c', 'd');
// => 'b'

var func = _.nthArg(-2);
func('a', 'b', 'c', 'd');
// => 'c'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15752 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.ntharg "See the npm package") [&#x24C9;][1]

Creates a function that gets the argument at index `n`. If `n` is negative,
the nth argument from the end is returned.

#### Since
4.0.0

#### Arguments
1. `[n=0]` *(number)*: The index of the argument to return.

#### Returns
*(Function)*: Returns the new pass-thru function.



---





## <a name="_overiteratees_identity"><code>_.over([iteratees=[_.identity]])</code></a>
```javascript
var func = _.over([Math.max, Math.min]);

func(1, 2, 3, 4);
// => [4, 1]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15777 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.over "See the npm package") [&#x24C9;][1]

Creates a function that invokes `iteratees` with the arguments it receives
and returns their results.

#### Since
4.0.0

#### Arguments
1. `[iteratees=[_.identity]]` *(...(Function|Function&#91;&#93;))*: The iteratees to invoke.

#### Returns
*(Function)*: Returns the new function.



---





## <a name="_overeverypredicates_identity"><code>_.overEvery([predicates=[_.identity]])</code></a>
```javascript
var func = _.overEvery([Boolean, isFinite]);

func('1');
// => true

func(null);
// => false

func(NaN);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15803 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.overevery "See the npm package") [&#x24C9;][1]

Creates a function that checks if **all** of the `predicates` return
truthy when invoked with the arguments it receives.

#### Since
4.0.0

#### Arguments
1. `[predicates=[_.identity]]` *(...(Function|Function&#91;&#93;))*: The predicates to check.

#### Returns
*(Function)*: Returns the new function.



---





## <a name="_oversomepredicates_identity"><code>_.overSome([predicates=[_.identity]])</code></a>
```javascript
var func = _.overSome([Boolean, isFinite]);

func('1');
// => true

func(null);
// => true

func(NaN);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15829 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.oversome "See the npm package") [&#x24C9;][1]

Creates a function that checks if **any** of the `predicates` return
truthy when invoked with the arguments it receives.

#### Since
4.0.0

#### Arguments
1. `[predicates=[_.identity]]` *(...(Function|Function&#91;&#93;))*: The predicates to check.

#### Returns
*(Function)*: Returns the new function.



---





## <a name="_propertypath"><code>_.property(path)</code></a>
```javascript
var objects = [
  { 'a': { 'b': 2 } },
  { 'a': { 'b': 1 } }
];

_.map(objects, _.property('a.b'));
// => [2, 1]

_.map(_.sortBy(objects, _.property(['a', 'b'])), 'a.b');
// => [1, 2]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15853 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.property "See the npm package") [&#x24C9;][1]

Creates a function that returns the value at `path` of a given object.

#### Since
2.4.0

#### Arguments
1. `path` *(Array|string)*: The path of the property to get.

#### Returns
*(Function)*: Returns the new accessor function.



---





## <a name="_propertyofobject"><code>_.propertyOf(object)</code></a>
```javascript
var array = [0, 1, 2],
    object = { 'a': array, 'b': array, 'c': array };

_.map(['a[2]', 'c[0]'], _.propertyOf(object));
// => [2, 0]

_.map([['a', '2'], ['c', '0']], _.propertyOf(object));
// => [2, 0]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15878 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.propertyof "See the npm package") [&#x24C9;][1]

The opposite of `_.property`; this method creates a function that returns
the value at a given path of `object`.

#### Since
3.0.0

#### Arguments
1. `object` *(Object)*: The object to query.

#### Returns
*(Function)*: Returns the new accessor function.



---





## <a name="_rangestart0-end-step1"><code>_.range([start=0], end, [step=1])</code></a>
```javascript
_.range(4);
// => [0, 1, 2, 3]

_.range(-4);
// => [0, -1, -2, -3]

_.range(1, 5);
// => [1, 2, 3, 4]

_.range(0, 20, 5);
// => [0, 5, 10, 15]

_.range(0, -4, -1);
// => [0, -1, -2, -3]

_.range(1, 4, 0);
// => [1, 1, 1]

_.range(0);
// => []
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15925 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.range "See the npm package") [&#x24C9;][1]

Creates an array of numbers *(positive and/or negative)* progressing from
`start` up to, but not including, `end`. A step of `-1` is used if a negative
`start` is specified without an `end` or `step`. If `end` is not specified,
it's set to `start` with `start` then set to `0`.
<br>
<br>
**Note:** JavaScript follows the IEEE-754 standard for resolving
floating-point values which can produce unexpected results.

#### Since
0.1.0

#### Arguments
1. `[start=0]` *(number)*: The start of the range.
2. `end` *(number)*: The end of the range.
3. `[step=1]` *(number)*: The value to increment or decrement by.

#### Returns
*(Array)*: Returns the range of numbers.



---





## <a name="_rangerightstart0-end-step1"><code>_.rangeRight([start=0], end, [step=1])</code></a>
```javascript
_.rangeRight(4);
// => [3, 2, 1, 0]

_.rangeRight(-4);
// => [-3, -2, -1, 0]

_.rangeRight(1, 5);
// => [4, 3, 2, 1]

_.rangeRight(0, 20, 5);
// => [15, 10, 5, 0]

_.rangeRight(0, -4, -1);
// => [-3, -2, -1, 0]

_.rangeRight(1, 4, 0);
// => [1, 1, 1]

_.rangeRight(0);
// => []
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15963 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.rangeright "See the npm package") [&#x24C9;][1]

This method is like `_.range` except that it populates values in
descending order.

#### Since
4.0.0

#### Arguments
1. `[start=0]` *(number)*: The start of the range.
2. `end` *(number)*: The end of the range.
3. `[step=1]` *(number)*: The value to increment or decrement by.

#### Returns
*(Array)*: Returns the range of numbers.



---





## <a name="_runincontextcontextroot"><code>_.runInContext([context=root])</code></a>
```javascript
_.mixin({ 'foo': _.constant('foo') });

var lodash = _.runInContext();
lodash.mixin({ 'bar': lodash.constant('bar') });

_.isFunction(_.foo);
// => true
_.isFunction(_.bar);
// => false

lodash.isFunction(lodash.foo);
// => false
lodash.isFunction(lodash.bar);
// => true

// Create a suped-up `defer` in Node.js.
var defer = _.runInContext({ 'setTimeout': setImmediate }).defer;
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L1427 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.runincontext "See the npm package") [&#x24C9;][1]

Create a new pristine `lodash` function using the `context` object.

#### Since
1.1.0

#### Arguments
1. `[context=root]` *(Object)*: The context object.

#### Returns
*(Function)*: Returns a new `lodash` function.



---





## <a name="_stubarray"><code>_.stubArray()</code></a>
```javascript
var arrays = _.times(2, _.stubArray);

console.log(arrays);
// => [[], []]

console.log(arrays[0] === arrays[1]);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L15983 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.stubarray "See the npm package") [&#x24C9;][1]

This method returns a new empty array.

#### Since
4.13.0

#### Returns
*(Array)*: Returns the new empty array.



---





## <a name="_stubfalse"><code>_.stubFalse()</code></a>
```javascript
_.times(2, _.stubFalse);
// => [false, false]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16000 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.stubfalse "See the npm package") [&#x24C9;][1]

This method returns `false`.

#### Since
4.13.0

#### Returns
*(boolean)*: Returns `false`.



---





## <a name="_stubobject"><code>_.stubObject()</code></a>
```javascript
var objects = _.times(2, _.stubObject);

console.log(objects);
// => [{}, {}]

console.log(objects[0] === objects[1]);
// => false
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16022 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.stubobject "See the npm package") [&#x24C9;][1]

This method returns a new empty object.

#### Since
4.13.0

#### Returns
*(Object)*: Returns the new empty object.



---





## <a name="_stubstring"><code>_.stubString()</code></a>
```javascript
_.times(2, _.stubString);
// => ['', '']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16039 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.stubstring "See the npm package") [&#x24C9;][1]

This method returns an empty string.

#### Since
4.13.0

#### Returns
*(string)*: Returns the empty string.



---





## <a name="_stubtrue"><code>_.stubTrue()</code></a>
```javascript
_.times(2, _.stubTrue);
// => [true, true]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16056 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.stubtrue "See the npm package") [&#x24C9;][1]

This method returns `true`.

#### Since
4.13.0

#### Returns
*(boolean)*: Returns `true`.



---





## <a name="_timesn-iteratee_identity"><code>_.times(n, [iteratee=_.identity])</code></a>
```javascript
_.times(3, String);
// => ['0', '1', '2']

 _.times(4, _.constant(0));
// => [0, 0, 0, 0]
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16079 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.times "See the npm package") [&#x24C9;][1]

Invokes the iteratee `n` times, returning an array of the results of
each invocation. The iteratee is invoked with one argument; *(index)*.

#### Since
0.1.0

#### Arguments
1. `n` *(number)*: The number of times to invoke `iteratee`.
2. `[iteratee=_.identity]` *(Function)*: The function invoked per iteration.

#### Returns
*(Array)*: Returns the array of results.



---





## <a name="_topathvalue"><code>_.toPath(value)</code></a>
```javascript
_.toPath('a.b.c');
// => ['a', 'b', 'c']

_.toPath('a[0].b.c');
// => ['a', '0', 'b', 'c']
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16114 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.topath "See the npm package") [&#x24C9;][1]

Converts `value` to a property path array.

#### Since
4.0.0

#### Arguments
1. `value` *(&#42;)*: The value to convert.

#### Returns
*(Array)*: Returns the new property path array.



---





## <a name="_uniqueidprefix"><code>_.uniqueId([prefix=''])</code></a>
```javascript
_.uniqueId('contact_');
// => 'contact_104'

_.uniqueId();
// => '105'
```
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16138 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.uniqueid "See the npm package") [&#x24C9;][1]

Generates a unique ID. If `prefix` is given, the ID is appended to it.

#### Since
0.1.0

#### Arguments
1. `[prefix='']` *(string)*: The value to prefix the ID with.

#### Returns
*(string)*: Returns the unique ID.



---



# Properties

## <a name="_version"><code>_.VERSION</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L16829 "View in source") [&#x24C9;][1]

(string): The semantic version number.


## <a name="_templatesettings"><code>_.templateSettings</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L1738 "View in source") [&#x24C3;](https://www.npmjs.com/package/lodash.templatesettings "See the npm package") [&#x24C9;][1]

(Object): By default, the template delimiters used by lodash are like those in
embedded Ruby *(ERB)* as well as ES2015 template strings. Change the
following template settings to use alternative delimiters.

---


## <a name="_templatesettingsescape"><code>_.templateSettings.escape</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L1746 "View in source") [&#x24C9;][1]

(RegExp): Used to detect `data` property values to be HTML-escaped.

---


## <a name="_templatesettingsevaluate"><code>_.templateSettings.evaluate</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L1754 "View in source") [&#x24C9;][1]

(RegExp): Used to detect code to be evaluated.


---

## <a name="_templatesettingsimports"><code>_.templateSettings.imports</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L1778 "View in source") [&#x24C9;][1]

(Object): Used to import variables into the compiled template.

---

## <a name="_templatesettingsinterpolate"><code>_.templateSettings.interpolate</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L1762 "View in source") [&#x24C9;][1]

(RegExp): Used to detect `data` property values to inject.

---


## <a name="_templatesettingsvariable"><code>_.templateSettings.variable</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L1770 "View in source") [&#x24C9;][1]

(string): Used to reference the data object in the template text.

---


# Methods

## <a name="_templatesettingsimports_"><code>_.templateSettings.imports._</code></a>
[&#x24C8;](https://github.com/lodash/lodash/blob/4.17.3/lodash.js#L1786 "View in source") [&#x24C9;][1]

A reference to the `lodash` function.
---


 [1]: #array "Jump back to the TOC."
