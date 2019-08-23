"# datapower" 

#git clone https://github.com/ibm-datapower/datapower-tutorials.git

#cat datapower-tutorials/using-datapower-in-kubernetes/datapower/config/foo/foo.cfg  | grep port

#sed -i -e "s/  port 80/  port 8181/g" datapower-tutorials/using-datapower-in-kubernetes/datapower/config/foo/foo.cfg 
#cat datapower-tutorials/using-datapower-in-kubernetes/datapower/config/foo/foo.cfg  | grep port

 mkdir $PWD/config
    mkdir $PWD/local
    chmod  777 $PWD
    chmod  777 $PWD/config
    chmod  777 $PWD/local

#docker-compose -f ./docker-compose.yml up -d 


#############################################################################################################################


	docker kill springbootsoapservice
	docker rm springbootsoapservice
	
	docker run --name springbootsoapservice -d -p 8080:8080  marcinkasinski/springbootsoapservice

    #rm -rf $PWD/config
    #rm -rf $PWD/local
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
   -p 9090:9090 \
   -p 9191:9191 \
   -p 8181:8181 \
   -p 7171:7171 \
   -p 6161:6161 \
   -p 9022:22 \
   -p 5554:5554 \
   -p 8000-8010:8000-8010 \
   --name datapower \
   ibmcom/datapower
   
   
   
   
   
    show int
    show int mode
    show web-mgmt
    write memory
    
    
    
    
    
    Navigate to Control Panel -> Network -> Management -> Web Management Service
Switch to the Advanced tab.
Select or create one of the Custom SSL server types with the corresponding certificate for the Web Management Service:

    Use a Server Profile with the Custom SSL server profile
    Use a Server SNI Profile with the Custom SSL SNI server profile 
    