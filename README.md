# CleanStore

[![IDE](https://img.shields.io/badge/Xcode-10-blue.svg)](https://developer.apple.com/xcode/)
[![Language](https://img.shields.io/badge/swift-4-orange.svg)](https://swift.org)
[![Platform](https://img.shields.io/badge/iOS-12-green.svg)](https://developer.apple.com/ios/)
[![License](https://img.shields.io/github/license/Clean-Swift/CleanStore.svg)](LICENSE)

A sample iOS app built using the Clean Swift architecture. Clean Swift is Uncle Bob's Clean Architecture applied to iOS and Mac projects. CleanStore demonstrates Clean Swift by implementing the create order use case described by in Uncle Bob's talks.

About the Clean Swift Architecture
	Clean Swift (a.k.a VIP) is Uncle Bob’s Clean Architecture applied to iOS and Mac projects. The Clean Swift Architecture is not a framework. It is a set of Xcode templates to generate the Clean Architecture components for you. That means you have the freedom to modify the templates to suit your needs.


Steps to setup Clean Architecture (a.k.a VIP - ViewController Interactor Presentor)
1. Download the template
	- https://drive.google.com/file/d/1BIj7j_4UZikdwVtIkoBZEgeijrWTNMP4/view
2. Install the template 
	- After unzipping the file, you should open Terminal and access the root directory of the folder by using cd CleanSwift .
	- Now, all you have to do is running the following command make install_templates. If you wish to uninstall the template just run make uninstall_templates.
	- To verify if the template has been installed properly, you should open the following path ~Library/Developer/Xcode/Templates/File Templates and search for a folder named CleanSwift.
3. Create a New Scene
	- Create a new test project (or open some of your existing ones), and go to File -> New -> File (or press ⌘N) -> Scroll down to CleanSwift section and Select 'Scene'
	- By pressing on the Scene and adding the desired name, it will generate all the needed files at once.

Refer link: https://medium.com/swift2go/installing-the-clean-swift-template-in-xcode-6b4367006827


Follow the following Folder Structure in Xcode
- Sample Project
	- Scenes 
		- Create Order (Group contains code that deals with Create an order)
			- CreateOrderModel
			- CreateOrderRouter
			- CreateOrderWorker
			- CreateOrderInteractor
			- CreateOrderPresenter
			- CreateOrderViewController
		- Delete Order
		- Update Order
	- Helper
		- Constants.swift (constants)
		- Extesntions.swift (contains extentions used in app)
		- DataManager.swift (Singleton class)

Note: Organize each use case under a new group nested within Scenes.


Communication
	- The communication between the components is done with protocols. Each component will contain protocols which will be used for receiving and passing data between them. Worker communicates with Interactor, then Interactor with Presenter and Presenter with ViewController.
