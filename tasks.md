# [Project Name] MVP - Development Task List

## Project File Structure

```
[project-name]/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── [FeatureA]/
│   │   │   ├── [Component1].jsx
│   │   │   ├── [Component2].jsx
│   │   │   └── [ComponentProvider].jsx
│   │   ├── [FeatureB]/
│   │   │   ├── [Component1].jsx
│   │   │   ├── [Component2].jsx
│   │   │   └── [Component3].jsx
│   │   ├── [FeatureC]/
│   │   │   ├── [Component1].jsx
│   │   │   ├── [Component2].jsx
│   │   │   └── [Component3].jsx
│   │   └── Layout/
│   │       ├── [LayoutComponent1].jsx
│   │       └── [LayoutComponent2].jsx
│   ├── services/
│   │   ├── [service-name].js
│   │   ├── [feature-a].js
│   │   ├── [feature-b].js
│   │   └── [feature-c].js
│   ├── hooks/
│   │   ├── [useFeatureA].js
│   │   ├── [useFeatureB].js
│   │   ├── [useFeatureC].js
│   │   └── [useFeatureD].js
│   ├── utils/
│   │   ├── constants.js
│   │   └── helpers.js
│   ├── contexts/
│   │   ├── [FeatureA]Context.jsx
│   │   └── [FeatureB]Context.jsx
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── tests/
│   ├── setup.js
│   ├── unit/
│   │   ├── utils/
│   │   │   └── helpers.test.js
│   │   ├── services/
│   │   │   ├── [service-a].test.js
│   │   │   └── [service-b].test.js
│   │   └── contexts/
│   │       └── [Context].test.js
│   └── integration/
│       ├── [flow-a].test.js
│       ├── [flow-b].test.js
│       └── [feature-integration].test.js
├── .env
├── .env.example
├── .gitignore
├── package.json
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
├── [backend-config].json
├── .[backend-rc]
└── README.md
```

---

## PR #1: Project Setup & [Backend] Configuration

**Branch:** `setup/initial-config`  
**Goal:** Initialize project with all dependencies and [backend] configuration

### Tasks:

- [ ] **1.1: Initialize [Framework] + [Build Tool] Project**

  - Files to create: `package.json`, `[config-file]`, `index.html`
  - Run: `npm create [build-tool]@latest [project-name] -- --template [template]`
  - Verify dev server runs

- [ ] **1.2: Install Core Dependencies**

  - Files to update: `package.json`
  - Install:
    ```bash
    npm install [dependency-1] [dependency-2] [dependency-3]
    npm install -D [dev-dependency-1] [dev-dependency-2] [dev-dependency-3]
    ```

- [ ] **1.3: Configure [CSS Framework]**

  - Files to create: `[css-config].js`, `postcss.config.js`
  - Files to update: `src/index.css`
  - Run: `npx [css-framework] init -p`
  - Add [CSS framework] directives to `index.css`

- [ ] **1.4: Set Up [Backend] Project**

  - Create [backend] project in console
  - Enable [Service A] ([specific configs])
  - Create [Database A]
  - Create [Database B]
  - Files to create: `.env`, `.env.example`
  - Add [backend] config keys to `.env`

- [ ] **1.5: Create [Backend] Service File**

  - Files to create: `src/services/[backend].js`
  - Initialize [backend] app
  - Export `[service-a]`, `[service-b]`, `[service-c]`

- [ ] **1.6: Configure Git & .gitignore**

  - Files to create/update: `.gitignore`
  - Ensure `.env` is ignored
  - Add `node_modules/`, `dist/`, `.[backend-folder]/` to `.gitignore`

- [ ] **1.7: Create README with Setup Instructions**
  - Files to create: `README.md`
  - Include setup steps, env variables needed, run commands

**PR Checklist:**

- [ ] Dev server runs successfully
- [ ] [Backend] initialized without errors
- [ ] [CSS framework] classes work in test component
- [ ] `.env` is in `.gitignore`

---

## PR #2: Authentication System

**Branch:** `feature/authentication`  
**Goal:** Complete user authentication with login/signup flows

### Tasks:

- [ ] **2.1: Create Auth Context**

  - Files to create: `src/contexts/AuthContext.jsx`
  - Provide: `currentUser`, `loading`, `login()`, `signup()`, `logout()`

