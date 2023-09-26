1. how does rust boot(call) the main() function?

   most languages have runtime system which is resposible 
   for things such as garbale collector in java, go-rutine 
   in go etc. this runtime need to be initialized before 
   running any program. there for need to initialized first.

    Before a Rust program actually starts running, there's a small helper program in the background (like a backstage worker) that gets everything ready. It's called crt0. This worker prepares things like a place to store information (a stack) and makes sure the program knows what it should do.

    crt0 is link to std lib. crt0 ---> initialized env ---> call main() function

    since we are not using std lib we need to define out own _start function


2. Linker error
   run : rustup target add thumbv7em-none-eabihf

