---
layout: "default"
title: "🌟 pic-opendal - Easily Upload Images to Cloud Storage"
description: "✨ Upload images effortlessly to multiple cloud storage services using a simple CLI tool with customizable options and profile support."
---
# 🌟 pic-opendal - Easily Upload Images to Cloud Storage

[![Download pic-opendal](https://img.shields.io/badge/Download-pic--opendal-blue)](https://github.com/Unostores/pic-opendal/releases)

## 🚀 Getting Started

Welcome to **pic-opendal**! This simple command-line tool lets you upload your images to many popular cloud storage services. With this guide, you will learn how to download, install, and set up pic-opendal.

## 📥 Download & Install

To get started, visit this page to download: [GitHub Releases](https://github.com/Unostores/pic-opendal/releases).

### Step-by-Step Installation

1. **Visit the Download Page:**
   Open your web browser and go to [GitHub Releases](https://github.com/Unostores/pic-opendal/releases).

2. **Select the Latest Release:**
   Look for the latest version and download the file that suits your operating system.

3. **Install the Tool:**
   For users with Rust installed, you can install pic-opendal using Cargo. Open your terminal and run this command:

   ```bash
   cargo install pic-od
   ```

## ⚙️ Configuration

After installing, you need to set up a configuration file for pic-opendal. Follow these steps:

1. **Create a Configuration File:**
   Use your favorite text editor to create a file at the following path:

   ```bash
   ~/.config/pic-od/config.toml
   ```

2. **Set Up Your Profiles:**
   Copy and paste the following example into your configuration file:

   ```toml
   current_profile = "default"

   [profiles.default]
   type = "s3"
   bucket = "my-bucket"
   region = "us-east-1"
   access_key_id = "YOUR_ACCESS_KEY"
   secret_access_key = "YOUR_SECRET_KEY"
   root = "/images"
   base_url = "https://cdn.example.com"
   filename_format = "{date}/{name}"

   [profiles.backup]
   type = "gcs"
   bucket = "backup-bucket"
   credential_path = "/path/to/credentials.json"
   base_url = "https://storage.googleapis.com/backup-bucket"
   ```

3. **Update Your Credentials:**
   Replace the placeholders like `YOUR_ACCESS_KEY` and `YOUR_SECRET_KEY` with your actual cloud storage credentials.

## 🌐 Supported Storage Backends

pic-opendal supports various cloud storage solutions, including:

- **S3** (Amazon Simple Storage Service)
- **GCS** (Google Cloud Storage)
- **Azure Blob** (Microsoft Azure)
- **OSS** (Alibaba Cloud)
- **COS** (Tencent Cloud Object Storage)

## 📂 How to Use

Using pic-opendal is straightforward once you have set up your configuration. Follow these steps to upload your images:

1. **Open the Terminal:**
   Launch your terminal application.

2. **Run the Command:**
   Use the following command to start uploading images:

   ```bash
   pic-od upload [path/to/your/image]
   ```

   Replace `[path/to/your/image]` with the location of your image file.

3. **Check Upload Status:**
   After the command runs, ensure that the upload was successful by checking your cloud storage.

## 📝 Advanced Configuration

You can customize filename formats using template variables in your configuration file. For example, `{date}` adds the current date, and `{name}` keeps the original filename.

## 🔧 Troubleshooting

If you encounter issues, check the following:

- **Credentials:** Ensure your access keys are correct.
- **Configuration File:** Verify your config.toml file is in the right location and properly formatted.

## 🙋 Frequently Asked Questions

**1. Can I use pic-opendal with multiple cloud services?**

Yes, you can set up different profiles in your configuration file, enabling easy switching between storage providers.

**2. Do I need programming experience to use pic-opendal?**

No, pic-opendal is designed for users with no programming background. Follow the simple steps to upload your images.

**3. Where can I find more help?**

Visit our [documentation](https://github.com/Unostores/pic-opendal) on GitHub for more detailed instructions and support.

## 🎉 Conclusion

Now you are ready to use pic-opendal to easily upload your images to cloud storage. If you have any questions or feedback, feel free to reach out through our GitHub page.

Remember, to download the tool, visit: [GitHub Releases](https://github.com/Unostores/pic-opendal/releases). Enjoy uploading!