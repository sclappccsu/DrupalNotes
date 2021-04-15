# Updating Drupal - D8+ - using Composer

{% embed url="https://www.drupal.org/docs/develop/using-composer/starting-a-site-using-drupal-composer-project-templates" %}

Check for available Drupal core and module updates \(also, see zsh note below\):

```text
composer outdated 'drupal/*'
```

All of your modules and themes can be updated along with Drupal core via:

```text
composer update
```

To update only Drupal core without any modules or themes, use:

```text
composer update drupal/core-recommended --with-dependencies
```

To update Drupal core and all dependencies, use:

```text
composer update drupal/core 'drupal/core-*' --with-all-dependencies
```

Note: zsh handles [asterisks](https://www.jeffgeerling.com/comment/7897#comment-7897) [differently](https://github.com/ohmyzsh/ohmyzsh/issues?q=is%3Aissue+%22no+matches+found%22+asterisk), so asterisk package wildcards need to be quoted.

