
<a name="paths"></a>
## Resources

<a name="dictionary_resource"></a>
### Dictionary
API from getting translations


<a name="dictionary-srclang-dstlang-text-get"></a>
#### translate word or phrase
```
GET /dictionary/{srcLang}/{dstLang}/{text}
```


##### Parameters

|Type|Name|Schema|
|---|---|---|
|**Path**|**dstLang**  <br>*required*|string|
|**Path**|**srcLang**  <br>*required*|string|
|**Path**|**text**  <br>*required*|string|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[DictionaryEntry](#dictionaryentry)|


<a name="subtitles_resource"></a>
### Subtitles
API for adding subtitles from different sources


<a name="subtitles-post"></a>
#### Add subtitles from Opensubtitles or YouTube
```
POST /subtitles
```


##### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[SubtitlesPost](#subtitlespost)|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[Subtitles](#subtitles)|


<a name="subtitles-id-get"></a>
#### Returns subtitles by id
```
GET /subtitles/{id}
```


##### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|ID of subtitles|integer|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|subtitle-like format|[Subtitles](#subtitles)|


<a name="user_resource"></a>
### User
API for working with users


<a name="user-post"></a>
#### Create user
```
POST /user
```


##### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[UserPost](#userpost)|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|No Content|


<a name="user-put"></a>
#### Edit user
```
PUT /user
```


##### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[UserPut](#userput)|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|No Content|


<a name="user-login-get"></a>
#### Get user info
```
GET /user/{login}
```


##### Parameters

|Type|Name|Schema|
|---|---|---|
|**Path**|**login**  <br>*required*|string|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[User](#user)|


<a name="user-login-delete"></a>
#### Delete user
```
DELETE /user/{login}
```


##### Parameters

|Type|Name|Schema|
|---|---|---|
|**Path**|**login**  <br>*required*|string|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|No Content|


<a name="vocabulary_resource"></a>
### Vocabulary
API for working with vocabularies


<a name="vocabulary-post"></a>
#### Create vocabulary
```
POST /vocabulary
```


##### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[VocabularyPost](#vocabularypost)|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|No Content|
|**400**|In case of wrong request|No Content|
|**401**|If user unauthorized|No Content|


<a name="vocabulary-get"></a>
#### Returns a list of vocabularies
```
GET /vocabulary
```


##### Description
If mineOnly=false return only published vocabularies, return all vocabularies otherwise


##### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**limit**  <br>*optional*|Number of items in response|integer|`30`|
|**Query**|**mineOnly**  <br>*optional*|Show only vocabularies created by current user|boolean|`"false"`|
|**Query**|**offset**  <br>*optional*|Offset for result list|integer|`0`|
|**Query**|**query**  <br>*optional*|String to provide search in titles|string||


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|A list of vocabularies.|[Vocabularies](#vocabularies)|
|**403**|If mineOnly=true and user not authorized|No Content|


##### Produces

* `application/json`


<a name="vocabulary-put"></a>
#### Edit vocabulary
```
PUT /vocabulary
```


##### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[VocabularyPut](#vocabularyput)|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|No Content|


<a name="vocabulary-id-get"></a>
#### Returns vocabulary by id
```
GET /vocabulary/{id}
```


##### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|ID of vocabulary|integer|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|A list of words|[Vocabulary](#vocabulary)|


<a name="vocabulary-id-delete"></a>
#### Delete vocabulary
```
DELETE /vocabulary/{id}
```


##### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|ID of vocabulary|integer|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|No Content|


<a name="vocabulary-id-save-get"></a>
#### Save ANKI file
```
GET /vocabulary/{id}/save
```


##### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|ID of vocabulary|integer|


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Anki file|No Content|



