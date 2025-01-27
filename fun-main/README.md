# fun

/* README.md */
# Project README

## Preprocessor
This project uses SCSS (Sassy CSS) for styling. SCSS was chosen because it offers CSS-like syntax and advanced features, making the code more maintainable and reusable.

## Design Choices
- **Colors**: Blue was selected as the primary color to give the website a clean, professional look.
- **Fonts**: Arial was chosen for readability and simplicity.
- **Layout**: A simple multi-page website structure with a header and navigation menu for easy access to different pages.

## SCSS Features
1. **Variables**:
   - Reused for consistent colors, fonts, and spacing values.
   ```scss
   $primary-color: #3498db;
   $font-family: 'Arial, sans-serif';
   $spacing: 16px;
   ```

2. **Mixins**:
   - Created reusable mixins for buttons.
   ```scss
   @mixin button($bg-color, $text-color) {
       background-color: $bg-color;
       color: $text-color;
       padding: $spacing;
       border: none;
       border-radius: 5px;
       cursor: pointer;
   }
   ```

3. **Nesting**:
   - Used for better readability and logical grouping of styles.
   ```scss
   header {
       nav {
           display: flex;
           a {
               color: white;
               &:hover {
                   text-decoration: underline;
               }
           }
       }
   }
   ```

4. **Partials**:
   - Styles were split into separate SCSS files (`_variables.scss`, `_mixins.scss`, `_base.scss`) for modularity and maintainability.

## Compilation
The SCSS files were compiled into a single `styles.css` file using the following command:
```bash
sass main.scss styles.css
```
