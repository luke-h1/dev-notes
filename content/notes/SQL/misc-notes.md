```

create table users (
    first_name varchar(255) not null,
    last_name text,
    age int,
    email text unique not null

);


insert into users
(first_name, last_name, age, email)
values
('John', 'Doe', 22, 'bob@bob.com');

select first_name, last_name, age from users;

select * from users;

alter table users drop column age;

alter table users add column age int default 20;

insert into users
(first_name, last_name, age, email)
values
('John', 'Doe', 22, 'bob@bob4.com');

SELECT * from users where id = 1;



SELECT * from users where id in (3, 4, 5)

SELECT * from users where age > 10;

SELECT * from users where coalesce(age, 1) > 10 ;

select * from users where age is null

select * from users where age is not null

update users
set age = 20
where id = 1

update users
set age = 21,
last_name = 'tom'
where id = 1

update users
set age = age + 1,
last_name = last_name || ' tom22'
where id = 1



update users
set age = 33
where age is null


update users
set age = age - 10
where age < 25


delete from users
where id = 3;

create table posts(
    id serial primary key,
    title text not null,
    body text default '...',
    creatorId int references  users(id) not null
)


insert into posts
(title, creatorId)
values ('my first post', 1)

select first_name from users
inner join posts on users.id = posts."creatorId"

select * from users
inner join posts on users.id = posts."creatorId"



select first_name from users u
inner join posts p on u.id = p."creatorId"

select first_name, p.title from users u
inner join posts p on u.id = p."creatorId"

select u.id, p.id, first_name, p.title from users u
inner join posts p on u.id = p."creatorId";

select u.id, p.id post_id, first_name, p.title from users u
left join posts p on u.id = p."creatorId";

select u.id user_id, p.id post_id, first_name, p.title from users u
left join posts p on u.id = p."creatorId";

select u.id user_id, p.id post_id, first_name, p.title from users u
inner join posts p on u.id = p."creatorId"
where u.id = 1;

select u.id user_id, p.id post_id, first_name, p.title from users u
inner join posts p on u.id = p."creatorId"
where p.title like '%first%'

select u.id user_id, p.id post_id, first_name, p.title from users u
inner join posts p on u.id = p."creatorId"
where p.title like '%the%'

```