
<a name="definitions"></a>
## Definitions

<a name="contentsource"></a>
### ContentSource
Respresents subtitles source


|Name|Description|Schema|
|---|---|---|
|**id**  <br>*optional*|**Example** : `53`|integer|
|**type**  <br>*optional*|**Example** : `"OpenSubtitles"`|enum (OpenSubtitles, Youtube)|
|**url**  <br>*optional*|**Example** : `"https://www.opensubtitles.org/en/subtitles/7047679/game-of-thrones-stormborn-en"`|string|


<a name="dictionaryentry"></a>
### DictionaryEntry
Represents dictionary entry


|Name|Description|Schema|
|---|---|---|
|**dstLang**  <br>*optional*|**Example** : `"RU"`|string|
|**source**  <br>*optional*|Dictionary name  <br>**Example** : `"ABBYY"`|enum (ABBYY)|
|**srcLang**  <br>*optional*|**Example** : `"EN"`|string|
|**translations**  <br>*optional*|**Example** : `[ "победа", "победить", "выиграть", "достичь" ]`|< string > array|
|**word**  <br>*optional*|**Example** : `"win"`|string|


<a name="line"></a>
### Line
Represents line in subtitles


|Name|Description|Schema|
|---|---|---|
|**endTime**  <br>*optional*|miliseconds  <br>**Example** : `2899`|integer|
|**id**  <br>*optional*|**Example** : `3676347`|integer|
|**startTime**  <br>*optional*|miliseconds  <br>**Example** : `2678`|integer|
|**subtitlesId**  <br>*optional*|**Example** : `42`|integer|
|**text**  <br>*optional*|**Example** : `"I won't return to King's Landing until I have that for you."`|string|


<a name="subtitles"></a>
### Subtitles
Represents subtitles


