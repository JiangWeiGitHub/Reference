1. 需求：读取终端输入的一行字符串，包括空格，敲击回车键结束输入：

  ```
  std::string tmp;
  getline(std::cin,tmp);
  ```

2. 需求：按照MD5规范，打印32位十六进制数字，例如9e107d9d372bb6826bd81d3542a419d6

  备注：

    因为MD5输出固定长度为128位的一串数字，所以可以使用16个unsigned char变量来存储（即包含16个元素的一维数组）


    格式转换如下（假设数据已经存储在md5数组中）：

    ```
    for(int i = 0; i < 16; i++)
        cout << hex << setw(2) << setfill('0') << (int)md5[i];
    ```

    其中，setw表示输出每个元素占两位，setfill表示用0来填充空白位
