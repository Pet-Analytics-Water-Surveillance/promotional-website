# Google OAuth Approval Guide for Team P.A.W.S Smart Pet Bowl

## 📋 Overview

This guide explains the website updates made to support Google OAuth approval for the PAWS Hydration Monitor mobile application and provides instructions for submitting your app for Google verification.

---

## ✅ Website Updates Summary

### 1. **Homepage (index.html) - Complete System Description**

The homepage now comprehensively describes all three components of your project:

#### **Mobile Application Section**
- Cross-platform iOS & Android app (React Native + Expo)
- Google Sign-In authentication
- Real-time hydration tracking
- Bluetooth device pairing
- Push notifications
- Cloud synchronization via Supabase

#### **Smart Bowl Hardware Section**
- ESP32-S3 microcontroller
- Grove AI Vision V2 camera (YOLOv5)
- RD-03 24GHz radar sensor
- Ultrasonic water level sensor
- Custom PCB design
- WiFi + Bluetooth connectivity

#### **Firmware & AI Section**
- YOLOv5 pet detection
- Feature matching for identification
- Real-time sensor processing
- BLE provisioning system
- Cloud synchronization
- FreeRTOS multi-tasking

### 2. **New Sections Added**

#### **System Overview Section**
- Three detailed cards explaining Mobile App, Hardware, and Firmware
- Technology stack for each component
- Feature lists for transparency

#### **How It Works Section**
- 5-step workflow showing complete system operation
- Motion detection → AI recognition → Water measurement → Cloud sync → Mobile app update

#### **Technology Stack Section**
- Comprehensive list of all technologies used
- Organized by category (Mobile, Hardware, Firmware, Backend)
- Shows Google OAuth 2.0 integration

#### **Enhanced About Section**
- Clear project scope description
- Team composition and expertise
- Authentication & Privacy subsection specifically mentioning Google Sign-In
- Links to Privacy Policy

### 3. **Privacy Policy (privacy.html) - Google OAuth Compliant**

The privacy policy now includes:

✅ **Clear data collection disclosure**
- Email address, name, profile picture from Google
- Pet information and photos
- Device information
- Hydration tracking data

✅ **Google OAuth specific section**
- Explains what data is received from Google
- Links to Google's privacy policy
- Clear purpose statement

✅ **Data usage transparency**
- How data is used
- Who data is shared with
- Retention policies

✅ **User rights**
- Right to access data
- Right to delete data
- Right to data portability
- CCPA and GDPR compliance

✅ **Third-party services disclosure**
- Supabase backend
- Google OAuth
- Expo services

✅ **Academic project disclosure**
- Clear statement that this is a student project
- Data usage for academic purposes
- Anonymization commitment

---

## 🔑 Key Requirements for Google OAuth Approval

### 1. **Homepage Requirements** ✅

Your website now includes:
- [x] Clear description of what your application does
- [x] How it uses Google user data (authentication)
- [x] Privacy Policy link in navigation and footer
- [x] Contact information
- [x] Professional appearance
- [x] Responsive design (mobile-friendly)

### 2. **Privacy Policy Requirements** ✅

Your privacy policy now includes:
- [x] What data is collected from Google (name, email, profile picture)
- [x] How the data is used (authentication, user profiles)
- [x] How the data is stored (Supabase backend)
- [x] How users can delete their data
- [x] Third-party services disclosure
- [x] Contact information
- [x] Last updated date

### 3. **Scope Justification**

For Google OAuth verification, you'll need to justify why you need each scope:

**Scopes Used:**
- `openid` - Required for OAuth 2.0 authentication
- `profile` - To get user's name and profile picture for personalized experience
- `email` - To identify users and enable account management

**Justification:**
> "Our IoT pet hydration monitoring system requires user authentication to:
> 1. Create personalized accounts for pet owners
> 2. Associate pets and devices with specific users
> 3. Enable household sharing features where multiple users can monitor the same pets
> 4. Send email notifications about pet hydration alerts
> 5. Provide a seamless cross-platform experience (iOS and Android)"

---

## 📝 Google OAuth Verification Submission Steps

### Step 1: Prepare Your OAuth Consent Screen

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Select your project (or create one)
3. Navigate to **APIs & Services** → **OAuth consent screen**
4. Fill out the form:

**Application Information:**
- **App name:** PAWS Hydration Monitor
- **User support email:** contact@teampaws.app (or your email)
- **App logo:** Upload your logo (assets/logo.png)
- **Application homepage:** https://teampaws.app (or your deployed URL)
- **Application privacy policy:** https://teampaws.app/privacy.html
- **Application terms of service:** (optional, can use privacy.html)