|Name|Description|Schema|
|---|---|---|
|**id**  <br>*optional*|**Example** : `1324`|integer|
|**lang**  <br>*optional*|**Example** : `"EN"`|string|
|**lines**  <br>*optional*||< [Line](#line) > array|
|**title**  <br>*optional*|**Example** : `"Game of Thrones subtitles S07E02"`|string|
|**type**  <br>*optional*|**Example** : `"OpenSubtitles"`|enum (OpenSubtitles, YouTube)|
|**url**  <br>*optional*|**Example** : `"https://www.opensubtitles.org/en/subtitles/7047679/game-of-thrones-stormborn-en"`|string|


<a name="subtitlespost"></a>
### SubtitlesPost
Entity for adding subtitles


|Name|Description|Schema|
|---|---|---|
|**lang**  <br>*optional*|**Example** : `"EN"`|string|
|**type**  <br>*optional*|**Example** : `"OpenSubtitles"`|enum (OpenSubtitles, YouTube)|
|**url**  <br>*optional*|**Example** : `"https://www.opensubtitles.org/en/subtitles/7047679/game-of-thrones-stormborn-en"`|string|


<a name="user"></a>
### User
Represents user entoty


|Name|Description|Schema|
|---|---|---|
|**id**  <br>*optional*|**Example** : `543`|integer|
|**learningLang**  <br>*optional*|**Example** : `"EN"`|string|
|**login**  <br>*optional*|**Example** : `"sntp"`|string|
|**name**  <br>*optional*|**Example** : `"Carl Ivanec"`|string|
|**nativeLang**  <br>*optional*|**Example** : `"RU"`|string|


<a name="userpost"></a>
### UserPost
Entity for creating user


|Name|Description|Schema|
|---|---|---|
|**learningLang**  <br>*optional*|**Example** : `"EN"`|string|
|**login**  <br>*optional*|**Example** : `"sntp"`|string|
|**name**  <br>*optional*|**Example** : `"Jon Petrov"`|string|
|**nativeLang**  <br>*optional*|**Example** : `"RU"`|string|
|**password**  <br>*optional*|**Example** : `"qwerty"`|string|


<a name="userput"></a>
### UserPut
Entity for update user


|Name|Description|Schema|
|---|---|---|
|**currentPassword**  <br>*optional*|**Example** : `"qwerty"`|string|
|**id**  <br>*optional*|**Example** : `13123`|integer|
|**learningLang**  <br>*optional*|**Example** : `"EN"`|string|
|**login**  <br>*optional*|**Example** : `"sntp"`|string|
|**name**  <br>*optional*|**Example** : `"Roma Romov"`|string|
|**nativeLang**  <br>*optional*|**Example** : `"RU"`|string|
|**newPasword**  <br>*optional*|**Example** : `"Super-$tronk_passw0rd!"`|string|


<a name="usershort"></a>
### UserShort
Entity to display briefly user info


|Name|Description|Schema|
|---|---|---|
|**id**  <br>*optional*|**Example** : `5434`|integer|
|**name**  <br>*optional*|**Example** : `"Jo Jo"`|string|


<a name="vocabularies"></a>
### Vocabularies
Response for search


|Name|Description|Schema|
|---|---|---|
|**count**  <br>*optional*|Overall number of vocabularies satisfying serch criteria  <br>**Example** : `42`|integer|
|**limit**  <br>*optional*|**Example** : `0`|integer|
|**offset**  <br>*optional*|**Example** : `30`|integer|
|**vocabularies**  <br>*optional*|List of briefly vocabulary information|< [VocabularyShort](#vocabularyshort) > array|


<a name="vocabulary"></a>
### Vocabulary
Represents full vocabulary info


|Name|Description|Schema|
|---|---|---|
|**author**  <br>*optional*||[UserShort](#usershort)|
|**created**  <br>*optional*|timestamp when vocabulary was created  <br>**Example** : `1500926232`|integer|
|**description**  <br>*optional*|**Example** : `"Top 30 useful words"`|string|
|**dstLang**  <br>*optional*|Language of vocabulary  <br>**Example** : `"RU"`|string|
|**id**  <br>*optional*|**Example** : `15324`|integer|
|**modified**  <br>*optional*|timestamp when vocabulary was modified for the last time  <br>**Example** : `1501039483`|integer|
|**rating**  <br>*optional*|average 5-point rating  <br>**Example** : `4.8`|number|
|**source**  <br>*optional*||[ContentSource](#contentsource)|
|**srcLang**  <br>*optional*|Language of subtitles  <br>**Example** : `"EN"`|string|
|**title**  <br>*optional*|**Example** : `"Inception 2010 Advanced"`|string|
|**words**  <br>*optional*||< [Word](#word) > array|


<a name="vocabularypost"></a>
### VocabularyPost
Entity for create vocatulary


|Name|Description|Schema|
|---|---|---|
|**description**  <br>*optional*|**Example** : `"Top 30 useful words"`|string|
|**dstLang**  <br>*optional*|Language of vocabulary  <br>**Example** : `"RU"`|string|
|**sourceId**  <br>*optional*|**Example** : `45`|integer|
|**srcLang**  <br>*optional*|Language of subtitles  <br>**Example** : `"EN"`|string|
|**title**  <br>*optional*|**Example** : `"Inception 2010 Advanced"`|string|
|**words**  <br>*optional*||< [WordPost](#wordpost) > array|


<a name="vocabularyput"></a>
### VocabularyPut
Entity for update vocabulary


|Name|Description|Schema|
|---|---|---|
|**description**  <br>*optional*|**Example** : `"Top 30 useful words"`|string|
|**dstLang**  <br>*optional*|Language of vocabulary  <br>**Example** : `"RU"`|string|
|**id**  <br>*optional*|ID of vocabulary to be updated  <br>**Example** : `15324`|integer|
|**srcLang**  <br>*optional*|Language of subtitles  <br>**Example** : `"EN"`|string|
|**title**  <br>*optional*|**Example** : `"Inception 2010 Advanced"`|string|
|**words**  <br>*optional*||< [WordPut](#wordput) > array|


<a name="vocabularyshort"></a>
### VocabularyShort
Short info for search


|Name|Description|Schema|
|---|---|---|
|**created**  <br>*optional*|timestamp  <br>**Example** : `1500926232`|integer|
|**id**  <br>*optional*|**Example** : `15324`|integer|
|**rating**  <br>*optional*|average 5-point rating  <br>**Example** : `4.8`|number|
|**title**  <br>*optional*|**Example** : `"Inception 2010 Advanced"`|string|
|**words**  <br>*optional*|Number of words in this vocabulary  <br>**Example** : `30`|integer|


<a name="word"></a>
### Word
Represents a word in vocabulary


|Name|Description|Schema|
|---|---|---|
|**context**  <br>*optional*||[WordContext](#wordcontext)|
|**id**  <br>*optional*|**Example** : `26534`|integer|
|**translation**  <br>*optional*|**Example** : `"сдаваться"`|string|
|**vocabularyId**  <br>*optional*|**Example** : `345`|integer|
|**word**  <br>*optional*|**Example** : `"give up"`|string|


<a name="wordcontext"></a>
### WordContext
Represents context in which word was occured


|Name|Description|Schema|
|---|---|---|
|**indexes**  <br>*optional*|**Example** : `[ 1 ]`|< integer > array|
|**text**  <br>*optional*|**Example** : `"djfklasjflksdjf win dfdfsf"`|string|


<a name="wordpost"></a>
### WordPost
Entity for adding a word


|Name|Description|Schema|
|---|---|---|
|**contextIndexes**  <br>*optional*|**Example** : `[ 1 ]`|< integer > array|
|**contextText**  <br>*optional*|**Example** : `"djfklasjflksdjf win dfdfsf"`|string|
|**lineId**  <br>*optional*|**Example** : `912384`|integer|
|**translation**  <br>*optional*|**Example** : `"победить"`|string|
|**vocabularyId**  <br>*optional*|**Example** : `345`|integer|
|**word**  <br>*optional*|**Example** : `"win"`|string|


<a name="wordput"></a>
### WordPut
Represents an entity for editing word


|Name|Description|Schema|
|---|---|---|
|**context**  <br>*optional*||[WordContext](#wordcontext)|
|**id**  <br>*optional*|**Example** : `432134`|integer|
|**translation**  <br>*optional*|**Example** : `"победить"`|string|
|**vocabularyId**  <br>*optional*|**Example** : `345`|integer|
|**word**  <br>*optional*|**Example** : `"win"`|string|



