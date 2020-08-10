node{
     
      stage('Checkout'){
         git 'https://github.com/Sandeep-Shrestha7/SpringbootRestDemo.git'
       
      }  
    
     stage('Compile Package'){
         def mvnHome = tool name: 'localMaven', type: 'maven'
          sh = "${mvnHome}/bin/mvn package"
        
    }
    
      stage('test'){
         def mvnHome = tool name: 'localMaven', type: 'maven'
          sh = "${mvnHome}/bin/mvn test"
        
    }
    
    
      stage('deploy'){
         def mvnHome = tool name: 'localMaven', type: 'maven'
          sh = "${mvnHome}/bin/mvn deploy"
        
    }
}
