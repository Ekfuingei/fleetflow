BACKEND STRUCTURE

📂 backend/
│── 📂 config/
│   │── db.js                     # ✅ Database connection setup (MongoDB, PostgreSQL)
│   │── env.js                    # ✅ Loads environment variables (dotenv package)
│   │── jwtConfig.js              # ✅ Configures JWT authentication settings
│   │── cloudConfig.js            # ✅ Cloud storage config (AWS S3, GCP, Azure Blob)
│   │── logger.js                 # ✅ Logging configuration (Winston, Pino, etc.)
│   │── aiConfig.js               # ✅ AI model configurations (file paths, versions)
│   │── paymentConfig.js          # ✅ Payment gateway credentials (Stripe, PayPal)
│
│── 📂 middleware/
│   │── authMiddleware.js         # ✅ Protects routes (JWT, session-based authentication)
│   │── errorHandler.js           # ✅ Centralized error-handling middleware
│   │── loggerMiddleware.js       # ✅ Logs requests & responses for debugging
│   │── validateRequest.js        # ✅ Validates API requests (Joi, express-validator)
│   │── rateLimiter.js            # ✅ Implements rate-limiting (express-rate-limit)
│   │── corsMiddleware.js         # ✅ Manages CORS policy settings
│   │── uploadMiddleware.js       # ✅ Handles file uploads (Multer for images/videos)
│   │── aiMiddleware.js           # ✅ AI request handling, input sanitization, rate-limiting
│
│── 📂 models/
│   │── User.js
│   │── Load.js
│   │── Truck.js
│   │── Bid.js
│   │── Payment.js
│   │── Dispute.js
│   │── Notification.js
│   │── Review.js
│   │── Ticket.js
│   │── LoadHistory.js
│   │── BidHistory.js
│   │── PaymentHistory.js
│   │── DisputeHistory.js
│   │── TicketHistory.js
│   │── WithdrawalHistory.js       # ✅ NEW: Tracks withdrawal transactions
│
│── 📂 routes/
│   │── authRoutes.js
│   │── userRoutes.js
│   │── loadRoutes.js
│   │── truckRoutes.js
│   │── bidRoutes.js
│   │── paymentRoutes.js
│   │── disputeRoutes.js
│   │── reviewRoutes.js
│   │── supportRoutes.js
│   │── notificationRoutes.js
│   │── analyticsRoutes.js
│   │── aiRoutes.js
│   │── loadHistoryRoutes.js
│   │── bidHistoryRoutes.js
│   │── paymentHistoryRoutes.js
│   │── disputeHistoryRoutes.js
│   │── ticketHistoryRoutes.js
│   │── withdrawalHistoryRoutes.js # ✅ NEW: Withdrawal history routes
│
│── 📂 controllers/
│   │── authController.js
│   │── userController.js
│   │── loadController.js
│   │── truckController.js
│   │── bidController.js
│   │── paymentController.js
│   │── disputeController.js
│   │── reviewController.js
│   │── supportController.js
│   │── notificationController.js
│   │── analyticsController.js
│   │── aiController.js
│   │── loadHistoryController.js
│   │── bidHistoryController.js
│   │── paymentHistoryController.js
│   │── disputeHistoryController.js
│   │── ticketHistoryController.js
│   │── withdrawalHistoryController.js # ✅ NEW: Handles withdrawal history
│
│── 📂 services/
│   │── authService.js
│   │── paymentService.js
│   │── notificationService.js
│   │── trackingService.js
│   │── analyticsService.js
│   │── aiService.js
│   │── loadHistoryService.js
│   │── bidHistoryService.js
│   │── paymentHistoryService.js
│   │── disputeHistoryService.js
│   │── ticketHistoryService.js
│   │── withdrawalHistoryService.js # ✅ NEW: Service for withdrawal history
│
│── 📂 ai/  
│   │── 📂 models/  
│   │   │── load_matching_model.pkl  
│   │   │── route_optimization_model.pkl  
│   │   │── price_prediction_model.pkl  
│   │  
│   │── 📂 data/  
│   │   │── raw_data.csv  
│   │   │── processed_data.csv  
│   │   │── feature_data.csv  
│   │  
│   │── 📂 training/  
│   │   │── train_load_matching.py  
│   │   │── train_route_optimization.py  
│   │   │── train_price_prediction.py  
│   │   │── preprocess_data.py  
│   │   │── feature_engineering.py  
│   │   │── model_evaluation.py  
│   │  
│   │── 📂 inference/  
│   │   │── match_load.py  
│   │   │── optimize_route.py  
│   │   │── predict_price.py  
│   │   │── real_time_ai_monitoring.py  
│   │  
│   │── 📂 services/  
│   │   │── loadMatchingService.js  
│   │   │── routeOptimizationService.js  
│   │   │── pricePredictionService.js  
│   │   │── aiMonitoringService.js  
│   │  
│   │── 📂 routes/  
│   │   │── aiRoutes.js  
│   │  
│   │── 📂 controllers/  
│   │   │── aiController.js  
│   │  
│   │── 📂 utils/  
│   │   │── data_loader.py  
│   │   │── metrics.py  
│   │   │── config.py  
│   │  
│   │── requirements.txt  
│   │── README.md  
│
│── .env
│── .gitignore
│── package.json
│── server.js
│── README.md
│
│── Dockerfile
│── docker-compose.yml
