``` sql

INSERT INTO Authors (name, bio) VALUES 
('George Orwell', 'English novelist and essayist.'),
('J.K. Rowling', 'British author of the Harry Potter series.');

INSERT INTO Genres (name) VALUES 
('Dystopian'),
('Fantasy');

INSERT INTO Books (title, author_id, genre_id, published_year) VALUES 
('1984', 1, 1, 1949),
('Harry Potter and the Sorcerer\'s Stone', 2, 2, 1997);
