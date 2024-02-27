# Lab1_2_Authentication_ElectronicVoting
Lab 1 - registration (user_db) and authentication (user_client)
Lab 2 - electronic voting (starts and ends by click)

database SQL scripts:
CREATE TABLE users (
      id SERIAL PRIMARY KEY,
      login VARCHAR,
      password VARCHAR,
      string VARCHAR, 
      timestamp TIMESTAMP,
      d bigint,
      fi bigint
);

CREATE TABLE RSA (
      id SERIAL PRIMARY KEY, 
      user_id int , 
      p bigint,
      q bigint,
      n bigint,
      phi bigint,
      e bigint,
      d bigint,
      foreign key (user_id) REFERENCES users (id)
  );
