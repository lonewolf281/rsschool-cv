# Aliaksandr Zdanovich

## Contacts
* **Telegram:** @lonewolf281
* **e-mail:** lonewolf0508@gmail.com
* **GitHub:** @lonewolf281
* **Skype:** lonewolf2811

## Skills
* C#
* SQL 
* HTML, CSS
* Git 
* SkethUp, Fusion 360, Blender
* Photoshop, Illustrator

## Education
* ** 2008-2013 Yanka Kupala State University of Grodno(Engineer-Programmer)**

## Work experience
* ** 2013-2017 LLC "Beldrev", Engineer-Programmer, ASP.Net
* ** 2017-2021 JSC "Grodno Azot", Engineer-Programmer, Oracle Sql, PL\SQL

## English
* **A2 (Pre-intermediate)** in accordance with EPAM Training test results

## Code examples

Javascript

```javascript
async function uploadFile(file) {
    if (file.type !== 'image/jpeg') {
        alert('Select image!')
    } else {
        const url = 'https://api.cloudinary.com/v1_1/hajyom5vd/image/upload'
        const formData = new FormData()
        formData.append('file', file)
        formData.append('upload_preset', 'chatitransition')

        const res = await fetch(
            'https://api.cloudinary.com/v1_1/hajyom5vd/image/upload',
            {
                method: 'POST',
                body: formData
            }
        )
        const result = await res.json()

        const userId = sessionStorage.getItem('userId')
        const name = sessionStorage.getItem('name')

        socket.emit('send message', userId, name, result.secure_url)
    }
}
```