[![Build Status](https://travis-ci.org/bravocart/api.svg?branch=master)](https://travis-ci.org/bravocart/api)
#api.bravocart

[![Join the chat at https://gitter.im/bravocart/bravocart-api](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/bravocart/bravocart-api?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

The [Bravocart](http://bravocart.io/) organisation helps you to build beautiful mobile shops. We have published this open-source module to get started with a backend for any Bravocart app. You can use the backend together with an [app.bravocart](https://github.com/bravocart/app) project, specifically an Angular.js/Ionic app. Or feel free to make use of this Node.js/Express app for any other purpose you have in mind. This software is licensed under [MIT](http://opensource.org/licenses/MIT), so the sky's the limit.

## When use api.bravocart

If you've already decided for a shop platform, such as [Magento](http://magento.com), [Shopify](http://shopify.com), [PrestaShop](http://prestashop.com), [OpenCart](http://opencart.com), [osCommerce](http://oscommerce.com), - you name it - keep on reading. Bravocart is complementary to your existing eCommerce installation. Bravocart will be the racer in your car pool.

![racer](http://assets.bravocart.io/racer.gif)

Bravocart brings along these components:

 * An ultra fast Node.js/Express JSON-API
 * A flexbile, change-responsive MongoDB layer
 * A payment bridge, with Paypal pre-installed
 * An application structure to [rapidly pivot to success](https://www.youtube.com/watch?v=1RTcXwJuCaU)
 * Connectors to favorite shopping cart systems

## When not use api.bravocart

As mentioned before, Bravocart is not a full-stack eCommerce platform with those crucial features, such inventory management, accounting, invoicing, smart pricing, gift card management. No, Bravocart is complementary to existing eCommerce platforms. Bravocart helps you to bring your data to an ultra-fast Node.js/Express JSON-backend, so that you can experiment with new app ideas.

## Getting started


### Deploy on Heroku

Probably nothing is easier than deploying api.bravocart on Heroku:

```
heroku create
git push heroku master
heroku open
```

### Deploy with Vagrant on AWS EC2

This repository comes with a handy [Vagrantfile](https://www.vagrantup.com/) that helps you to deploy Bravocart in a super professionel production environment in the Amazon cloud. Make sure you have [installed Vagrant](http://www.vagrantup.com/downloads), and set environment settings for the [Vagrant AWS Provider](https://github.com/mitchellh/vagrant-aws#configuration) before following these steps from your project's root directory:

```
./bin/aws up
```

If you have done any changes on the code and want to commit your changes to the EC2 machine, run the following command:

```
./bin/aws push
```

The upper command will sync your project folder with the running EC2 instance and finally do a ```npm install```, so that all your packages are up to date. Be careful when running in production, because your EC2 machine will shutdown for the installation.

## FAQ

### Is Bravocart really for free?

Yes, Bravocart is absolutely free. Any modules from the Bravocart core team, published at this [Github endpoint](https://github.com/bravocart/) are licensed under MIT. However, if you're in a hurry and want to quickly get started with your mCommerce project, you can sign up for an account at [bravocart.io/signup](http://bravocart.io/signup/), offering you free and paid plans.

### Why MongoDB? It does not support ACID transactions!

MongoDB supports ACID transactions only [in a limited sense](https://www.mongodb.com/faq#acid-transactions/). So if you're now scared that your purchases [may never reach your database](http://stackoverflow.com/questions/7149890/what-does-mongodb-not-being-acid-compliant-really-mean) at times, then you should familiarise with Bravocart's [data structure](api/). Each document reflects a single transaction. So there is no need for complex transactions and thus **no reason to worry** using MongoDB.

### Which connectors to shopping cart systems are available?

Currently only Magento is supported. More adapters will follow. You are more than welcome to contribute.

### How can I contribute to Bravocart?

If you have a feautre idea, an extension for the payment bridge or a connector to a shopping cart system you can submit [a pull request](https://github.com/bravocart/api/pulls). Feel free to reach the community on Gitter [#bravocart/api](https://gitter.im/bravocart/api) before you start coding.

## Community

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/bravocart/api?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

## Further Reading

  * [API Documentation](https://api.com)
  * [Changelog](https://github.com/bravocart/api/wiki/Changelog)
  * [Release Notes](https://github.com/bravocart/api/releases)
  * [Roadmap](https://github.com/bravocart/api/wiki/Roadmap)
  * [More Resources](https://github.com/bravocart/api/wiki/Resources)
