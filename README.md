I learn [Next.js](https://nextjs.org/)     
with the help of the official 
tutorial     
[Learn Next.js](https://nextjs.org/learn?utm_source=next-site&utm_medium=homepage-cta&utm_campaign=home)

While making Chapter 5, Section "Pattern: Showing active links" I faced the annoying error , something like :   
```
Unhandled Runtime Error
Error: Unsupported Server Component type: undefined
``` 
The solution was to terminate the program and restart it with the   
```
pnpm dev
```

Chapter 6 : some problems (at 09/10/2024), see [issue on GitHub too](https://github.com/vercel/next-learn/issues/883)
If you will literally follow the tutorial how to seed the DB, you will get 
```
'Uncomment this file and remove this line. You can delete this file when you are finished.'
```
at the 
```
localhost:3000/seed 
```
not 
```
'Database seeded successfully'
```
To seed the DB it is need to delete first 'Return' statement, this one: 
```
  return Response.json({
    message:
      'Uncomment this file and remove this line. You can delete this file when you are finished.',
  });
``` 
Otherwise the code, which actually seed the DB ( the 'try' block) is not reachable. 
