# python #
## AnalysisPcap.py
* 在AnalysisPcapTest.py中，通过对pcap文件进行解析，将tcp下的应用层数据解析存为本地的txt文件中。
* 该tcp下的数据在存储在analysispcap/analysispcap/XX.txt
* 在def dump_reassemble_stream(self, client_ads, server_ads):函数中，可实现对特定tcp流的提取，前提为利用抓包工具，先去查看自己想要获取的指定流，或者调用def dump_tcp_content去查看所有的TCP流，然后提供该流的client和server端的[ip，port]

## TcpData.py
* 在TcpData.py中，将传入的Tcp Stream List 进行处理过滤，返回无重传的，无重流的Tcp Stream List


## test/AnalysisPcapTest.py
* 在test文件夹中的AnalysisPcapTest.py中,对AnalysisPcap.py进行单元测试
* 本单元测试采用pytest测试框架
* 首先将analysispcap包通过pip install XX(analysispcap包在本地的绝对路径)或python setup.py install安装到python库中,方可直接运行AnalysisPcapTest.py
* 安装成功后，在cmd中运行pytest AnalysisPcapTest.py，或在pycharm中的Edit configurations下的interpreter options中输入-m pytset后，直接运行。

## test/TcpDataTest.py
* 在test文件夹中的TcpDataTestTest.py中,对TcpData.py进行单元测试

