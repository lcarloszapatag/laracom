[![Build Status](https://travis-ci.org/Laracommerce/laracom.svg?branch=master)](https://travis-ci.org/Laracommerce/laracom)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/Laracommerce/laracom/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/Laracommerce/laracom/?branch=master)
[![Code Intelligence Status](https://scrutinizer-ci.com/g/Laracommerce/laracom/badges/code-intelligence.svg?b=master)](https://scrutinizer-ci.com/code-intelligence)
[![Test Coverage](https://img.shields.io/codecov/c/github/Laracommerce/laracom/master.svg)](https://codecov.io/github/Laracommerce/laracom?branch=master)
[![Fork Status](https://img.shields.io/github/forks/Laracommerce/laracom.svg)](https://github.com/Laracommerce/laracom)
[![Star Status](https://img.shields.io/github/stars/Laracommerce/laracom.svg)](https://github.com/Laracommerce/laracom)
[![Gitter chat](https://badges.gitter.im/gitterHQ/gitter.png)](https://gitter.im/larac0m/Lobby)

# Laravel FREE E-Commerce Software

- See full [documentation](https://shop.laracom.net/docs)

# Author

[Jeff Simons Decena](https://jsdecena.me)

Requirements

    PHP 7.1 or higher
    Laravel 5.6 or higher
    Composer




Configuracion

Composer update
php artisan migrate --seed
npm install && npm run dev
php artisan storage:link
php artisan serve

Other settings
By default, Paypal (Express Checkout) is the default payment gateway. You must configure the credentials in the payment methods admin:
PP_ACCOUNT_ID=xxxxx-facilitator@email.com
PP_CLIENT_ID=xxxxxx
PP_CLIENT_SECRET=xxxx
PP_API_URL=https://api.sandbox.paypal.com
PP_REDIRECT_URL=http://localhost/execute
PP_CANCEL_URL=http://localhost/cancel
PP_FAILED_URL=http://localhost/failed
PP_MODE=sandbox

You can enable / disable the payment gateways via the .env.
PAYMENT_METHODS=paypal,stripe,bank-transfer

Stripe
STRIPE_KEY=xxxx
STRIPE_SECRET=xxxx
STRIPE_REDIRECT_URL=http://localhost/execute?stripe
STRIPE_CANCEL_URL=http://localhost/cancel?stripe
STRIPE_FAILED_URL=http://localhost/failed?stripe

Bank Transfer
BANK_TRANSFER_NAME=xxxx
BANK_TRANSFER_ACCOUNT_TYPE=xxxx
BANK_TRANSFER_ACCOUNT_NAME=xxxx
BANK_TRANSFER_ACCOUNT_NUMBER=xxx
BANK_TRANSFER_SWIFT_CODE=xxx
BANK_TRANSFER_SWIFT_NOTE=xxx

Shop settings
SHOP_NAME=
SHOP_COUNTRY_ISO=
SHOP_COUNTRY_ID=
# options - gms, kgs, oz, lbs
SHOP_WEIGHT=lbs
SHOP_EMAIL=your@email.com
SHIPPING_COST=0
TAX_RATE=10
DEFAULT_CURRENCY=USD

You can activate SHIPPO shipping if you need it else set 0 to deactivate
ACTIVATE_SHIPPING=0
SHIPPING_API_TOKEN=shippo_test_xxxxxx

MailChimp Newsletter settings should be set in .env
MAILCHIMP_API_KEY=
MAILCHIMP_LIST_ID=

Set your mail server in the .env
MAIL_DRIVER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=
MAIL_PASSWORD=



Admin dashboard
In order to enter the administration dashboard, you have to hit the /admin route. E.g enter http://localhost/admin or in general http://your-domain/admin in your browser.
If you're not already logged in, you are redirected to the admin login screen. There you can use one of the following credentials to access the admin dashboard.
Email and Passwords
john@doe.com / secret (role:superadmin)
admin@doe.com / secret (role:admin)
clerk@doe.com / secret (role:user)

