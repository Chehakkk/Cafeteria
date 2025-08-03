# Cafeteria - Pure Veg Cafe & Restaurant Explorer

A Django-based cafe discovery platform focused on Jain and pure vegetarian restaurants. Discover, explore, and reserve your perfect dining experience based on your mood and cravings.

## 🌱 Features

- **Pure Veg Focus**: Exclusively Jain and pure vegetarian restaurants and cafes
- **Mood-Based Discovery**: Find dining spots based on your current cravings and mood
- **Seat Reservation**: Book tables with special offers and discounts
- **Event Discovery**: Explore upcoming events, late-night parties, and special occasions
- **Dessert Places**: Dedicated section for favorite dessert spots and sweet treats
- **Secure Payments**: Razorpay integration for seamless payment processing
- **Email Confirmation**: Automatic booking confirmations and notifications

## 📁 Project Structure

```
projet/
├── projet/                      # Main project directory
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── cafeteria/                   # Main cafeteria app
│   ├── models.py               # Restaurant, Booking, Event models
│   ├── views.py                # Search, booking, event views
│   ├── urls.py                 # URL patterns
│   ├── forms.py                # Reservation and search forms
│   └── templates/              # HTML templates
├── static/                      # CSS, JS, images
├── media/                       # Restaurant images
├── requirements.txt
└── manage.py
```

## 🛠️ Technology Stack

- **Backend**: Django 4.x, Python 3.x
- **Database**: SQLite/PostgreSQL/MySQL
- **Payment**: Razorpay integration
- **Email**: Django SMTP backend
- **Frontend**: HTML5, CSS3, JavaScript, Bootstrap
- **Authentication**: Django Auth system

## ⚙️ Quick Setup

1. **Clone and setup**
   ```bash
   git clone <repository-url>
   cd projet
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

2. **Environment configuration**
   Create `.env` file:
   ```env
   SECRET_KEY=your_secret_key
   DEBUG=True
   DATABASE_URL=your_database_url
   RAZORPAY_KEY_ID=your_razorpay_key_id
   RAZORPAY_KEY_SECRET=your_razorpay_secret
   EMAIL_HOST_USER=your_email@gmail.com
   EMAIL_HOST_PASSWORD=your_app_password
   ```

3. **Database setup**
   ```bash
   python manage.py makemigrations cafeteria
   python manage.py migrate
   python manage.py createsuperuser
   python manage.py runserver
   ```

Visit `http://127.0.0.1:8000` to start exploring cafes!

## 🏗️ App Architecture

### Core Models
- **Restaurant**: Pure veg/Jain restaurants with cuisine types, location, ratings
- **Booking**: Table reservations with date, time, guest count, special offers
- **Event**: Upcoming events, late-night parties, special occasions
- **Category**: Mood-based categories (romantic, family, party, dessert spots)
- **Offer**: Special discounts and promotional deals

### Key Functionality

**Cafe Discovery:**
- Browse by mood (romantic dinner, family outing, quick bite)
- Filter by cuisine type, location, ratings, price range
- Special focus on Jain and pure vegetarian options
- Featured dessert places and sweet spots

**Reservation System:**
- Real-time table availability checking
- Seat booking with guest count and special requests
- Offer application during booking process
- Razorpay payment integration for advance booking

**Event Management:**
- Upcoming events and late-night parties listing
- Event-based restaurant recommendations
- Special event booking and ticket purchasing
- Notification system for favorite events

## 💳 Payment Integration

```python
# Razorpay Configuration
RAZORPAY_KEY_ID = 'your_key_id'
RAZORPAY_KEY_SECRET = 'your_key_secret'

# Payment flow: Booking → Payment → Confirmation Email
```

## 📧 Email System

- Booking confirmation emails
- Event notifications
- Offer alerts and promotional updates
- Reminder emails for upcoming reservations

## 🎯 Core Features

### Mood-Based Exploration
- **Romantic**: Cozy cafes for couples
- **Family**: Kid-friendly restaurants
- **Party**: Late-night spots and party venues
- **Quick Bite**: Fast service cafes
- **Dessert Lover**: Sweet shops and dessert cafes

### Pure Veg Focus
- Strict vegetarian and Jain food options
- No onion, no garlic filters for Jain users
- Certified pure veg restaurant verification
- Special Jain festival menus and events

### Reservation Benefits
- Exclusive offers for app users
- Table booking without waiting
- Special occasion booking (birthdays, anniversaries)
- Group booking discounts

## 📱 Usage

**For Food Lovers:**
1. Browse restaurants by mood and cuisine preference
2. Check upcoming events and late-night parties
3. Reserve tables with special offers
4. Make secure payments through Razorpay
5. Receive email confirmations and reminders

**For Restaurant Owners:**
1. List pure veg/Jain restaurants on platform
2. Manage table availability and bookings
3. Create events and promotional offers
4. Track reservations and customer feedback

## 🔒 Security & Validation

- Secure Razorpay payment processing
- CSRF protection for all forms
- Email verification for bookings
- Input validation and sanitization
- Restaurant verification system

## 🧪 Testing

```bash
python manage.py test cafeteria           # Run app tests
python manage.py test cafeteria.tests.test_booking  # Test booking system
```

## 🚀 Deployment

**Production Checklist:**
- Configure production database
- Set up Razorpay production keys
- Configure email SMTP settings
- Set `DEBUG = False`
- Collect static files
- Set up domain and SSL

## 📈 Future Enhancements

- Mobile app development
- AI-based mood detection
- Social sharing features
- Loyalty program for frequent diners
- Integration with food delivery services
- Advanced event management system

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/NewFeature`)
3. Commit changes (`git commit -m 'Add NewFeature'`)
4. Push to branch and create Pull Request

## 📄 License

MIT License - see LICENSE file for details.

---

**Version**: 1.0.0 | **Focus**: Pure Veg & Jain Dining | **Payment**: Razorpay Integrated
