
Deliverable for Task 1: Take a screenshot of all the GPOs created for this homework assignment. To find these, launch the Group Policy Management tool, select Group Policy Objects, and take a screenshot of the GPOs you've created.

![pic 1](IMAGE/TASK1GPO.png)

Deliverable for Task 2: Submit a screenshot of the different Account Lockout policies in Group Policy Management Editor. It should show the three values you set under the Policy and Policy Setting columns.

![pic 1](IMAGE/TASK2LOCKOUT.png)

Deliverable for Task 3: Submit a screenshot of the different Windows PowerShell policies within the Group Policy Management Editor. Four of these should be enabled.

![pic 1](IMAGE/TASK3POWERSHELL.png)

Deliverable for Task 4: Submit a copy of your enum_acls.ps1 script.

![pic 1](IMAGE/TASK4.png)

<br>

Updated version
![pic 1](IMAGE/2ndscript.png)

Deliverable for Bonus Task 5: Submit a screenshot of the contents of one of your transcribed PowerShell logs or a copy of one of the logs.

![pic 1](IMAGE/BONUS5LOG1.png)

<br>
#############################################
<br>
A copy of my powershell script below.

$directory = $(Get-ChildItem '*') 

foreach ( $item in $directory) {
   Get-Acl $item | Out-File -FilePath C:\Users\sysadmin\Documents\enum_acls.txt -Append
}
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 P a t h       O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                       
 
 - - - -       - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                       
 
 a d d i n s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                 
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h             O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                 
 
 - - - -             - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                 
 
 a p p c o m p a t   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                   
 
 - - - -           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                   
 
 a p p p a t c h   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 A p p R e a d i n e s s   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ A u t h e n t i c a t e d   U s e r s   A l l o w     R e a d ,   S y n c h r o n i z e . . .                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                     A c c e s s                                                                                                                                                                                                                                                                                                             
 
 - - - -           - - - - -                                     - - - - - -                                                                                                                                                                                                                                                                                                             
 
 a s s e m b l y   B U I L T I N \ A d m i n i s t r a t o r s   B U I L T I N \ A d m i n i s t r a t o r s   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                 
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                   
 
 - - - -           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                   
 
 b c a s t d v r   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 B o o t   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     - 1 6 1 0 6 1 2 7 3 6 . . .                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                   
 
 - - - -           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                   
 
 B r a n d i n g   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h         O w n e r                                     A c c e s s                                                                                                                                                                                                                                                                                                               
 
 - - - -         - - - - -                                     - - - - - -                                                                                                                                                                                                                                                                                                               
 
 C b s T e m p   B U I L T I N \ A d m i n i s t r a t o r s   B U I L T I N \ A d m i n i s t r a t o r s   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h               O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                               
 
 - - - -               - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                               
 
 C o n t a i n e r s   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                         
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                               A c c e s s                                                                 
 
 - - - -   - - - - -                               - - - - - -                                                                 
 
 C S C     N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     F u l l C o n t r o l 
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h         O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                     
 
 - - - -         - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                     
 
 C u r s o r s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h     O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                         
 
 - - - -     - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                         
 
 d e b u g   N T   A U T H O R I T Y \ S Y S T E M   A P P L I C A T I O N   P A C K A G E   A U T H O R I T Y \ A L L   A P P L I C A T I O N   P A C K A G E S   D e n y     F u l l C o n t r o l . . .                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                 O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                             
 
 - - - -                 - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                             
 
 d i a g n o s t i c s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     - 1 6 1 0 6 1 2 7 3 6 . . .                                                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h             O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                 
 
 - - - -             - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                 
 
 D i a g T r a c k   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                     O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                         
 
 - - - -                     - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                         
 
 D i g i t a l L o c k e r   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                                           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                   
 
 - - - -                                           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                   
 
 D o w n l o a d e d   P r o g r a m   F i l e s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h     O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                         
 
 - - - -     - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                         
 
 e n - U S   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h     O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                         
 
 - - - -     - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                         
 
 F o n t s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                                     O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                         
 
 - - - -                                     - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                         
 
 G a m e B a r P r e s e n c e W r i t e r   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                     O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                         
 
 - - - -                     - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                         
 
 G l o b a l i z a t i o n   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                           
 
 H e l p   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                 O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                             
 
 - - - -                 - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                             
 
 I d e n t i t y C R L   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 I M E     N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                                     O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                         
 
 - - - -                                     - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                         
 
 I m m e r s i v e C o n t r o l P a n e l   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 I N F     N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                 O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                             
 
 - - - -                 - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                             
 
 I n p u t M e t h o d   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h             O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                 
 
 - - - -             - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                 
 
 L 2 S c h e m a s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                             O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                 
 
 - - - -                             - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                 
 
 L i v e K e r n e l R e p o r t s   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                           
 
 L o g s   N T   A U T H O R I T Y \ S Y S T E M   B U I L T I N \ A d m i n i s t r a t o r s   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h     O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                         
 
 - - - -     - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                         
 
 M e d i a   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                     O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                         
 
 - - - -                     - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                         
 
 M i c r o s o f t . N E T   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h             O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                 
 
 - - - -             - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                 
 
 M i g r a t i o n   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h             O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                 
 
 - - - -             - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                 
 
 M o d e m L o g s   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 O C R     N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     - 1 6 1 0 6 1 2 7 3 6 . . .                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                             O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                 
 
 - - - -                             - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                 
 
 O f f l i n e   W e b   P a g e s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h         O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                     
 
 - - - -         - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                     
 
 P a n t h e r   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                 O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                             
 
 - - - -                 - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                             
 
 P e r f o r m a n c e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                           
 
 P L A     N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                             O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                 
 
 - - - -                             - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                 
 
 P o l i c y D e f i n i t i o n s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                     A c c e s s                                                                                                                                                       
 
 - - - -           - - - - -                                     - - - - - -                                                                                                                                                       
 
 P r e f e t c h   B U I L T I N \ A d m i n i s t r a t o r s   B U I L T I N \ A d m i n i s t r a t o r s   A l l o w     F u l l C o n t r o l . . .                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                 O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                             
 
 - - - -                 - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                             
 
 P r i n t D i a l o g   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                           
 
 P r o v i s i o n i n g   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                                     A c c e s s                                                                                                                                                                                                                                             
 
 - - - -                   - - - - -                                     - - - - - -                                                                                                                                                                                                                                             
 
 R e g i s t r a t i o n   B U I L T I N \ A d m i n i s t r a t o r s   E v e r y o n e   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                       O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                       
 
 - - - -                       - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                       
 
 R e m o t e P a c k a g e s   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ A u t h e n t i c a t e d   U s e r s   A l l o w     - 1 6 1 0 6 1 2 7 3 6 . . .                                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                   
 
 - - - -           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                   
 
 r e s c a c h e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     - 1 6 1 0 6 1 2 7 3 6 . . .                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h             O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                 
 
 - - - -             - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                 
 
 R e s o u r c e s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                   
 
 - - - -           - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                   
 
 S c h C a c h e   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h         O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                     
 
 - - - -         - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                     
 
 s c h e m a s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                   
 
 - - - -           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                   
 
 s e c u r i t y   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                         O w n e r                                     A c c e s s                                                                                                                                                                                                                                                                                               
 
 - - - -                         - - - - -                                     - - - - - -                                                                                                                                                                                                                                                                                               
 
 S e r v i c e P r o f i l e s   B U I L T I N \ A d m i n i s t r a t o r s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                         
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 S e r v i c e S t a t e   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S E R V I C E   A l l o w     E x e c u t e F i l e . . .                                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h             O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                 
 
 - - - -             - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                 
 
 s e r v i c i n g   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     - 1 6 1 0 6 1 2 7 3 6 . . .                                                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h     O w n e r                                     A c c e s s                                                                                                                                                                                                                                                                                                                   
 
 - - - -     - - - - -                                     - - - - - -                                                                                                                                                                                                                                                                                                                   
 
 S e t u p   B U I L T I N \ A d m i n i s t r a t o r s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                         O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                     
 
 - - - -                         - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                     
 
 S h e l l C o m p o n e n t s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                   
 
 - - - -                           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                   
 
 S h e l l E x p e r i e n c e s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 S K B     N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                                   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                           
 
 - - - -                                   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                           
 
 S o f t w a r e D i s t r i b u t i o n   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h       O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                       
 
 - - - -       - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                       
 
 S p e e c h   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                 
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                       O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                       
 
 - - - -                       - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                       
 
 S p e e c h _ O n e C o r e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                 
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h       O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                       
 
 - - - -       - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                       
 
 S y s t e m   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                 
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                   
 
 - - - -           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                   
 
 S y s t e m 3 2   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h               O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                               
 
 - - - -               - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                               
 
 S y s t e m A p p s   N T   A U T H O R I T Y \ S Y S T E M   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                         
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                         O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                     
 
 - - - -                         - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                     
 
 S y s t e m R e s o u r c e s   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     - 1 6 1 0 6 1 2 7 3 6 . . .                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                   
 
 - - - -           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                   
 
 S y s W O W 6 4   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                           
 
 T A P I   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                         
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h     O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                         
 
 - - - -     - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                         
 
 T a s k s   N T   A U T H O R I T Y \ S Y S T E M   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                           
 
 T e m p   N T   A U T H O R I T Y \ S Y S T E M   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h         O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                     
 
 - - - -         - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                     
 
 t r a c i n g   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                   
 
 - - - -           - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                   
 
 t w a i n _ 3 2   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                             
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                           
 
 V s s     N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ L O C A L   S E R V I C E   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 W a a S   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     - 1 6 1 0 6 1 2 7 3 6 . . .                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 W e b     N T   S E R V I C E \ T r u s t e d I n s t a l l e r   C R E A T O R   O W N E R   A l l o w     2 6 8 4 3 5 4 5 6 . . .                                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h       O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                       
 
 - - - -       - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                       
 
 W i n S x S   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     - 1 6 1 0 6 1 2 7 3 6 . . .                                                                                                                                                                                                                                 
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h             O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                 
 
 - - - -             - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                 
 
 b f s v c . e x e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                           
 
 b o o t s t a t . d a t   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                       O w n e r                                     A c c e s s                                                                                                                                                                                                                                                                                                 
 
 - - - -                       - - - - -                                     - - - - - -                                                                                                                                                                                                                                                                                                 
 
 D t c I n s t a l l . l o g   B U I L T I N \ A d m i n i s t r a t o r s   B U I L T I N \ A d m i n i s t r a t o r s   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                               O w n e r                                     A c c e s s                                                                                                                                                                                                                                                                                         
 
 - - - -                               - - - - -                                     - - - - - -                                                                                                                                                                                                                                                                                         
 
 E n t e r p r i s e E v a l . x m l   B U I L T I N \ A d m i n i s t r a t o r s   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                   
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                           
 
 e x p l o r e r . e x e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                           
 
 H e l p P a n e . e x e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h       O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                       
 
 - - - -       - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                       
 
 h h . e x e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                                 
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                                     A c c e s s                                                                                                                                                                                                                                                                                                     
 
 - - - -                   - - - - -                                     - - - - - -                                                                                                                                                                                                                                                                                                     
 
 l s a s e t u p . l o g   B U I L T I N \ A d m i n i s t r a t o r s   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h         O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                     
 
 - - - -         - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                     
 
 m i b . b i n   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                 O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                             
 
 - - - -                 - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                             
 
 n o t e p a d . e x e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h           O w n e r                                     A c c e s s                                                                                                                                                                                                                                                                                                             
 
 - - - -           - - - - -                                     - - - - - -                                                                                                                                                                                                                                                                                                             
 
 P F R O . l o g   B U I L T I N \ A d m i n i s t r a t o r s   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                 O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                             
 
 - - - -                 - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                             
 
 r e g e d i t . e x e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                       
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                           
 
 s p l w o w 6 4 . e x e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h               O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                               
 
 - - - -               - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                               
 
 s y s t e m . i n i   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                         
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                           
 
 t w a i n _ 3 2 . d l l   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h         O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                                     
 
 - - - -         - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                                     
 
 w i n . i n i   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                                               
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                             O w n e r                               A c c e s s                                                                                                                                                                                                                                                                                                 
 
 - - - -                             - - - - -                               - - - - - -                                                                                                                                                                                                                                                                                                 
 
 W i n d o w s U p d a t e . l o g   N T   A U T H O R I T Y \ S Y S T E M   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     F u l l C o n t r o l . . .                                                                                                                                                                                                                           
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                           
 
 w i n h l p 3 2 . e x e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h                   O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                           
 
 - - - -                   - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                           
 
 W M S y s P r 9 . p r x   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                     
 
 
 
 
 
 
 
 
 
         D i r e c t o r y :   C : \ W i n d o w s 
 
 
 
 
 
 P a t h             O w n e r                                               A c c e s s                                                                                                                                                                                                                                                                                                 
 
 - - - -             - - - - -                                               - - - - - -                                                                                                                                                                                                                                                                                                 
 
 w r i t e . e x e   N T   S E R V I C E \ T r u s t e d I n s t a l l e r   N T   A U T H O R I T Y \ S Y S T E M   A l l o w     R e a d A n d E x e c u t e ,   S y n c h r o n i z e . . .                                                                                                                                                                                           
 
 
 
 
 
 
