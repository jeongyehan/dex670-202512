# Anypoint Platform Development: Production-Ready Integrations - DEX670

## Local Path
- PROJECT_HOME=/Users/yehan.jeong/Desktop/dex670-202512
- STUDENT_FILE=/Users/yehan.jeong/Desktop/CDEV-DEX670-EN-25oct2024-Student-Files

## Anypoint Platform Information
- Mule Account:

### Business Group
- Business Group ID: c1f2340a-aef7-421e-aab8-07e0d3afb5da
- Client ID: df537775a27643b6a341a4bb16798f7e
- Client Secret: 0F1Cf7c4226745f1983237244315DCaD

### Connected App
- Exchange Viewer ID: 21b54d06e0474ba78116c292a0f6522a
- Exchange Viewer Secret: 1FF50f72035648Be9Fb35F7d844Edf2a
- Exchange Contributor ID: ec57cd5eba094e81b19a735bf6fa1063
- Exchange Contributor Secret: a391cB0EA81A460cbe76CF254012B0D7

## Commands
- export PROJECT_HOME=/Users/yehan.jeong/Desktop/dex670-202512
- export STUDENT_FILE=/Users/yehan.jeong/Desktop/CDEV-DEX670-EN-25oct2024-Student-Files
- cp $STUDENT_FILE/etc/settings.xml ~/.m2/
- mkdir bom
- mkdir parent-pom
- mvn install:install-file -Dfile=bom/pom.xml -DpomFile=bom/pom.xml
- mvn install:install-file -Dfile=parent-pom/pom.xml -DpomFile=parent-pom/pom.xml
- cp -r $STUDENT_FILE/walkthroughs/devint/module01/wt1-1_starter/apps-commons ./
- mvn clean verify -U -Dencrypt.key=secure12345 -DskipTests=true
- curl -ik -X PUT -H "Content-Type: application/json" -d "{\"lastName\" :\"Smith\",\"numBags\":2}" https://localhost:8081/api/v1/tickets/PNR123/checkin
- curl -ik -X PUT -H "Content-Type: application/json" -d "{\"payerID\": \"STJ8222K092ST\", \"paymentID\": \"PAY-1AKD7482FAB9STATKO\"}" https://localhost:8081/api/v1/tickets/N123/paymentApproval
- curl -ik https://localhost:8081/alive
- curl -ik https://localhost:8081/ready
- curl -ik -X PUT -H "Content-Type: application/json" -d "{\"lastName\":\"Mule\",\"numBags\":2}" https://localhost:8081/api/v1/tickets/PNR123/checkin
