# TheBooking language files
Welcome to the official repository for TheBooking's language files.

## How to contribute

1. Fork the repository.
2. Clone your fork locally:

   `git clone https://github.com/[YourUsername]/thebooking-languages.git`

3. Navigate to the appropriate folder or file for the language you want to contribute to or edit.
4. Edit the .po or .mo file using a tool like Poedit or any text editor you prefer.
5. Commit and Push your changes:

    ```
    git add .
    git commit -m "Updated [LanguageName] translation"
    git push origin main
    ```
    
6. Navigate back to your forked repo on GitHub and click the "New pull request" button. Fill out the pull request template, and then submit it. We will review your changes and merge them if everything looks good.

### Generate json files (optional)

TheBooking is not just a PHP plugin: a portion of it is built using JavaScript. Due to WordPress's internationalization standards, certain strings in the JavaScript realm require JSON translation files. Here's how you can generate those JSON files:

Prerequisites:
- Node environment: ensure you have Node.js installed.
- npx: this should come pre-installed with Node.js. If not, you can install it using `npm install -g npx`.
- po2json: this is a necessary package. Install it with `npm install -g po2json`.

For every .po file that you've edited or added, execute the following commands (this example uses team-booking-en_US.po):

   ```
   npx po2json ./languages/team-booking-en_US.po ./languages/team-booking-en_US-tbk-scripts.json -d team-booking -f jed1.x
   npx po2json ./languages/team-booking-en_US.po ./languages/team-booking-en_US-tbk-backend-scripts.json -d team-booking -f jed1.x
   ```

## Guidelines
- Ensure your translations are clear and contextually correct.
- Avoid using machine translation tools like Google Translate. We value human-made translations as they tend to be more accurate and context-aware.
- Maintain the integrity and meaning of the original English phrases.

## Issues
If you find any issues with existing translations or want to discuss nuances related to a particular language, please open an issue.

## License
All translations are licensed under GNU General Public License v3.0. Please see the LICENSE file for more details.
