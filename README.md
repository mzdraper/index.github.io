# BlackLandscapesMatter

## What is this?

BlackLandscapesMatter is a working atlas of events related to BlackLivesMatter and African-American Diaspora. This map juxtaposes murders--both convicted and non-convicted--that fueled the movement with protests that have empowered the movement.

[Check out the map!](https://mzdraper.github.io/index.github.io/)

## How do I edit?

If you're not an experienced coder, don't worry! I've written extensive comments throughout the code that tells you what's going on. You can edit on the GitHub file [here](https://github.com/mzdraper/index.github.io/blob/master/index.html).

1. To edit the file, click the pencil icon on the top right. This will bring you to Edit Mode.
2. If you're adding a protest, first figure out what size range it fits inside of: 100-499, 500-999 or 1000+. These numerical categories are named `geojsonSmallProtests`, `geojsonMediumProtests` and `geojsonLargeProtests` respectively. (GeoJSON is the structure and file type for the data).
3. One you have figured out which category you want to add the data, copy and paste the following at the end of the file, but just before the `]};`.
```
,{
    type: 'Feature',
    geometry: {
        type: 'Point',
        coordinates: [Longitude, Latitude]
    },
        properties: {}
}
```
4. Replace your longitutde and latitude points where indicated. If you're using Google or another conventional site to get the data points, they typically come in `Latitude, Longitude` format, so it might be useful to double check them if you're feeling unsure.
5. If you're adding a murder data point, edit geojson for `convicted` or `notConvicted`.
6. Copy and paste the same data and paste it using the same directions.
7. To add their name, follow the same conventions as the others, editing the `property` value as needed.
8. Press the green Commit button at the bottom and leave a brief message about what you edited using the following convention: `[protest or murder] | [category] | [victim or city name] | [date]`

Whether you edit, add or delete anything, please leave a commit message with your data source eg a link to a news article or video.

Thanks so much for checking out this project, and I hope you'll add to it! Reach out if you have any questions!
