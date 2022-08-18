# Google-Auth-Blazor-Demo

### program.cs
`code` 
builder.Services.AddAuthentication()
    .AddIdentityServerJwt()
    .AddGoogle(options =>
    {
        //google cloud console -> project -> redirect-url:https://localhost:5001/signin-google
        options.ClientId = builder.Configuration["Authentication:Google:ClientId"];
        options.ClientSecret = builder.Configuration["Authentication:Google:ClientSecret"];
    });
