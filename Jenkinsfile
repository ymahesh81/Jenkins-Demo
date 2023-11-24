pipeline {
    agent any

    stages {
        stage('Parse CSV') {
            steps {
                script {
                    def csvFile = readFile 'file.csv'
                    def rows = csv file: csvFile, returnRows: true
                    
                    // Now 'rows' is a list of lists representing the CSV content
                    for (row in rows) {
                        echo "Row: ${row.join(', ')}"
                    }
                }
            }
        }
    }
}
