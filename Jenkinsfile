pipeline {
    agent any

    stages {
        stage('Parse CSV') {
            steps {
                script {
                    def csvFile = readFile('file.csv')
                    def data = readCSV text: csvFile
                    
                    // Now 'data' is a list of maps representing the CSV content
                    for (row in data) {
                        echo "Row: ${row}"
                    }
                }
            }
        }
    }
}
