# B��
## ʲô��B����
B����һ�����ε����ݽṹ��������дΪB- Tree����Ȼ��B- Tree����B+ Tree�����ε����ݽṹ��һ�ַǳ��ʺ���������ص��㷨ʵ�ֵ����ݽṹ������͵�Ӧ�ó����������ݿ��������

## ���ݿ������ΪʲôҪʹ��B- Tree?
���˽⵽���ݿ����������B- Tree�����ݽṹʱ���ܶ��˿��ܻ������ʣ�ΪʲôҪ��B- Tree��Ϊʲô��ֱ�������飬Ϊʲô���ö�����������Ϊʲô��ֱ����������ʵ���㷨��ʱ�临�Ӷ���˵�������Ѿ��ǳ����ˣ�O��logN���������Ƕ������ݿ��������˵��������Ҫ�洢��Ӳ���ϣ�һ���洢����Ӳ���ϣ�IO�������һ�������⣬����Ӱ��Ч�ʵľͲ������㷨��Ч�ʶ���IO�����ĵ�ʱ�䡣ÿ��IO��ʱ��ֻ��ͨ��Ӳ���������������Ʋ��ˣ����ԣ�ֻ�ܴ�IO�Ĳ��Ҵ��������ˣ��������ҵ�Ŀ����Ҫ10��IO����B- Tree��Ҫ<10��IO��������㹻������ѡ��B- Tree��

## B-Tree��ԭ��
������������������������˵��Ӱ����Ƚϴ����ľ������ĸ߶ȣ�������������IO�Ĵ���������ͨ���������ĸ߶���ʵ�֣�B-���Ļ���ԭ�����������

һ��m�׵�B���������¼���������
1. ���ڵ�������������Ů
2. ÿ���м�ڵ㶼����k-1��Ԫ�غ�k�����ӣ�����m/2<=k<=m
3. ÿһ��Ҷ�ӽڵ㶼����k-1��Ԫ�أ�����m/2<=k<=m
4. ���е�Ҷ�ӽڵ㶼λ��ͬһ��
5. ÿ���ڵ��Ԫ�ش�С�������򣬽ڵ㵱��k-1��Ԫ��������k�����Ӱ�����Ԫ�ص�ֵ��Ļ���

## B-�Ĳ���
��1�δ���IO��

![](http://upload-images.jianshu.io/upload_images/1975419-d3041b0215c42148?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

���ڴ��ж�λ����9�Ƚϣ���

![](http://upload-images.jianshu.io/upload_images/1975419-a3953a5f3a618078?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

��2�δ���IO��

![](http://upload-images.jianshu.io/upload_images/1975419-02072bdd25eed2b5?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

���ڴ��ж�λ����2��6�Ƚϣ���

![](http://upload-images.jianshu.io/upload_images/1975419-530b47ac087b1e81?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

��3�δ���IO��

![](http://upload-images.jianshu.io/upload_images/1975419-7beb51451f650442?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

���ڴ��ж�λ����3��5�Ƚϣ���

![](http://upload-images.jianshu.io/upload_images/1975419-c6567e2f52bd7359?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## B-����ڵ�
����4
�Զ����²���4�Ľڵ�λ�ã�����4Ӧ�����뵽�ڵ�Ԫ��3��5֮�䡣

![](http://upload-images.jianshu.io/upload_images/1975419-735fd0910ba71ed5?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

�ڵ�3��5�Ѿ�����Ԫ�ؽڵ㣬�޷������ӡ����׽ڵ� 2�� 6 Ҳ����Ԫ�ؽڵ㣬Ҳ�޷������ӡ����ڵ�9�ǵ�Ԫ�ؽڵ㣬��������Ϊ��Ԫ�ؽڵ㡣����**���**�ڵ�3��5��ڵ�2��6���ø��ڵ�9����Ϊ��Ԫ�ؽڵ�4��9���ڵ�6����Ϊ���ڵ�ĵڶ������ӡ�

![](http://upload-images.jianshu.io/upload_images/1975419-aa87aa954404f186?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## B-ɾ���ڵ�
�Զ����²���Ԫ��11�Ľڵ�λ�á�

![](http://upload-images.jianshu.io/upload_images/1975419-9c8fb0c0981905a9?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

ɾ��11�󣬽ڵ�12ֻ��һ�����ӣ�������B���淶������ҳ�12,13,15�����ڵ����λ��13��ȡ���ڵ�12�����ڵ�12�������Ƴ�Ϊ��һ�����ӡ���������̳�Ϊ**����**��

![](http://upload-images.jianshu.io/upload_images/1975419-6b8481b474d4c420?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](http://upload-images.jianshu.io/upload_images/1975419-084b797a85fe44f3?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

�����ݽṹ�㷺��Ӧ�����ļ�ϵͳ�����������ݿ����������MongoDb,��ʵ�ӱ�������˵�������ݽṹ��������ں�IO�����Ƚ�Ƶ����Ӧ�ó����������Ż���ͨ�������ڴ��е��������������Ч�ʡ