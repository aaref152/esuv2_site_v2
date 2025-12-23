# GitHub Repository Setup Guide
# Руководство по настройке репозитория GitHub

## English Version

### Step 1: Create a New GitHub Repository

1. Go to [GitHub](https://github.com) and log in to your account
2. Click the **"+"** button in the top right corner and select **"New repository"**
3. Fill in the repository details:
   - **Repository name**: `esuv2_site_v2` (or any name you prefer)
   - **Description**: "Service Platform website with multilingual support (English/Thai)"
   - **Visibility**: Choose "Public" (required for free GitHub Pages)
   - **DO NOT** initialize with README, .gitignore, or license (we already have files)
4. Click **"Create repository"**

### Step 2: Initialize Git and Push Your Code

Open your terminal in the project directory (`/home/aaref/code/esuv2_site_v2`) and run these commands:

```bash
# Initialize git repository (if not already initialized)
git init

# Add all files to git
git add .

# Create your first commit
git commit -m "Initial commit: Multilingual service platform website (EN/TH)"

# Add GitHub repository as remote origin
# Replace YOUR_USERNAME with your GitHub username
git remote add origin https://github.com/YOUR_USERNAME/esuv2_site_v2.git

# Push to GitHub
git branch -M main
git push -u origin main
```

**Note**: Replace `YOUR_USERNAME` with your actual GitHub username in the command above.

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **"Settings"** tab
3. In the left sidebar, click **"Pages"**
4. Under **"Source"**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **"Save"**
6. Wait a few minutes for GitHub to deploy your site
7. Your site will be available at: `https://YOUR_USERNAME.github.io/esuv2_site_v2/`

### Step 4: Configure Custom Domain (Optional)

#### Option A: Using GitHub Pages with Custom Domain

1. **Update CNAME file**:
   ```bash
   # Edit the CNAME file in your project
   echo "yourdomain.com" > CNAME

   # Commit and push
   git add CNAME
   git commit -m "Update CNAME for custom domain"
   git push
   ```

2. **Configure DNS Settings** (at your domain registrar):

   For a root domain (e.g., `servicerplatform.com`):
   ```
   Type: A Record
   Name: @
   Value: 185.199.108.153

   Type: A Record
   Name: @
   Value: 185.199.109.153

   Type: A Record
   Name: @
   Value: 185.199.110.153

   Type: A Record
   Name: @
   Value: 185.199.111.153
   ```

   For a subdomain (e.g., `www.serviceplatform.com`):
   ```
   Type: CNAME
   Name: www
   Value: YOUR_USERNAME.github.io
   ```

3. **Enable HTTPS in GitHub Pages Settings**:
   - Go to repository Settings → Pages
   - Enter your custom domain in the "Custom domain" field
   - Click "Save"
   - Wait for DNS check to complete
   - Enable "Enforce HTTPS" checkbox

#### Option B: Using Different Domain

If you want to use a completely different domain from your original Russian site:

1. Purchase a new domain (e.g., from Namecheap, GoDaddy, Cloudflare, etc.)
2. Follow the DNS configuration steps above
3. Update the CNAME file with your new domain
4. Configure GitHub Pages settings as described

### Step 5: Verify Your Site

1. Visit your GitHub Pages URL or custom domain
2. Test the language switcher:
   - Click **EN** button - site should display in English
   - Click **TH** button - site should display in Thai
3. Verify all links work correctly
4. Check that legal documents open properly

---

## Русская версия

### Шаг 1: Создание нового репозитория на GitHub

1. Перейдите на [GitHub](https://github.com) и войдите в свой аккаунт
2. Нажмите кнопку **"+"** в правом верхнем углу и выберите **"New repository"**
3. Заполните детали репозитория:
   - **Repository name**: `esuv2_site_v2` (или любое другое имя)
   - **Description**: "Платформа услуг с поддержкой нескольких языков (Английский/Тайский)"
   - **Visibility**: Выберите "Public" (необходимо для бесплатного GitHub Pages)
   - **НЕ** инициализируйте с README, .gitignore или лицензией (у нас уже есть файлы)
4. Нажмите **"Create repository"**

### Шаг 2: Инициализация Git и загрузка кода

Откройте терминал в директории проекта (`/home/aaref/code/esuv2_site_v2`) и выполните команды:

```bash
# Инициализировать git репозиторий (если еще не инициализирован)
git init

# Добавить все файлы в git
git add .

# Создать первый коммит
git commit -m "Initial commit: Multilingual service platform website (EN/TH)"

# Добавить GitHub репозиторий как remote origin
# Замените YOUR_USERNAME на ваше имя пользователя GitHub
git remote add origin https://github.com/YOUR_USERNAME/esuv2_site_v2.git

# Отправить на GitHub
git branch -M main
git push -u origin main
```

**Примечание**: Замените `YOUR_USERNAME` на ваше реальное имя пользователя GitHub в команде выше.

### Шаг 3: Включение GitHub Pages

1. Перейдите в ваш репозиторий на GitHub
2. Нажмите на вкладку **"Settings"**
3. В левой боковой панели нажмите **"Pages"**
4. В разделе **"Source"** выберите:
   - Branch: `main`
   - Folder: `/ (root)`
5. Нажмите **"Save"**
6. Подождите несколько минут, пока GitHub развернет ваш сайт
7. Ваш сайт будет доступен по адресу: `https://YOUR_USERNAME.github.io/esuv2_site_v2/`

### Шаг 4: Настройка собственного домена (опционально)

#### Вариант А: Использование GitHub Pages с собственным доменом

1. **Обновите файл CNAME**:
   ```bash
   # Отредактируйте файл CNAME в вашем проекте
   echo "ваш-домен.com" > CNAME

   # Закоммитьте и отправьте
   git add CNAME
   git commit -m "Update CNAME for custom domain"
   git push
   ```

2. **Настройте DNS** (у вашего регистратора доменов):

   Для корневого домена (например, `serviceplatform.com`):
   ```
   Тип: A запись
   Имя: @
   Значение: 185.199.108.153

   Тип: A запись
   Имя: @
   Значение: 185.199.109.153

   Тип: A запись
   Имя: @
   Значение: 185.199.110.153

   Тип: A запись
   Имя: @
   Значение: 185.199.111.153
   ```

   Для поддомена (например, `www.serviceplatform.com`):
   ```
   Тип: CNAME
   Имя: www
   Значение: YOUR_USERNAME.github.io
   ```

3. **Включите HTTPS в настройках GitHub Pages**:
   - Перейдите в Settings → Pages репозитория
   - Введите ваш домен в поле "Custom domain"
   - Нажмите "Save"
   - Дождитесь завершения проверки DNS
   - Включите чекбокс "Enforce HTTPS"

#### Вариант Б: Использование другого домена

Если вы хотите использовать полностью другой домен от вашего оригинального русского сайта:

1. Купите новый домен (например, на Namecheap, GoDaddy, Cloudflare и т.д.)
2. Следуйте шагам настройки DNS выше
3. Обновите файл CNAME с вашим новым доменом
4. Настройте GitHub Pages как описано

### Шаг 5: Проверка вашего сайта

1. Посетите ваш URL GitHub Pages или собственный домен
2. Проверьте переключатель языков:
   - Нажмите кнопку **EN** - сайт должен отобразиться на английском
   - Нажмите кнопку **TH** - сайт должен отобразиться на тайском
3. Убедитесь, что все ссылки работают корректно
4. Проверьте, что юридические документы открываются правильно

---

## Common Issues / Частые проблемы

### Site not loading after enabling GitHub Pages
**Solution**: Wait 5-10 minutes for initial deployment. Clear browser cache.

**Решение**: Подождите 5-10 минут для первоначального развертывания. Очистите кэш браузера.

### Custom domain not working
**Solution**:
1. Verify DNS settings are correct
2. Wait up to 24 hours for DNS propagation
3. Check CNAME file is in repository root

**Решение**:
1. Проверьте, что настройки DNS правильные
2. Подождите до 24 часов для распространения DNS
3. Убедитесь, что файл CNAME находится в корне репозитория

### Language switcher not working
**Solution**:
1. Check browser console for JavaScript errors
2. Ensure `js/translations.js` is loaded correctly
3. Clear browser cache and reload

**Решение**:
1. Проверьте консоль браузера на наличие JavaScript ошибок
2. Убедитесь, что `js/translations.js` загружается правильно
3. Очистите кэш браузера и перезагрузите

---

## Additional Resources / Дополнительные ресурсы

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Configuring a custom domain for GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Git Basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)
