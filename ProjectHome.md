mega.co.nz api's for java.
This API needs the JSON, so before using API's please import the json's jar into your project.

1) Import com.mega.mady.api (i.e import MegaAPI.jar)

2) create MegaAPI class object with "username" and "password" as parameters.

3) call login() method on above created object.

4) Enjoy :)

Features supported.

1] Login
3] Find Files
2] downloading
3] list directories & files
4] get download link
5] add contacts
6] get remaining quata left

# How to Login #
```
MegaAPI Ma = new MegaAPI("user@mail.com", "password");
Ma.login();

```

---

# Find Files #
```
 ArrayList<MegaFile> mfa = Ma.find_files("file_name");
 for(int i=0; i < mfa.size();i++)
 System.out.println("Found files with name ico="+mfa.get(i).getName());
```

---


# Get User Info #
```
Ma.get_user()
```

---

# Get All Files #
```
  ArrayList<MegaFile> mfa = Ma.get_files();
  for(int i = 0;i<mfa.size();i++)
  System.out.println("Files ="+mf.get(i).getName());
```

---


# Download file #
```
try {
  Ma.download("https://mega.co.nz/#!-url-of-file", "D:\\My_Folder");
} catch (InvalidAlgorithmParameterException e) {
  e.printStackTrace();
}
```

---

# Get Url of file #
```
Ma.get_url(MegaFile);
```

---


# Add User #
```
Ma.add_user("friends-email-addres");
```

---


# Get Space Information #
```
Ma.get_quota();
```

---



