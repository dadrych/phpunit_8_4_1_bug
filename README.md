    /home/www/phpunit:$ php vendor/phpunit/phpunit/phpunit --version && php vendor/phpunit/phpunit/phpunit --configuration=phpunit.xml --filter "/(::testFoo)( .*)?$/" App\\\\Tests\\\\FooTest tests/FooTest.php
    PHPUnit 8.3.5 by Sebastian Bergmann and contributors.
    
    PHPUnit 8.3.5 by Sebastian Bergmann and contributors.
    
    Runtime:       PHP 7.3.10-1+ubuntu18.04.1+deb.sury.org+1
    Configuration: /home/www/phpunit/phpunit.xml
    
    .                                                                   1 / 1 (100%)
    
    Time: 34 ms, Memory: 4.00 MB
    
    OK (1 test, 1 assertion)
    
    
    /home/www/phpunit:$ php vendor/phpunit/phpunit/phpunit --version && php vendor/phpunit/phpunit/phpunit --configuration=phpunit.xml --filter "/(::testFoo)( .*)?$/" App\\\\Tests\\\\FooTest tests/FooTest.php
    PHPUnit 8.4.1 by Sebastian Bergmann and contributors.
    
    PHP Fatal error:  Uncaught PHPUnit\Runner\Exception: Class 'App\\Tests\\FooTest' could not be found in '/home/www/phpunit/tests/FooTest.php'. in /home/www/phpunit/vendor/phpunit/phpunit/src/Runner/StandardTestSuiteLoader.php:69
    Stack trace:
    #0 /home/www/phpunit/vendor/phpunit/phpunit/src/Runner/BaseTestRunner.php(141): PHPUnit\Runner\StandardTestSuiteLoader->load('App\\\\Tests\\\\Foo...', '/home/www/phpun...')
    #1 /home/www/phpunit/vendor/phpunit/phpunit/src/Runner/BaseTestRunner.php(101): PHPUnit\Runner\BaseTestRunner->loadSuiteClass('App\\\\Tests\\\\Foo...', '/home/www/phpun...')
    #2 /home/www/phpunit/vendor/phpunit/phpunit/src/TextUI/Command.php(177): PHPUnit\Runner\BaseTestRunner->getTest('App\\\\Tests\\\\Foo...', '/home/www/phpun...', Array)
    #3 /home/www/phpunit/vendor/phpunit/phpunit/src/TextUI/Command.php(159): PHPUnit\TextUI\Command->run(Array, true)
    #4 /home/www/phpunit/vendor/phpunit/phpunit/phpunit(61): PHPUnit\TextUI\Command::main()
    #5 {main}
      thrown in /home/www/phpunit/vendor/phpunit/phpunit/src/Runner/StandardTestSuiteLoader.php on line 69