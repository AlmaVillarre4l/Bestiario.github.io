# Bestiario
![descarga (5)](https://user-images.githubusercontent.com/100175361/155770663-5f3f8f0a-8163-4c73-bafb-1cf72c1ff68c.jpg)
![descarga (4)](https://user-images.githubusercontent.com/100175361/156892880-c6721f57-1672-4eff-8f46-c6b9918ce19c.jpg)
![Simbolos-Edad-Media](https://user-images.githubusercontent.com/100175361/156892891-be51a0b3-5b52-43c0-80a8-2647fda98da5.jpg) ![BESTIARIO](https://user-images.githubusercontent.com/100175361/156892912-5b227a08-4f4c-4e89-9488-d4f925a48b4b.jpg)

### La Edad Media 


*Cursiva* **Negritas** 

### Sobre ángeles y demonios 

### Sobre las bestias

**Comic** 

/*
Add additional fields to the Contact Form.p
*/

We are going to add another field above this one for the subject of the email. Copy and paste this code above the block of code (name field) referenced above.

------------------------------------------------------------------------

<div class="input-box">
    <label for="subject"><?php echo Mage::helper('contacts')->__('Subject') ?> <span class="required">*</span></label><br />
    <input name="subject" id="subject" title="<?php echo Mage::helper('contacts')->__('Subject') ?>" value="" class="required-entry input-text" type="text"/>
</div>


------------------------------------------------------------------------

As far as Magento is concerned, it doesnt care what fields we add to this form. It is written in such a way that it accepts all of the field posted for processing and send that out to the transactional e-mail form that you create. Now, go to System->Transactional E-mails in the Magento Admin section. Click "Add New Template" and from the "Template" dropdown box select "Contact Form" then "Load Template". Under template content you will see:

------------------------------------------------------------------------

Name: {{var data.name}}
E-mail: {{var data.email}}
Telephone: {{var data.telephone}}

Comment: {{var data.comment}}

------------------------------------------------------------------------

Add your new field before Name: {{var data.name}} so that now it should looks like this:

Subject: {{var data.subject}}
Name: {{var data.name}}
E-mail: {{var data.email}}
Telephone: {{var data.telephone}}

Comment: {{var data.comment}}


------------------------------------------------------------------------



Enter a new name under "Template Name" to save your new Template and click on "Save Template". Now we need to tell Magento to use this new template for the Contact form. Go to System->Configuration and select "Contacts". Under "Email Options", select your new template under the "Email Template" dropdown box. Click on "Save Config". 
