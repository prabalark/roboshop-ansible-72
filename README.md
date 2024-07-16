# location /api/catalogue/ { proxy_pass http://localhost:8080/; }
# location /api/user/ { proxy_pass http://localhost:8080/; } # user.devops72bat.online
# location /api/cart/ { proxy_pass http://localhost:8080/; } # cart.devops72bat.online
# location /api/shipping/ { proxy_pass http://localhost:8080/; } #shipping.devops72bat.online
# location /api/payment/ { proxy_pass http://localhost:8080/; } # payment.devops72bat.online

#location /api/catalogue/ { proxy_pass {{ lookup('aws_ssm','dev.frontend.catalogue_url',region='us-east-1') }}; }