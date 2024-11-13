# Static Prefix Adder

**Static Prefix Adder** is a web-based tool that helps developers easily add a static file prefix to URLs in HTML content. This is particularly useful for web developers working with frameworks like **Django**, where static files are often referenced with a specific syntax (e.g., `{% static 'path/to/file' %}`). With this tool, you can quickly add prefixes to your URLs without manually editing each one.

## Features

- **Prefix & Suffix Customization**: Add a static prefix and suffix to your URLs (e.g., `{% static 'path/to/file' %}`).
- **Conditional File Patterns**: Apply the prefix only to specific file types (e.g., `css/`, `js/`).
- **Automatic URL Processing**: Paste your HTML content with URLs, and the tool will automatically add the specified static prefix to matching links.
- **Copy Output**: Once the processing is complete, you can easily copy the modified HTML to the clipboard.

## How It Works

1. **Input HTML**: Paste your HTML code containing URLs (e.g., `<script src="js/app.js"></script>`).
2. **Set Prefix & Suffix**: Define the static prefix and suffix. For example:
   - **Prefix**: `{% static '`
   - **Suffix**: `' %}`
3. **Define Conditions**: Specify folder name patterns (e.g., `js/`, `css/`) to apply the prefix only to matching files.
4. **Run the Tool**: Click "**RUN**" to process the HTML content and add the static prefix.
5. **Copy Output**: After the tool processes your content, click "**COPY**" to copy the updated HTML to your clipboard.

## Usage

1. **Enter Prefix & Suffix**: 
   - In the **Prefix** field, enter the static prefix (e.g., `{% static '`).
   - In the **Suffix** field, enter the suffix (e.g., `' %}`).

2. **Add Folder Name Patterns**: 
   - In the "**ENTER THE FOLDER NAME**" section, enter folder patterns (e.g., `css/`, `js/`). These patterns help the tool know which URLs should be updated with the static prefix.
   - You can add more patterns by clicking the "**+ Add Pattern**" button and remove unwanted ones by clicking the "**Remove**" button next to a pattern.

3. **Paste HTML Content**: Paste your HTML content, including URLs (e.g., `<script src="js/app.js"></script>`) in the `input-links` textarea.

4. **Process the Content**: Click "**RUN**" to apply the static prefix and suffix to the relevant URLs.

5. **Copy the Output**: Once the content is processed, the modified HTML will appear in the "Output" section. Click "**COPY**" to copy the updated content to your clipboard.

## Example

### Before:
```
html
<link href="css/styles.css" rel="stylesheet">
<script src="js/app.js"></script>
<img src="images/logo.png" alt="Logo">
```
### After:
Assuming you set the prefix to {% static ' and the suffix to ' %}, and added css/ and js/ as folder patterns, the output would be:
```
html    
<link href="{% static 'css/styles.css' %}" rel="stylesheet">
<script src="{% static 'js/app.js' %}"></script>
<img src="images/logo.png" alt="Logo">
```
Note: Images or other non-matching file paths won't be altered unless you specify a pattern for them , (e.g., images/) will not be altered.
      
