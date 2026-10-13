# Session 11 - Homework Ex1: Workflow chạy Unit Test với Gradle

## Mục tiêu
Khởi tạo GitHub Actions Workflow cho Spring Boot (Gradle) chạy JUnit test tự động.

## Cấu trúc
- `src/main/java/com/example/ex1/hello/HelloService.java` — service mẫu
- `src/test/...` — `contextLoads` + `HelloServiceTest` (JUnit 5 + AssertJ)
- `.github/workflows/ci.yml` — Job `Run Unit Tests` trên `ubuntu-latest`:
  - `actions/checkout@v5`
  - `actions/setup-java@v5` (JDK 17, Temurin)
  - `chmod +x gradlew`
  - `./gradlew test`

## Chạy локально
```bash
./gradlew test
```

## Kiểm tra trên GitHub
Push lên nhánh `main`, mở tab Actions, xác nhận Job `Run Unit Tests` màu xanh.