- [ ] **2.2: Create Auth Service**

  - Files to create: `src/services/auth.js`
  - Functions: `signUp(email, password, [additional-fields])`, `signIn(email, password)`, `signInWith[Provider]()`, `signOut()`, `updateUserProfile([fields])`
  - [Specific logic]: [describe any special handling]

- [ ] **2.3: Create Auth Hook**

  - Files to create: `src/hooks/useAuth.js`
  - Return auth context values

- [ ] **2.4: Build Signup Component**

  - Files to create: `src/components/Auth/Signup.jsx`
  - Form fields: [list required fields]
  - Handle signup errors
  - Redirect to [destination] on success

- [ ] **2.5: Build Login Component**

  - Files to create: `src/components/Auth/Login.jsx`
  - Form fields: [list required fields]
  - Add "[Provider] login" button(s)
  - Handle login errors
  - Link to signup page

- [ ] **2.6: Create Auth Provider Wrapper**

  - Files to create: `src/components/Auth/AuthProvider.jsx`
  - Wrap entire app with AuthContext
  - Show loading state during auth check

- [ ] **2.7: Update App.jsx with Protected Routes**

  - Files to update: `src/App.jsx`
  - Show Login/Signup if not authenticated
  - Show [main component] if authenticated
  - Basic routing logic

- [ ] **2.8: Create Navbar Component**
  - Files to create: `src/components/Layout/Navbar.jsx`
  - Display current user [identifier]
  - Logout button

**PR Checklist:**

- [ ] Can create new account with email/password
- [ ] Can login with existing account
- [ ] Can sign in with [provider]
- [ ] [Display element] appears correctly ([specific logic])
- [ ] [Display element] truncates at [X] chars if too long
- [ ] Logout works and redirects to login
- [ ] Auth state persists on page refresh

---

## PR #3: Basic [Primary Feature] Setup

**Branch:** `feature/[primary-feature]-basic`  
**Goal:** [Primary feature] with [key capabilities] and basic stage setup

### Tasks:

- [ ] **3.1: Create [Feature] Constants**

  - Files to create: `src/utils/constants.js`
  - Define: `[CONSTANT_A] = [value]`, `[CONSTANT_B] = [value]`, `[CONSTANT_C]`, `[CONSTANT_D]`

- [ ] **3.2: Create [Feature] Context**

  - Files to create: `src/contexts/[Feature]Context.jsx`
  - State: `[entities]`, `[selectedId]`, `[ref]`
  - Provide methods to add/update/delete [entities]

- [ ] **3.3: Build Base [Feature] Component**

  - Files to create: `src/components/[Feature]/[Feature].jsx`
  - Set up [rendering library] [elements]
  - Container div with fixed dimensions
  - Background color/grid (optional)

- [ ] **3.4: Implement [Navigation Action A] Functionality**

  - Files to update: `src/components/[Feature]/[Feature].jsx`
  - Handle `[event-handler]` on [element]
  - Constrain [action] to [boundaries]
  - Prevent [entities] from being placed/moved outside boundaries

- [ ] **3.5: Implement [Navigation Action B] Functionality**

  - Files to update: `src/components/[Feature]/[Feature].jsx`
  - Handle `[event-handler]` event
  - [Action] to [target] position
  - Min [value]: [X], Max [value]: [Y]

- [ ] **3.6: Create [Feature] Controls Component**

  - Files to create: `src/components/[Feature]/[Feature]Controls.jsx`
  - Buttons: "[Action A]", "[Action B]", "[Action C]", "[Action D]"
  - Position: Fixed/floating on [feature]

- [ ] **3.7: Add [Feature] to App**
  - Files to update: `src/App.jsx`
  - Wrap [Feature] in [Feature]Context
  - Include Navbar and [Feature]

**PR Checklist:**

- [ ] [Feature] renders at correct size
- [ ] Can [navigate] by [interaction method]
- [ ] Can [zoom/scale] with [input method]
- [ ] [Action] centers on [target] position
- [ ] Reset view button works
- [ ] [Boundary] constraints are enforced
- [ ] [Performance metric] maintained during [actions]

---

## PR #4: [Entity] Creation & Manipulation

**Branch:** `feature/[entities]`  
**Goal:** Create, select, and move [entities] on [system]

