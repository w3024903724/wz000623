package com.yychatclient.controller;

import java.io.IOException;
import java.io.ObjectOutputStream;
import java.net.Socket;

import com.yychat.model.User;

public class ClientConnect {
	Socket s;
	
	public ClientConnect(){
		try{
			s=new Socket("127.0.0.1",3456);
		}catch(IOException e){
			e.printStackTrace();
		}
	}
	
	public void loginValidate(User user){
		//输入输出流，发送对象
		ObjectOutputStream oos;
		try{
			oos=new ObjectOutputStream(s.getOutputStream());
			//对象输出流,字节输出流对象类
			//把字节输出流，包装成对象
			oos.writeObject(user);
		}catch(IOException e){
			e.printStackTrace();
		}
	}
}
