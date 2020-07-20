Scenario: SET <set-string-test-desc> to a NUMBER PROPERTY
      Given the Application
          * get link school
       When set prop name to 10
       Then wait for exception
       Then [Exception:PropertyNotExists: Property name does not exist. Property name must be a string value.] 

Scenario: GET <get-string-test-desc> from a NUMBER PROPERTY
      Given the Application
          * get link school
          # FIXME: When get prop name after the UpdateTime
          # for now, instead do the following
       When set prop name 10
       Then wait for exception
       Then [Exception:PropertyNotExists: Property name does not exist. Property name must be a string value.] 

Scenario: SET <set-string-test-desc> to a BOOLEAN PROPERTY
      Given the Application
          * get link school
       When set prop name to TRUE
       Then wait for exception
       Then [Exception:PropertyNotExists: Property name does not exist. Property name must be a string value.]

Scenario: GET <get-string-test-desc> from a BOOLEAN PROPERTY
      Given the Application
          * get link school
          # FIXME: When get prop name after the UpdateTime
          # for now, instead do the following
       When set prop name TRUE
       Then wait for exception
       Then [Exception:PropertyNotExists: Property name does not exist. Property name must be a string value.]

Scenario: SET <set-boolean-test-desc> to a STRING PROPERTY
      Given the Application
          * get link school
          * get list students
          * get first
       When set prop active to Paul
       Then wait for exception
       Then [Exception:PropertyNotExists: Property active does not exist. Property active must be a boolean value.] 

Scenario: GET <get-boolean-test-desc> from a STRING PROPERTY
      Given the Application
          * get link school
          * get list students
          * get first
          # FIXME: When get prop active after the UpdateTime
       When get prop active
       Then wait for exception
       Then [Exception:PropertyNotExists: Property active does not exist. Property active must be a boolean value.] 

Scenario: SET <set-boolean-test-desc> to a NUMBER PROPERTY
      Given the Application
          * get link school
          * get list students
          * get first
       When set prop active to 78
       Then wait for exception
       Then [Exception:PropertyNotExists: Property active does not exist. Property active must be a boolean value.] 

Scenario: GET <get-boolean-test-desc> from a NUMBER PROPERTY
      Given the Application
          * get link school
          * get list students
          * get first
          # FIXME: When get prop active after the UpdateTime
       When get prop active
       Then wait for exception
       Then [Exception:PropertyNotExists: Property active does not exist. Property active must be a boolean value.] 