### Tasks:

- [ ] **4.1: Create [Entity] Component**

  - Files to create: `src/components/[Feature]/[Entity].jsx`
  - Support: **[Specific types] only for MVP**
  - Props: `id`, `[attr1]`, `[attr2]`, `[attr3]`, `[attr4]`, `isSelected`, `isLocked`, `lockedBy`

- [ ] **4.2: Add [Entity] Creation Logic**

  - Files to update: `src/contexts/[Feature]Context.jsx`
  - Function: `add[Entity](type, position)`
  - Generate unique ID for each [entity]
  - Default properties: [dimensions], fixed [styling]

- [ ] **4.3: Implement [Entity] Rendering**

  - Files to update: `src/components/[Feature]/[Feature].jsx`
  - Map over `[entities]` array
  - Render [Entity] component for each

- [ ] **4.4: Add [Entity] Selection**

  - Files to update: `src/components/[Feature]/[Entity].jsx`
  - Handle `onClick` to set selected
  - Visual feedback: [style] when selected
  - Files to update: `src/contexts/[Feature]Context.jsx`
  - State: `selectedId`

- [ ] **4.5: Implement [Entity] Dragging**

  - Files to update: `src/components/[Feature]/[Entity].jsx`
  - Enable `draggable={true}`
  - Handle `[dragEndEvent]` to update position
  - Files to update: `src/contexts/[Feature]Context.jsx`
  - Function: `update[Entity](id, updates)`

- [ ] **4.6: Add Click-to-Deselect**

  - Files to update: `src/components/[Feature]/[Feature].jsx`
  - Handle [Stage/Container] `onClick` to deselect when clicking background

- [ ] **4.7: Connect "Add [Entity]" Button**

  - Files to update: `src/components/[Feature]/[Feature]Controls.jsx`
  - Button creates [entity] at center of current viewport

- [ ] **4.8: Add Delete Functionality**
  - Files to update: `src/contexts/[Feature]Context.jsx`
  - Function: `delete[Entity](id)`
  - Files to update: `src/components/[Feature]/[Feature].jsx`
  - Add keyboard listener for [Delete keys]
  - Delete selected [entity] when key pressed
  - Cannot delete [entities] locked by other users

**PR Checklist:**

- [ ] Can create [entities] via button
- [ ] [Entities] render at correct positions with [default styling]
- [ ] Can select [entities] by clicking
- [ ] Can drag [entities] smoothly
- [ ] Selection state shows visually
- [ ] Can delete selected [entity] with [keyboard shortcut]
- [ ] Clicking another [entity] deselects the previous one (single-select mode)
- [ ] Clicking empty [system] deselects current selection
- [ ] [Entities] cannot be moved outside [system] boundaries
- [ ] No lag with [X]+ [entities]

---

## PR #5: Real-Time [Entity] Synchronization

**Branch:** `feature/realtime-sync`  
**Goal:** Sync [entity] changes across all connected users
**Status:** [Status emoji/text]

### Tasks:

- [ ] **5.1: Design [Database] Schema**

  - Collection: `[collection]` (single document: `[document-id]`)
  - Document structure:
    ```
    {
      [primaryId]: "[value]",
      [entities]: [
        {
          id: string,
          type: '[type]',
          [attr1]: type,
          [attr2]: type,
          [attr3]: type,
          [attr4]: type,
          createdBy: string (userId),
          createdAt: timestamp,
          lastModifiedBy: string,
          lastModifiedAt: timestamp,
          isLocked: boolean,
          lockedBy: string (userId) or null
        }
      ],
      lastUpdated: timestamp
    }
    ```

- [ ] **5.2: Create [Feature] Service**

  - Files to create: `src/services/[feature].js`
  - Function: `subscribeTo[Entities]([id], callback)`
  - Function: `create[Entity]([id], [entity]Data)`
  - Function: `update[Entity]([id], [entity]Id, updates)`
  - Function: `delete[Entity]([id], [entity]Id)`

- [ ] **5.3: Create [Feature] Hook**

  - Files to create: `src/hooks/use[Feature].js`
  - Subscribe to [Database] on mount
  - Sync local state with [Database]
  - Return: `[entities]`, `add[Entity]()`, `update[Entity]()`, `delete[Entity]()`

