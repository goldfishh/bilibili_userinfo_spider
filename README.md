# B站用户信息爬虫

功能实现   √  
信息爬取   ing  
反爬虫     80%  


头像批量抓取  =>   代码  
大数据分析:  
  等级  
  经验  
  昵称  => 有趣的大数据项目  
  头像挂件  
  认证信息  
  地区  
  视频总播放数  =>  
  rank   ???  =>意义待商榷  
  签名  => 有趣的api接口  
  粉丝数  
  关注数   
  会员信息  => 大会员 年费大会员 普通用户  
   
 1.22  
※※※※※※※※※※※※※※※※  
封IP => IP proxy_pool  
※※※※※※※※※※※※※※※※  
fans following 网页api 失效了  => 重新找到新api  
速度太慢 sleep  => multiprocessing  
线程 不好用  =>  加入代理池解决  
  
  
1.23   
中途会有停顿  => 增加输出信息  
然后13 突然抓到27 不是特例  => 线程非线性抓取 13可能线程出了问题(被封ip等)中断  
mysql 2013错误 lose connection  => mysql连接有时限,更改代码为每插入一次连接一次(后期可优化)  
  
1.24  
发现新的反爬虫机制,程序运行到一定数据量后会强制重定向到 http://www.youdao.com  
这个时候出现新bug  
暂时更换程序运行入口,遇到重定向强制退出程序后休眠再抓取  
  
3亿数据抓取速度太慢,反爬虫正常的话一天能抓25W个页面,这样也要1200天...  
后期考虑分布式架构爬取数据  
  
