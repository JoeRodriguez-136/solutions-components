# feature-list



<!-- Auto Generated Below -->


## Properties

| Property                  | Attribute                     | Description                                                                                                                                          | Type                 | Default     |
| ------------------------- | ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- | ----------- |
| `applyLayerViewFilter`    | `apply-layer-view-filter`     | boolean: If true will consider the FeatureFilter applied on the layerview                                                                            | `boolean`            | `false`     |
| `highlightOnHover`        | `highlight-on-hover`          | boolean: Highlight feature on map optional (default false) boolean to indicate if we should highlight when hover on Feature in list                  | `boolean`            | `false`     |
| `highlightOnMap`          | `highlight-on-map`            | boolean: Highlight feature on map optional (default false) boolean to indicate if we should highlight and zoom to the extent of the feature geometry | `boolean`            | `false`     |
| `mapView`                 | --                            | esri/views/View: https://developers.arcgis.com/javascript/latest/api-reference/esri-views-MapView.html                                               | `MapView`            | `undefined` |
| `noFeaturesFoundMsg`      | `no-features-found-msg`       | string: Message to be displayed when features are not found                                                                                          | `string`             | `undefined` |
| `pageSize`                | `page-size`                   | number: Number features to be fetched per page, by default 100 features will be fetched                                                              | `number`             | `100`       |
| `reportingOptions`        | --                            | IReportingOptions: Key options for reporting                                                                                                         | `IReportingOptions`  | `undefined` |
| `selectedLayerId`         | `selected-layer-id`           | string: Layer id of the feature layer to show the list                                                                                               | `string`             | `undefined` |
| `showErrorWhenNoFeatures` | `show-error-when-no-features` | boolean: If true will show error msg when features are not present                                                                                   | `boolean`            | `true`      |
| `showFeatureSymbol`       | `show-feature-symbol`         | boolean: If true display's feature symbol on each feature item                                                                                       | `boolean`            | `false`     |
| `showInitialLoading`      | `show-initial-loading`        | boolean: Show initial loading indicator when creating list                                                                                           | `boolean`            | `true`      |
| `showUserImageInList`     | `show-user-image-in-list`     | boolean: If true display's profile img on each feature item                                                                                          | `boolean`            | `false`     |
| `sortingInfo`             | --                            | ISortingInfo: Sorting field and order using which features list will be sorted                                                                       | `ISortingInfo`       | `undefined` |
| `textSize`                | `text-size`                   | string(small/large): Controls the font size of the title                                                                                             | `"large" \| "small"` | `"large"`   |
| `whereClause`             | `where-clause`                | string: where clause to filter the features list                                                                                                     | `string`             | `undefined` |


## Events

| Event           | Description                                               | Type                   |
| --------------- | --------------------------------------------------------- | ---------------------- |
| `featureSelect` | Emitted on demand when feature is selected using the list | `CustomEvent<Graphic>` |


## Methods

### `refresh(maintainPageState?: boolean) => Promise<void>`

Refresh the feature list which will fetch the latest features and update the features list

#### Parameters

| Name                | Type      | Description                                        |
| ------------------- | --------- | -------------------------------------------------- |
| `maintainPageState` | `boolean` | If true feature list page state will be maintained |

#### Returns

Type: `Promise<void>`

Promise that resolves when the operation is complete


## Dependencies

### Used by

 - [crowdsource-reporter](../crowdsource-reporter)
 - [feature-details](../feature-details)

### Depends on

- calcite-panel
- calcite-loader
- calcite-notice
- calcite-list
- calcite-pagination
- calcite-list-item
- calcite-avatar
- calcite-icon
- calcite-tooltip

### Graph
```mermaid
graph TD;
  feature-list --> calcite-panel
  feature-list --> calcite-loader
  feature-list --> calcite-notice
  feature-list --> calcite-list
  feature-list --> calcite-pagination
  feature-list --> calcite-list-item
  feature-list --> calcite-avatar
  feature-list --> calcite-icon
  feature-list --> calcite-tooltip
  calcite-panel --> calcite-action
  calcite-panel --> calcite-action-menu
  calcite-panel --> calcite-scrim
  calcite-action --> calcite-loader
  calcite-action --> calcite-icon
  calcite-action-menu --> calcite-action
  calcite-action-menu --> calcite-popover
  calcite-popover --> calcite-action
  calcite-popover --> calcite-icon
  calcite-scrim --> calcite-loader
  calcite-notice --> calcite-icon
  calcite-list --> calcite-scrim
  calcite-list --> calcite-stack
  calcite-list --> calcite-filter
  calcite-filter --> calcite-input
  calcite-input --> calcite-progress
  calcite-input --> calcite-icon
  calcite-pagination --> calcite-icon
  calcite-list-item --> calcite-icon
  calcite-list-item --> calcite-handle
  calcite-list-item --> calcite-action
  calcite-handle --> calcite-icon
  calcite-avatar --> calcite-icon
  crowdsource-reporter --> feature-list
  feature-details --> feature-list
  style feature-list fill:#f9f,stroke:#333,stroke-width:4px
```

----------------------------------------------

*Built with [StencilJS](https://stenciljs.com/)*
