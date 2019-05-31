# Hagerty - Batch Update Vlocity Component Documentation

<img src="https://github.com/dbandi/Hagerty/blob/master/image4.png" width="300">

## vehicleGrid

Data grid / accordion and record editor component.
#### template: forceIQ-vlcEditBlock
<img src="https://github.com/dbandi/Hagerty/blob/master/image1.png" width="300">

The forceIQ-vlcEdit block works like a regular edit block. In the structure under design mode,
you can load standard vlocity components from the “Inputs” category. This will drive the
expanded section of the grid.

The grid columns and row are configured through Edit as JSON.

JSON Configuration
<img src="https://github.com/dbandi/Hagerty/blob/master/image10.png" width="300">

The allowed maximum height for the grid record expansion.
```
maxExpansionHeight = 1000px
```

Adding this property will create an index for each record
```
trackingIndexField = vehicleIndex
```

Columns define the grid columns. Each entry will have a label which will represent the header
and the fields which will define the data displayed in the column.
```
columns = []
```
```
{
  "label": "Vehicle",
  "field": [
    "vehicleYear",
    "vehicleMake",
    "vehicleModel";
  ]
}
```

## vehicleGridBatchEdit

Batch edit component for an edit block within the same step.
```
template = forceIQ-vlcBatchUpdate
```
<img src="https://github.com/dbandi/Hagerty/blob/master/image5.png" width="300">
<img src="https://github.com/dbandi/Hagerty/blob/master/image9.png" width="300">

The forceIQ-vlcBatchUpdate works like a regular edit block. In the structure under design mode,
you can load standard vlocity components from the “Inputs” category. This will drive the fields
that can be updated in a forceIQ-vlcEditBlock within the same step. The field names requires an
“edit_” prefix then the name of element on the grid block to define which field will be updated.

The batch update will display a button which will pop a screen where you can enter values to
run a batch edit. Each record from the edit block will require to be selected before it can be
updated. The values for the batch edit form will be prepopulated by values where all the
selected values have the same value.


<img src="https://github.com/dbandi/Hagerty/blob/master/image2.png" width="300">

JSON Configuration
<img src="https://github.com/dbandi/Hagerty/blob/master/image8.png" width="300">

```
  "target": "vehicleGrid"
```
Target defines the element name of the `forceIQ-vlcEditBlock` where the batch update will be applied.

## storageManager

Storage location data management
`template: hagerty-vlcStorageManager`
<img src="https://github.com/dbandi/Hagerty/blob/master/image7.png" width="300">

The hagerty-vlcStorageManager works like a regular edit block. In the structure under design mode, you can load standard vlocity components from the “Inputs” category. This will drive the fields that will be assigned on vlocity omniscript response data. Each field will require a prefix, the prefix is assigned in component JSON configuration.

<img src="https://github.com/dbandi/Hagerty/blob/master/image6.png" width="300">

JSON Configuration
<img src="https://github.com/dbandi/Hagerty/blob/master/image3.png" width="300">
