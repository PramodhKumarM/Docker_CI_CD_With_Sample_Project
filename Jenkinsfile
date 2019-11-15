#!/usr/bin/env groovy
import java.net.URL
node{
    stage('git checkout'){
        git 'https://github.com/PramodhKumarM/Docker_CI_CD_With_Sample_Project.git'
    }
    stage('AB Compile'){
        withMaven(maven:'my maven'){
            sh 'mvn compile'
        }
    }
    stage('AB Review'){
        withMaven(maven:'my maven'){
            sh 'mvn pmd:pmd'
        }
    }
    stage('AB Package'){
        withMaven(maven:'my maven'){
            sh 'mvn package'
        }
    }
}
