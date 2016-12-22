---
layout: docs
permalink: /docs/
links: [
  { title: 'Overview', id: 'overview' },
  { title: 'Prerequisits', id: 'prerequisits' },
  { title: 'Installation', id: 'installation' },
  { title: 'Folder Structure', id: 'folders' },
  { title: 'API Controllers', id: 'controllers' },
  { title: 'API Models', id: 'models' },
  { title: 'API Routing', id: 'routing' },
  { title: 'Config', id: 'config' },
  { title: 'Troubleshooting', id: 'troubleshooting' },
  { title: 'CLI', id: 'cli' },
  { title: 'Angular CLI', id: 'ngcli' },
  { title: 'More Information', id: 'moreinfo' },
  { title: 'Credits', id: 'credits' },
  { title: 'License', id: 'license' },
]
---

<h1 id="overview">Overview</h1>

<p>These docs will cover the basics of using the CLI and developing your app.</p>

<p>Before you begin, we recommend you read about the basic building blocks that make up a MEAN2 application:</p>

<p class="strong">MongoDB</p>

<p>The <a href="http://mongodb.org/manual/" target="_blank">MongoDB Official Manual</a> is a great place to get you started in understanding NoSQL and MongoDB</p>

<p class="strong">Express</p>

<p>The <a href="http://expressjs.com/" target="_blank">Express</a> website is the best place to learn about the API application framework that powers MEAN2.</p>

<p class="strong">Angular 2</p>

<p>The AngularJS team have tirelessly created documentation for the latest iteration of their framework that can be found on <a href="https://angular.io/" target="_blank">their website</a>. If books are more your thing, <a href="https://ng-book.com/2/" target="_blank">ng-book 2</a> is currently the most in-depth, complete and up-to-date book on Angular 2 currently on the market.</p>

<p class="strong">Node.js</p>

<p>The <a href="https://nodejs.org/en/" target="_blank">NodeJS</a> webiste contains enough information and resources to get you up and running with Node in no time.</p>

<p class="strong">Angular CLI</p>

<p>** add content **</p>

<p class="strong">TypeScript</p>

<p>** add content **</p>

<h1 id="prerequisits">Prerequisits</h1>

<p>** add content **</p>

<h1 id="installation">Installation</h1>

<p>** add content **</p>

<h1 id="folders">Folder Structure</h1>

{% highlight shell %}
# API assets
api/
  controllers/
  models/
  services/

# server configuration
config/
  bootstrap.js
  routes.js
  server.js

# end to end tests
e2e/
  app.e2e-spec.ts
  app.po.ts
  tsconfig.json

# where most of your client side work will be
src/

  # public assets
  assets/

  # client configuration
  environments/
    environment.prod.ts
    environment.ts

  # main client side files
  favicon.ico
  index.html
  main.ts
  polyfills.ts
  styles.sass
  test.ts
  tsconfig.json
  typings.d.ts
  .editorconfig
  .gitignore
  angular-cli.json
  karma.conf.js
  package.json
  protractor.conf.js
  tslint.json

  # server entry point
  server.js
{% endhighlight %}

<h1 id="controllers">API Controllers</h1>
<p>** add content **</p>

{% highlight javascript %}
let UserController = {
  index: (req, res) => {
    User
      .findOne(reqparam('id'))
      .then(user => req.json(user))
      .catch(err => req.status(500).json(err));
  }
}
{% endhighlight %}

<h1 id="models">API Models</h1>

<p>** add content **</p>

{% highlight javascript %}
var UserSchema = mongoose.Schema({
  email: {
    type: String,
    required: true
  },

  password: {
    type: String,
    required: true
  },

  createdOn: {
    type: Date,
    default: Date.now
  },

  modifiedOn: {
    type: Date,
    default: Date.now
  }
});

UserSchema.pre('save', next => {
  this.modifiedOn = Date.now();
  next();
});

module.exports = mongoose.model('User', UserSchema);
{% endhighlight %}

<h1 id="routing">API Routing</h1>

<p>** add content **</p>

{% highlight javascript %}
router.get('/user/:id', UserController.index);
{% endhighlight %}

<h1 id="config">Config</h1>

<p>** add content **</p>

<h1 id="cli">CLI</h1>

<p>** add content **</p>

<h2>New Project</h2>

{% highlight shell %}
$ mean2 new <project>
{% endhighlight %}

<p>Creates a new Mean 2 project.</p>

<h2>End to End Tests</h2>

{% highlight shell %}
$ mean2 e2e
{% endhighlight %}

<p>Runs all end-to-end tests defined in your application, using protractor.</p>

<h2>Unit Tests</h2>

{% highlight shell %}
$ mean2 test
{% endhighlight %}

<p>Run unittests, using karma.</p>

<h2>Generate</h2>

{% highlight shell %}
$ mean2 generate <type> <name>
{% endhighlight %}

{% highlight shell %}
$ mean2 g <type> <name>
{% endhighlight %}

<p>Generate new code inside your project.</p>

{% highlight shell %}
# generates a component.
$ mean2 generate component <path/to/component>

# generates a directive.
$ mean2 generate directive <path/to/directive>

# generates a route. The name should be the route used 
# in the RouteConfig.
$ mean2 generate route <route/to/route>

# generates a pipe.
$ mean2 generate pipe <path/to/pipe>

# generates a service.
$ mean2 generate service <path/to/service>

# generates an API controller & model.
$ mean2 generate api <api/name>

# generates just the API controller.
$ mean2 generate api controller <controller/name>

# generates just the API model.
$ mean2 generate api model <model/name>
{% endhighlight %}

<h2>Serve</h2>

{% highlight shell %}
$ mean2 serve
{% endhighlight %}

<p>Run Angular 2 application with development server.</p>

<h1 id="ngcli">Angular CLI</h1>

<p>** add content **</p>

<h1 id="troubleshooting">Troubleshooting</h1>

<p>** add content **</p>

<h1 id="moreinfo">More Information</h1>

<p>** add content **</p>

<h1 id="credits">Credits</h1>

<p>Special mentions to go:</p>

<ul>
  <li><a href="https://twitter.com/hashtagserg" taget="_blank">Sergio Cruz</a></li>
</ul>

<h1 id="license">License</h1>

<a href="http://opensource.org/licenses/MIT" target="_blank">Licensed under MIT. Documentation licensed under CC BY 3.0</a>
