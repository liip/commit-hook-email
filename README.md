# GitLab Commit Email Hook

This PHP script is a GitLab hook and sends your commits including
the diff to a configured email address.

## Installation

```
curl -s https://getcomposer.org/installer | php
php composer.phar install
cp config.php.sample config.php
```

## Configuration

- Configure your GitLab token, the email address and a random
  secret in `config.php`
- Now add your URL in your GitLab project in Hooks
  (e.q. http://example.org/hook.php?secret=ABC)
