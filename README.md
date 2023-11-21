# Postman(JavaScript) 
// Проверка статуса ответа    Checking the response status
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

// Проверка наличия определенных данных в ответе     Checking for the presence of certain data in the response
pm.test("Response body should contain 'success'", function () {
    pm.expect(pm.response.text()).to.include("success");
});
