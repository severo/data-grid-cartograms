# data-grid-cartograms

A curated collection of grid cartograms, in a machine-readable format.

> A grid cartogram is a representation barely similar to a map, that distorts the forms and areas, and assigns to every subdivision one and only one unit of a grid. They are also referred as grid map, mosaic cartogram, pseudo-Demers cartogram, square cartograph maps, geofacets, geogrid, tile grid map, or tile map. For example, the following map represents every state of the United States by exactly one square in a rectangular grid:

![Example of a grid cartogram, with one cell by state](./cartogram_us_example.png)

## Structure of this collection

The collected grid cartograms are stored in a directory structure that follows the pattern:

```
.
└── <category>
    └── <whole>
        └── <parts>
            └── <name>
                ├── grid.csv
                ├── ids.csv
                └── README.md
```

Where:

- <category> is a broad category of the cartogram, such as "continents" or "countries".
- <whole> is the whole entity that the cartogram represents, such as "us", "africa", or "world".
- <parts> is the parts that the whole is divided into, such as "States", "Countries", or "Seats".
- <name> is the name of the cartogram
- `grid.csv` contains the grid cartogram as ASCII art. A filled cell is represented by an identifier. For readability, all the identifiers should have the same length and an empty cell should be contain the same number of spaces. For countries or states, the identifier can be the ISO 3166-1 alpha-2 or alpha-3 code.
- `ids.csv` contains the mapping between the identifiers in `grid.csv` and the actual names of the parts. The first column contains the identifier, and the second column contains the name. Additional columns can be added for metadata.
- `README.md` contains a description of the cartogram, including the source, date, and any other relevant information.

The ASCII-art CSV is self-explaining, here is a grid cartogram if the world, by @clemsos:

```csv
   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,ISL,   ,   ,   ,DNK,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,NOR,SWE,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,FIN,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,   ,CAN,   ,   ,   ,   ,   ,   ,   ,GBR,   ,   ,NLD,EST,LVA,LTU,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,   ,USA,   ,   ,   ,BHS,   ,   ,   ,IRL,   ,BEL,LUX,DEU,POL,CZE,BLR,SVK,RUS,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,MEX,   ,   ,   ,CUB,HTI,DOM,   ,   ,   ,FRA,CHE,LIE,AUT,BGR,HUN,MDA,UKR,UZB,KAZ,MNG,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,GTM,BLZ,   ,   ,JAM,ATG,KNA,   ,   ,   ,AND,MCO,ITA,SVN,MNE,SRB,ROU,   ,ARM,TKM,KGZ,CHN,PRK,KOR,   ,JPN,   ,   ,   ,   
   ,   ,   ,SLV,   ,   ,LCA,VCT,DMA,   ,   ,PRT,ESP,   ,SMR,HRV,MKD,BIH,CYP,TUR,GEO,AZE,TJK,NPL,BTN,   ,   ,   ,   ,   ,   ,   
   ,   ,   ,HND,   ,   ,   ,   ,GRD,BRB,   ,   ,MLT,   ,   ,ALB,GRC,   ,   ,SYR,IRQ,IRN,AFG,PAK,BGD,MMR,THA,LAO,   ,   ,   ,   
   ,   ,   ,NIC,CRI,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,LBN,KWT,   ,   ,IND,   ,   ,KHM,VNM,   ,   ,   ,   
   ,   ,   ,   ,PAN,   ,   ,   ,   ,   ,   ,   ,   ,MAR,DZA,TUN,LBY,EGY,ISR,JOR,SAU,BHR,   ,   ,LKA,   ,MYS,   ,   ,   ,   ,   
   ,   ,   ,ECU,COL,VEN,   ,   ,   ,   ,   ,   ,SEN,MRT,MLI,NER,TCD,SDN,ERI,   ,ARE,QAT,   ,MDV,   ,SGP,BRN,   ,PHL,   ,   ,   
   ,   ,   ,PER,GUY,SUR,TTO,   ,   ,   ,   ,GMB,GIN,BFA,NGA,CAF,SSD,ETH,DJI,   ,YEM,OMN,   ,   ,   ,   ,IDN,PNG,   ,   ,   ,   
   ,   ,   ,   ,BRA,   ,   ,   ,   ,   ,   ,   ,GNB,SLE,CIV,TGO,CMR,UGA,SOM,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,   ,   ,BOL,   ,   ,   ,   ,   ,   ,   ,LBR,GHA,BEN,COG,COD,KEN,   ,   ,   ,   ,   ,   ,TLS,   ,MHL,KIR,PLW,   ,   ,   
   ,   ,   ,PRY,URY,   ,   ,   ,   ,   ,   ,   ,CPV,   ,STP,GNQ,RWA,TZA,   ,   ,   ,   ,   ,AUS,   ,   ,TUV,FSM,NRU,   ,   ,   
   ,   ,   ,   ,ARG,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,GAB,BDI,MWI,   ,   ,COM,   ,   ,   ,NZL,   ,WSM,TON,   ,   ,   ,   
   ,   ,   ,   ,CHL,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,AGO,ZMB,MOZ,   ,MDG,MUS,   ,   ,   ,   ,   ,FJI,SLB,VUT,   ,   ,   
   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,NAM,BWA,ZWE,   ,   ,SYC,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,ZAF,LSO,SWZ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   ,   
```

## Contribute

You want to signal a grid cartogram should be added to the collection? Please open an [issue](https://github.com/severo/data-grid-cartograms/issues/new?template=propose-a-new-grid-cartogram.md) and paste the reference URL. We will then take care of transcribing it to the ASCII-art data format.

You want to add the data for a grid cartogram? Open a [pull request](https://github.com/severo/data-grid-cartograms/pulls) where you add a new directory to the collection. Take care of following the [structure](#structure-of-this-collection) and the formats of `grid.csv` and `ids.csv`. Also, please add a `README.md` file with a description of the cartogram, including the source, date, and any other relevant information. Finally, update the root `index.json` file to include the new cartogram.

Other ideas? Open an issue or a pull request and let's discuss!

## Explore the collection

You can browse all grid cartograms contributed so far in this [observable notebook](https://observablehq.com/@mauforonda/grid-cartogram-collection).

## Read more on grid cartograms

In 2020, I wrote a [review about grid cartograms](https://observablehq.com/@severo/grid-cartograms) on Observable. It contains a good list of grid cartograms for countries, continents and the world, and I discussed the terms and the uses for such a chart.

I also wrote some other notebooks around grid cartograms: utilities to load, convert and display the data, intents to automatically create grid cartograms, and tools to compare the accuracy of grid cartograms. You can check them ut in the [Grid cartograms Observable's collection](https://observablehq.com/collection/@severo/grid-maps).

## Tools

Some visualization and mapping tools that could work well with the grid cartograms in this repository:

- https://eurostat.github.io/gridviz/: JavaScript library for visualizing gridded data

Open a PR/issue to propose other tools!

## Related projects

- https://github.com/hafen/grid-designer/ / https://github.com/hafen/geofacet: Geo Grid Designer publishes dozens of grid cartograms in tidy CSV files.

