We derive the steady state function distribution from Osipkov-Merrit anisotropic model. ( Jpp_NoteBook_V2.ipynb file , will be Uploaded soon.. )

taking : 


![FQ](https://github.com/user-attachments/assets/4e04a156-0631-4ca0-b3c2-a9e2a5b6207c)


we can find :

![image](https://github.com/user-attachments/assets/ad11ffe5-41da-47e2-811a-df6b93c69920)


We can truncate the distribution to keep only bounded particles : 

![image](https://github.com/user-attachments/assets/011e87fc-e501-4ebe-b739-970dd25f4917)

after some calculations with "u,v" space coordinate tricks we can find :

![image](https://github.com/user-attachments/assets/26d47def-189a-4581-8e3c-02683c024c2c)

Taking this new expression for the density distribution of the the galaxy , and making a self consistency solver with the "Backwarded" negative fluids 
we can find steady state solution of both fluids at same time , producing stable steady states :

![image](https://github.com/user-attachments/assets/81fafaae-dfd8-43b3-8acc-f7a583b1daef)


and produce spiral galaxy when adding some rotation to the steady state init : 

![image](https://github.com/user-attachments/assets/e6cf28e7-cdab-482f-879c-02d158ad4645)
