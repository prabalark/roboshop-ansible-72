# location /api/catalogue/ { proxy_pass http://localhost:8080/; }
# location /api/user/ { proxy_pass http://localhost:8080/; } # user.devops72bat.online
# location /api/cart/ { proxy_pass http://localhost:8080/; } # cart.devops72bat.online
# location /api/shipping/ { proxy_pass http://localhost:8080/; } #shipping.devops72bat.online
# location /api/payment/ { proxy_pass http://localhost:8080/; } # payment.devops72bat.online

# location /api/catalogue/ { {{ lookup('aws_ssm','dev.frontend.catalogue_url',region='us-east-1') }}; }
# location /api/user/ { {{ lookup('aws_ssm','dev.frontend.user_url',region='us-east-1') }}; }
# location /api/cart/ { {{ lookup('aws_ssm','dev.frontend.cart_url',region='us-east-1') }}; }
# location /api/shipping/ { {{ lookup('aws_ssm','dev.frontend.shipping_url',region='us-east-1') }}; }
# location /api/payment/ { {{ lookup('aws_ssm','dev.frontend.payment_url',region='us-east-1') }}; }