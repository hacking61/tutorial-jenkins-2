#!groovy

node {
   // ejemplo de prueba
   //
   // ------------------------------------
   // -- ETAPA: Compilar
   // ------------------------------------
   stage 'CHECK OUT CODIGO'
   
   // -- Configura variables
   echo 'Configurando variables'
   def mvnHome = tool 'M3'
   env.PATH = "${mvnHome}/bin:${env.PATH}"
   echo "var mvnHome='${mvnHome}'"
   echo "var env.PATH='${env.PATH}'"
   
   // -- Descarga código desde SCM
   echo 'Descargando código de SCM'
   //sh 'rm -rf *'
   checkout scm
   
   // -- Compilando
   echo 'Compilando aplicación'
   sh 'mvn clean compile'
   }
