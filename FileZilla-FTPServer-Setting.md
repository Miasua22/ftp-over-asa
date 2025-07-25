### 1. FTPS Server Configuration

- **Passive Mode Port Range**  
  Set: From `50000` To `50009`  
  👉 *Reserves 10 ports so 10 users can connect simultaneously*  
  ![Passive mode Settings](images/Passive-mode-Settings.jpg)

- **Public IP**  
  Set to: *Retrieve public IP automatically*  
  ![Passive mode Settings](images/Passive-mode-Settings.jpg)

- **User Configuration**  
  Add username/password, then set Mount Point  
  👉 *Virtual Path = Folder name shown to client*  
  👉 *Native Path = Actual file system path*  
  ![User Add Settings](images/User-Add-Settings.jpg)

---

### 2. Internal FTP Connection Test

- **Clients:** Use WinSCP / FileZilla  
  Connect to: `127.0.0.1` or local IP  
  👉 *127.0.0.1 = loopback, usable only on server*  
  ![Local Test](images/Internal-IP-test.jpg)

- **Confirm Connection**  
  ![Connection Confirmed](images/External-Access-success.jpg)
