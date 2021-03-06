# Adquery QID

Adquery QID Module. For assistance setting up your module please contact us at [prebid@adquery.io](prebid@adquery.io).

### Prebid Params

Individual params may be set for the Adquery ID Submodule. At least one identifier must be set in the params.

```
pbjs.setConfig({
    usersync: {
        userIds: [{
            name: 'qid',
            storage: {
                name: 'qid',
                type: 'html5'
            }
        }]
    }
});
```
## Parameter Descriptions for the `usersync` Configuration Section
The below parameters apply only to the Adquery User ID Module integration.

| Param under usersync.userIds[] | Scope | Type | Description | Example |
| --- | --- | --- | --- | --- |
| name | Required | String | ID value for the Adquery ID module - `"qid"` | `"qid"` |
| storage | Required | Object | The publisher must specify the local storage in which to store the results of the call to get the user ID. | |
| storage.type | Required | String | This is where the results of the user ID will be stored. The recommended method is `localStorage` by specifying `html5`. | `"html5"` |
| storage.name | Required | String | The name of the html5 local storage where the user ID will be stored. | `"qid"` |
| storage.expires | Optional | Integer | How long (in days) the user ID information will be stored. | `365` |
| value | Optional | Object | Used only if the page has a separate mechanism for storing the Adquery ID. The value is an object containing the values to be sent to the adapters. In this scenario, no URL is called and nothing is added to local storage | `{"qid": "2abf9f001fcd81241b67"}` |
| params | Optional | Object | Used to store params for the id system |
| params.url | Optional | String | Set an alternate GET url for qid with this parameter |
| params.urlArg | Optional | Object | Optional url parameter for params.url |
