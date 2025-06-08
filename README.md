pom.xml 

<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>devopsmaven</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>
    <dependencies>
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>4.33.0</version>
        </dependency>
        <dependency>
            <groupId>org.testng</groupId>
            <artifactId>testng</artifactId>
            <version>7.11.0</version>
            <scope>test</scope>
        </dependency>
    </dependencies>



</project>


Main.java


package org.example;

//TIP To <b>Run</b> code, press <shortcut actionId="Run"/> or
// click the <icon src="AllIcons.Actions.Execute"/> icon in the gutter.
public class Main {
    public static void main(String[] args) {
        //TIP Press <shortcut actionId="ShowIntentionActions"/> with your caret at the highlighted text
        // to see how IntelliJ IDEA suggests fixing it.
        System.out.printf("Hello and welcome!");

    }
}



index.html


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sample Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <img src="logo.png" alt="Logo" class="logo">
        <h1>Welcome to My Website</h1>
    </header>
    <main>
        <p>This is a simple webpage using HTML and CSS.</p>
    </main>
    <footer>
        <p>&copy; 2025 Sample Website</p>
    </footer>
</body>
</html>


style.css


body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 20px;
}

.logo {
    width: 100px;
    height: auto;
}

main {
    margin: 20px;
    padding: 20px;
    background-color: white;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}

footer {
    background-color: #333;
    color: white;
    padding: 10px;
    position: fixed;
    width: 100%;
    bottom: 0;
}

TERMINAL 

git init 
git add .                                                          git status
git commit -m "Initial commit"                
git remote add origin "<your-repository-url>"                      git remote add origin https://github.com/Lavzgoyal999/project2.git
                                                                   git remote show origin
git push -u origin master --->x



mvn clean install 
git add docs/*
git commit -m "Deploy site to GitHub Pages"
git push origin master



src/test/java   
right click
new
package
org.test   enter


copy this ctrl+c

package org.test;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.Assert;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

import static org.testng.Assert.assertTrue;

public class WebPageTest {
 private static WebDriver driver;

 @BeforeTest
public void openBrowser() throws InterruptedException {
 driver = new ChromeDriver();
 driver.manage().window().maximize();
 Thread.sleep(2000);
 driver.get("https://sauravsarkar-codersarcade.github.io/CA-MVN/"); // "Note:You should use your GITHUB-URL here...!!!"
 }

 @Test
public void titleValidationTest(){
 String actualTitle = driver.getTitle();
 String expectedTitle = "Tripillar Solutions";
 Assert.assertEquals(actualTitle, expectedTitle);
 assertTrue(true, "Title should contain 'Tripillar'");
 }

 @AfterTest
public void closeBrowser() throws InterruptedException {
 Thread.sleep(1000);
 driver.quit();
 }
}

right click org.test
paste 

WebPageTest.java open ho jayega 

right click WebPageTest.java
run

DONE


