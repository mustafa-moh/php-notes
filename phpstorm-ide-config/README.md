# Configure PhpStorm Code Schema

### Import PhpStorm Laravel built-in schema 
1. Navigate to the project **settings** from `File -> Settings`
2. Then select from the left sidebar menu **Editor -> Code Style** then select **PHP** from code style sub-menu.
3. To use the predefined Laravel code schema/style in PhpStorm, After choosing PHP in prev step, navigate to **Set Form...** link which appears on the top right content.
4. Then select **Predefine Style**  and select **Laravel** from the built-in schema list.

### Import Custom Laravel code style with some modifications
The predefined Laravel code style on PhpStorm not cover all Laravel code standards, so i built new schema from the built-in schema with some modifications. Follow these steps to import it:
1. Download `Laravel.codestyle.json` file from current dir.
2. Then on PhpStorm navigate to `File -> Settings ->  Editor -> Code Styles -> PHP`.
3. Navigate to **Schema** dropdown which appears on the top of the right section.
4. Then click on **Schema** gear icon and select `Import schema -> JSCS config file` and attache `Laravel.codestyle.json` 
5. Select the imported schema. Apply and Save the configurations.  
