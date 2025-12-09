# Car Rental System - Complete Team Distribution Guide

**Project:** Final Project Milestone 1 - Group 9  
**Team Size:** 5 Members  
**Total Design Patterns:** 15  
**Distribution:** 3 Design Patterns per person

---

# 📋 Table of Contents

1. [Overview](#overview)
2. [Person 1: Adapter, Bridge, Builder](#person-1)
3. [Person 2: Command, Composite, Decorator](#person-2)
4. [Person 3: Facade, Factory, Flyweight](#person-3)
5. [Person 4: Observer, Prototype, Singleton](#person-4)
6. [Person 5: State, Strategy, Template](#person-5)
7. [Shared Files](#shared-files)
8. [Commit Checklist](#commit-checklist)

---

# Overview

## Design Pattern Distribution

| Person | Design Patterns | Count |
|--------|----------------|-------|
| Person 1 | Adapter, Bridge, Builder | 3 |
| Person 2 | Command, Composite, Decorator | 3 |
| Person 3 | Facade, Factory, Flyweight | 3 |
| Person 4 | Observer, Prototype, Singleton | 3 |
| Person 5 | State, Strategy, Template | 3 |
| **Total** | | **15** |

## Distribution Strategy
- Each person is assigned 3 Design Patterns
- Related files (controllers, services, entities, frontend) are grouped with their patterns
- Modified files (M) are assigned to the person whose pattern they relate to
- New files (??) are assigned based on functionality

---

# Raveena: Adapter, Bridge, Builder Patterns {#person-1}

## Your Design Patterns (3):
1. ✅ **Adapter Pattern** - Payment gateway integration
2. ✅ **Bridge Pattern** - Rental pricing abstraction
3. ✅ **Builder Pattern** - Car and Brand construction

## Files to Commit:

### New Files (Untracked):
```
src/main/java/edu/neu/csye7374/adapter/PaymentGatewayAdapter.java
src/main/java/edu/neu/csye7374/adapter/StripePaymentAdapter.java
src/main/java/edu/neu/csye7374/adapter/PayPalPaymentAdapter.java

src/main/java/edu/neu/csye7374/bridge/RentalAbstraction.java
src/main/java/edu/neu/csye7374/bridge/RentalImplementation.java
src/main/java/edu/neu/csye7374/bridge/DailyRental.java
src/main/java/edu/neu/csye7374/bridge/WeeklyRental.java
src/main/java/edu/neu/csye7374/bridge/StandardRentalImplementation.java
src/main/java/edu/neu/csye7374/bridge/PremiumRentalImplementation.java
```

### Modified Files:
```
src/main/java/edu/neu/csye7374/builder/CarBuilder.java
src/main/java/edu/neu/csye7374/dto/PaymentRequest.java
src/main/java/edu/neu/csye7374/dto/PaymentResponse.java
```

## Git Commands:

```bash
# Add your files
git add src/main/java/edu/neu/csye7374/adapter/
git add src/main/java/edu/neu/csye7374/bridge/
git add src/main/java/edu/neu/csye7374/builder/CarBuilder.java
git add src/main/java/edu/neu/csye7374/dto/PaymentRequest.java
git add src/main/java/edu/neu/csye7374/dto/PaymentResponse.java

# Commit
git commit -m "feat: Implement Adapter, Bridge, and Builder Design Patterns

- Added PaymentGatewayAdapter for Stripe and PayPal integration (Adapter Pattern)
- Implemented Bridge pattern for rental pricing (Daily/Weekly with Standard/Premium)
- Enhanced CarBuilder with fluent API (Builder Pattern)
- Updated PaymentService to use Adapter pattern
- Added print statements for all pattern activations"
```

## Testing Checklist:
- [ ] Test payment processing with Stripe adapter
- [ ] Test payment processing with PayPal adapter
- [ ] Test daily rental with standard pricing
- [ ] Test daily rental with premium pricing
- [ ] Test weekly rental with discount
- [ ] Verify CarBuilder creates cars correctly
- [ ] Verify BrandBuilder creates brands correctly
- [ ] Check console for pattern activation print statements

---

# Puja: Facade, Factory, Flyweight Patterns {#person-3}

## Your Design Patterns (3):
1. ✅ **Facade Pattern** - Service interaction simplification
2. ✅ **Factory Pattern** - Object creation
3. ✅ **Flyweight Pattern** - Car specification caching

## Files to Commit:

### New Files (Untracked):
```
src/main/java/edu/neu/csye7374/facade/ManagementFacade.java
src/main/java/edu/neu/csye7374/factory/ApiResponseFactory.java
src/main/java/edu/neu/csye7374/flyweight/CarSpecification.java
src/main/java/edu/neu/csye7374/flyweight/CarSpecificationFactory.java

src/main/java/edu/neu/csye7374/service/CarAvailabilityService.java
src/main/java/edu/neu/csye7374/service/BookingStatisticsService.java
src/main/java/edu/neu/csye7374/controller/admin/AdminDashboardController.java
src/main/java/edu/neu/csye7374/controller/ReportController.java
src/main/java/edu/neu/csye7374/dto/CarDTO.java
src/main/java/edu/neu/csye7374/dto/CarWithBookingDetailsDTO.java
src/main/java/edu/neu/csye7374/dto/CarAvailabilitySummaryDTO.java

src/main/java/edu/neu/csye7374/frontend/src/pages/CarAvailabilityDashboard.jsx
```

### Modified Files:
```
src/main/java/edu/neu/csye7374/facade/RentalFacade.java
src/main/java/edu/neu/csye7374/entity/Car.java
src/main/java/edu/neu/csye7374/service/CarService.java
src/main/java/edu/neu/csye7374/frontend/src/pages/CarList.jsx
src/main/java/edu/neu/csye7374/frontend/src/pages/CarSearch.jsx
src/main/java/edu/neu/csye7374/frontend/src/pages/CarForm.jsx
```

## Git Commands:

```bash
# Add your files
git add src/main/java/edu/neu/csye7374/facade/
git add src/main/java/edu/neu/csye7374/factory/
git add src/main/java/edu/neu/csye7374/flyweight/
git add src/main/java/edu/neu/csye7374/service/CarAvailabilityService.java
git add src/main/java/edu/neu/csye7374/service/BookingStatisticsService.java
git add src/main/java/edu/neu/csye7374/service/CarService.java
git add src/main/java/edu/neu/csye7374/controller/admin/AdminDashboardController.java
git add src/main/java/edu/neu/csye7374/controller/ReportController.java
git add src/main/java/edu/neu/csye7374/controller/CarController.java
git add src/main/java/edu/neu/csye7374/entity/Car.java
git add src/main/java/edu/neu/csye7374/dto/CarDTO.java
git add src/main/java/edu/neu/csye7374/dto/CarWithBookingDetailsDTO.java
git add src/main/java/edu/neu/csye7374/dto/CarAvailabilitySummaryDTO.java
git add src/main/java/edu/neu/csye7374/frontend/src/pages/CarList.jsx
git add src/main/java/edu/neu/csye7374/frontend/src/pages/CarSearch.jsx
git add src/main/java/edu/neu/csye7374/frontend/src/pages/CarForm.jsx
git add src/main/java/edu/neu/csye7374/frontend/src/pages/CarAvailabilityDashboard.jsx

# Commit
git commit -m "feat: Implement Facade, Factory, and Flyweight Design Patterns

- Added RentalFacade and ManagementFacade to simplify service interactions (Facade Pattern)
- Implemented ApiResponseFactory for standardized API responses (Factory Pattern)
- Added Flyweight pattern for car specifications caching (Flyweight Pattern)
- Updated CarService and controllers to use Facade pattern
- Enhanced car listing, search, and availability features
- Added print statements for all pattern activations"
```

## Testing Checklist:
- [ ] Test car search through RentalFacade
- [ ] Test car retrieval through RentalFacade
- [ ] Test booking management through ManagementFacade
- [ ] Verify ApiResponseFactory creates consistent responses
- [ ] Test car specification caching (request same spec twice)
- [ ] Test car listing functionality
- [ ] Test car search functionality
- [ ] Test car availability checking
- [ ] Check console for pattern activation print statements

---

# Chethan: Observer, Prototype, Singleton Patterns {#person-4}

## Your Design Patterns (3):
1. ✅ **Observer Pattern** - Customer notifications
2. ✅ **Prototype Pattern** - Car cloning
3. ✅ **Singleton Pattern** - Application logging

## Files to Commit:

### New Files (Untracked):
```
src/main/java/edu/neu/csye7374/observer/CustomerObserver.java
src/main/java/edu/neu/csye7374/observer/EmailNotificationObserver.java
src/main/java/edu/neu/csye7374/observer/SmsNotificationObserver.java

src/main/java/edu/neu/csye7374/prototype/CarPrototype.java
src/main/java/edu/neu/csye7374/prototype/ConcreteCarPrototype.java

src/main/java/edu/neu/csye7374/singleton/ApplicationLogger.java

src/main/java/edu/neu/csye7374/service/DesignPatternDemoService.java
src/main/java/edu/neu/csye7374/controller/CustomerController.java
src/main/java/edu/neu/csye7374/entity/Customer.java
src/main/java/edu/neu/csye7374/repository/CustomerRepository.java

src/main/java/edu/neu/csye7374/frontend/src/pages/Profile.jsx
```

### Modified Files:
```
src/main/java/edu/neu/csye7374/frontend/src/pages/CustomerList.jsx
```

## Git Commands:

```bash
# Add your files
git add src/main/java/edu/neu/csye7374/observer/
git add src/main/java/edu/neu/csye7374/prototype/
git add src/main/java/edu/neu/csye7374/singleton/
git add src/main/java/edu/neu/csye7374/service/DesignPatternDemoService.java
git add src/main/java/edu/neu/csye7374/service/CustomerService.java
git add src/main/java/edu/neu/csye7374/controller/CustomerController.java
git add src/main/java/edu/neu/csye7374/entity/Customer.java
git add src/main/java/edu/neu/csye7374/repository/CustomerRepository.java
git add src/main/java/edu/neu/csye7374/frontend/src/pages/CustomerList.jsx
git add src/main/java/edu/neu/csye7374/frontend/src/pages/Profile.jsx

# Commit
git commit -m "feat: Implement Observer, Prototype, and Singleton Design Patterns

- Added Observer pattern for customer notifications (Email, SMS) (Observer Pattern)
- Implemented Prototype pattern for car cloning (Prototype Pattern)
- Added Singleton ApplicationLogger for centralized logging (Singleton Pattern)
- Updated CustomerService to use Observer pattern for notifications
- Added DesignPatternDemoService to demonstrate all patterns
- Enhanced customer management UI
- Added print statements for all pattern activations"
```

## Testing Checklist:
- [ ] Test customer creation triggers email notification (Observer)
- [ ] Test customer creation triggers SMS notification (Observer)
- [ ] Test customer update triggers notifications (Observer)
- [ ] Test car cloning (Prototype)
- [ ] Verify cloned car has same attributes but new ID
- [ ] Test ApplicationLogger singleton (getInstance multiple times)
- [ ] Verify only one logger instance exists
- [ ] Test logger methods (info, error, warn)
- [ ] Check console for pattern activation print statements

---

# Shared Files {#shared-files}

## Configuration Files (Coordinate with team):
```
pom.xml (M) - Dependency updates
src/main/resources/data.sql (M) - Data initialization
src/main/java/edu/neu/csye7374/config/DataInitializer.java
src/main/java/edu/neu/csye7374/config/JacksonConfig.java (new)
src/main/java/edu/neu/csye7374/config/RoleBasedAccessInterceptor.java (new)
```

## Core Application Files:
```
src/main/java/edu/neu/csye7374/CarRentalApplication.java
src/main/java/edu/neu/csye7374/CarRentalFeature.java (new)
src/main/java/edu/neu/csye7374/Driver.java
```

## Additional Services (May need coordination):
```
src/main/java/edu/neu/csye7374/service/admin/AdminFleetManagementService.java (new)
src/main/java/edu/neu/csye7374/service/user/UserBookingService.java (new)
src/main/java/edu/neu/csye7374/service/user/UserCarSearchService.java (new)
src/main/java/edu/neu/csye7374/service/user/UserProfileService.java (new)
```

## Additional Controllers:
```
src/main/java/edu/neu/csye7374/controller/StaticController.java (new)
src/main/java/edu/neu/csye7374/controller/user/UserCarSearchController.java (new)
src/main/java/edu/neu/csye7374/controller/user/UserPaymentController.java (new)
src/main/java/edu/neu/csye7374/controller/user/UserProfileController.java (new)
```

## Frontend Utilities:
```
src/main/java/edu/neu/csye7374/frontend/src/services/managementApi.js (new)
src/main/java/edu/neu/csye7374/frontend/src/utils/ (new)
```

**Note:** These shared files should be coordinated among team members to avoid conflicts.

---

# Commit Checklist {#commit-checklist}

## Before Committing, Each Person Should:

### Pre-Commit:
- [ ] Pull latest changes from repository
- [ ] Resolve any merge conflicts
- [ ] Test all assigned design patterns
- [ ] Verify all related files compile without errors
- [ ] Check for print statements in design pattern files
- [ ] Verify frontend files (if assigned) work correctly
- [ ] Run the application and test functionality

### During Commit:
- [ ] Use the provided git commands from your assignment
- [ ] Use the provided commit message (or customize it)
- [ ] Verify only your assigned files are being committed
- [ ] Double-check file paths are correct

### After Commit:
- [ ] Push to repository
- [ ] Verify commit appears in repository
- [ ] Coordinate with team if there are conflicts
- [ ] Update this document with your name (optional)

## Commit Message Format:
```
feat: Implement [Pattern1], [Pattern2], and [Pattern3] Design Patterns

- Brief description of Pattern 1
- Brief description of Pattern 2
- Brief description of Pattern 3
- Additional features or updates
- Added print statements for all pattern activations
```

---

# Design Pattern Summary

## All 15 Design Patterns:

1. **Adapter** - Payment gateway integration (Person 1)
2. **Bridge** - Rental pricing abstraction (Person 1)
3. **Builder** - Object construction (Person 1)
4. **Command** - Operation encapsulation (Person 2)
5. **Composite** - Tree structure for bookings (Person 2)
6. **Decorator** - Dynamic feature addition (Person 2)
7. **Facade** - Service simplification (Person 3)
8. **Factory** - Object creation (Person 3)
9. **Flyweight** - Memory optimization (Person 3)
10. **Observer** - Event notification (Person 4)
11. **Prototype** - Object cloning (Person 4)
12. **Singleton** - Single instance (Person 4)
13. **State** - State management (Person 5)
14. **Strategy** - Algorithm selection (Person 5)
15. **Template** - Algorithm skeleton (Person 5)

---

# Important Notes

1. **No Overlap**: Each file is assigned to only one person
2. **Pattern Ownership**: Each person owns 3 design patterns completely
3. **Related Files**: Services, controllers, and entities are grouped with their patterns
4. **Frontend Files**: Distributed based on functionality
5. **Modified Files**: Assigned to person whose pattern they relate to
6. **Print Statements**: All design patterns must have print statements showing activation
7. **Testing**: Each person should test their patterns before committing
8. **Coordination**: Communicate with team for shared files

---

# Quick Reference

## Person 1 Quick Commands:
```bash
git add src/main/java/edu/neu/csye7374/adapter/ src/main/java/edu/neu/csye7374/bridge/ src/main/java/edu/neu/csye7374/builder/CarBuilder.java src/main/java/edu/neu/csye7374/dto/PaymentRequest.java src/main/java/edu/neu/csye7374/dto/PaymentResponse.java
```

## Person 2 Quick Commands:
```bash
git add src/main/java/edu/neu/csye7374/command/ src/main/java/edu/neu/csye7374/composite/ src/main/java/edu/neu/csye7374/decorator/ src/main/java/edu/neu/csye7374/controller/BookingController.java src/main/java/edu/neu/csye7374/controller/user/UserBookingController.java src/main/java/edu/neu/csye7374/service/BookingService.java src/main/java/edu/neu/csye7374/entity/Booking.java
```

## Person 3 Quick Commands:
```bash
git add src/main/java/edu/neu/csye7374/facade/ src/main/java/edu/neu/csye7374/factory/ src/main/java/edu/neu/csye7374/flyweight/ src/main/java/edu/neu/csye7374/service/CarService.java src/main/java/edu/neu/csye7374/controller/CarController.java
```

## Person 4 Quick Commands:
```bash
git add src/main/java/edu/neu/csye7374/observer/ src/main/java/edu/neu/csye7374/prototype/ src/main/java/edu/neu/csye7374/singleton/ src/main/java/edu/neu/csye7374/service/CustomerService.java src/main/java/edu/neu/csye7374/controller/CustomerController.java
```

## Person 5 Quick Commands:
```bash
git add src/main/java/edu/neu/csye7374/state/ src/main/java/edu/neu/csye7374/strategy/ src/main/java/edu/neu/csye7374/template/ src/main/java/edu/neu/csye7374/service/AuthService.java src/main/java/edu/neu/csye7374/controller/AuthController.java src/main/java/edu/neu/csye7374/config/JwtAuthenticationFilter.java
```

---

**End of Document**

*Last Updated: [Date]*  
*Team: Group 9*  
*Project: Car Rental System - Final Project Milestone 1*

