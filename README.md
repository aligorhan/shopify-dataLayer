# Analytics ve Tag Manager İçin Shopify dataLayer Eklenmesi

### URL'ler
- [Analytics E-Ticaret Ölçme](https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?client_type=gtm#product_list_and_promotion_actions)
- [dataLayer Açıklaması](https://developers.google.com/tag-platform/devguides/datalayer?hl=en)


1) **theme.liquid** sayfasına </head> kapanışının hemen üzerine eklenecek. --> ```{% include 'dataLayer-allPages' %}```
2) ```{% include 'dataLayer-allPages' %}```'in hemen alt tarafına GTM kodu eklenecek.
3) ```<body>``` etiketinin altına GTM'nin 2. kodu eklenecek.

### Tag Manager

| İzlenebilecek Etkinlikler |
| --------|
|*view_item*|
|*view_item_list*|
|*add_to_cart*|
|*view_cart*|
|*begin_checkout*|
|*shipping_method*|
|*payment_method*|
|*purchase*|
|*search*|
|*first_time_visitor*|
|*blog*|
|*logState*|
|*homepage*|
|*404*|

### Kurulum:
1) **theme.liquid** sayfasına </head> kapanışının hemen üzerine bu kod eklenecek.
```{% include 'dataLayer-allPages' %}```

2) Bu kodun hemen altına Tag Manager'dan aldığınız GTM kodunuz eklenecek.
3) Snippets (Parçacıklar) kısmına [dataLayer-allPages](https://github.com/aligorhan/shopify-dataLayer/blob/main/dataLayer-allPages) eklenecek ve ismi, **dataLayer-allPages** (Büyük - küçük harf önemli) yapılacak.

4) Optional
Sepete ürün eklendiğinde sayfa yenilenmiyorsa kodun içindeki "dynamicCart: true" bölümü true olarak ayarlanmalı.