- [ ] **5.4: Integrate Real-Time Updates in Context**

  - Files to update: `src/contexts/[Feature]Context.jsx`
  - Replace local state with `use[Feature]` hook
  - Listen to [Database] changes
  - Update local [entities] array on remote changes

- [ ] **5.5: Implement Object Locking**

  - Files to update: `src/services/[feature].js`
  - Strategy: First user to select/drag acquires lock
  - Function: `lock[Entity]([id], [entity]Id, userId)`
  - Function: `unlock[Entity]([id], [entity]Id)`
  - Function: `staleLockSweeper([id])` - cleans locks older than [X]s
  - Auto-release lock after drag completes or timeout ([X] seconds)
  - Visual indicator showing which user has locked an object
  - Other users cannot move locked objects
  - **Evidence:** [Validation method once complete]

- [ ] **5.6: Add Loading States**

  - Files to update: `src/contexts/[Feature]Context.jsx`
  - Show loading spinner while initial [entities] load
  - Files to update: `src/components/[Feature]/[Feature].jsx`
  - Display "Loading [system]..." message

- [ ] **5.7: Handle Offline/Reconnection**
  - Files to update: `src/hooks/use[Feature].js`
  - Enable [Database] offline persistence
  - Show reconnection status

**PR Checklist:**

- [ ] Open two browsers: creating [entity] in one appears in other
- [ ] User A starts dragging [entity] → [entity] locks for User A
- [ ] User B cannot move [entity] while User A has it locked
- [ ] Lock shows visual indicator ([describe])
- [ ] Lock releases automatically when User A stops dragging
- [ ] Lock releases after timeout ([X] seconds) via staleLockSweeper
- [ ] Moving [entity] in one browser updates in other (<[X]ms)
- [ ] Deleting [entity] in one removes from other
- [ ] Cannot delete [entities] locked by other users
- [ ] Page refresh loads all existing [entities]
- [ ] All users leave and return: [entities] still there
- [ ] No duplicate [entities] or sync issues

**Evidence:** [Description of validation method once complete]

---

## PR #6: Multiplayer [Real-time Element]

**Branch:** `feature/[real-time-element]`  
**Goal:** Real-time [element] tracking for all connected users
**Status:** [Status emoji/text]

### Tasks:

- [ ] **6.1: Design Realtime Database Schema**

  - Path: `/[parent]/[session-id]/{userId}`
  - Data structure:
    ```
    {
      displayName: string,
      [attribute1]: string,
      [attribute2]: number,
      [attribute3]: number,
      lastSeen: timestamp
    }
    ```

- [ ] **6.2: Create [Element] Service**

  - Files to create: `src/services/[elements].js`
  - Function: `update[Element]Position([id], userId, [attr1], [attr2], name, [attr3])`
  - Function: `subscribeTo[Elements]([id], callback)`
  - Function: `remove[Element]([id], userId)`

- [ ] **6.3: Create [Elements] Hook**

  - Files to create: `src/hooks/use[Elements].js`
  - Track [input] position on [system]
  - Convert screen coords to [system] coords
  - Throttle updates to ~[X]Hz ([Y]ms)
  - Return: `[elements]` object (keyed by userId)

- [ ] **6.4: Build [Element] Component**

  - Files to create: `src/components/Collaboration/[Element].jsx`
  - [Visual representation] with user [attribute]
  - Name label next to [element]
  - Smooth CSS transitions for movement

- [ ] **6.5: Integrate [Elements] into [System]**

  - Files to update: `src/components/[Feature]/[Feature].jsx`
  - Add `[eventHandler]` handler to [Container]
  - Update [element] position in RTDB
  - Render [Element] components for all other users

- [ ] **6.6: Assign User [Attributes]**

  - Files to create: `src/utils/helpers.js`
  - Function: `generateUser[Attribute](userId)` - randomly assigned on join
  - [Attribute] palette: [X-Y] distinct [attributes] with sufficient contrast
  - Maintain [attribute] consistency per user throughout session

- [ ] **6.7: Handle [Element] Cleanup**

  - Files to update: `src/hooks/use[Elements].js`
  - Remove [element] on component unmount
  - Use `onDisconnect()` in RTDB to auto-cleanup

