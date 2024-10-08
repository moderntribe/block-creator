## Block creation command

### Installation 

Edit composer.json by adding new repository
```json
{
    "type": "vcs",
    "url": "https://github.com/moderntribe/block-creator.git"
}
```

Run 
```
composer require --dev moderntribe/block-creator:dev-main
```

### Usage

Run 

```
./vendor/bin/block-creator
```
Command will display prompt for block attributes:
```
Namespace (Default: tribe): tribe
Block Name (Default: example-block): example-block
Block Title (Default: Example): Example
Block Description: Some description
Block Category (Default: theme): 
Path to theme blocks folder (Default: <path_to_project>/wp-content/themes/core/blocks): 
Start block creation from template? (Y/n): 
```
After command finishes run new block will be created under the path provided
It will have basic block.json with pre-defined data from inputs, styles, basic js files and render file

You can avoid prompting into the terminal by running command with params:
```
./vendor/bin/block-creator namespace=tribe block_name=example-block block_title=Example block_description="Some description" block_category=theme path_to_dir="/app/www/"
```
