# login/signup

logging in on the signup page sends a request to `https://bliish.com/api/v1/auth/magic-link`

request payload looks like the following more or less
{"email":"example@mail.com","turnstileToken":"0.0ywc46IsTk8kc9HP_ajdsfashdfj","intent":"signup"}

email is the email thats attempting to signup, turnstile token is the token given after passing the cloudflare challenge, and intent can either be "signup" or "login" depending on what action the user is doing

magic link authentication has been removed in bliish lite but the endpoint used to be `https://bliish.com/lite/auth?next=%2Flite&sent=1&email=emailhere` with the email parameter being the email that the magic link would get sent to