- [ ] **6.8: Optimize [Element] Updates**
  - Files to update: `src/hooks/use[Elements].js`
  - Throttle [input] events to [X]-[Y] FPS (not full [Z]Hz)
  - Only send if position changed significantly (>[X]px)

**PR Checklist:**

- [ ] Moving [input] shows [element] to other users
- [ ] [Element] has correct user name and [attribute]
- [ ] [Elements] move smoothly without jitter
- [ ] [Element] disappears when user leaves
- [ ] Updates happen within [X]ms
- [ ] No performance impact with [Y] concurrent [elements]

**Evidence:** [Description of validation method once complete]

---

## PR #7: User Presence System

**Branch:** `feature/presence`  
**Goal:** Show who's online and active on the [system]
**Status:** [Status emoji/text]

### Tasks:

- [ ] **7.1: Design Presence Schema**

  - Path: `/[parent]/[session-id]/{userId}` (same as [real-time element])
  - Data structure (combined with [element] data):
    ```
    {
      displayName: string,
      [attribute1]: string,
      [attribute2]: number,
      [attribute3]: number,
      lastSeen: timestamp
    }
    ```
  - Note: Presence and [element] data share same RTDB location

- [ ] **7.2: Create Presence Service**

  - Files to create: `src/services/presence.js`
  - Function: `setUserOnline([id], userId, name, [attr])`
  - Function: `setUserOffline([id], userId)`
  - Function: `subscribeToPresence([id], callback)`
  - Use `onDisconnect()` to auto-set offline

- [ ] **7.3: Create Presence Hook**

  - Files to create: `src/hooks/usePresence.js`
  - Set user online on mount
  - Subscribe to presence changes
  - Return: `onlineUsers` array

- [ ] **7.4: Build Presence List Component**

  - Files to create: `src/components/Collaboration/PresenceList.jsx`
  - Display list of online users
  - Show user [attribute] [visual] + name
  - Show count: "[X] users online"

- [ ] **7.5: Build User Presence Badge**

  - Files to create: `src/components/Collaboration/UserPresence.jsx`
  - Avatar/initial with user [attribute]
  - Tooltip with full name

- [ ] **7.6: Add Presence to Navbar**

  - Files to update: `src/components/Layout/Navbar.jsx`
  - Include PresenceList component
  - Position in [location]

- [ ] **7.7: Integrate Presence System**
  - Files to update: `src/App.jsx`
  - Initialize presence when [system] loads
  - Clean up on unmount

**PR Checklist:**

- [ ] Current user appears in presence list
- [ ] Other users appear when they join
- [ ] Users disappear when they leave (onDisconnect)
- [ ] User count is accurate (includes self)
- [ ] [Attributes] match [element] [attributes] (same generate function)
- [ ] Updates happen in real-time

**Evidence:** [Description of validation method once complete]

---

## PR #8: Testing, Polish & Bug Fixes

**Branch:** `fix/testing-polish`  
**Goal:** Ensure MVP requirements are met and fix critical bugs

### Tasks:

- [ ] **8.1: Multi-User Testing**

  - Test with [X-Y] concurrent users
  - Create [entities] simultaneously
  - Move [entities] simultaneously
  - Check for race conditions
  - **Status:** Needs manual testing

- [ ] **8.2: Performance Testing**

  - Create [X]+ [entities] and test FPS
  - Test [navigation actions] with many objects
  - Monitor [Database] read/write counts
  - Optimize if needed
  - **Status:** Needs manual testing with [X]+ [entities]

- [ ] **8.3: Persistence Testing**

  - All users leave [system]
  - Return and verify [entities] remain
  - Test page refresh mid-edit
  - Test browser close and reopen
  - **Status:** Persistence works, needs comprehensive testing

- [ ] **8.4: Error Handling**

  - Files to update: All service files
  - Add try/catch blocks
  - Display user-friendly error messages
  - Handle network failures gracefully

- [ ] **8.5: UI Polish**

  - Files to update: All component files
  - Consistent spacing and colors
  - Responsive button states
  - Loading states for all async operations

