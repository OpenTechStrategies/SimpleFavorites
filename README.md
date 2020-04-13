The '''SimpleFavorites''' extension makes it easy for users to add pages to their personal favorites list with just one click, so they can browse through them again later or share their favorites with others. It creates a new special page that contains a list of SimpleFavorites for each user, similar to the Watchlist. It also allows for the list of favorites to be publicly embedded on a page using a tag.

This extension was forked from
[the main mediawiki extension](https://www.mediawiki.org/wiki/Extension:SimpleFavorites)
and then updated to be more streamlined.  Those include, but aren't limited to:

* Changing some looking and feel
* Removing a lot of the uneeded functionality, especially in the Special page
* Updating how the extension is loaded
* Removing some of the configuration because it's unneeded
* Removing the parser tag

# Usage

Users add items to the SimpleFavorite list by by clicking the Heart icon.  Conversely, removing a SimpleFavorite from the list is a matter of clicking the heart a second time.

## Special Page

This extension also creates a new Special page called "Special:SimpleFavoritelist". This special page allows users to view their list of favorites. .

# Installation

* Download and place the file(s) in a directory called SimpleFavorites in your extensions/ folder.
* Add the following code at the bottom of your LocalSettings.php:

```
wfLoadExtension('SimpleFavorites');
```

* Run the update script which will automatically create the necessary database tables that this extension needs.
* Navigate to Special:Version on your wiki to verify that the extension is successfully installed.

Installation can be verified through Special:Version

# Uninstalling
Most extensions can be removed by deleting them and editing LocalSettings.php to remove references to it. Since this extension makes changes to your database, removing it additionally requires undoing database changes. It's as simple as removing the favoritelist table from the database.

If you have access to your database using a tool like PHPMyAdmin, you can just delete the table. For commandline access or to use a script, you would use this command:

```sql
drop table simplefavoritelist;
```
