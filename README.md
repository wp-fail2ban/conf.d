# wp-fail2ban/conf.d
A collection of standard configurations for *WP fail2ban*.

## Usage

First, copy the configuration file to your `wp-content` directory. Be sure to name it `wp-fail2ban-config.php`.

```ShellSession
[invisnet@test wp-content]$ ls -p
db.php          languages/      themes/          uploads/
index.php       plugins/        upgrade/
[invisnet@test wp-content]$ cp plugins/wp-fail2ban/conf.d/default-all.php wp-fail2ban-config.php
[invisnet@test wp-content]$ ls -p
db.php          plugins/        uploads/
index.php       themes/         wp-fail2ban-config.php
languages/      upgrade/
[invisnet@test wp-content]$
```

Next, edit your `wp-config.php` file and add the following line:

```PHP
include __DIR__.'/wp-content/wp-fail2ban-config.php';
```

Be sure to add it **before** the line that says:

```PHP
/* That's all, stop editing! Happy blogging. */
```

Finally, if there are any changes you want to make, edit `wp-fail2ban-config.php`.

----

**default-all.php**:
  * Default logs
  * All features enabled
