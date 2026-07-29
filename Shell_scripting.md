
## 🔹 Square Brackets `[ ]`
- **Use**: Test conditions (same as `test` command).
- **Example**:  
  ```bash
  if [ -f /etc/passwd ]; then
      echo "File exists"
  fi
  ```
- **DevOps use case**: Checking if config/log files exist before deploying or restarting services.

---

## 🔹 Double Square Brackets `[[ ]]`
- **Use**: Advanced test syntax (Bash/Ksh only). Safer than `[ ]`.
- Supports regex `=~`, logical operators `&& ||`, and no word-splitting issues.
- **Example**:  
  ```bash
  if [[ $USER =~ ^dev.* ]]; then
      echo "Dev user detected"
  fi
  ```

  >[!NOTE]  
  >in if block Use [ ] for portable POSIX scripts (works in sh in -gt like condition)
  >in if block Use[[ ]] for Bash/Ksh scripts (safer, more features in both manner like <= and -le).
  >In if block Use (( )) for arithmetic.


- **Production use case**: Validating usernames, branch names, or environment variables in CI/CD pipelines.

---

## 🔹 Curly Braces `{ }`
- **Use**:  
  1. **Variable expansion** → `${var}` avoids ambiguity.  
  2. **Brace expansion** → Generate strings/sequences.  
- **Examples**:  
  ```bash
  echo "Hello ${USER}!"
  echo file{1..3}.log   # file1.log file2.log file3.log
  ```
- **Production use case**: Creating multiple log files, batch renaming, or looping over ranges in automation scripts.

---

## 🔹 Parentheses `( )`
- **Use**:  
  1. **Subshell** → Commands inside run in a new shell.  
  2. **Arrays** → Define Bash arrays.  
- **Examples**:  
  ```bash
  (cd /tmp && ls)   # runs in subshell, doesn’t affect current dir
  arr=(one two three)
  echo ${arr[1]}    # two
  ```
- **Production use case**:  
  - Running isolated commands without changing current environment.  
  - Managing arrays of servers or configs in deployment scripts.

---

## 🔹 Double Parentheses `(( ))`
- **Use**: Arithmetic evaluation.  
- **Example**:  
  ```bash
  count=0
  ((count++))
  echo $count   # 1
  ```
- **Production use case**: Counters in retry loops, monitoring scripts, or resource checks.

---

## ✅ Interview-style Question Examples
1. **Condition check**: “How would you verify if a log file exists before parsing it?” → `[ -f logfile ]`.  
2. **Regex validation**: “Check if a branch name starts with `feature/`.” → `[[ $branch =~ ^feature/ ]]`.  
3. **Batch file creation**: “Generate 10 numbered config files.” → `touch config{1..10}.yaml`.  
4. **Subshell isolation**: “Run a command in `/tmp` without leaving current directory.” → `(cd /tmp && ls)`.  
5. **Retry logic**: “Increment a counter until a service responds.” → `((count++))`.

---


Here’s a **cheat sheet of 10 real-world DevOps/production interview questions** focused on bracket usage in Linux shell scripting, with short answers:

---

## 🔹 Bracket Interview Questions

1. **File existence check**  
   *Q:* How do you check if `/etc/passwd` exists?  
   *A:* `if [ -f /etc/passwd ]; then echo "exists"; fi`

2. **String pattern match**  
   *Q:* Validate if `$branch` starts with `feature/`.  
   *A:* `if [[ $branch =~ ^feature/ ]]; then echo "valid"; fi`

3. **Multiple file creation**  
   *Q:* Create 10 numbered log files in one command.  
   *A:* `touch log{1..10}.txt`

4. **Variable expansion safety**  
   *Q:* Print `$HOME` followed by `_backup`.  
   *A:* `echo "${HOME}_backup"`

5. **Subshell isolation**  
   *Q:* List files in `/tmp` without leaving current directory.  
   *A:* `(cd /tmp && ls)`

