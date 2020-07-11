# WHMCS_Trojan_Admin
Make WHMCS Great Again.

### Important Notification
Please move the products_JSON.php to a directory unreachable by web access. Otherwise your password will be exposed to everyone!

### MySQL DB Structure

CREATE TABLE users (
    id INT UNSIGNED NOT NULL AUTO_INCREMENT,
    password CHAR(56) NOT NULL,
    quota BIGINT NOT NULL DEFAULT 0,
    download BIGINT UNSIGNED NOT NULL DEFAULT 0,
    upload BIGINT UNSIGNED NOT NULL DEFAULT 0,
    pid INT NOT NULL,
    PRIMARY KEY (id),
    INDEX (password),
    INDEX (pid)
);
