# Postman(JavaScript) 
// Проверка статуса ответа    Checking the response status
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

// Проверка наличия определенных данных в ответе     Checking for the presence of certain data in the response
pm.test("Response body should contain 'success'", function () {
    pm.expect(pm.response.text()).to.include("success");
});
Проверка соответствия значения переменной ожидаемому результату
pm.test("Значение переменной 'result' должно быть равно 42", function () {
    pm.expect(pm.environment.get("result")).to.eql(42);
});
Проверка времени ответа:
pm.test("Время ответа менее 500 миллисекунд", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});
