#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
    	
    	stage('Build') {
            node {
        		checkout scm
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