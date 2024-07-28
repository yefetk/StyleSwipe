<script>
import { supabase } from "$lib/supabaseClient.js"

let email = ""
let password = ""

function checkifPasswordIsOK(passW) {
    // ensures that there's at least one digit, one lowercase, one uppercase, and one symbol in the string and is at least 6 characters long
    let pattern = /^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[!@#$%^&*/<>,.+-=~$ß]).{6,}$/;
    return pattern.test(passW);
}

async function userSignUp(useremail, userpassword) {
    // checks if the password matches the requirements 
    const doesItPass = checkifPasswordIsOK(userpassword) 
    if (!doesItPass) {
        alert("Password must be at least 6 characters long, must contain lowercase, uppercase, a number and a special character")
    } else {
        // uses the supabase sdk to sign up the user
        try { 
    const { data, error } = await supabase.auth.signUp({email: useremail, password: userpassword, options: {emailRedirectTo: "/welcome"}})
    alert(`Confirm your email! We've sent a confirmation email to ${email}`)
    return data
        } catch (err) {
            console.error(err)
        }
    }
}

async function handleSignInWithGoogle() {
await supabase.auth.signInWithOAuth({
  provider: "google",
  options: {
    redirectTo: `/auth/callback`,
  },
})

}
</script>

<body>

<h1 style="text-align:center">Welcome to StyleSwipe</h1>

<div class="signup_panel">
<h3>Sign up</h3>
<form>
    <button on:click={() => userSignUp(email, password)}>Join StyleSwipe</button>
</form>
<p>Or</p>

<button on:click={handleSignInWithGoogle}> Sign up with Google </button>

<hr>
<p>Already have an account? <a href="/login">Log in</a></p>
</div>
</body>
<style>
body {
    font-family: Arial, Helvetica, sans-serif;
}
.signup_panel {
    text-align: center;
}

</style>



<div class="flex flex-col w-full md:w-1/2 xl:w-2/5 2xl:w-2/5 3xl:w-1/3 mx-auto p-8 md:p-10 2xl:p-12 3xl:p-14 bg-[#ffffff] rounded-2xl shadow-xl">
    <div class="flex flex-col justify-center mx-auto items-center gap-3 pb-4">
         <h1 class="text-5xl font-bold text-[#4B5563] text-[#4B5563] my-auto">StyleSwipe</h1>

    </div>
    <div class="text-xl font-light text-[#6B7280] pb-8 mx-auto">Sign up for an account</div>
    <form class="flex flex-col">
        <div class="pb-2">
            <label for="email" class="block mb-2 text-sm font-medium text-[#111827]">Email</label>
            <div class="relative text-gray-400"><span class="absolute inset-y-0 left-0 flex items-center p-1 pl-3"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-mail"><rect width="20" height="16" x="2" y="4" rx="2"></rect><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"></path></svg></span> 
                <input type="email" name="email" id="email" bind:value={email} class="pl-12 mb-2 bg-gray-50 text-gray-600 border focus:border-transparent border-gray-300 sm:text-sm rounded-lg ring ring-transparent focus:ring-1 focus:outline-none focus:ring-gray-400 block w-full p-2.5 rounded-l-lg py-3 px-4" placeholder="name@company.com" autocomplete="off">
            </div>
        </div>
        <div class="pb-6">
            <label for="password" class="block mb-2 text-sm font-medium text-[#111827]">Password</label>
            <div class="relative text-gray-400"><span class="absolute inset-y-0 left-0 flex items-center p-1 pl-3"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-asterisk"><rect width="18" height="18" x="3" y="3" rx="2"></rect><path d="M12 8v8"></path><path d="m8.5 14 7-4"></path><path d="m8.5 10 7 4"></path></svg></span> 
                <input type="password" name="password" id="password" bind:value={password} placeholder="••••••••••" class="pl-12 mb-2 bg-gray-50 text-gray-600 border focus:border-transparent border-gray-300 sm:text-sm rounded-lg ring ring-transparent focus:ring-1 focus:outline-none focus:ring-gray-400 block w-full p-2.5 rounded-l-lg py-3 px-4" autocomplete="new-password">
            </div>
        </div>
        <button type="submit" on:click={() = userSignUp(email, password)} class="w-full text-[#FFFFFF] bg-[#4F46E5] focus:ring-4 focus:outline-none focus:ring-primary-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center mb-6">Sign Up</button>
        <div class="text-xl font-light text-[#6B7280] text-center">Already have an account? <a href="/login" class="font-medium text-[#4F46E5] hover:underline">Login</a>

        </div>
    </form>
    <div class="relative flex py-8 items-center">
        <div class="flex-grow border-t border-[1px] border-gray-200"></div> <span class="flex-shrink mx-4 font-medium text-gray-500">OR</span> 
        <div class="flex-grow border-t border-[1px] border-gray-200"></div>
    </div>
    <form>
        <div class="flex flex-row gap-2 justify-center">
            <button on:click={handleSignInWithGoogle}> Sign up with Google </button>
        </div>
    </form>
</div>