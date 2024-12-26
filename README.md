# ICP-
# PhoneBook and Message History in Motoko

This project demonstrates a simple phone book and message history application built using the Motoko programming language. It allows users to manage contact entries and send/store messages using `HashMap` from the `mo:base` library.

## Features
- **Add a Contact**: Insert a new contact into the phone book.
- **Retrieve Contact Details**: Query the phone book to fetch contact details by name.
- **Send Messages**: Send and store messages linked to a phone number.
- **Retrieve Message History**: Fetch messages sent from a specific phone number.

## Code Structure
### Types
- **`Name`**: Alias for `Text`, representing the name of a contact.
- **`Phone`**: Alias for `Text`, representing a phone number.
- **`Entry`**: A record containing:
  - `desc`: Description of the contact (e.g., role or details).
  - `phone`: The phone number.
- **`Message`**: A record containing:
  - `receiver`: The recipient's phone number.
  - `mess`: The message content.

### Functions
#### 1. **`insert`**
- Adds a contact to the phone book.
- **Input**: 
  - `name: Name`: The contact's name.
  - `entry: Entry`: The contact's details.
- **Output**: `async ()`

#### 2. **`getPhone`**
- Fetches contact details by name.
- **Input**: `name: Name`
- **Output**: `async ?Entry` (returns the contact details or `null` if not found).

#### 3. **`sendMessage`**
- Stores a message for a specific sender's phone number.
- **Input**: 
  - `senderPhone: Phone`: The sender's phone number.
  - `message: Message`: The message record (receiver and content).
- **Output**: `async ()`

#### 4. **`getMessages`**
- Retrieves messages sent from a specific phone number.
- **Input**: `senderPhone: Phone`
- **Output**: `async ?Message` (returns the message or `null` if not found).

## Getting Started
### Prerequisites
