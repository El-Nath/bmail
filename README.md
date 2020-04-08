
# bmail

Simple email sender for go, credit to stackoverflow


## Installation

    $ go get -u github.com/El-Nath/bmail

## Usage

    package main
    
    import (
    	"fmt"
    	"github.com/El-Nath/bmail"
    )
    
    func main() {
      rP := "someone@mail.com" // can be multiple, ex : someone@mail.com,somehow@mail.com
      sB := "Email's Subject"
      eM := "Input you message"

      sD := bmail.NewSender("from@mail.com", "password", "mail.server.com", "1337")
      rV := []string{rP}
      
      bM := sD.WriteHTMLEmail(rV, sB, eM)
      sT, m := sender.SendMail(rV, sB, bM)
      
      //Do your thing based on the result
      fmt.Println(sT, m)
    }
### Success sending an email
Message :

    true sent


### Failed sending an email
Message (example using gmail) :

   

    535 5.7.8 Username and Password not accepted. Learn more at
    5.7.8  https://support.google.com/mail/?p=BadCredentials r70sm14794160pfr.116 - gsmtpfalse
