

Firmware upgrade
http://websphereeai.blogspot.com/2015/10/upgrading-firmware-on-your-websphere.html


#############################################################################################################################


	docker kill springbootsoapservice
	docker rm springbootsoapservice
	
	docker run --name springbootsoapservice -d -p 8888:8080  marcinkasinski/springbootsoapservice

    rm -rf $PWD/config
    rm -rf $PWD/local
    mkdir $PWD/config
    mkdir $PWD/local
    chmod  777 $PWD
    chmod  777 $PWD/config
    chmod  777 $PWD/local
	docker kill  datapower 
	docker rm  datapower 
	docker run -it \
   -v $PWD/config:/drouter/config \
   -v $PWD/local:/drouter/local \
   -e DATAPOWER_ACCEPT_LICENSE=true \
   -e DATAPOWER_INTERACTIVE=true \
   -p 9191:9090 \
   -p 9999:9999 \
   -p 7171:7171 \
   -p 6161:6161 \
   -p 9022:22 \
   -p 5554:5554 \
   -p 8000-8010:8000-8010 \
   --name datapower \
   ibmcom/datapower
   
   
   
      
    configure; web-mgmt 0 9090 9090; write memory
   
    show int
    show int mode
    show web-mgmt
    write memory
    
    
    
Zmiana certyfikatu konsoli administracyjnej.
 
http://www-01.ibm.com/support/docview.wss?uid=swg21577098
    
    Navigate to Control Panel -> Network -> Management -> Web Management Service
Switch to the Advanced tab.
Select or create one of the Custom SSL server types with the corresponding certificate for the Web Management Service:

    Use a Server Profile with the Custom SSL server profile
    Use a Server SNI Profile with the Custom SSL SNI server profile 
    