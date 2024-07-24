# location /api/catalogue/ { proxy_pass http://localhost:8080/; } #catalogue.devops72bat.online
# location /api/user/ { proxy_pass http://localhost:8080/; } # user.devops72bat.online
# location /api/cart/ { proxy_pass http://localhost:8080/; } # cart.devops72bat.online
# location /api/shipping/ { proxy_pass http://localhost:8080/; } #shipping.devops72bat.online
# location /api/payment/ { proxy_pass http://localhost:8080/; } # payment.devops72bat.online

#location /api/catalogue/ { proxy_pass {{ lookup('aws_ssm','dev.frontend.catalogue_url',region='us-east-1') }}; }
#location /api/user/ { proxy_pass {{ lookup('aws_ssm','dev.frontend.user_url',region='us-east-1') }}; }
#location /api/cart/ { proxy_pass {{ lookup('aws_ssm','dev.frontend.cart_url',region='us-east-1') }}; }
#location /api/shipping/ { proxy_pass {{ lookup('aws_ssm','dev.frontend.shipping_url',region='us-east-1') }}; }
#location /api/payment/ { proxy_pass {{ lookup('aws_ssm','dev.frontend.payment_url',region='us-east-1') }}; }

#{ name= "dev.frontend.catalogue_url" , value= "http://catalogue.devops72bat.online:8080/" },
#{ name= "dev.frontend.cart_url" , value= "http://cart.devops72bat.online:8080/" },
#{ name= "dev.frontend.user_url" , value= "http://user.devops72bat.online:8080/" },
#{ name= "dev.frontend.shipping_url" , value= "http://shipping.devops72bat.online:8080/" },
#{ name= "dev.frontend.payment_url" , value= "http://payment.devops72bat.online:8080/" },

#catalogue
#location /api/catalogue/ { proxy_pass {{ lookup('aws_ssm','dev.frontend.catalogue_url',region='us-east-1') }}; }
#{ name= "dev.frontend.catalogue_url" , value= "http://catalogue.devops72bat.online:8080/" },

#{ name= "dev.frontend.catalogue_mongoendpoint" , value= "mongodb.devops72bat.online" },
#{ name= "dev.frontend.catalogue_montru" , value= "MONGO=true" },
#{ name= "dev.frontend.catalogue_monurl" , value= "mongodb://mongodb.devops72bat.online:27017/catalogue" }

#user
#{ name= "dev.frontend.user_REDIS_HOST" , value= "redis.devops72bat.online" },
#{ name= "dev.frontend.user_montru" , value= "MONGO=true" },
#{ name= "dev.frontend.user_monurl" , value= "mongodb://mongodb.devops72bat.online:27017/users" }

#cart
#{ name= "dev.frontend.cart_REDIS_HOST" , value= "redis.devops72bat.online" },
#{ name= "dev.frontend.cart_CATALOGUE_HOST" , value= "catalogue.devops72bat.online" },
#{ name= "dev.frontend.cart_CATALOGUE_PORT" , value= "8080" }
