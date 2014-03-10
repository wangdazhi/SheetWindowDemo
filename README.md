SheetWindowDemo
===============

NSWindows show as Sheet 

#import <Cocoa/Cocoa.h>

@interface SheetDemoWC : NSWindowController
{
    IBOutlet NSPanel *theSheet;
    
}
- (IBAction) showTheSheet:(id)sender ;
@end



- (IBAction) showTheSheet:(id)sender {
    
    [NSApp beginSheet:theSheet
       modalForWindow:self.window
        modalDelegate:self
       didEndSelector:nil
          contextInfo:nil];
    
}

-(IBAction)endTheSheet:(id)sender {
    
    [NSApp endSheet:theSheet];
    [theSheet orderOut:sender];
    
}

