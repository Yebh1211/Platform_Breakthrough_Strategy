# Platform_Breakthrough_Strategy         
After reading Sinolink Security's research report, reproduce the platform breakthrough strategy and test the benefits       
Task1：阅读研报后，进行基础的准备工作 用日频数据识别Peak和Platform 找到突破Platform的日期 绘制突破后0-5天的平均收益K线图 观察收益情况      
Task2：在Task1基础上，根据Platform长度分类绘制突破后0-5天的平均收益K线图 寻找platform_length参数对收益的影响      
Task3：利用前面找到的信号和分钟频收益数据，根据Platform长度分类绘制突破后0-5天的平均分钟收益图       
Task4：绘制突破后0-5天的总平均分钟收益图     
Task5:根据信号，模拟交易（突破平台次日开盘买入，第二天收盘卖出），用两日收益的均值作为当天收益。绘制2020年以来的收益曲线图          
Task6：发现收益一般 可能是市场中某几日突破平台数量较多 于是先合成日内平均收益再进行日间平均 根据Platform长度分类绘制突破后0-5天的平均收益K线图         
Task7：先合成日内平均收益再进行日间平均，根据Platform长度分类绘制突破后0-5天的平均分钟收益图       
Task8:研究平台特征对突破后收益的影响 先对突破后收益率进行分组 取前p%和后p% 分别绘制平台内的平均每日K线图 观察形态      
Task9:想到可以利用平台内特征以及突破当日特征来判断突破当天突破后是否会连续突破 利用机器学习模型（rf）进行分类。            
       首先提取特征：1.平台最后一天open / 平台第一天open 衡量平台内价格变化趋势
                    2.平台后50%时间的平均vol / 平台前50%时间的平均vol 衡量平台内成交量变化趋势
                    3.平台内最高价 / 平台内最低价 衡量平台振幅
                    4.突破当日close / 突破当日open 衡量突破力度
                    5.突破当日最高价/  平台最高价 衡量突破力度
       发现效果一般 放弃                         
Task10：利用2020-2025年相关系数矩阵观察 发现breakthrough_validity和platform_volatility_open与daily return相关性较高 于是用两个指标综合筛选（筛选platform_volatility_open的前30% 再从中选择increase_validity最小的10只股票） 绘制累计收益图 并在2010年后数据集内测试发现未失效 收益约年化30%   
Task11：绘制新策略K线图、分钟收益图，观察是否有更高收益 注意到可能在第二天买入第三天卖出收益更高                
Task12：绘制第二天买入第三天卖出收益的累计收益曲线 年化确实提升到35%以上       
                    
