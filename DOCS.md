Use the rancher plugin to upgrade a service in [rancher](http://rancher.com).

The following parameters are used to configure this plugin:

- `url` - url to your rancher server, including protocol and port
- `access_key` - rancher api access key
- `secret_key` - rancher api secret key
- `service` - ID of rancher service to act on
- `docker_image` - new image to assign to service, including tag (`drone/drone:latest`)
- `start_first` - start the new container before stopping the old one, defaults to `true`
- `confirm` - auto confirm the service upgrade if successful, defaults to `false`
- `timeout` - the maximum wait time in seconds for the service to upgrade, default to `30`

The following is a sample Rancher configuration in your `.drone.yml` file:

```yaml
deploy:
  rancher:
    url: https://example.rancher.com
    access_key: 1234567abcdefg
    secret_key: abcdefg1234567
    service: 1s20
    docker_image: drone/drone:latest
```
