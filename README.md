# TYPO3 Backend Module 'slug'
Official Repository of the 'slug' Backend Module for TYPO3 9.5

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/typo3freelancer/5)

The Slug backend module is designed to help manage large amounts of slugs for pages and extension records. Currently, it provides a simple list for pages and news records, which can be filtered with different parameters. Slugs can be edited and saved quickly and efficiently. The News module already includes the functionality to regenerate or save all slugs of the current list view with just one click. I have tested the functionality with 500 empty news records so far, without any problem.

## Important Note

Please use the latest version from the official TYPO3 repository (https://extensions.typo3.org/extension/slug/), if you want to make sure that nothing happens to your website. In any case I highly recommend a database backup as long as the extension is in BETA mode. If you use the current version from github, you use it at your own risk!

## 1. Features

- Quickly edit, save and regenerate slugs for pages and news records
- Mass generation and storage of news slugs (up to 500 at once)
- List views filterable with different parameters
- Search engine entry Preview for pages, displays the updated slug as you type
- Uses TYPO3 core slug generation functions
- Extension configuration for default values like sorting, entries per page etc.

## 2. Usage

### Installation

- Download the latest version here: https://extensions.typo3.org/extension/slug/ or install it with the extension manager of your TYPO3 installation
- No further configuration is required, but you should delete all the backend caches after installation to make sure the extension is working properly.

## 3. Known problems

### Slug generation for News records failed?

- If a news record has no pid set in the database, the slug generation will fail. This may happen when you have imported news records from a third party extension or manually. Solution: Check, if all entries in the table 'tx_news_domain_model_news' have the field 'pid' set to a page or folder in the page tree.

### Error, when 'Unassigned site configurations' have been found

- The error "Argument 2 passed to TYPO3\CMS\Core\Imaging\IconFactory::getIconForRecord() must be of the type array, null given..." can be a result of "Unassigned site configurations"

## 4. Want to report an issue?

- https://github.com/koehlersimon/slug/issues