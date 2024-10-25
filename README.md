# Pretask  
真的真的没有时间了，所以只写完了一部分XD  
我学习态度敲端正的，求善良QAQ  
[![pAwSdSJ.png](https://s21.ax1x.com/2024/10/24/pAwSdSJ.png)](https://imgse.com/i/pAwSdSJ)  
```
#include<stdio.h>
#include<string.h>
int main(){
    FILE* fp=fopen("C:\\Users\\deathknight\\Desktop\\CS_M_02.txt","r");//请自行修改文件路径
    char c[1000];
    int t,q,d[1000];
    float s=0,p;
    while(fgets(c,1000,fp)){
        if(c[strlen(c)-2]=='D'){//最后一位是换行符
            printf("%s",c);
        }else{
            s=0;
            p=1;
            printf("%c ",c[0]);
            for(int i=2;i<strlen(c)-2;i++){
                if(c[i]=='.'){//以小数点点为分界点
                    t=i;
                }
                d[i]=c[i]-'0';//将字符数组转化为数字
            }
            for(int i=t-1;i>=2;i--){二进制转十进制
                s=s+d[i]*p;
                p=p*2;
            }
            p=2;
            for(int i=t+1;i<strlen(c)-2;i++){
                s=s+d[i]/p*1.0;
                p=p*2;
            }
            printf("%gD\n",s);
        }
    }
    fclose(fp);
    return 0;
}
```
