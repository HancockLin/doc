## memcache协程客户端
memcache协程客户端,由swoole 协程client实现   
github地址: https://github.com/easy-swoole/memcache 

## composer安装   
```
composer require easyswoole/memcache
```

## 使用客户端(需要协程环境):  
```php
$config = new \EasySwoole\Memcache\Config([
    'host' => '127.0.0.1',
    'port' => 11211
]);
$client = new EasySwoole\Memcache\Memcache($config);
```

## 使用示例:  
```php
$config = new \EasySwoole\Memcache\Config([
    'host' => '127.0.0.1',
    'port' => 11211
]);
$client = new EasySwoole\Memcache\Memcache($config);
$client->set('a',1);
$client->get('a');
```

## 使用方法:   
### touch摸一下(刷新有效期)  
touch($key, $expiration, $timeout = null)

### increment自增KEY  

increment($key, $offset = 1, $initialValue = 0, $expiration = 0, $timeout = null)

### decrement自减KEY  
decrement($key, $offset = 1, $initialValue = 0, $expiration = 0, $timeout = null)

### set设置KEY(覆盖)  
set($key, $value, $expiration = 0, $timeout = null)

### add增加KEY(非覆盖)  
add($key, $value, $expiration = 0, $timeout = null)

### replace替换一个KEY  
replace($key, $value, $expiration = 0, $timeout = null)

### append追加数据到末尾  
append($key, $value, $timeout = null)

### prepend追加数据到开头  
prepend($key, $value, $timeout = null)

### get获取KEY  
get($key, $timeout = null)

### delete删除一个key  
delete($key, $timeout = null)

### stats获取服务器状态  
stats($type = null, $timeout = null)

### version获取服务器版本  
version(int $timeout = null)

### flush  清空缓存  
flush(int $expiration = null, int $timeout = null)



