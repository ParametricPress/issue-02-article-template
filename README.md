# Article Title

TK short description of article.

## Local Setup

To run the article locally, make sure you have NodeJS and NPM installed. Then clone or download this repository.

### Installing dependencies

1. Install `idyll` globally (only need to do this once): `npm install -g idyll`
2. Install local dependencies: `npm install`

### Running local dev server

1. Run `idyll --template _local.html` in the root of this project.

## How do I...

### Import a dataset?

- Add your data to the `data` folder, either as a CSV or JSON file.

Then use the `[data /]` tag to load it as a variable. For example to
load a dataset and provide it as input to a table component:

```
[data name:"myDatasetName" source:"my-dataset-file.csv"  /]

[Table data:myDatasetName /]
```

### Make a custom component?

- Add your component to the `components` folder. Use either of the existing components in there as a guide. If you're familiar with React, start with `custom-component.js`, otherwise if you are more comfortable using a tool like D3 where you manually handle updates / redraws, start with `custom-d3-component.js`.

- Any component that you put in that folder will immediately be available in the Idyll markup. Files named like `custom-component.js` can be imported as `[CustomComponent /]`.

