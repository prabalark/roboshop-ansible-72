# location /api/catalogue/ { proxy_pass http://localhost:8080/; } #catalogue.{{env}}ops72bat.online
# location /api/user/ { proxy_pass http://localhost:8080/; } # user.{{env}}ops72bat.online
# location /api/cart/ { proxy_pass http://localhost:8080/; } # cart.{{env}}ops72bat.online
# location /api/shipping/ { proxy_pass http://localhost:8080/; } #shipping.{{env}}ops72bat.online
# location /api/payment/ { proxy_pass http://localhost:8080/; } # payment.{{env}}ops72bat.online

#location /api/catalogue/ { proxy_pass {{ lookup('aws_ssm','{{env}}.frontend.catalogue_url',region='us-east-1') }}; }
#location /api/user/ { proxy_pass {{ lookup('aws_ssm','{{env}}.frontend.user_url',region='us-east-1') }}; }
#location /api/cart/ { proxy_pass {{ lookup('aws_ssm','{{env}}.frontend.cart_url',region='us-east-1') }}; }
#location /api/shipping/ { proxy_pass {{ lookup('aws_ssm','{{env}}.frontend.shipping_url',region='us-east-1') }}; }
#location /api/payment/ { proxy_pass {{ lookup('aws_ssm','{{env}}.frontend.payment_url',region='us-east-1') }}; }

#{ name= "{{env}}.frontend.catalogue_url" , value= "http://catalogue.{{env}}ops72bat.online:8080/" },
#{ name= "{{env}}.frontend.cart_url" , value= "http://cart.{{env}}ops72bat.online:8080/" },
#{ name= "{{env}}.frontend.user_url" , value= "http://user.{{env}}ops72bat.online:8080/" },
#{ name= "{{env}}.frontend.shipping_url" , value= "http://shipping.{{env}}ops72bat.online:8080/" },
#{ name= "{{env}}.frontend.payment_url" , value= "http://payment.{{env}}ops72bat.online:8080/" },

#catalogue
#location /api/catalogue/ { proxy_pass {{ lookup('aws_ssm','{{env}}.frontend.catalogue_url',region='us-east-1') }}; }
#{ name= "{{env}}.frontend.catalogue_url" , value= "http://catalogue.{{env}}ops72bat.online:8080/" },

#{ name= "{{env}}.frontend.catalogue_mongoendpoint" , value= "mongodb.{{env}}ops72bat.online" },
#{ name= "{{env}}.frontend.catalogue_montru" , value= "MONGO=true" },
#{ name= "{{env}}.frontend.catalogue_monurl" , value= "mongodb://mongodb.{{env}}ops72bat.online:27017/catalogue" }

#user
#{ name= "{{env}}.frontend.user_REDIS_HOST" , value= "redis.{{env}}ops72bat.online" },
#{ name= "{{env}}.frontend.user_montru" , value= "MONGO=true" },
#{ name= "{{env}}.frontend.user_monurl" , value= "mongodb://mongodb.{{env}}ops72bat.online:27017/users" }

#cart
#{ name= "{{env}}.frontend.cart_REDIS_HOST" , value= "redis.{{env}}ops72bat.online" },
#{ name= "{{env}}.frontend.cart_CATALOGUE_HOST" , value= "catalogue.{{env}}ops72bat.online" },
#{ name= "{{env}}.frontend.cart_CATALOGUE_PORT" , value= "8080" }
