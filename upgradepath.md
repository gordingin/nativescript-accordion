# NativeScript-Accordion Upgrade Guide

This pull request upgrades the nativescript-accordion plugin to work with the latest versions of:
- Angular 17.x
- TypeScript 5.x
- NativeScript 8.x

## Major Changes

### 1. Dependencies Updated
- Angular updated from 6.1.0 to 17.0.0
- TypeScript updated from 2.9.2 to 5.2.0
- NativeScript packages updated to latest versions
  - `tns-core-modules` replaced with `@nativescript/core`
  - `nativescript-angular` replaced with `@nativescript/angular`
  - Platform requirements updated to NativeScript 8.x

### 2. Import Paths Changed
- Updated all imports from `tns-core-modules/*` to `@nativescript/core`
- Updated Angular imports to be compatible with Angular 17

### 3. TypeScript Configuration
- Updated TypeScript configuration to use modern settings:
  - Target changed to ES2020
  - Module system changed to ESNext
  - Added moduleResolution and esModuleInterop options

### 4. Angular Component Updates
- Added `static` flag to `@ViewChild` and `@ContentChild` decorators
- Updated how components handle templates to be compatible with Angular 17

### 5. Build System
- Updated webpack configuration to be compatible with latest NativeScript

## How to Test
1. Clone the repository
2. Run `npm install` in the root directory
3. Run `cd demo-ng && npm install`
4. Run `cd ../src && npm run build`
5. Test the Angular demo with `npm run demo.android` or `npm run demo.ios`

## Known Issues
- Some third-party plugins may need to be updated to be compatible with NativeScript 8.x
- Additional Angular template syntax changes may be needed depending on app complexity

## Benefits of Upgrade
- Better performance with modern JavaScript features
- Access to latest Angular features and improvements
- Improved typing with latest TypeScript
- Compatibility with latest NativeScript plugins and features