6. **Array usage**  
   *Q:* Store three server names and print the second.  
   *A:*  
   ```bash
   servers=(app1 app2 app3)
   echo ${servers[1]}
   ```

7. **Arithmetic increment**  
   *Q:* Increase a retry counter by 1.  
   *A:* `((retry++))`

8. **Logical AND condition**  
   *Q:* Check if `$user` is `admin` AND `$env` is `prod`.  
   *A:* `if [[ $user == "admin" && $env == "prod" ]]; then echo "ok"; fi`

9. **Brace expansion with ranges**  
   *Q:* Generate filenames `configA`, `configB`, `configC`.  
   *A:* `echo config{A..C}`

10. **Numeric comparison**  
    *Q:* Check if `$count` is greater than 5.  
    *A:* `if (( count > 5 )); then echo "high"; fi`



Here’s a **mini practice test** with 5 timed-style questions on bracket usage in Linux shell scripting, designed like real DevOps interview scenarios. Try answering them quickly as if you’re in an interview:

---

Here’s a **20-question full mock test** on Linux shell scripting bracket usage, styled like real DevOps/production interview scenarios. Each question is practical, concise, and tests logic you’d actually use in CI/CD, monitoring, or support scripts.  

---

## 📝 20-Question Mock Test – Brackets in Shell Scripting

### 🔹 File & Condition Checks
1. Check if `/etc/hosts` exists before appending a new entry.  
2. Verify if `/var/log/app.log` is non-empty.  
3. Ensure `$USER` is not equal to `root`.  
4. Test if `$PORT` is greater than 1024.  
5. Confirm that `$env` is either `dev` or `test`.

---

### 🔹 Regex & String Validation
6. Validate if a branch name starts with `feature/`.  
7. Ensure a filename ends with `.yaml`.  
8. Check if `$email` contains `@company.com`.  
9. Verify if `$version` matches semantic versioning (`X.Y.Z`).  
10. Confirm `$hostname` starts with `prod-`.

---

### 🔹 Brace Expansion
11. Generate 10 numbered log files (`log1.log` … `log10.log`).  
12. Create configs named `configA`, `configB`, `configC`.  
13. Expand `{dev,test,prod}` into environment names.  
14. Produce a sequence of numbers from 5 to 15.  
15. Generate filenames `server1.conf` to `server3.conf`.

---

### 🔹 Parentheses (Subshells & Arrays)
16. Run `ls` inside `/tmp` without leaving current directory.  
17. Store three IPs in an array and print the second.  
18. Execute `(cd /var && ls)` and confirm your current directory remains unchanged.  
19. Use an array to loop over servers `app1`, `app2`, `app3`.  
20. Run two commands in a subshell: change directory and list files.

---

## ✅ Answer Key (Short Syntax)

1. `[ -f /etc/hosts ]`  
2. `[ -s /var/log/app.log ]`  
3. `[ "$USER" != "root" ]`  
4. `(( PORT > 1024 ))`  
5. `[[ $env == "dev" || $env == "test" ]]`  
6. `[[ $branch =~ ^feature/ ]]`  
7. `[[ $file == *.yaml ]]`  
8. `[[ $email == *@company.com ]]`  
9. `[[ $version =~ ^[0-9]+\.[0-9]+\.[0-9]+$ ]]`  
10. `[[ $hostname =~ ^prod- ]]`  
11. `touch log{1..10}.log`  
12. `touch config{A..C}`  
13. `echo {dev,test,prod}`  
14. `echo {5..15}`  
15. `echo server{1..3}.conf`  
16. `(cd /tmp && ls)`  
17. `ips=(10.0.0.1 10.0.0.2 10.0.0.3); echo ${ips[1]}`  
18. `(cd /var && ls); pwd`  
19. `servers=(app1 app2 app3); for s in "${servers[@]}"; do echo $s; done`  
20. `(cd /etc && ls)`  

---


