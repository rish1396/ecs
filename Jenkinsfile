pipeline {
    agent any

    stages {

        stage('Logging into AWS ECR') {
            steps {
                script {
                    sh "aws ecr --region us-east-1 | docker login -u AWS -p eyJwYXlsb2FkIjoiVCtWNmh5WWlQV0JyaDdoZUxFU3N4MTQxN2krWjNhdkVxRFdwaWppak0zL2QvTitXT0NCNkhURnlSK2pmT2IzdWR5MDQxTGhjaWJidjJjNTdreUp5Nkc4N1Z2clNyZnBKcXdrbG90SWVzNENTWithTkZMeHRLNWhsQyt2bE1UQlZpMElIUEIrNG1BS1BrRFh6dGRFUVNSSFN5V3lsMWdCVVhnS3BseFJ4ZVJ6SkFKMFByVUpQWlhRZUlCeFY3bVcySGhzblVZQXl4WG9iQkxCVDRVc2h1TnBTYUZvcWNjU0tLTGFJbmlVazhWbGtyem1XRlRYRkJyNithR05UcEJaanBNSitNdHJVZTlmUThUQVUrUVIwY2pvTnVmaTlVWm15dEYwWVdrbDA3KzVXNjRHUEh4QkVhcVRhSWFmNko2RytmWFpMenhqTUhabjJHcTZGYVhrc2ppaEVtN29sOHVVa1BkL1RjSnNwTUxDa1d1QTJBY2QrRVViSTY0cTgxQmo4Mll6Z2cwME56cDUxU2RTaVE2N0FiQ3lMQ25HdzRWYnE5MmVPVVpUUmVCUEJGN0ZPOEpCU0ZmSHZoV004K252UVc0bEk0djNPWkg3NDZBajUrT3VBUE0zTkhmT0REeVhKaEVkSURISmVsdTEyQUNjQ0Y5dEhReE1UQi9OalJmSEpXM21OTmNOU3FFdUJFU3NqbWtXZXpxcDNGZHFTZ2M1ajRuMk5NaXVLazU4bENoZVF6dUUzeEppN29NQWNDSkVOc2gzaDVzejYvenVyZytJNTdlZlJXSElhOE93T2tTMlc4eC9Mcm1vVGhVMXlxZ3pTOVVzVGs3UXNPMEFJMi83bDQ5OW1nRWN0SnE4elFlMEV2eFVkT20vNVJDSEJhckU1NGk4bkhpMURwY2V0L1RMZmFpSUkvb0xoRjR1MXErS3ZmenVVWjdqOVZGeTlxQzBMejNxVHRmQzNRNnhGT2pqbHpuc2Z5emdFWWNlaFo0NFpKUGt4dzZNbGd3bk9iVWtoVnFvSDBIczYzbnplc2lsVmxYSFVFb0RKU0Z0QUdDU09rckhHQm9OeGdkdUxKYWRONG04b3FnTURhOUlnZC81N25rUThzY09wQ3Q3cDhOeDQvRm9QLytmR3paZklaQWYwd0dpbVZRTnJyZVZxWktXd2xSdSt1YmUxZmpWZnBZL1Rvc05pcVFNRFdJbGcwWkkybXVpR0VETCtHMXFHMHhjNjAzdmV0dGd4VnhpOUdtK1liaXNkNXlHRmg5KzI3N214QWpOa3dnK2w0b1VRRVlBZ2U5eGh2Q204U2tZTW1WQlVyNUJ1a1RYcTBMbHM2aERpd0pvQXlDTUdqVlByU1hjWm5vZnRtRG9mUFIrKzkzYi9Vdz09IiwiZGF0YWtleSI6IkFRRUJBSGh3bTBZYUlTSmVSdEptNW4xRzZ1cWVla1h1b1hYUGU1VUZjZTlScTgvMTR3QUFBSDR3ZkFZSktvWklodmNOQVFjR29HOHdiUUlCQURCb0Jna3Foa2lHOXcwQkJ3RXdIZ1lKWUlaSUFXVURCQUV1TUJFRUROMW9CVXRVZmhPTE5OMVBjZ0lCRUlBN3E4Nit0ZGtzdnVpa1NVUUhTM2R3MXJKWEkyRWcrRmpMMlMvalkxbXJRODh0VWlvNWFvTzRreXJFaDE3NWZrUnJtOEVBdlltT3YyNTdPbG89IiwidmVyc2lvbiI6IjIiLCJ0eXBlIjoiREFUQV9LRVkiLCJleHBpcmF0aW9uIjoxNjQ4NTc3MjkwfQ== 177558318616.dkr.ecr.us-east-1.amazonaws.com"
                }
            }
        }
        
        stage('Building image') {
            steps{
                script {
                    sh "docker build -t test ."
                    sh "docker tag test:latest 177558318616.dkr.ecr.us-east-1.amazonaws.com/test:latest"
                }
            }
        }
    }
}
