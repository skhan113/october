#!/usr/bin/env groovy
import hudson.model.*
import hudson.EnvVars
import java.net.URL

node{
    stage('Get checkout'){
        git 'https://github.com/skhan113/DevOpsClassCodes.git'
    }
    stage('Addressbook Compile'){
        withMaven(maven:'mymaven'){
            sh 'mvn compile'
        }
    }
    stage('Addressbook Review'){
        withMaven(maven:'mymaven'){
            sh 'mvn pmd:pmd'
        }
    }
    stage('Addressbook Package'){
        withMaven(maven:'mymaven'){
            sh ('mvn package')
        }
    }
    
}
