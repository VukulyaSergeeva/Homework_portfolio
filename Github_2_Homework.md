{
	"info": {
		"_postman_id": "da754b8f-ee7c-4bb4-8190-b5a7164c355b",
		"name": "Postman_HW2",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "24360846"
	},
	"item": [
		{
			"name": "/first",
			"event": [
				{
					"listen": "test",
					"script": {
						"exec": [
							"//Статус код 200\r",
							"pm.test(\"Status code is 200\", function () {\r",
							"    pm.response.to.have.status(200);\r",
							"});\r",
							"\r",
							"//Проверить, что в body приходит правильный string.\r",
							"pm.test(\"Body is correct\", function () {\r",
							"    pm.response.to.have.body(\"This is the first responce from server!ss\");\r",
							"});"
						],
						"type": "text/javascript"
					}
				}
			],
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"method": "GET",
				"header": [],
				"body": {
					"mode": "formdata",
					"formdata": [
						{
							"key": "auth_token",
							"value": "{{auth_token}}",
							"type": "text"
						}
					]
				},
				"url": {
					"raw": "http://162.55.220.72:5005/first",
					"protocol": "http",
					"host": [
						"162",
						"55",
						"220",
						"72"
					],
					"port": "5005",
					"path": [
						"first"
					]
				}
			},
			"response": []
		},
		{
			"name": "/user_info_3",
			"event": [
				{
					"listen": "test",
					"script": {
						"exec": [
							"//Статус код 200\r",
							"pm.test(\"Status code is 200\", function () {\r",
							"    pm.response.to.have.status(200);\r",
							"});\r",
							"\r",
							"// Спарсить response body в json.\r",
							"var resp_Data=pm.response.json();\r",
							"var resp_name =resp_Data.name;\r",
							"var resp_age =resp_Data.age;\r",
							"var resp_salary =resp_Data.salary;\r",
							"\r",
							"//Проверить, что name в ответе равно name s request (name вбить руками.)\r",
							"pm.test(\"Check user_name\", function(){\r",
							"    pm.expect(resp_name).to.eql(\"Alex\")\r",
							"});\r",
							"\r",
							"//Проверить, что age в ответе равно age s request (age вбить руками.)\r",
							"pm.test(\"Check user_age\", function(){\r",
							"    pm.expect(resp_age).to.eql(\"33\")\r",
							"});\r",
							"\r",
							"//Проверить, что salary в ответе равно salary s request (salary вбить руками.)\r",
							"pm.test(\"Check user_salary\", function(){\r",
							"    pm.expect(resp_salary).to.eql(1000)\r",
							"});\r",
							"\r",
							"//Спарсить request\r",
							"var req_Data =request.data;\r",
							"var req_name =req_Data.name;\r",
							"var req_age =req_Data.age;\r",
							"var req_salary =req_Data.salary;\r",
							"var req_u_salary_1_5_year =req_Data.req_u_salary_1_5_year;\r",
							"\r",
							"//Проверить, что name в ответе равно name s request (name забрать из request.)\r",
							"\r",
							"pm.test(\"Check user_name from request\", function () {\r",
							"    pm.expect(req_name).to.eql(req_name);\r",
							"});\r",
							"\r",
							"//Проверить, что age в ответе равно age s request (age забрать из request.)\r",
							"pm.test(\"Check user_age from request\", function () {\r",
							"    pm.expect(req_age).to.eql(req_age);\r",
							"});\r",
							"//Проверить, что salary в ответе равно salary s request (salary забрать из request.)\r",
							"pm.test(\"Check user_salary from request\", function () {\r",
							"    pm.expect(req_salary).to.eql(req_salary);\r",
							"});\r",
							"// Вывести в консоль параметр family из response.\r",
							"console.log(\"family\",resp_Data.family);\r",
							"\r",
							"//Проверить что u_salary_1_5_year в ответе равно salary*4 (salary забрать из request)\r",
							"pm.test(\"Check user_u_salary_1_5_year from request \", function () {\r",
							"    pm.expect(req_u_salary_1_5_year).to.eql(req_u_salary_1_5_year);\r",
							"});"
						],
						"type": "text/javascript"
					}
				}
			],
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "formdata",
					"formdata": [
						{
							"key": "name",
							"value": "Alex",
							"type": "text"
						},
						{
							"key": "age",
							"value": "33",
							"type": "text"
						},
						{
							"key": "salary",
							"value": "1000",
							"type": "text"
						}
					]
				},
				"url": {
					"raw": "http://162.55.220.72:5005/user_info_3?auth_token={{auth_token}}",
					"protocol": "http",
					"host": [
						"162",
						"55",
						"220",
						"72"
					],
					"port": "5005",
					"path": [
						"user_info_3"
					],
					"query": [
						{
							"key": "auth_token",
							"value": "{{auth_token}}"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "/object_info_3",
			"event": [
				{
					"listen": "test",
					"script": {
						"exec": [
							"// Статус код 200\r",
							"pm.test(\"Status code is 200\", function () {\r",
							"    pm.response.to.have.status(200);\r",
							"});\r",
							"// Спарсить response body в json.\r",
							"\r",
							"// Спарсить request.\r",
							"\r",
							"// Проверить, что name в ответе равно name s request (name забрать из request.)\r",
							"\r",
							"// Проверить, что age в ответе равно age s request (age забрать из request.)\r",
							"\r",
							"// Проверить, что salary в ответе равно salary s request (salary забрать из request.)\r",
							"\r",
							"// Вывести в консоль параметр family из response.\r",
							"\r",
							"// Проверить, что у параметра dog есть параметры name.\r",
							"\r",
							"// Проверить, что у параметра dog есть параметры age.\r",
							"\r",
							"// Проверить, что параметр name имеет значение Luky.\r",
							"\r",
							"// Проверить, что параметр age имеет значение 4."
						],
						"type": "text/javascript"
					}
				}
			],
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"method": "GET",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://162.55.220.72:5005/object_info_3?name=Alex&age=33&salary=1000&auth_token={{auth_token}}",
					"protocol": "http",
					"host": [
						"162",
						"55",
						"220",
						"72"
					],
					"port": "5005",
					"path": [
						"object_info_3"
					],
					"query": [
						{
							"key": "name",
							"value": "Alex"
						},
						{
							"key": "age",
							"value": "33"
						},
						{
							"key": "salary",
							"value": "1000"
						},
						{
							"key": "auth_token",
							"value": "{{auth_token}}"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "/object_info_4",
			"event": [
				{
					"listen": "test",
					"script": {
						"exec": [
							"//Статус код 200\r",
							"\r",
							"// Спарсить response body в json.\r",
							"\r",
							"// Спарсить request.\r",
							"\r",
							"// Проверить, что name в ответе равно name s request (name забрать из request.)\r",
							"\r",
							"// Проверить, что age в ответе равно age из request (age забрать из request.)\r",
							"\r",
							"// Вывести в консоль параметр salary из request.\r",
							"\r",
							"// Вывести в консоль параметр salary из response.\r",
							"\r",
							"// Вывести в консоль 0-й элемент параметра salary из response.\r",
							"\r",
							"// Вывести в консоль 1-й элемент параметра salary параметр salary из response.\r",
							"\r",
							"// Вывести в консоль 2-й элемент параметра salary параметр salary из response.\r",
							"\r",
							"// Проверить, что 0-й элемент параметра salary равен salary из request (salary забрать из request.)\r",
							"\r",
							"// Проверить, что 1-й элемент параметра salary равен salary*2 из request (salary забрать из request.)\r",
							"\r",
							"// Проверить, что 2-й элемент параметра salary равен salary*3 из request (salary забрать из request.)\r",
							"\r",
							"// Создать в окружении переменную name\r",
							"\r",
							"// Создать в окружении переменную age\r",
							"\r",
							"// Создать в окружении переменную salary\r",
							"\r",
							"// Передать в окружение переменную name\r",
							"\r",
							"// Передать в окружение переменную age\r",
							"\r",
							"// Передать в окружение переменную salary\r",
							"\r",
							"// Написать цикл который выведет в консоль по порядку элементы списка из параметра salary.\r",
							""
						],
						"type": "text/javascript"
					}
				}
			],
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "http://162.55.220.72:5005/object_info_4?auth_token={{auth_token}}",
					"protocol": "http",
					"host": [
						"162",
						"55",
						"220",
						"72"
					],
					"port": "5005",
					"path": [
						"object_info_4"
					],
					"query": [
						{
							"key": "auth_token",
							"value": "{{auth_token}}"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "/user_info_2",
			"event": [
				{
					"listen": "test",
					"script": {
						"exec": [
							"// Вставить параметр salary из окружения в request\r",
							"\r",
							"// Вставить параметр age из окружения в age\r",
							"\r",
							"// Вставить параметр name из окружения в name\r",
							"\r",
							"// Отправить запрос.\r",
							"\r",
							"// Статус код 200\r",
							"\r",
							"// Спарсить response body в json.\r",
							"\r",
							"// Спарсить request.\r",
							"\r",
							"// Проверить, что json response имеет параметр start_qa_salary\r",
							"\r",
							"// Проверить, что json response имеет параметр qa_salary_after_6_months\r",
							"\r",
							"// Проверить, что json response имеет параметр qa_salary_after_12_months\r",
							"\r",
							"// Проверить, что json response имеет параметр qa_salary_after_1.5_year\r",
							"\r",
							"// Проверить, что json response имеет параметр qa_salary_after_3.5_years\r",
							"\r",
							"// Проверить, что json response имеет параметр person\r",
							"\r",
							"// Проверить, что параметр start_qa_salary равен salary из request (salary забрать из request.)\r",
							"\r",
							"// Проверить, что параметр qa_salary_after_6_months равен salary*2 из request (salary забрать из request.)\r",
							"\r",
							"// Проверить, что параметр qa_salary_after_12_months равен salary*2.7 из request (salary забрать из request.)\r",
							"\r",
							"// Проверить, что параметр qa_salary_after_1.5_year равен salary*3.3 из request (salary забрать из request.)\r",
							"\r",
							"// Проверить, что параметр qa_salary_after_3.5_years равен salary*3.8 из request (salary забрать из request.)\r",
							"\r",
							"// Проверить, что в параметре person, 1-й элемент из u_name равен salary из request (salary забрать из request.)\r",
							"\r",
							"// Проверить, что что параметр u_age равен age из request (age забрать из request.)\r",
							"\r",
							"// Проверить, что параметр u_salary_5_years равен salary*4.2 из request (salary забрать из request.)\r",
							"\r",
							"// ***Написать цикл который выведет в консоль по порядку элементы списка из параметра person.\r",
							""
						],
						"type": "text/javascript"
					}
				}
			],
			"request": {
				"method": "POST",
				"header": [],
				"url": {
					"raw": "http://162.55.220.72:5005/user_info_2?auth_token={{auth_token}}",
					"protocol": "http",
					"host": [
						"162",
						"55",
						"220",
						"72"
					],
					"port": "5005",
					"path": [
						"user_info_2"
					],
					"query": [
						{
							"key": "auth_token",
							"value": "{{auth_token}}"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "login",
			"event": [
				{
					"listen": "test",
					"script": {
						"exec": [
							"var json_data = pm.response.json();\r",
							"\r",
							"var tokenData = json_data.token\r",
							"\r",
							"pm.environment.set(\"auth_token\", tokenData);\r",
							"\r",
							""
						],
						"type": "text/javascript"
					}
				}
			],
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "formdata",
					"formdata": [
						{
							"key": "login",
							"value": "vika",
							"type": "text"
						},
						{
							"key": "password",
							"value": "523g",
							"type": "text"
						}
					]
				},
				"url": {
					"raw": "http://162.55.220.72:5005/login",
					"protocol": "http",
					"host": [
						"162",
						"55",
						"220",
						"72"
					],
					"port": "5005",
					"path": [
						"login"
					]
				}
			},
			"response": []
		}
	]
}