- [ ] **8.6: Verify Keyboard Shortcuts**

  - Files to verify: `src/components/[Feature]/[Feature].jsx`
  - [Shortcut A]: [action] (already implemented in PR #[X])
  - [Shortcut B]: [action] (optional enhancement)
  - Note: [Advanced feature] is out of scope for MVP

- [ ] **8.7: Cross-Browser Testing**

  - Test in Chrome, Firefox, Safari
  - Fix any compatibility issues
  - **Status:** Needs manual testing

- [ ] **8.8: Document Known Issues**
  - Files to update: `README.md`
  - List any known bugs or limitations
  - Add troubleshooting section

**PR Checklist:**

- [ ] All MVP requirements pass
- [ ] No console errors
- [ ] Smooth performance on test devices
- [ ] Works in multiple browsers
- [ ] Error messages are helpful

---

## PR #9: Deployment & Final Prep

**Branch:** `deploy/production`  
**Goal:** Deploy to production and finalize documentation

### Tasks:

- [ ] **9.1: Configure [Hosting Service]**

  - Files to create: `[hosting-config].json`, `.[hosting-rc]`
  - Run: `[hosting-cli] init hosting`
  - Set public directory to `dist`

- [ ] **9.2: Update Environment Variables**

  - Create production [backend] project (or use same)
  - Files to update: `.env.example`
  - Document all required env vars

- [ ] **9.3: Build Production Bundle**

  - Run: `npm run build`
  - Test production build locally
  - Check bundle size

- [ ] **9.4: Deploy to [Hosting Service]**

  - Run: `[deployment-command]`
  - Test deployed URL
  - Verify all features work in production
  - **Status:** Ready to deploy, not yet deployed

- [ ] **9.5: Set Up [Database A] Security Rules**

  - Files to create: `[database-a].rules`
  - Allow authenticated users to read/write
  - Validate [entity] schema
  - Deploy rules: `[deployment-command]`

- [ ] **9.6: Set Up [Database B] Rules**

  - Files to create: `[database-b].rules.json`
  - Allow authenticated users read/write
  - Deploy rules: `[deployment-command]`

- [ ] **9.7: Update README with Deployment Info**

  - Files to update: `README.md`
  - Add live demo link
  - Add deployment instructions
  - Add architecture diagram (optional)

- [ ] **9.8: Final Production Testing**

  - Test with [X] concurrent users on deployed URL
  - Verify auth works
  - Verify [entities] sync
  - Verify [real-time elements] work
  - Verify presence works
  - **Status:** Needs testing after deployment

- [ ] **9.9: Create Demo Video Script**
  - Outline key features to demonstrate
  - Prepare [X] browser windows for demo
  - **Status:** Needs creation

**PR Checklist:**

- [ ] App deployed and accessible via public URL
- [ ] Auth works in production
- [ ] Real-time features work in production
- [ ] [X]+ concurrent users tested successfully
- [ ] README has deployment link and instructions
- [ ] Security rules deployed and working

---

## MVP Completion Checklist

### Required Features:

- [ ] Basic [system] with [key capabilities] ([dimensions/limits])
- [ ] [Entity types] with [default styling]
- [ ] Ability to create, move, and delete [entities]
- [ ] Object locking (first user to drag locks the object)
- [ ] Real-time sync between [X]+ users (<[Y]ms)
- [ ] Multiplayer [real-time elements] with [identifiers] and unique [attributes]
- [ ] Presence awareness (who's online)
- [ ] User authentication ([auth methods])
- [ ] Deployed and publicly accessible

### Performance Targets:

- [ ] [Target FPS] during all interactions
- [ ] [Entity] changes sync in <[X]ms
- [ ] [Element] positions sync in <[Y]ms
- [ ] Support [X]+ simple [entities] without FPS drops
- [ ] Support [Y]+ concurrent users without degradation

### Testing Scenarios:

- [ ] [X] users editing simultaneously in different browsers
- [ ] User A drags [entity] → User B sees it locked and cannot move it
- [ ] Lock releases when User A stops dragging → User B can now move it
- [ ] User A deletes [entity] → disappears for User B immediately
- [ ] One user refreshing mid-edit confirms state persistence
- [ ] Multiple [entities] created and moved rapidly to test sync performance
- [ ] Test with [X]+ [entities] to verify performance target

---

## Post-MVP: Phase 2 Preparation

**Next PRs (After MVP Deadline):**

- PR #10: [Enhancement A]
- PR #11: [Enhancement B]
- PR #12: [Feature C]
- PR #13: [Feature D]
- PR #14: [Feature E]
- PR #15: [Feature F]