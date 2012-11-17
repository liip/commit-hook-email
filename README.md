# Commit Email Hook

This PHP script is a web hook and sends your commits including
the diff to a configured email address. It works with GitLab and GitHub.

## Installation

```
curl -s https://getcomposer.org/installer | php
php composer.phar install
cp config.php.sample config.php
```

## Configuration

### GitLab

- Configure your GitLab token, the email address and a random
  secret in `config.php`
- Now add your URL in your GitLab project in Hooks
  (e.q. http://example.org/gitlab.php?secret=YOUR_RANDOM_SECRET)

### GitHub

- Create a GitHub OAuth token with the following command:
```
curl -u YOUR_GITHUB_USERNAME -d '{"scopes":["repo"],"note":"Commit Emails"}' https://api.github.com/authorizations
```
- Configure the GitHub OAuth token, the email address and a random secret
  in `config.php`
- Now add your URL in your GitHub project admin in Service Hooks as a WebHook (e.q. http://example.org/github.php?secret=YOUR_RANDOM_SECRET)
