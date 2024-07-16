# location /api/catalogue/ { {{ lookup('aws_ssm','dev.frontend.catalogue_url',region='us-east-1') }}; }
# location /api/user/ { {{ lookup('aws_ssm','dev.frontend.user_url',region='us-east-1') }}; }
# location /api/cart/ { {{ lookup('aws_ssm','dev.frontend.cart_url',region='us-east-1') }}; }
# location /api/shipping/ { {{ lookup('aws_ssm','dev.frontend.shipping_url',region='us-east-1') }}; }
# location /api/payment/ { {{ lookup('aws_ssm','dev.frontend.payment_url',region='us-east-1') }}; }