**Developer contact information:**
- Email addresses: Your team email(s)

**Authorized domains:**
- Add your website domain (e.g., teampaws.app)
- Add your Supabase domain if applicable

### Step 2: Configure Scopes

Add the following scopes:
- `openid`
- `https://www.googleapis.com/auth/userinfo.email`
- `https://www.googleapis.com/auth/userinfo.profile`

For each scope, provide justification as mentioned above.

### Step 3: Add Test Users (During Development)

While your app is in testing mode, add test users:
- Your team members' Gmail addresses
- Any beta testers

### Step 4: Submit for Verification

1. Complete all required fields in the OAuth consent screen
2. Click **Submit for Verification**
3. Google will review your application (typically 3-7 days)

**What Google Reviews:**
- Your website and privacy policy
- Scope justifications
- App functionality
- Data handling practices

### Step 5: Prepare Supporting Documentation

Google may request:

1. **Video demonstration** showing:
   - User signing in with Google
   - How user data is displayed in the app
   - Pet management features
   - Device pairing process

2. **Written explanation** of:
   - Why you need each scope
   - How user data is protected
   - Your data retention policy

3. **Screenshots** of:
   - Login screen
   - User profile screen
   - Main app features

---

## 🎥 Video Demo Script (for Google Review)

Create a 2-3 minute video showing:

1. **Introduction (15 seconds)**
   - "This is PAWS Hydration Monitor, an IoT pet hydration tracking system"
   - Show your website homepage

2. **Google Sign-In (30 seconds)**
   - Open mobile app
   - Click "Sign in with Google"
   - Show Google consent screen
   - Successfully sign in

3. **User Data Usage (45 seconds)**
   - Show user profile with Google name and picture
   - Explain: "We use the user's name and email to create their account"
   - Show household feature: "Multiple users can share access to pets"

4. **Core Functionality (60 seconds)**
   - Add a pet with photo
   - Show device pairing via Bluetooth
   - Display hydration tracking data
   - Explain: "The system monitors which pet drinks and how much"

5. **Privacy & Data Management (30 seconds)**
   - Show settings screen
   - Demonstrate account deletion option
   - Show privacy policy link in app

---

## 🚀 Deployment Checklist

Before submitting for Google verification:

### Website Deployment
- [ ] Deploy website to production (Vercel, Netlify, etc.)
- [ ] Ensure HTTPS is enabled
- [ ] Verify all links work
- [ ] Test on mobile devices
- [ ] Confirm privacy policy is accessible

### Mobile App
- [ ] Configure OAuth client IDs for iOS and Android
- [ ] Update redirect URIs in Google Cloud Console
- [ ] Test Google Sign-In on both platforms
- [ ] Ensure error handling works properly

### Documentation
- [ ] Privacy policy is complete and accurate
- [ ] Contact email is monitored
- [ ] Terms of service (if required)
- [ ] Data deletion instructions are clear

---

## 📧 Sample Email Response to Google (if they request more info)

```
Subject: Re: OAuth Verification for PAWS Hydration Monitor

Dear Google OAuth Review Team,

Thank you for reviewing our application. PAWS Hydration Monitor is a Senior Design 
project developed by students at San Diego State University's College of Engineering.

Our application is a complete IoT pet hydration monitoring system consisting of:
1. Mobile app (iOS/Android) - for pet owners to track their pets' water intake
2. Smart hardware device (ESP32-based) - monitors water consumption with AI vision
3. Cloud backend (Supabase) - stores user data and synchronizes across devices

We use Google Sign-In to:
- Authenticate users securely without managing passwords
- Create personalized accounts for pet owners
- Enable household sharing where multiple users monitor the same pets
- Send email notifications about low water levels and hydration alerts

Data we collect from Google:
- Email address (for account identification and notifications)
- Name (for personalized user experience)
- Profile picture (for user profile display)

This data is stored securely in our Supabase backend and is only used for the 
purposes stated in our privacy policy: https://teampaws.app/privacy.html

Users can delete their account and all associated data at any time through the 
app settings.

Please find attached:
- Video demonstration of Google Sign-In flow
- Screenshots of key app features
- Detailed scope justification document

We are committed to protecting user privacy and complying with all Google OAuth 
policies. Please let us know if you need any additional information.

Best regards,
Team P.A.W.S
San Diego State University
contact@teampaws.app
```

---

## 🔍 Common Google OAuth Rejection Reasons & Solutions

