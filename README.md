# node-connect-datadog-graphql

Datadog middleware for Connect JS / Express with support for GraphQL operations.


## Usage

Add middleware immediately before your router.

	app.use(require("connect-datadog-graphql")({}));
	app.use(app.router);

## Options

All options are optional.

* `dogstatsd` hot-shots client. `default = new require("hot-shots").StatsD()`
* `stat` *string* name for the stat. `default = "node.express.router"`
* `tags` *array* of tags to be added to the histogram. `default = []`
* `path` *boolean* include path tag. `default = false`
* `base_url` *boolean* include baseUrl. `default = false`
* `method` *boolean* include http method tag. `default = false`
* `protocol` *boolean* include protocol tag. `default = false`
* `response_code` *boolean* include http response codes. `default = false`
* `delim` *string* char to replace pipe char with in the route `default = '-'`
* `graphql_paths` *array* of path strings where we should check for graphql requests
* `extra_attributes` *array* arbitrary extra tags to include

## License

View the [LICENSE](https://github.com/politics-rewired/node-connect-datadog-graphql/blob/master/LICENSE) file.

