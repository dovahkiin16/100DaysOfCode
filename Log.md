## Day 0: Re-do
I'm going to Re-do my 100 days of code challenge. I've been so busy in the last few 
because of school and personal related things. I've thought of making a medium blog, but
it seems like long posts aren't my thing. Maybe this kind of micro blogging works out for me.

## Day 1: I've already started
I already have an on-going project that I'll be personally using on a day to day basis.
Its the web-based expense tracking app. The plan is after I finished the front-end, I'll
move my data from firebase to other free hosting such as heroku.

I've already added the table for transactions. Although its not much, it should be fine for
starters. And so today I added a couple of formatting, refactoring, and transaction form and dialog.

## Day 2: Still a long way to go
I've only coded for less than an hour today. Although I've only coded for a short time, I've learned
an important lesson (for me at least) that I should always put the mutations and actions to the
methods section of a vue component. I refactored the form of the transaction to use the store for its
data model.

## Day 3: Transaction complete
I added the firestore integration for the addition of transaction. I used 
`firestore.firebase.Timestamp.fromDate(new Date())` to get the current time and date for my
transaction dates since Firebase doesn't have their own `NOW()` equivalent from SQL aside from the said 
technique.

## Day 4: Google, Who is this?
Today, I added a way to login. Currently, I'm only using google's firebase auth and will
add new ways to login if I see it fit. I refactored the `route.js` to have its own directory since
I'll have new files like `routeRules.js` that is related to the routes. Refactor routes so that
they'll use names defined on a constants file. Refactor store so that they're in a directory and
add constants file.

## Day 5: Refactor
Today I refactored the store to be on their own module. I also namespaced them. I might remove
the namespacing since I believe it introduced more layers of the store than wanted eg. rootGetters etc.
I removed the type column on the transaction table and add the type indication via text color and
additional indication via text (+ and -).

## Day 6: New Version
I found out that there is a new version of Vue. So without hesitation, I updated my project's 
dependency. On the new version of Vue, there is a change of syntax for slots. So, I refactored my
project to use the new syntax.

## Day 7: A new list
I believe my old list of transaction isn't really that nice. So I redesigned it. I stopped using
the data table and just used a `v-list`. It gives a much better look just like a native android app.
For today, I also added the login persistence.

## Day 8: New feature
I've been thinking should should I make a balance feature where you can see what's left of 
money. So, I started making those changes a few days now. But I'm still thinking of where to
put it. So, for today. I only made the category as a list. So that I can make a median expense
for each category.

## Day 9: Moment
I added moment for formatting my date on the transaction items.

## Day 10: Navigation Drawer
I added the navigation drawer for today.

## Day 11: Fixing typos, Refactor and Adding Firebase rules
I fixed some typos. I refactored the transaction form by removing the type. The type is based on
the transaction category so I just made it rely on the category. And also, I replaced the `v-select`
text to be '**_category_** (**_type_**)'. I'm also adding Firebase security rules as I haven't touched
it ever since I created the app. It kept bugging me since I left my firebase unsecured.
