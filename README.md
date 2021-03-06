# VUECLI LUMEN template

### Folder structure: <br>
<pre ><code>
    +-- /htdocs
        +-- /public_html
        +-- /backend
        +-- /frontend
</code></pre>

### Move to backend folder:<br>
<strong>composer install</strong>
<br><strong>Do not forget about .env file configuration</strong>

### Move to frontend folder:<br>
<strong>npm install</strong>

### Last steps:<br>
<br><strong> * rm -r public_html</strong>
<br><strong> * ln -s frontend/dist public_html</strong>
<br><strong> * Then we navigate to cd /htdocs/frontend/dist</strong>
<br><strong> * ln -s ../../backend/public app</strong>
<br><strong> * Here you go, now we should configure .htaccess (located in htdocs/frontend/dist) in order to proceed.</strong>

<pre>
    <code>
        RewriteEngine On
        RewriteCond %{REQUEST_URI} ^/api
        RewriteCond %{REQUEST_FILENAME} !-d
        RewriteCond %{REQUEST_FILENAME} !-f
        RewriteRule ^ app/index.php [L]

        RewriteCond %{REQUEST_FILENAME} !-d
        RewriteCond %{REQUEST_FILENAME} !-f
        RewriteRule ^ index.html [L]
    </code>
</pre>

<br><strong> If you have any questions related, just hit me up. Email: azarguliyev@outlook.com</strong>