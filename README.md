# 🗞️ Habercilik.com - Modern News Platform

**Habercilik.com**, Türkiye'nin en modern ve kullanıcı dostu haber platformudur. Node.js, Express.js, MongoDB ve Bootstrap 5 teknolojileri kullanılarak geliştirilmiştir.

## ✨ Özellikler

### 🎯 Temel Özellikler
- **Modern Responsive Tasarım**: Bootstrap 5 ile mobil uyumlu arayüz
- **Dark/Light Tema**: Kullanıcı tercihine göre tema değiştirme
- **Gerçek Zamanlı Haberler**: Anlık haber güncellemeleri
- **Kategori Sistemi**: Renkli ve ikonlu kategori yönetimi
- **Arama ve Filtreleme**: Gelişmiş arama ve filtreleme seçenekleri
- **Yorum Sistemi**: Haberler için interaktif yorum sistemi
- **Beğeni Sistemi**: Haber beğenme/beğenmeme özelliği

### 👤 Kullanıcı Özellikleri
- **Kullanıcı Kayıt/Giriş**: JWT tabanlı güvenli kimlik doğrulama
- **Profil Yönetimi**: Kişisel profil düzenleme
- **Profil Fotoğrafı**: Resim yükleme ve düzenleme
- **Şifre Değiştirme**: Güvenli şifre güncelleme
- **Kullanıcı İstatistikleri**: Haber ve yorum sayıları

### 🔧 Admin Özellikleri
- **Admin Paneli**: Kapsamlı yönetim arayüzü
- **Kategori Yönetimi**: CRUD operasyonları ile kategori yönetimi
- **Haber Yönetimi**: Haber oluşturma, düzenleme, silme
- **Kullanıcı Yönetimi**: Kullanıcı listesi ve yönetimi
- **İstatistikler**: Detaylı platform istatistikleri

### 🎨 Tasarım Özellikleri
- **Modern UI/UX**: Kullanıcı dostu arayüz tasarımı
- **Responsive Design**: Tüm cihazlarda mükemmel görünüm
- **Dark/Light Mode**: Göz yormayan tema seçenekleri
- **Smooth Animations**: Akıcı geçiş animasyonları
- **Color Consistency**: Tutarlı renk paleti

## 🚀 Teknolojiler

### Backend
- **Node.js**: JavaScript runtime environment
- **Express.js**: Web framework
- **TypeScript**: Type-safe JavaScript
- **MongoDB**: NoSQL database
- **Mongoose**: MongoDB object modeling
- **JWT**: JSON Web Token authentication
- **Multer**: File upload handling
- **Express Validator**: Input validation
- **Winston**: Logging system

### Frontend
- **Bootstrap 5**: CSS framework
- **EJS**: Template engine
- **jQuery**: JavaScript library
- **Font Awesome**: Icon library
- **Custom CSS**: Theme system

### Development Tools
- **Nodemon**: Development server
- **ts-node-dev**: TypeScript development
- **Jest**: Testing framework
- **Swagger**: API documentation
- **ESLint**: Code linting

## 📦 Kurulum

### Gereksinimler
- Node.js (v16 veya üzeri)
- MongoDB (v4.4 veya üzeri)
- npm veya yarn

### Adım 1: Projeyi Klonlayın
```bash
git clone https://github.com/yourusername/habercilik.com.git
cd habercilik.com
```

### Adım 2: Bağımlılıkları Yükleyin
```bash
npm install
```

### Adım 3: Ortam Değişkenlerini Ayarlayın
`.env` dosyasını oluşturun:
```env
NODE_ENV=development
PORT=3000
MONGO_URI=mongodb://localhost:27017/habercilik
JWT_SECRET=your_jwt_secret_here
JWT_EXPIRE=7d
```

### Adım 4: Veritabanını Başlatın
MongoDB'yi başlatın:
```bash
# Windows
net start MongoDB

# macOS/Linux
sudo systemctl start mongod
```

### Adım 5: Uygulamayı Çalıştırın
```bash
# Development
npm run dev

# Production
npm start
```

## 🌐 API Endpoints

### Authentication
- `POST /api/auth/register` - Kullanıcı kaydı
- `POST /api/auth/login` - Kullanıcı girişi
- `POST /api/auth/logout` - Kullanıcı çıkışı

