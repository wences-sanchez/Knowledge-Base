title:: Readwise/What Is /Dev/Null 2>&1? (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "What Is /Dev/Null 2>&1?"
category:: #articles
url:: https://stackoverflow.com/questions/10508843/what-is-dev-null-21

- Highlights first synced by [[Readwise]] [[Tuesday, 07-02-2023]]
	- -
		- About how to redirect to /dev/null .bash #flashcard
			- >> /dev/null redirects standard output (stdout) to /dev/null, which discards it.
			  
			  (The >> seems sort of superfluous, since >> means append while > means truncate and write, and either appending to or writing to /dev/null has the same net effect. I usually just use > for that reason.)
			  
			  2>&1 redirects standard error (2) to standard output (1), which then discards it as well since standard output has already been redirected.
			    
			    
			        
			            
			            
			                
			  
			  
			  
			    
			  
			            
			                ShareShare a link to this answer Copy linkCC BY-SA 3.0
			            
			  
			  
			  
			            
			                
			                    Follow
			                Follow this answer to receive notifications
			            
			  
			  
			  
			  
			  
			  
			    
			    
			  
			            
			            
			  
			    
			        edited Apr 9 '14 at 12:27
			    
			    
			        
			    
			    
			        
			        
			            
			        
			    
			  
			            
			  
			  
			            
			                
			    
			        answered May 9 '12 at 1:49
			    
			    
			        
			    
			    
			        ziggzigg
			        
			            18.6k77 gold badges3434 silver badges5454 bronze badges
			        
			    
			  
			  
			  
			            
			        
			        
			    
			    
			    
			  
			  
			  
			  
			  
			            5 
			    
			        
			            
			  
			                        
			        
			            
			                    18
			            
			        
			        
			            
			                
			                What does the & symbol indicate in there 2>&1.
			                
			              
			  – Nobody
			                
			                Jun 28 '17 at 9:47
			            
			        
			    
			    
			        
			            
			                    32
			            
			        
			        
			            
			                
			                & indicates a file descriptor. There are usually 3 file descriptors - standard input, output, and error.
	- -