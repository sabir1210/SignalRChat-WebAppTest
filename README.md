app.UseCors(options => options.WithOrigins("http://localhost:8080").AllowAnyMethod()
                         .AllowAnyHeader()
                         .AllowCredentials()); 

app.UseEndpoints(endpoints =>
                         {
                             endpoints.MapControllers();
                             endpoints.MapHub<ChatHub>("/chatHub");
                         });

add this code to program.cs