### 1. **"Privacy policy doesn't adequately describe data usage"**
**Solution:** ✅ Your updated privacy policy now includes:
- Specific mention of Google OAuth data
- Clear data usage descriptions
- Third-party services disclosure

### 2. **"Website doesn't clearly describe app functionality"**
**Solution:** ✅ Your homepage now includes:
- Detailed system overview section
- How it works workflow
- Complete feature descriptions

### 3. **"Scope justification is unclear"**
**Solution:** Use the justification template above, emphasizing:
- User authentication necessity
- Household sharing features
- Email notifications for pet health

### 4. **"App appears to be in development/testing"**
**Solution:** 
- Deploy a working version
- Add "Academic Project" disclaimer
- Show it's a functional Senior Design project

### 5. **"Cannot verify app functionality"**
**Solution:**
- Provide detailed video demo
- Offer test account credentials
- Include comprehensive screenshots

---

## 📱 Mobile App Configuration

### iOS (app.json / app.config.js)

```json
{
  "expo": {
    "scheme": "pawshydration",
    "ios": {
      "bundleIdentifier": "com.teampaws.hydration",
      "config": {
        "googleSignIn": {
          "reservedClientId": "YOUR_IOS_CLIENT_ID"
        }
      }
    }
  }
}
```

### Android (app.json / app.config.js)

```json
{
  "expo": {
    "android": {
      "package": "com.teampaws.hydration",
      "googleServicesFile": "./google-services.json"
    }
  }
}
```

### Google Cloud Console - Authorized Redirect URIs

Add these redirect URIs:
- `https://auth.expo.io/@your-username/your-app-slug`
- `com.teampaws.hydration:/oauth2redirect/google` (for iOS)
- Your custom scheme if different

---

## 🎯 Success Criteria

Your app is ready for Google OAuth verification when:

✅ Website clearly describes the complete system (mobile app + hardware + firmware)
✅ Privacy policy is comprehensive and Google OAuth compliant
✅ All links work and website is deployed with HTTPS
✅ Mobile app successfully authenticates with Google
✅ You can demonstrate the full user flow
✅ Data deletion process is documented and functional
✅ Contact information is accurate and monitored

---

## 📞 Support & Resources

### Google Resources
- [OAuth 2.0 Policies](https://developers.google.com/identity/protocols/oauth2/policies)
- [OAuth Consent Screen](https://support.google.com/cloud/answer/10311615)
- [Verification FAQ](https://support.google.com/cloud/answer/9110914)

### Your Resources
- Website: https://teampaws.app (update with your actual URL)
- Privacy Policy: https://teampaws.app/privacy.html
- GitHub: https://github.com/Pet-Analytics-Water-Surveillance
- Contact: contact@teampaws.app

### Team P.A.W.S
- Tri Bui (Computer Engineering)
- Abdulmohsen Almunayes (Computer Engineering)
- Ehren Abeto (Electrical Engineering)
- Brandon Lord (Electrical Engineering)
- Zachary Xavier Encarnacion (Electrical Engineering)

---

## 🎓 Academic Project Notes

Since this is a Senior Design project:

1. **Mention it prominently** - Google is generally supportive of educational projects
2. **Be transparent** - Clearly state it's for academic purposes
3. **Show professionalism** - Demonstrate industry-standard practices
4. **Limit scope** - You don't need to request sensitive scopes
5. **Document well** - Good documentation helps approval

**Academic Project Statement for Google:**
> "PAWS Hydration Monitor is a Senior Design capstone project at San Diego State 
> University's College of Engineering (EE/COMPE 491W). This project demonstrates 
> our team's expertise in mobile development, embedded systems, IoT integration, 
> and machine learning. We implement industry-standard security practices and are 
> committed to protecting user privacy in accordance with all applicable laws and 
> Google's OAuth policies."

---

## ✨ Final Checklist Before Submission

- [ ] Website deployed and accessible via HTTPS
- [ ] Privacy policy reviewed and accurate
- [ ] All navigation links work
- [ ] Mobile app builds successfully
- [ ] Google Sign-In works on test devices
- [ ] Video demo recorded (2-3 minutes)
- [ ] Screenshots prepared
- [ ] Scope justifications written
- [ ] Contact email is monitored
- [ ] Team is ready to respond to Google's questions

---

**Good luck with your Google OAuth verification!** 🚀

Your website now meets all the requirements for Google OAuth approval. The comprehensive 
system description, detailed privacy policy, and clear data usage statements should 
satisfy Google's review team.

If you have any questions during the verification process, refer to this guide and 
Google's official documentation.

---

*Last Updated: September 23, 2025*
*Team P.A.W.S - San Diego State University*