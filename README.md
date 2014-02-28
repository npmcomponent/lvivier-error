*This repository is a mirror of the [component](http://component.io) module [lvivier/error](http://github.com/lvivier/error). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/lvivier-error`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# error

Error constructor factory.

Constructors returned have all the bells and whistles:

```js
var NotFoundError = error('NotFoundError', {status:404})
var err = new NotFoundError('ohnoes')

err
//-> NotFoundError {}
err instanceof NotFoundError
//-> true
err instanceof Error
//-> true
'NotFoundError' === err.name
//-> true
```

## Install

With [component][1] or [npm][2]:

```
$ component install lvivier/error

$ npm install git://github.com/lvivier/error.git
```

### Add to package.json

As of [npm 1.1.65][3]:

```
{"error": "lvivier/error"}
```

## Usage

### error(name, [parent], [opts])

- returns a Function
- **parent** is the prototype, or `Error` if omitted
- **opts** is an object whose members will become properties of the error instance
- **opts.stack** if set to `false`, errors won't have stack traces


[1]:http://github.com/component/component
[2]:http://npmjs.org/
[3]:https://npmjs.org/doc/json.html#GitHub-URLs