package com.blog;

import org.hibernate.Session;

import java.util.Scanner;

public class Run {
	public static void main(String[] args) {

		Session session = HibernateSessionManager.getSessionFactory().openSession();
		session.beginTransaction();
		
		Scanner scanner = new Scanner(System.in);
		Post post = new Post();
		System.out.println("Enter Number of Post's you want to insert: ");
		int count = scanner.nextInt();

		Post[] arr = new Post[count];
		for(int i = 0; i < count; i++){
			System.out.println("Please Enter Title: ");
			post.setTitle(scanner.next());
			System.out.println("Please Enter Body: ");
			post.setBody(scanner.next());
		}

		session.save(post);
		session.getTransaction().commit();

	}

}
