# Use a lightweight base image
FROM python:3.9-slim

# Create a non-root user
RUN useradd -m appuser

# Set the working directory
WORKDIR /app

# Copy the application files
COPY simple_time_service.py requirements.txt ./

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Change ownership and switch to non-root user
RUN chown -R appuser:appuser /app
USER appuser

# Expose the application port
EXPOSE 6000

# Command to run the application
CMD ["python", "simple_time_service.py"]

