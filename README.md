Scenario: Test if "Year Founded" has right type of value
      Given the AoS
          * get property value[Year Founded]
          * remember it as the YearFounded
      When set property value[Year Founded] to NineteenHundredNinetyEight
      Then wait until done
      When get property value[Year Founded]
      Then it is not equal to NineteenHundredNinetyEight

Scenario: SET <set-string-test-desc> to a BOOLEAN PROPERTY
      Given the Application
          * get link school
       When set property [name] to TRUE
       Then wait for exception
       Then [Exception:PropertyNotExists: Property name does not exist. Property name must be a string value.]

Scenario: GET <get-string-test-desc> from a BOOLEAN PROPERTY
      Given the Application
          * get link school
       When set property[name] to TRUE
       Then wait for exception
       Then [Exception:PropertyNotExists: Property name does not exist. Property name must be a string value.]

Scenario: SET <set-boolean-test-desc> to a STRING PROPERTY
      Given the Application
          * get link school
          * get list students
          * get first
       When set property [active] to Paul
       Then wait for exception
       Then [Exception:PropertyNotExists: Property active does not exist. Property active must be a boolean value.] 

Scenario: GET <get-boolean-test-desc> from a STRING PROPERTY
      Given the Application
          * get link school
          * get list students
          * get first
       When get property [active]
       Then wait for exception
       Then [Exception:PropertyNotExists: Property active does not exist. Property active must be a boolean value.] 

Scenario: SET <set-boolean-test-desc> to a NUMBER PROPERTY
      Given the Application
          * get link school
          * get list students
          * get first
       When set property[active] to 78
       Then wait for exception
       Then [Exception:PropertyNotExists: Property active does not exist. Property active must be a boolean value.] 

Scenario: GET <get-boolean-test-desc> from a NUMBER PROPERTY
      Given the Application
          * get link school
          * get list students
          * get first
       When get property[active]
       Then wait for exception
       Then [Exception:PropertyNotExists: Property active does not exist. Property active must be a boolean value.] 



