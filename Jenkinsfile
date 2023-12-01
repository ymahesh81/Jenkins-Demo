pipeline {
    agent any

    stages {
        stage('Parse CSV') {
            steps {
                script {
                    // Define the path to your CSV file
                    def csvFilePath = "file.csv"

                    // Read and parse the CSV file
                    def csvData = csvRead file: csvFilePath, separator: ','

                    // Iterate through the rows and print them
                    csvData.each { row ->
                        // Filter out null values and join the elements
                        def joinedRow = row.findAll { it != null }.join(', ')
                        echo "Row: ${joinedRow}"
                    }
                }
            }
        }
    }
}
