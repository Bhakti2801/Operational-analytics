-- Create the database
CREATE DATABASE operational_analytics;

-- Use the created database
USE operational_analytics;

-- Creating the job_data table with the correct date format
CREATE TABLE job_data (
    ds VARCHAR(10),
    job_id INT,
    actor_id INT,
    event VARCHAR(20),
    language VARCHAR(20),
    time_spent INT,
    org VARCHAR(5)
);

-- Create users table with VARCHAR for date columns initially
CREATE TABLE users (
    user_id INT PRIMARY KEY,
    created_at VARCHAR(50),
    company_id INT,
    language VARCHAR(20),
    activated_at VARCHAR(50),
    state VARCHAR(20)
);

-- Create events table with VARCHAR for date column initially
CREATE TABLE events (
    user_id INT,
    occurred_at VARCHAR(50),
    event_type VARCHAR(50),
    event_name VARCHAR(50),
    location VARCHAR(50),
    device VARCHAR(50),
    user_type INT
);

-- Create email_events table with VARCHAR for date column initially
CREATE TABLE email_events (
    user_id INT,
    occurred_at VARCHAR(50),
    action VARCHAR(50),
    user_type INT
);
