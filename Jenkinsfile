node(''){
     stage('git'){
         checkout scm       
     }
     dir('C:/Users/SESA528099/Desktop/Binaries'){
    stage('upload firmware'){
    // I have to give the location of shared or copy directory
   try{
    bat 'robocopy "C:/Users/SESA528099/Desktop/Firmware_upgrade" "C:/Users/SESA528099/Desktop/Binaries" '
   }
   catch(err){
   }
   try{
   bat '''
   //python fimrware_upgrade.py
   echo "hello"
   '''
   }
   catch(err){
   }          
    }
    stage(' Wait Time'){
         sleep 120
    }
    stage('check for firmware update'){
    bat '''
      python Fimrware_check.py 
    '''
    }
}
}
