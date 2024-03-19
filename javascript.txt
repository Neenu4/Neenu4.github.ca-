<script>
    document.getElementById('submitForm').addEventListener('click', function() {
        const formData = {
            name: document.getElementById('name').value,
            email: document.getElementById('email').value,
            gender: document.querySelector('input[name="gender"]:checked') ? document.querySelector('input[name="gender"]:checked').value : '',
            interests: [...document.querySelectorAll('input[name="interests"]:checked')].map(el => el.value),
            message: document.getElementById('message').value,
            experience: document.getElementById('experience').value
        };
        localStorage.setItem('formData', JSON.stringify(formData));
        alert('Your data has been saved.');
    });

    document.getElementById('resetForm').addEventListener('click', function() {
        document.getElementById('contactForm').reset();
    });
</script>
