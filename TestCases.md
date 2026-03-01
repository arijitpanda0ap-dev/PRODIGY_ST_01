# Simple Calculator Application  
## Test Case Document  

**Project Name:** Simple Calculator  
**Module:** Arithmetic Operations  
**Prepared By:** Arijit Panda  
**Environment:** Web/Desktop Application  
**Version:** 1.0  

---

## Assumptions

- Calculator supports addition (+), subtraction (-), multiplication (×), and division (÷)
- Supports integers and decimal numbers
- Supports negative numbers
- Displays appropriate error messages for invalid inputs
- Supports expression evaluation following BODMAS rule

---

# Functional Test Cases

---

## TC_CALC_001 – Addition of Two Positive Integers

**Test Case ID:** TC_CALC_001  
**Test Description:** Verify addition of two positive integers  
**Test Type:** Functional  
**Priority:** High  
**Severity:** Major  

### Preconditions
- Application is launched  
- Calculator is in default state  

### Test Steps
1. Enter `10` in the input field  
2. Click on `+` operator  
3. Enter `5`  
4. Click on `=`  

### Expected Result
- Result displayed should be `15`  
- No error message should appear  

---

## TC_CALC_002 – Subtraction with Negative Numbers

**Test Case ID:** TC_CALC_002  
**Test Description:** Verify subtraction when both inputs are negative  
**Test Type:** Functional  
**Priority:** High  
**Severity:** Major  

### Preconditions
- Calculator is active  

### Test Steps
1. Enter `-10`  
2. Click on `-` operator  
3. Enter `-5`  
4. Click on `=`  

### Expected Result
- Result displayed should be `-5`  

---

## TC_CALC_003 – Multiplication of Decimal Values

**Test Case ID:** TC_CALC_003  
**Test Description:** Verify multiplication of decimal numbers  
**Test Type:** Functional  
**Priority:** High  
**Severity:** Major  

### Preconditions
- Calculator is active  

### Test Steps
1. Enter `2.5`  
2. Click on `×` operator  
3. Enter `4.2`  
4. Click on `=`  

### Expected Result
- Result displayed should be `10.5`  
- Decimal precision should be maintained correctly  

---

## TC_CALC_004 – Division of Two Positive Numbers

**Test Case ID:** TC_CALC_004  
**Test Description:** Verify division operation  
**Test Type:** Functional  
**Priority:** High  
**Severity:** Critical  

### Preconditions
- Calculator is active  

### Test Steps
1. Enter `20`  
2. Click on `/` operator  
3. Enter `4`  
4. Click on `=`  

### Expected Result
- Result displayed should be `5`  
- Application should not display any error  

---

# Negative Test Cases

---

## TC_CALC_005 – Division by Zero

**Test Case ID:** TC_CALC_005  
**Test Description:** Verify system behavior when dividing by zero  
**Test Type:** Negative  
**Priority:** High  
**Severity:** Critical  

### Preconditions
- Calculator is active  

### Test Steps
1. Enter `10`  
2. Click on `/` operator  
3. Enter `0`  
4. Click on `=`  

### Expected Result
- System should display error message:  
  `Error: Division by zero is not allowed`  
- Application should not crash  

---

## TC_CALC_006 – Non-Numeric Input Validation

**Test Case ID:** TC_CALC_006  
**Test Description:** Verify system behavior when non-numeric input is entered  
**Test Type:** Negative  
**Priority:** Medium  
**Severity:** Major  

### Preconditions
- Calculator is active  

### Test Steps
1. Enter `abc`  
2. Click on `+` operator  
3. Enter `5`  
4. Click on `=`  

### Expected Result
- System should display validation message:  
  `Invalid input. Please enter numeric values.`  
- Calculation should not proceed  

---

## TC_CALC_007 – Empty Input Field Validation

**Test Case ID:** TC_CALC_007  
**Test Description:** Verify behavior when input field is left empty  
**Test Type:** Negative  
**Priority:** Medium  
**Severity:** Minor  

### Preconditions
- Calculator is active  

### Test Steps
1. Leave first input field blank  
2. Enter `5`  
3. Click on `+` operator  
4. Click on `=`  

### Expected Result
- System should display message:  
  `Input field cannot be empty`  
- Calculation should not proceed  

---

# Operator Precedence Validation

---

## TC_CALC_008 – BODMAS Rule Verification

**Test Case ID:** TC_CALC_008  
**Test Description:** Verify operator precedence as per BODMAS rule  
**Test Type:** Functional  
**Priority:** High  
**Severity:** Major  

### Preconditions
- Calculator supports full expression input  

### Test Steps
1. Enter expression `2 + 3 × 4`  
2. Click on `=`  

### Expected Result
- Result displayed should be `14`  
- Multiplication should be executed before addition  

---

# Boundary & Edge Case Testing

---

## TC_CALC_009 – Large Number Calculation

**Test Case ID:** TC_CALC_009  
**Test Description:** Verify calculator behavior with very large numbers  
**Test Type:** Boundary  
**Priority:** Medium  
**Severity:** Major  

### Preconditions
- Calculator is active  

### Test Steps
1. Enter `999999999`  
2. Click on `+` operator  
3. Enter `999999999`  
4. Click on `=`  

### Expected Result
- Correct result should be displayed  
- Application should handle large numbers without overflow error  
