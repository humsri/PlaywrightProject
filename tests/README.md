## Automated  Web Testing using Playwright


## 1. Introduction
Playwright is a open-source end to end testing framework

## 2. Objectives
- Automate web test cases using Playwright
- Validate UI 
- Generate reports

## 3. Tools & Requirement
- Node.js
- Playwright
- VS Code
- Browsers(Chromium, Firefox, WebKit )

## 4. Implementaion
Intallation
------------
npm init playwright@latest


Example Test Script
-------------------
'''' javascript ''''

import { test, expect } from '@playwright/test';
test ('Login test', async ({ page }) => {
    await page.goto('https://example.com/login');
    await page.fill('#username','admin');
    await page.fill ('#password','password123');
    await page.click ('button[type="submit"]');
    await expect(page).toHaveURL('https://example.com/dashboard');
});

Running Test Cases:
--------------------
npx playwright test

Viewing Reports:
----------------
npx playwright show-report

