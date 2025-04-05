# SecureFileTrans2.0
This is the new and reorganized version of my SecureFileTrans project.

My previous implementation was a mess — mainly because of poor structure, rushed development, and lack of clear planning. 
I've already set that old repo to private, and I'm now rebuilding everything properly in this one.

I'm currently in the process of follow the Secure Software Development Lifecycle to reorganizing the entire project from the ground up with a cleaner architecture, improved security practices, and better scalability. 

A web-based application for secure, private, and temporary file sharing using end-to-end encryption,role-based access control, and time-limited shareable links.

========================================

Following core ideas and features in this version are based on my previous SecureFileTrans project’s README.

========================================
Feature Breakdown and Security Principles
========================================

1. User Registration and Authentication
   - Secure login with MFA readiness
   - Passwords hashed with bcrypt and salted
   - [Safe Defaults, Least Privilege]

2. File Encryption and Decryption
   - Files are encrypted on the client side
   - Temporary encrypted files stored on server
   - [Defense in Depth, Time-Tested Tools]

3. Access Control
   - Only file owners can access/delete/share
   - Shareable token links with expiration 
   - [Complete Mediation, Least Privilege]

4. Secure File Transfer
   - Assumes HTTPS for all communication
   - No unencrypted file stored server-side
   - [Defense in Depth, Small Trusted Bases]

5. Logs
   - Tracks upload, download, delete actions
   - Supports auditing and user accountability
   - [Evidence Production, User Buy-In]

- Encrypted files are not persistently stored
- Files are streamed temporarily for access/download
- No server or DB holds user file contents post-transfer
- [Minimizing Attack Surface, Reluctant Allocation, Least Privilege]

========================================
Tech Stack
========================================

- **Backend**: FastAPI (Python)
- **Security**: JWT (python-jose), bcrypt (passlib)
- **Transfer**: HTTPS assumed with TLS support
- **Storage**: Temporary file buffer 
- **Logs**: Console based
- **Testing**: TBD
