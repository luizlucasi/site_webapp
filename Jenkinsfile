#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
    	
    	
    	stage('Checkout repository') {
        	git 'https://github.com/luizlucasi/site_webapp.git'
    	}
    	
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

// vim: ft=groovy