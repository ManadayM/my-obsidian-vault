---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1456428199391-a3b1cb5e93ab?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjY2NzA3ODE1&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-10-25) | (time:: 19:53)

# Nest.js 101

## Install Nest CLI
```shell
npm install @nestjs/cli --global
```

## New Nest.js Project
```shell
nest new project-name
```

## Generate a new module
```shell
nest g module <module-name>
```

```typescript
import { Module } from '@nestjs/common';

@Module({
	imports: [AuthModule, UserModule, BookmarkModule, PrismaModule],
})
export class AppModule {}
```

## Controllers
Responsible for handling incoming **requests** and returning **responses** to the client.

```typescript
import { Controller } from '@nestjs/common';

@Controller('auth')
export class AuthController {
	constructor(private authService: AuthService) {}
	
	// POST auth/signup
	@Post('signup')
	signup() {
		return this.authService.signup();
	}
}
```

## Providers
They are services responsible for executing **business logic**.

```typescript
import { Injectable } from '@nestjs/common';

@Injectable({})
export class AuthService {
	signup() {
		return 'I am signup';
	}
}
```


---
## Internal Links
[[2022-10-25]], [[Nest.js]]