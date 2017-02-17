#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
    	
    	
    	stage('Checkout repository') {
        	checkout scm
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