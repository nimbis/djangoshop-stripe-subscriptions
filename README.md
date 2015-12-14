# Stripe Payment Provider Integration for django-shop

This integrates Stripe for django-shop version 0.3 and above.


## Installation

In ``settings.py`` of your project

Add ``'shop_stripe'`` to ``INSTALLED_APPS``.

At https:://stripe.com/ create an account and apply for a public/private key-pair. Then add these
keys:

```
SHOP_STRIPE = {
    'PUBKEY': 'pk_<public-key-as-delivered-by-Stripe>',
    'APIKEY': 'sk_<api-key-as-delivered-by-Stripe>',
    'PURCHASE_DESCRIPTION': _("Thanks for purchasing at MyShop"),
}
```

Add ``'shop_stripe.modifiers.StripePaymentModifier'`` to ``SHOP_CART_MODIFIERS``.

Add ``'shop_stripe.payment.OrderWorkflowMixin'`` to ``SHOP_ORDER_WORKFLOWS``.
