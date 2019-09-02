---
title: 通过反向代理访问解析未备案的域名
date:

---
国内域名必须要求备案，不备案无法解析到国内的服务器。尤其是当你访问http web服务时，无论时80端口还是443端口，其他的端口都会被拦截到备案警告的页面。🐎。备案和实名认证一个性质，只是为了你犯事了方便抓你，对用户来说真没一点好处，每年都要拍照上传认证，公安备案，繁琐的域名备案过程真让人抓狂。大一的时候还想折腾一下备个案就算了，到了后来变本加厉要求还很高，随即放弃国内的域名厂商，转到国外域名厂商。目前在使用namecheap。爽歪歪，没那些多余的事儿。
国内腾讯那里薅羊毛搞来一台学生机器，性能凑活着用，有时候需要使用域名访问web服务时就会拦截到备案警告的界面。想了想我就死和这个ICP备案杠上，使用nginx反向代理过去，这样使用域名也能间接地访问过去。只不过只能监听特定的端口，如果由其他端口还要一个一个配，LVS或许可以解决。因为nginx反向代理基于`IP:PORT`