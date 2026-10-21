USE classicmodels;
-- 1. Kiểm tra truy vấn trước khi đánh index
EXPLAIN SELECT * FROM customers WHERE customerName = 'Land of Toys Inc.';

-- 2. Thêm chỉ mục cho cột customerName
ALTER TABLE customers ADD INDEX idx_customerName(customerName);

-- 3. Kiểm tra lại truy vấn sau khi đã đánh index
EXPLAIN SELECT * FROM customers WHERE customerName = 'Land of Toys Inc.';

-- 4. Thêm index theo cặp cột
ALTER TABLE customers ADD INDEX idx_full_name(contactFirstName, contactLastName);

-- 5. Kiểm tra truy vấn với cặp cột đã đánh index
EXPLAIN SELECT * FROM customers WHERE contactFirstName = 'Jean' or contactFirstName = 'King';

-- 6. Xóa chỉ mục sau khi thực hành xong
ALTER TABLE customers DROP INDEX idx_full_name;
