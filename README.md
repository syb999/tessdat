# tessdat fork from https://github.com/tesseract-ocr/tessdata

 chi_sim.traineddata           简体中文通用语言包                                                             

 chi_sim_vert.traineddata      垂直书写的简体中文通用语言包                          
            
 chi_tra.traineddata           繁体中文通用语言包                                 
                             
 chi_tra_vert.traineddata      垂直书写的繁体中文通用语言包                          
                              
 eng.traineddata               英文通用语言包                                         
                            
 osd.traineddata               OSD识别包                                               
                                  


# 关于openwrt使用tesseract-orc的tessdat识别字库的方法:
 1.把需要用到的语言包上传到/tessdat目录内                                       

 2.修改/etc/profile文件,添加如下内容:                                       

  export TESSDATA_PREFIX="/tessdata"
 
  export PATH=$PATH:$TESSDATA_PREFIX

 3.ssh中输入命令，使路径生效:
   source /etc/profile

# 关于tesseract识别带有大量数字的图片时，漏数字的解决方法：
  图片背景色改成白色即可。
  比如原图黑色背景，数字为多种色彩。这时可以使用画图的反色功能来处理图片，
  然后再使用tessract识别即可。
