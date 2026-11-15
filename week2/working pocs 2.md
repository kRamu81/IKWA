**1. Form Layout**
I organized the Student form fields into four clear sections: Student Details, Contact Information, Course Information, and Face Recognition Consent. This makes the form clean and easy for staff to fill in.

<img width="1366" height="343" alt="image" src="https://github.com/user-attachments/assets/5dede80e-006a-4fd7-8b62-3d0993d3521f" />

**2. UI Policies**
UI Policies control the fields on the form. They can show, hide, lock, or make fields mandatory, but they don't know what the user types. I created three:
- **Consent Date:** shows the field only when Biometric Consent is ticked.
- **Inactive Student:** locks the consent fields when Active is false, because the student has left the college.
- **Course Information:** makes Programme and Year of Study mandatory when Active is true, because attendance needs to know the student's class and year.


<img width="1366" height="279" alt="image" src="https://github.com/user-attachments/assets/f4f7dfb0-95c6-46ea-8081-9fa49017f095" />


**3. Client Scripts**
Client Scripts run in the browser and react to what the user does. They guide the user before saving. I created two:
- **Validate Student ID:** if staff enter a wrong Student ID, a message pops up right away.
- **Consent Message:** when the consent checkbox changes, a message reminds staff what it means.

  <img width="1366" height="258" alt="image" src="https://github.com/user-attachments/assets/830a58a2-18e1-402b-a564-ce88b2af1cc4" />


**4. Script Include (GlideAjax)**
This checks for duplicate Student IDs. The form asks the server through GlideAjax, and the user is warned immediately if the ID already exists.
```

var StudentFormUtils = Class.create();
StudentFormUtils.prototype = Object.extendsObject(
    global.AbstractAjaxProcessor, {

    idExists: function() {
        var studentId = this.getParameter('sysparm_student_id');
        var sysId = this.getParameter('sysparm_sys_id');

        var gr = new GlideRecord('x_ikwa_campus_at_0_student');
        gr.addQuery('student_id', studentId);

        if (sysId) {
            gr.addQuery('sys_id', '!=', sysId);
        }

        gr.setLimit(1);
        gr.query();

        return gr.hasNext() ? 'true' : 'false';
    },

    type: 'StudentFormUtils'
});
```

**5. Business Rules**
Business Rules run on the server and enforce Student ID, email, and consent validations. They are the final check and cannot be bypassed by imports or APIs, unlike Client Scripts.

Test Server-side Validation : 
 1. if the studentID is ABC123 like but start with S :
    <img width="1366" height="389" alt="image" src="https://github.com/user-attachments/assets/0e59500d-05e8-404b-a3e1-f9f62d1c4a99" />

 2. Duplicate Student ID
    <img width="1366" height="389" alt="image" src="https://github.com/user-attachments/assets/e4adf96d-a7b7-4258-81b0-1ac4a13f11e2" />
    
 3. Student is Active must fill the mandatory details 
   <img width="1366" height="543" alt="image" src="https://github.com/user-attachments/assets/c9d22778-a76f-44cb-b350-ec9ce45d7f86" />

 4. Active student without Year of Study
    <img width="1366" height="416" alt="image" src="https://github.com/user-attachments/assets/8b0a846a-8edb-4964-9888-15b8e9bf7231" />

 5. Invalid email 
    <img width="1366" height="520" alt="image" src="https://github.com/user-attachments/assets/83e8f669-81b7-4dae-85c3-76b24f2557c4" />


