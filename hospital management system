-- Creating tables for hospital management system

-- Patients table
CREATE TABLE patients (
  patient_id INT PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  patient_age INT,
  patient_gender VARCHAR(10),
  patient_address VARCHAR(255),
  patient_phone_number VARCHAR(20)
);

-- Doctors table
CREATE TABLE doctors (
  doctor_id INT PRIMARY KEY,
  doctor_name VARCHAR(255) NOT NULL,
  doctor_specialization VARCHAR(255),
  doctor_phone_number VARCHAR(20),
  doctor_email VARCHAR(255)
);

-- Appointments table
CREATE TABLE appointments (
  appointment_id INT PRIMARY KEY,
  patient_id INT,
  doctor_id INT,
  appointment_date DATE,
  appointment_time TIME,
  appointment_notes TEXT,
  FOREIGN KEY (patient_id) REFERENCES patients(patient_id),
  FOREIGN KEY (doctor_id) REFERENCES doctors(doctor_id)
);

-- Medicines table
CREATE TABLE medicines (
  medicine_id INT PRIMARY KEY,
  medicine_name VARCHAR(255) NOT NULL,
  medicine_description TEXT,
  medicine_price DECIMAL(10, 2)
);

-- Prescriptions table
CREATE TABLE prescriptions (
  prescription_id INT PRIMARY KEY,
  appointment_id INT,
  medicine_id INT,
  prescription_quantity INT,
  FOREIGN KEY (appointment_id) REFERENCES appointments(appointment_id),
  FOREIGN KEY (medicine_id) REFERENCES medicines(medicine_id)
);
