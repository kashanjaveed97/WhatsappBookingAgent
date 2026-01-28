# WhatsappBookingAgent
An AI-powered virtual receptionist that handles table reservations and cancellations for a Chinese restaurant, assists customers with menu inquiries, and provides accurate, real-time responses without human intervention

Workflow Architecture
The workflow follows a deterministic, tool-driven execution model:

WhatsApp Trigger
Receives incoming customer messages.

OpenAI Chat Model + Simple Memory

Interprets user intent (booking, modification, cancellation, inquiry)

Extracts structured reservation details

Maintains short-term conversation context

Google Calendar – Availability Check
Confirms whether the requested date and time are available.

Google Calendar – Create Event
Creates a reservation event only if the slot is available.

Google Sheets – Get Reservations
Retrieves existing reservations when needed (for validation or updates).

Google Sheets – Add / Update Reservation
Persists booking data in a structured format.

WhatsApp Send Message
Sends confirmation, rejection, or clarification messages to the customer.
