pipeline {
    agent any
    // environment {
    //     name = "Mohit"
    // }
    parameters {
        string(name: 'Name', defaultValue: '', description: "You can eneter your name !!")
        choice(name: 'City', choices: ['Jaipur' ,'Delhi','Rajasthan'], description: "Enter your city")
        booleanParam(name: 'IsGender', defaultValue: true )
        password(name: 'password',  defaultValue: 'Rajveer' ,description: 'Enter your password')
        
    }
    
    stages {
        stage('User Input') {
            steps {
                echo "Hello world !!"
                sh 'echo my Name is :  ${Name}'
                sh 'echo my city is :  ${City}'
                sh 'echo my gender is : ${IsGender}'
                sh 'echo my password is : ${password}'
            }
        }
        
        stage('Continue ?') {
            input{
                message "Should we continue"
                ok "Yes we should"
            }
            
            steps {
                echo "whatsup"
            }
        }

        stage('Deploy on prod') {
            steps {
                echo 'Continuing the pipeline...'
                sh 'exit 1'
            }
        }
    }
    post{
        always{
            echo "Hello world"
        }
    }
}
