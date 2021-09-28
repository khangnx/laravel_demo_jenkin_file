node {
    stage('preparation') {
        // Checkout the master branch, with credential
        git credentialsId: 'khangnx', url: 'https://github.com/khangnx/laravel_demo_jenkin_file.git'
    }
    //stage("composer_update_no_script") {
        //bat 'composer update --no-scripts '
    //}
    stage("composer_install") {
        // Run composer install
        bat 'composer install'
    }
    stage("phpunit") {
        bat 'vendor/bin/phpunit'
    }
}