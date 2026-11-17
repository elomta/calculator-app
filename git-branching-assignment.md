# Git Branching Assignment

## Prerequisites
- Java development environment
- IntelliJ IDEA installed
- Maven installed
- Git installed and configured
- GitHub account created

---

## Part 1: Initial Setup

### Step 1: Create a New Maven Project
1. Open IntelliJ IDEA
2. Create a new Maven project named `calculator-app`

### Step 2: Create Initial Java Class
Create a file `src/main/java/ge/tbc/testautomation/Calculator.java`:

```java
package ge.tbc.testautomation;

public class Calculator {
    public static void main(String[] args) {
        System.out.println("Calculator App");
        System.out.println("Addition: 5 + 3 = 8");
        System.out.println("Subtraction: 5 - 3 = 2");
    }
}
```

### Step 3: Initialize Git and Push to GitHub
1. Initialize Git in your project directory
2. Create a new repository on GitHub named `calculator-app`
3. Link your local repository to GitHub and push
---

## Part 2: Feature Branch Workflow

### Step 4: Create and Work on a Feature Branch
1. Create a new branch for adding multiplication
2. Check out the new branch
3. Add a multiplication line to the `main` method in `Calculator.java`:
   ```java
   System.out.println("Multiplication: 5 * 3 = 15");
   ```

4. Commit your changes
5. Push the branch to GitHub:

### Step 5: Merge Using Pull Request
1. Go to your GitHub repository
2. Click "Pull requests" → "New pull request"
3. Select `feature/multiplication` as the compare branch
4. Create the pull request with a descriptive title
5. Merge the pull request on GitHub

### Step 6: Update Local Repository
1. Switch back to main branch
2. Pull the latest changes
---

## Part 3: Local Merging Practice

### Step 7: Create and Merge Locally
1. Create a new branch for division:
2. Add a division line to the `main` method in `Calculator.java`:
   ```java
   System.out.println("Division: 6 / 3 = 2");
   ```

3. Commit the changes:
4. Switch back to main and merge
5. Push to GitHub
---

## Part 4: Simulating Conflict Scenario

### Step 8: Create Developer 1's Branch
1. Ensure you're on the latest main
2. Create a branch for Developer 1
3. Modify the `main` method in `Calculator.java` to improve output formatting:
   ```java
   public static void main(String[] args) {
       System.out.println("=== Calculator Results ===");
       System.out.println("Addition: 5 + 3 = 8");
       System.out.println("Subtraction: 5 - 3 = 2");
       System.out.println("Multiplication: 5 * 3 = 15");
       System.out.println("Division: 6 / 3 = 2");
       System.out.println("=========================");
   }
   ```

4. Commit the changes
5. Push the branch

### Step 9: Create Pull Request for Developer 1
1. Go to GitHub and create a pull request for `feature/improve-output-dev1`
2. **DO NOT merge yet** - leave it open

### Step 10: Create Developer 2's Branch
1. Switch back to main (simulating a different developer starting from main):
2. Create a branch for Developer 2:
3. Modify the `main` method differently (same section of code):
   ```java
   public static void main(String[] args) {
       System.out.println("*** Calculator Demo ***");
       System.out.println("Addition: 5 + 3 = 8");
       System.out.println("Subtraction: 5 - 3 = 2");
       System.out.println("Multiplication: 5 * 3 = 15");
       System.out.println("Division: 6 / 3 = 2");
       System.out.println("*** End of Demo ***");
   }
   ```
4. Commit the changes
5. Push the branch

### Step 11: Merge Developer 1's Pull Request
1. Go to GitHub
2. Merge the pull request for `feature/improve-output-dev1`

### Step 12: Attempt to Merge Developer 2's Pull Request
1. Create a pull request for `feature/improve-output-dev2`
2. **Notice**: GitHub will show a merge conflict
3. You now need to resolve this conflict
4. Resolve the conflict and complete the merge

