## Dark Theme for ownCloud

### Use the theme-dark App

To use the `theme-dark` app, clone or [download](https://github.com/dtrunk90/theme-dark/archive/refs/heads/master.zip) this repository to the `owncloud/apps` folder on your server. Please note that the Apache user needs access rights to the folder and its content. As an example, use the following command to adjust the permissions: `chown -R www-data:www-data theme-example`.

When you _download_ this repository the extracted folder name will be `owncloud-theme-dark-master`. You must change the folder name to `theme-dark` to get the theme working out of the box.

If you change the name of the app (the folder name) from `theme-dark` to another name, be sure to change the `<id>` in the file `appinfo/info.xml` as well. The folder name and the `<id>` must be identical.

### Edit images
To edit images it is best to open the original images from the `core\img` folder with Gimp or Photoshop. After you have made changes, overwrite the originals.

Please note that the browser stores images in the cache, so this should always be deleted after changes. (https://en.wikipedia.org/wiki/Wikipedia:Bypass_your_cache)

### Change design values
In the file `core/css/styles.css` you will find the adjustments. You can change everything you want there. More classes and their values can be found easily with the browser console (F12 key). There you can also test directly in the browser how the change of values will be reflected. If it fits you can transfer the values to `styles.css`.

### Integrity check

Since files in the theme must be changeable, it has not been signed. Therefore an `integrity check warning` appears in your ownCloud instance. You can deactivate it for the `theme-dark` app by adding following config parameter to `config/config.php`. You can find the config directory in the root folder of your instance.

```
'integrity.ignore.missing.app.signature' => [
      'theme-dark',
 ],
```
