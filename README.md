# OmniAuth Dribbble

This is an OmniAuth strategy for authenticating with Dribbble. To
use it, you'll need to register for an OAuth2 Client ID and Secret
on your [Dirbbble Applications Page](https://dribbble.com/account/applications).

**Important:** this library requires [Dribbble API v2](http://developer.dribbble.com/v2).

## Basic Usage

    use OmniAuth::Builder do
      provider :dribbble, ENV['DRIBBLE_CLIENT_KEY'], ENV['DRIBBBLE_CLIENT_SECRET']
    end

## Scopes

Dribbble API v2 lets you set scopes to provide granular access. `public` is the default scope:

    use OmniAuth::Builder do
      provider :dribbble, ENV['DRIBBLE_CLIENT_KEY'], ENV['DRIBBBLE_CLIENT_SECRET'], scope: 'public'
    end

More info on [Scopes](http://developer.dribbble.com/v2/oauth/#scopes).
