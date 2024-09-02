## Initialize a Gutenberg Block

1. Go to the `wp-content/plugins`folder.
   ![Nagivate to the wordpress plugin directory](./previews/navigate_to_plugin_directory.jpg)

2. Run this command to create a plugin called `bwl-todo-list`.

```bash
npx @wordpress/create-block@latest bwl-todo-list
```

3. Type `y` to proceed with the installation.

![continue npm packages installation](/previews/continue_package_installation.jpg)

4. Based on your internet speed, completing the installation process will take a while. So, keep patience.

![Installing packages](/previews/installing_packages.jpg)

5. Once everything is completed, you will get this screen.

![success screen](/previews/success_screen.jpg)

6. Now, inside the plugins folder, you will see the new plugin.

![new plugin installed](/previews/new_plugin_installed.jpg)

7. Using the command line, enter that folder and run the following command.

```bash
npm start
```

It will compile all the JavaScript and SASS files. Also, keep watching for any changes and automatically compile the new SASS and JavaScript files.

![npm start command](/previews/npm_start_command.jpg)

8. Now, change the meta information inside the bwl-todo-list.php file.

![changne plugin meta information](/previews/change_plugin_meta_information.jpg)

9. Next, go to the src/block.json file.

![update block.json file](/previews/update_block_json_file.jpg)

In the `block.json` file, the most important tag is the **name**. So, do not forget to update the name value.

![update name value](/previews/update_name_value.jpg)

10. All is good! Now, we have to log in to the WordPress admin panel and activate the plugin.

![activate the plugin](/previews/activate_the_plugin.jpg)

11. Now, our plugin is activated, and we should see our new block. Go to any page. Click the **Plus** icon to add a new block and search for the **to-do**. You will see the output in the following screenshot.

![search for the todo block](/previews/search_for_todo_block.jpg)

### Change the block icon

1. Navigate to the **block.json** file. From the [WordPress Dashicon](https://developer.wordpress.org/resource/dashicons) site, we can choose our icon. Replace the icon value with your preferred icon.

![change block icons](/previews/change_icon.jpg)

#### Example

![change block icons](/previews/example_of_change_icon_output.jpg)

### Block File Structure

1. There are a couple of files inside the src folder. Index.js file loads the required files from the back-end and front-end editors. The edit.js file is used for the back-end editor, and the save.js file produces the output for the front end.
2. React and JSX knowledge are required to add options to the blocks.
3. Do not use any direct HTML inside the edit function. Instead, use the **wp-components** to create all the input, textarea, and dropdown fields.
