Chef Solo is a standalone mode of Chef that allows you to run Chef recipes on a node without the need for a Chef Server. Here are some common `chef-solo` commands along with examples:

### 1. Running Chef Solo:

- **Basic Chef Solo Run:**
  ```bash
  chef-solo -c solo.rb -j node.json
  ```
  This command runs Chef Solo using the specified configuration file (`solo.rb`) and node JSON file (`node.json`).

- **Specify Cookbook Path:**
  ```bash
  chef-solo -c solo.rb -j node.json -o "recipe[my_cookbook::my_recipe]"
  ```
  Runs a specific recipe from a cookbook. The `-o` option allows you to specify the run list.

### 2. Configuration Files:

- **Specify Alternate Configuration File:**
  ```bash
  chef-solo -c path/to/alternate/solo.rb -j node.json
  ```
  If your `solo.rb` is in a different location, you can specify it with the `-c` option.

### 3. Node JSON:

- **Use a Different Node JSON File:**
  ```bash
  chef-solo -c solo.rb -j path/to/alternate/node.json
  ```
  Allows you to use a different JSON file for node attributes.

### 4. Cookbooks:

- **Specify Cookbook Path:**
  ```bash
  chef-solo -c solo.rb -j node.json -o "recipe[my_cookbook::my_recipe]" -r path/to/cookbooks
  ```
  Specifies the path to the cookbooks to be used by Chef Solo.

### 5. Other Options:

- **Run in Debug Mode:**
  ```bash
  chef-solo -c solo.rb -j node.json -l debug
  ```
  Runs Chef Solo in debug mode for more detailed output.

- **Print the Version:**
  ```bash
  chef-solo -v
  ```
  Prints the Chef Solo version.

### Example Files:

#### `solo.rb`:

```ruby
file_cache_path "/var/chef-solo"
cookbook_path "/path/to/cookbooks"
```

#### `node.json`:

```json
{
  "run_list": ["recipe[my_cookbook::my_recipe]"],
  "my_cookbook": {
    "my_attribute": "attribute_value"
  }
}
```

These examples assume that you have a Chef cookbook (`my_cookbook`) with a recipe (`my_recipe`). Adjust the paths and attributes based on your project structure and requirements.
