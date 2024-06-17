using System;
using System.IO; 

public class CPHInline
{
	
	public string originalFolder; 
	public string destinationFolder; 
	
	public bool Execute()
	{
		originalFolder = @"G:\My Drive\Twitch Cards\AllCards";
		destinationFolder = @"D:\Streaming Files\Card Pack Opener";
		
		
		//get 5 random images from the original folder. 
		
		string[] imageFiles = Directory.GetFiles(originalFolder);
		string[] randomImages = new string[5]; 
		int maxNumber = imageFiles.Length; 
		
		Random random = new Random();
		int randomNumber = random.Next(maxNumber); 
		for(int i = 0; i < 5; i++)
		{
			randomImages[i] =imageFiles[randomNumber]; 
			randomNumber = random.Next(maxNumber); 
		}
		
		//Copy the images to the destination folder. 
		for(int i = 0; i < randomImages.Length; i++)
		{
			string sourcePath = randomImages[i]; 
			string destinationPath = Path.Combine(destinationFolder, $"card{i + 1}.png"); 
			File.Copy(sourcePath, destinationPath, true); 
		}
		

		return true;
	}
}
