1. **Mount the image:**

2. **Navigate to the source directory:**
   ```bash
   cd /usr/local/src
   ```

3. **Clone the repository:**
   ```bash
   git clone https://github.com/shinsakukataoka/arm-memcached.git
   ```

4. **Navigate to the memcached directory:**
   ```bash
   cd /usr/local/src/arm-memcached/memcached
   ```

5. **Run memcached:**
   ```bash
   ./memcached -d -t 2 -m 2040 -n 550 -u nobody
   ```

6. **Navigate to the load tester directory:**
   ```bash
   cd ../memcached-loadtester
   ```

7. **Make the entrypoint script executable:**
   ```bash
   chmod +x entrypoint.sh
   ```

8. **Run the entrypoint script:**
   ```bash
   ./entrypoint.sh --m="W" --S=28 --D=10240 --w=8 --T=2
   ```

