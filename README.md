# Patient Record Management System

A console-based patient record manager written in C. It stores records in a singly linked list and lets you add, view, search, update, delete, and sort patient entries from a simple menu.

## Features

- **Add patient**: registers a new patient with a unique, positive registration number
- **Display all**: lists every record in a readable format
- **Search**: finds a patient by registration number
- **Update**: edit a patient's name, phone number, age, or medical history
- **Delete**: removes a record by registration number
- **Sort**: orders records by registration number (insertion sort on the linked list)
- **Input validation**: numeric fields reject non-numeric input, age must be 0–120, and duplicate registration numbers are refused
- **Safe string input**: uses `fgets` with buffer sizes to avoid overflows, and frees all memory on exit

## Data stored per patient

| Field | Description |
|---|---|
| Registration number | Unique positive integer |
| Name, guardian | Patient and guardian names |
| Gender, age, blood group | Basic demographics |
| Phone, address, city, state | Contact details |
| Disease/problem | Reason for visit |
| Referred doctor | Assigned doctor |
| Medical history | Free-text notes |

## Getting started

### Requirements

- A C compiler such as GCC or Clang

### Build

```bash
gcc -Wall -Wextra -o patient_system main.c
```

### Run

```bash
./patient_system
```

## Usage

```
===== PATIENT RECORD MANAGEMENT SYSTEM =====
1. Add patient
2. Display all patients
3. Search patient
4. Update patient
5. Delete patient
6. Sort by registration number
7. Exit
```

Enter the number of the option you want and follow the prompts.

## Limitations

- Records live in memory only and are lost when the program exits
- Lookups are linear, so it is best suited to small datasets
- Update supports only four fields

## Future work

- Save and load records from a file
- Edit any field
- Search by name or phone number
- Sort by other fields
