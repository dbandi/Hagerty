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