### Articles
- `GET /api/articles` - Tüm haberler
- `GET /api/articles/featured` - Öne çıkan haberler
- `GET /api/articles/:id` - Tekil haber
- `POST /api/articles` - Haber oluştur (Admin)
- `PUT /api/articles/:id` - Haber güncelle (Admin)
- `DELETE /api/articles/:id` - Haber sil (Admin)
- `POST /api/articles/:id/like` - Haber beğen
- `POST /api/articles/:id/dislike` - Haber beğenme

### Categories
- `GET /api/categories` - Tüm kategoriler
- `POST /api/categories` - Kategori oluştur (Admin)
- `PUT /api/categories/:id` - Kategori güncelle (Admin)
- `DELETE /api/categories/:id` - Kategori sil (Admin)

### Comments
- `GET /api/comments/article/:articleId` - Haber yorumları
- `POST /api/comments` - Yorum oluştur
- `GET /api/comments/user/:userId` - Kullanıcı yorumları

### Users
- `GET /api/users` - Tüm kullanıcılar (Admin)
- `PUT /api/users/profile` - Profil güncelle
- `PUT /api/users/change-password` - Şifre değiştir
- `POST /api/users/profile-image` - Profil fotoğrafı yükle

## 🎨 Tema Sistemi

### Dark Mode
- Koyu arka plan renkleri
- Açık metin renkleri
- Göz yormayan kontrast oranları
- Gece kullanımı için optimize edilmiş

### Light Mode
- Açık arka plan renkleri
- Koyu metin renkleri
- Gün ışığında okunabilirlik
- Gündüz kullanımı için optimize edilmiş

### Tema Değiştirme
- Navbar'daki tema butonu ile anlık değiştirme
- Kullanıcı tercihi localStorage'da saklanır
- Sayfa yenilemelerinde tema korunur

## 📱 Responsive Design

### Breakpoints
- **Mobile**: < 768px
- **Tablet**: 768px - 992px
- **Desktop**: > 992px

### Özellikler
- Mobil öncelikli tasarım
- Touch-friendly arayüz
- Optimize edilmiş görsel boyutları
- Hızlı yükleme süreleri

## 🔒 Güvenlik

### Authentication
- JWT tabanlı kimlik doğrulama
- Güvenli şifre hashleme (bcrypt)
- Token süre sonu yönetimi
- Oturum yönetimi

### Authorization
- Rol tabanlı erişim kontrolü
- Admin yetkileri
- API endpoint koruması
- Güvenli dosya yükleme

### Data Protection
- Input validation
- SQL injection koruması
- XSS koruması
- CSRF koruması

## 📊 Performans

### Optimizasyonlar
- Görsel sıkıştırma
- Lazy loading
- Caching stratejileri
- Database indexing

### Monitoring
- Winston logging
- Error tracking
- Performance metrics
- User analytics

## 🧪 Test

### Test Komutları
```bash
# Tüm testleri çalıştır
npm test

# Watch mode
npm run test:watch

# Coverage raporu
npm run test:coverage
```

### Test Kapsamı
- Unit testler
- Integration testler
- API endpoint testleri
- Authentication testleri

## 📚 API Dokümantasyonu

Swagger UI ile interaktif API dokümantasyonu:
```
http://localhost:3000/api-docs
```

### Özellikler
- Tüm endpoint'lerin detaylı açıklaması
- Request/Response örnekleri
- Authentication gereksinimleri
- Error kodları ve açıklamaları

## 🚀 Deployment

### Production Build
```bash
npm run build
```

### Environment Variables
```env
NODE_ENV=production
PORT=3000
MONGO_URI=mongodb://your-mongo-uri
JWT_SECRET=your-production-secret
```

### Docker Support
```dockerfile
FROM node:16-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "start"]
```

## 🤝 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Commit yapın (`git commit -m 'Add amazing feature'`)
4. Push yapın (`git push origin feature/amazing-feature`)
5. Pull Request oluşturun

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.

## 👥 Geliştirici

**Furkan Işınak**
- GitHub: [@furkanisnak](https://github.com/furkanisnak)
- LinkedIn: [Furkan Işınak](https://linkedin.com/in/furkanisnak)

## 📞 İletişim

- **Email**: furkan@habercilik.com
- **Website**: https://habercilik.com
- **Issues**: [GitHub Issues](https://github.com/furkanisnak/habercilik.com/issues)

## 🙏 Teşekkürler

- Bootstrap ekibine modern CSS framework için
- MongoDB ekibine güçlü veritabanı için
- Express.js ekibine hızlı web framework için
- Tüm açık kaynak katkıcılarına

---

**Habercilik.com** - Türkiye'nin en modern haber platformu! 🚀