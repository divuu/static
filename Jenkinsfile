pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
          withAWS(region:'ap-south-1' ,credentials:'s3-access-credential') {
          sh 'echo "Uploading content with AWS creds"'
            s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'my-s3-utkarsh')
          }
      }
    }
  }
}