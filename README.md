# Loopback-style REST Client for react-admin

Loopback-style REST Client for [react-admin](https://github.com/marmelab/react-admin), the frontend framework for building admin applications on top of REST services.

## Prerequisite

* Your loopback server must response `X-Total-Count` header when querying list. Please use [loopback3-xTotalCount](https://github.com/kimkha/loopback3-xTotalCount) on your server end.

## How to use

1. `yarn add ra-loopback`
2. On your `App.js`, add this:

```
import loopbackApiClient from 'ra-loopback';

...

    <Admin restClient={loopbackApiClient('http://my.api.url/api')} ...>
```

3. If you want this module handle authentication, add this:

```
import loopbackApiClient, {authClient} from 'ra-loopback';

...

    <Admin restClient={loopbackApiClient('http://my.api.url/api')} authClient={authClient('http://my.api.url/api/users/login')} ...>
```

## License

This module is licensed under the [MIT Licence](LICENSE).
