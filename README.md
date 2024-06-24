# Hugo Preview of ACT Rules Branches

This quickly generates an HTML preview of the ACT Rules markdown files on your current branch,
so can be used to check your own PRs before committing and to review other peoples PRs.

- no dependencies other than Hugo (and Hugo itself has no dependencies) so easy to get working
- very quick to generate a preview (less than 0.2 seconds to process all markdown files)

## Getting started 

1. Download the `act-rules-preview` repo as a sibling folder of `act-rules` repo
2. Download and install hugo from https://gohugo.io/installation/ 
3. `cd` to the `act-rules-preview` folder which contains `config.toml` (see below)
4. Run the `hugo` command with no parameters

The published rules files are in the `public` folder.

## Structure

- `config.toml` is the main hugo configuration file
- `layouts/_default/home.html` is the template that generates the home page
- `layouts/_default/list.html` is currently unused
- `layouts/_default/single.html` is the template that generates rules pages
- `layouts/partials/single.html` is the template that generates rules pages
- `static/css/preview.css` is the CSS file for the generated pages
- `public` contains the generated html files

## Known Problems

- local definitions like `[attribute value ][]` are not included in built HTML