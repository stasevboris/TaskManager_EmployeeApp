# EmployeeApp — распределение обязанностей сотрудников (WPF + MySQL)

Настольное приложение для руководителя проекта: задачи, обязанности сотрудников и контроль сроков.

* вход в систему и роли (администратор / сотрудник) — `Services/AuthService.cs`;
* создание задач и обязанностей с проверкой пересечения дат у одного сотрудника;
* просмотр обязанностей по сотруднику и по задаче;
* MVVM (`ViewModels/MainViewModel.cs`), отдельные окна входа и основной работы;
* unit-тесты на NUnit с EF Core InMemory (`EmployeeApp.Tests`).

**Стек:** C#, .NET 8, WPF, Entity Framework Core 8, Pomelo MySQL, NUnit.

## Запуск

1. Восстановите базу: `mysql -u <user> -p EmployeeDB < backup_employeedb.sql`.
2. Укажите свой пароль в строке подключения в `EmployeeManagementSolution/EmployeeApp/Data/EmployeeDbContext.cs`
   (в репозитории — заглушка `<PASSWORD>`).
3. Откройте `EmployeeManagementSolution/EmployeeManagementSolution.sln` и запустите проект `EmployeeApp`.
4. Тесты: `dotnet test EmployeeManagementSolution/EmployeeApp.Tests`.

Ветка `master` — первая версия приложения, актуальная — `version2.0`.
