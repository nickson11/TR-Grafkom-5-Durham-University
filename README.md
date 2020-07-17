# TR-Grafkom-5-Durham-University

#include<windows.h>
#include <GL/freeglut.h>

void init(void);
void tampil(void);
void mouse(int button, int state, int x, int y);
void keyboard(unsigned char, int, int);
void ukuran(int, int);
void mouseMotion(int x,int y);

float xrot = 0.0f;
float yrot = 0.0f;
float xdiff = 0.0f;
float ydiff = 0.0f;
bool mouseDown = false;
int is_depth;

int main (int argc, char **argv)
{
    glutInit(&argc, argv);
    glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGB);
    glutInitWindowSize(800, 800);
    glutInitWindowPosition(250, 80);
    glutCreateWindow("Kevin Harlim - 672018250");
    init();
	glutDisplayFunc(tampil);
	glutKeyboardFunc(keyboard);
	glutMouseFunc(mouse);
    glutMotionFunc(mouseMotion);
	glutReshapeFunc(ukuran);
    glutMainLoop();
    return 0;
}

void init(void)
{
    glClearColor(0.0, 0.0, 0.0, 1.0);
    //glMatrixMode(GL_PROJECTION);
    //glEnable(GL_LIGHTING);
    //glEnable(GL_COLOR_MATERIAL);
    //glEnable(GL_LIGHT0);
    glEnable(GL_DEPTH_TEST);
    is_depth = 1;
    glMatrixMode(GL_MODELVIEW);
    glPointSize(9.0);
    glLineWidth(6.0f);

}
void castil(){
				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,0);
				glVertex3f(-60,23,0);
				glVertex3f(-55,23,0);
				glVertex3f(-55,18.2,0);
				glEnd();

				glBegin(GL_POLYGON); // BALOK PENDEK
				glColor3ub(158, 55, 0);
				glVertex3f(-55,18.2,0);
				glVertex3f(-55,21,0);
				glVertex3f(-50,21,0);
				glVertex3f(-50,18.2,0);
				glEnd();

}

void castil1(){
				glBegin(GL_POLYGON); // BALOK PENDEK
				glColor3ub(158, 55, 0);
				glVertex3f(-55,18.2,0);
				glVertex3f(-55,21,0);
				glVertex3f(-50,21,0);
				glVertex3f(-50,18.2,0);
				glEnd();

}

void castil2(){

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,0);
				glVertex3f(-60,23,0);
				glVertex3f(-55,23,0);
				glVertex3f(-55,18.2,0);
				glEnd();
}
void bangun1(){

		glBegin(GL_POLYGON); // belakang
		glColor3ub(255, 154, 54);
		glVertex3f(-60,-18,-30);
		glVertex3f(-36,-18,-30);
		glVertex3f(-36,18,-30);
		glVertex3f(-60,18,-30);
		glEnd();

		glBegin(GL_POLYGON); // atas
		glColor3ub(150, 150, 150);
		glVertex3f(-60,18,0);
		glVertex3f(-40,18,0);
		glVertex3f(-36,18,-5.0);
		glVertex3f(-36,18,-30);
		glVertex3f(-60,18,-30);
		glEnd();

		glBegin(GL_POLYGON); // bawah
		glColor3ub(8, 48, 48);
		glVertex3f(-60,-18,0);
		glVertex3f(-40,-18,0);
		glVertex3f(-36,-18,-5.0);
		glVertex3f(-36,-18,-30);
		glVertex3f(-60,-18,-30);
		glEnd();

		glBegin(GL_POLYGON); // kiri
		glColor3ub(255, 145, 36);
		glVertex3f(-60,-18,-30);
		glVertex3f(-60,-18,0);
		glVertex3f(-60,18,0);
		glVertex3f(-60,18,-30);
		glEnd();

		glBegin(GL_POLYGON); // kanan
		glColor3ub(255, 145, 36);
		glVertex3f(-36,-18,-5.0);
		glVertex3f(-36,-18,-30);
		glVertex3f(-36,18,-30);
		glVertex3f(-36,18,-5.0);
		glEnd();

		glBegin(GL_POLYGON); // depan-samping
		glColor3ub(179, 89, 0);
		glVertex3f(-40,-18,0);
		glVertex3f(-36,-18,-5.0);
		glVertex3f(-36,18,-5.0);
		glVertex3f(-40,18,0);
		glEnd();

		glBegin(GL_POLYGON); // depan
		glColor3ub(255, 145, 36);
		glVertex3f(-60,-18,0);
		glVertex3f(-40,-18,0);
		glVertex3f(-40,18,0);
		glVertex3f(-60,18,0);
		glEnd();

		//------------------------------------
		//kastil atas
			glBegin(GL_LINE_LOOP); // LINE LOOP
			glColor3ub(8, 8, 8);
			glVertex3f(-60,18.2,0);
			glVertex3f(-40,18.2,0);
			glVertex3f(-36,18.2,-5.0);
			glVertex3f(-36,18.2,-30);
			glVertex3f(-60,18.2,-30);
			glEnd();

			//DEPAN
				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,0);
				glVertex3f(-60,23,0);
				glVertex3f(-55,23,0);
				glVertex3f(-55,18.2,0);
				glEnd();

				glBegin(GL_POLYGON); // BALOK PENDEK
				glColor3ub(158, 55, 0);
				glVertex3f(-55,18.2,0);
				glVertex3f(-55,21,0);
				glVertex3f(-50,21,0);
				glVertex3f(-50,18.2,0);
				glEnd();

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-50,18.2,0);
				glVertex3f(-50,23,0);
				glVertex3f(-45,23,0);
				glVertex3f(-45,18.2,0);
				glEnd();

				glBegin(GL_POLYGON); // BALOK PENDEK
				glColor3ub(158, 55, 0);
				glVertex3f(-45,18.2,0);
				glVertex3f(-45,21,0);
				glVertex3f(-40,21,0);
				glVertex3f(-40,18.2,0);
				glEnd();

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-40,18.2,0);
				glVertex3f(-40,23,0);
				glVertex3f(-36,23,-5);
				glVertex3f(-36,18.2,-5);
				glEnd();

			//BELAKANG
				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,-30);
				glVertex3f(-60,23,-30);
				glVertex3f(-55,23,-30);
				glVertex3f(-55,18.2,-30);
				glEnd();

				glBegin(GL_POLYGON); // BALOK PENDEK
				glColor3ub(158, 55, 0);
				glVertex3f(-55,18.2,-30);
				glVertex3f(-55,21,-30);
				glVertex3f(-50,21,-30);
				glVertex3f(-50,18.2,-30);
				glEnd();

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-50,18.2,-30);
				glVertex3f(-50,23,-30);
				glVertex3f(-45,23,-30);
				glVertex3f(-45,18.2,-30);
				glEnd();

				glBegin(GL_POLYGON); // BALOK PENDEK
				glColor3ub(158, 55, 0);
				glVertex3f(-45,18.2,-30);
				glVertex3f(-45,21,-30);
				glVertex3f(-40,21,-30);
				glVertex3f(-40,18.2,-30);
				glEnd();

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-40,18.2,-30);
				glVertex3f(-40,23,-30);
				glVertex3f(-36,23,-30);
				glVertex3f(-36,18.2,-30);
				glEnd();
			//KIRI
				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,0);
				glVertex3f(-60,23,0);
				glVertex3f(-60,23,-5);
				glVertex3f(-60,18.2,-5);
				glEnd();

				glBegin(GL_POLYGON); //BALOK SEDANG
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,-5);
				glVertex3f(-60,21,-5);
				glVertex3f(-60,21,-10);
				glVertex3f(-60,18.2,-10);
				glEnd();

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,-10);
				glVertex3f(-60,23,-10);
				glVertex3f(-60,23,-15);
				glVertex3f(-60,18.2,-15);
				glEnd();

				glBegin(GL_POLYGON); //BALOK SEDANG
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,-15);
				glVertex3f(-60,21,-15);
				glVertex3f(-60,21,-20);
				glVertex3f(-60,18.2,-20);
				glEnd();

				glBegin(GL_POLYGON); //BALOK SEDANG
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,-20);
				glVertex3f(-60,23,-20);
				glVertex3f(-60,23,-25);
				glVertex3f(-60,18.2,-25);
				glEnd();

				glBegin(GL_POLYGON); //BALOK SEDANG
				glColor3ub(158, 55, 0);
				glVertex3f(-60,18.2,-25);
				glVertex3f(-60,21,-25);
				glVertex3f(-60,21,-30);
				glVertex3f(-60,18.2,-30);
				glEnd();
			//Kanan

				glBegin(GL_POLYGON); //BALOK SEDANG
				glColor3ub(158, 55, 0);
				glVertex3f(-36,18.2,-5);
				glVertex3f(-36,21,-5);
				glVertex3f(-36,21,-10);
				glVertex3f(-36,18.2,-10);
				glEnd();

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-36,18.2,-10);
				glVertex3f(-36,23,-10);
				glVertex3f(-36,23,-15);
				glVertex3f(-36,18.2,-15);
				glEnd();

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-36,18.2,-15);
				glVertex3f(-36,21,-15);
				glVertex3f(-36,21,-20);
				glVertex3f(-36,18.2,-20);
				glEnd();

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-36,18.2,-20);
				glVertex3f(-36,23,-20);
				glVertex3f(-36,23,-25);
				glVertex3f(-36,18.2,-25);
				glEnd();

				glBegin(GL_POLYGON); // BALOK TINGGI
				glColor3ub(158, 55, 0);
				glVertex3f(-36,18.2,-25);
				glVertex3f(-36,21,-25);
				glVertex3f(-36,21,-30);
				glVertex3f(-36,18.2,-30);
				glEnd();
	}

	void bangun2(){
glBegin(GL_QUADS); // BAWAH
    glColor3f(1, 1, 1);
    glVertex3f(-60,-18,-30.0);
    glVertex3f(65.8,-18,-30.0);
    glVertex3f(65.8,-18,-60.0);
    glVertex3f(-60,-18,-60);
    //kecil
    glVertex3f(-36,-18,-25.0);
    glVertex3f(10.8,-18,-25.0);
    glVertex3f(10.8,-18,-30.0);
    glVertex3f(-36,-18,-30);
	//kecil2
    glVertex3f(26,-18,-25.0);
    glVertex3f(40,-18,-25.0);
    glVertex3f(40,-18,-30.0);
    glVertex3f(26,-18,-30);

    //atas
    glVertex3f(-60, 18,-30.0);
    glVertex3f(65.8, 18,-30.0);
    glVertex3f(65.8, 18,-60.0);
    glVertex3f(-60, 18,-60);
    //kecil
    glVertex3f(-36, 18,-25.0);
    glVertex3f(10.8, 18,-25.0);
    glVertex3f(10.8, 18,-30.0);
    glVertex3f(-36, 18,-30);
	//kecil2
    glVertex3f(26, 18,-25.0);
    glVertex3f(40, 18,-25.0);
    glVertex3f(40, 18,-30.0);
    glVertex3f(26, 18,-30);

    //tembok
    //belakang
    glColor3ub(255, 154, 54);
    glColor3ub(255, 154, 54);
    glVertex3f(-60, 18, -60.0);
    glVertex3f(65.8, 18, -60.0);
    glVertex3f(65.8, -18, -60.0);
    glVertex3f(-60, -18, -60);
    //depan kecil 1
    glVertex3f(-36, 18, -25.01);
    glVertex3f(10.8, 18, -25.01);
    glVertex3f(10.8, -18, -25.01);
    glVertex3f(-36, -18, -25.01);
    //depan kecil 1
	glVertex3f(26, 18, -25.01);
    glVertex3f(40, 18, -25.01);
    glVertex3f(40, -18, -25.01);
    glVertex3f(26, -18, -25.01);

    //samping
    //kiri
    glColor3ub(255, 154, 54);
    glVertex3f(-60, 18, -30.0);
    glVertex3f(-60, -18, -30.0);
    glVertex3f(-60, -18, -60.0);
    glVertex3f(-60, 18, -60);

    //ornamen
    //depan
    glColor3ub(158, 55, 0);
    glVertex3f(-36, 21, -25.01);
    glVertex3f(10.8, 21, -25.01);
    glVertex3f(10.8, 18, -25.01);
    glVertex3f(-36, 18, -25.01);
    //
    glVertex3f(26, 21, -25.01);
    glVertex3f(40, 21, -25.01);
    glVertex3f(40, 18, -25.01);
    glVertex3f(26, 18, -25.01);
    //1
    glVertex3f(-36, 23, -25.01);
    glVertex3f(-32, 23, -25.01);
    glVertex3f(-32, 21, -25.01);
    glVertex3f(-36.0, 21, -25.01);
    //2
    glVertex3f(-27, 23, -25.01);
    glVertex3f(-22, 23, -25.01);
    glVertex3f(-22, 21, -25.01);
    glVertex3f(-27.0, 21, -25.01);
    //3
    glVertex3f(-17, 23, -25.01);
    glVertex3f(-12, 23, -25.01);
    glVertex3f(-12, 21, -25.01);
    glVertex3f(-17.0, 21, -25.01);
    //4
    glVertex3f(-7, 23, -25.01);
    glVertex3f(-2, 23, -25.01);
    glVertex3f(-2, 21, -25.01);
    glVertex3f(-7.0, 21, -25.01);
    //5
    glVertex3f(3, 23, -25.01);
    glVertex3f(8, 23, -25.01);
    glVertex3f(8, 21, -25.01);
    glVertex3f(3.0, 21, -25.01);
    //7
    glVertex3f(26, 23, -25.01);
    glVertex3f(28, 23, -25.01);
    glVertex3f(28, 21, -25.01);
    glVertex3f(26, 21, -25.01);
    //8
    glVertex3f(33, 23, -25.01);
    glVertex3f(38, 23, -25.01);
    glVertex3f(38, 21, -25.01);
    glVertex3f(33, 21, -25.01);

    //belakang
    glVertex3f(-60, 21, -60.0);
    glVertex3f(65.8, 21, -60.0);
    glVertex3f(65.8, 18, -60.0);
    glVertex3f(-60, 18, -60);
    //1
    glVertex3f(-60, 23, -60.0);
    glVertex3f(-54, 23, -60.0);
    glVertex3f(-54, 21, -60.0);
    glVertex3f(-60.0, 21, -60);
    //2
    glVertex3f(-49, 23, -60.0);
    glVertex3f(-43, 23, -60.0);
    glVertex3f(-43, 21, -60.0);
    glVertex3f(-49.0, 21, -60);
    //3
    glVertex3f(-38, 23, -60.0);
    glVertex3f(-32, 23, -60.0);
    glVertex3f(-32, 21, -60.0);
    glVertex3f(-38.0, 21, -60);
    //4
    glVertex3f(-27, 23, -60.0);
    glVertex3f(-22, 23, -60.0);
    glVertex3f(-22, 21, -60.0);
    glVertex3f(-27.0, 21, -60);
    //5
    glVertex3f(-17, 23, -60.0);
    glVertex3f(-12, 23, -60.0);
    glVertex3f(-12, 21, -60.0);
    glVertex3f(-17.0, 21, -60);
    //6
    glVertex3f(-7, 23, -60.0);
    glVertex3f(-2, 23, -60.0);
    glVertex3f(-2, 21, -60.0);
    glVertex3f(-7.0, 21, -60);
    //7
    glVertex3f(3, 23, -60.0);
    glVertex3f(8, 23, -60.0);
    glVertex3f(8, 21, -60.0);
    glVertex3f(3.0, 21, -60);
    //8
    glVertex3f(13, 23, -60.0);
    glVertex3f(18, 23, -60.0);
    glVertex3f(18, 21, -60.0);
    glVertex3f(13, 21, -60);
    //9
    glVertex3f(23, 23, -60.0);
    glVertex3f(28, 23, -60.0);
    glVertex3f(28, 21, -60.0);
    glVertex3f(23, 21, -60);
    //10
    glVertex3f(33, 23, -60.0);
    glVertex3f(38, 23, -60.0);
    glVertex3f(38, 21, -60.0);
    glVertex3f(33, 21, -60);
    //11
    glVertex3f(43, 23, -60.0);
    glVertex3f(48, 23, -60.0);
    glVertex3f(48, 21, -60.0);
    glVertex3f(43, 21, -60);
    //12
    glVertex3f(53, 23, -60.0);
    glVertex3f(58, 23, -60.0);
    glVertex3f(58, 21, -60.0);
    glVertex3f(53, 21, -60);
    //13
    glVertex3f(63, 23, -60.0);
    glVertex3f(65.8, 23, -60.0);
    glVertex3f(65.8, 21, -60.0);
    glVertex3f(63, 21, -60);

    //samping
    //kiri
    glVertex3f(-60, 21, -30.0);
    glVertex3f(-60, 18, -30.0);
    glVertex3f(-60, 18, -60.0);
    glVertex3f(-60, 21, -60);
    //1
    glVertex3f(-60, 23, -55.0);
    glVertex3f(-60, 21, -55.0);
    glVertex3f(-60, 21, -60.0);
    glVertex3f(-60, 23, -60);
    //2
    glVertex3f(-60, 23, -45.0);
    glVertex3f(-60, 21, -45.0);
    glVertex3f(-60, 21, -50.0);
    glVertex3f(-60, 23, -50);
    //3
    glVertex3f(-60, 23, -35.0);
    glVertex3f(-60, 21, -35.0);
    glVertex3f(-60, 21, -40.0);
    glVertex3f(-60, 23, -40);


    //samping
    //kanan
    glVertex3f(65.8, 21, -30.0);
    glVertex3f(65.8, 18, -30.0);
    glVertex3f(65.8, 18, -60.0);
    glVertex3f(65.8, 21, -60);
    //1
    glVertex3f(65.8, 23, -55.0);
    glVertex3f(65.8, 21, -55.0);
    glVertex3f(65.8, 21, -60.0);
    glVertex3f(65.8, 23, -60);
    //2
    glVertex3f(65.8, 23, -45.0);
    glVertex3f(65.8, 21, -45.0);
    glVertex3f(65.8, 21, -50.0);
    glVertex3f(65.8, 23, -50);
    //3
    glVertex3f(65.8, 23, -35.0);
    glVertex3f(65.8, 21, -35.0);
    glVertex3f(65.8, 21, -40.0);
    glVertex3f(65.8, 23, -40);


glEnd();
    //garis list
glBegin(GL_LINES);// LINE LOOP
    glColor3ub(8, 8, 8);
    glVertex3f(-60,18.2,-60.0);
    glVertex3f(-60,18.2,-30);
    glVertex3f(-36, 18.2, -25.01);
    glVertex3f(10.8, 18.2, -25.01);
    glVertex3f(26, 18.2, -25.01);
    glVertex3f(40, 18.2, -25.01);
	glVertex3f(65.8, 18.2, -30);
    glVertex3f(65.8, 18.2, -60);
    glVertex3f(65.8, 18.2, -60);
    glVertex3f(-60, 18.2, -60);
glEnd();
}

	void bangun3(){
		glBegin(GL_POLYGON); // BAWAH
		glColor3ub(2, 145, 36);
		glVertex3f(-35.8,-18,-11.0);
		glVertex3f(10.8,-18,-11.0);
		glVertex3f(10.8,-18,-25.0);
		glVertex3f(-35.8,-18,-25);
		glEnd();

		glBegin(GL_POLYGON); // ATAS
		glColor3ub(2, 145, 36);
		glVertex3f(-35.8,3,-11.0);
		glVertex3f(10.8,3,-11.0);
		glVertex3f(10.8,3,-25.0);
		glVertex3f(-35.8,3,-25);
		glEnd();

		glBegin(GL_POLYGON); // KANAN
		glColor3ub(2, 145, 36);
		glVertex3f(10.8,-18,-11.0);
		glVertex3f(10.8,-18,-25.0);
		glVertex3f(10.8,3,-25.0);
		glVertex3f(10.8,3,-11.0);
		glEnd();

		glBegin(GL_POLYGON); // KIRI
		glColor3ub(2, 145, 36);
		glVertex3f(-35.8,-18,-11.0);
		glVertex3f(-35.8,-18,-25.0);
		glVertex3f(-35.8,3,-25.0);
		glVertex3f(-35.8,3,-11.0);
		glEnd();

		glBegin(GL_POLYGON); // DEPAN
		glColor3ub(152, 125, 36);
		glVertex3f(-35.8,-18,-11.0);
		glVertex3f(-5.8,-18,-11.0);
		glVertex3f(-5.8,3,-11.0);
		glVertex3f(-35.8,3,-11.0);
		glEnd();

		glBegin(GL_POLYGON); // PINTU
		glColor3ub(12, 15, 36);
		glVertex3f(-5.8,-18,-11.0);
		glVertex3f(10.8,-18,-11.0);
		glVertex3f(10.8,9,-11.0);
		glVertex3f(-5.8,9,-11.0);
		glEnd();

		//------------------------------------
		//kastil atas

			glPushMatrix();
			glTranslatef(24,-15.2,-25); //belakang
			castil();
			glPopMatrix();

			glPushMatrix();
			glTranslatef(34,-15.2,-25); //belakang
			castil();
			glPopMatrix();

			glPushMatrix();
			glTranslatef(44,-15.2,-25); //belakang
			castil();
			glPopMatrix();

			glPushMatrix();
			glTranslatef(54,-15.2,-25); //belakang
			castil();
			glPopMatrix();
			glPushMatrix();
			glTranslatef(64,-15.2,-25); //belakang
			castil();
			glPopMatrix();

				glPopMatrix();
				glPushMatrix();
				glTranslatef(24,-15.2,-11); //depan
				castil();
				glPopMatrix();

				glPushMatrix();
				glTranslatef(34,-15.2,-11); //depan
				castil();
				glPopMatrix();

				glPushMatrix();
				glTranslatef(44,-15.2,-11); //depan
				castil();
				glPopMatrix();

				glPushMatrix();
				glTranslatef(55,-9.2,-11); //depan
				castil();
				glPopMatrix();

				glPushMatrix();
				glTranslatef(65,-9.2,-11); //depan
				castil2();
				glPopMatrix();

	}

	void bangun4(){

		glBegin(GL_POLYGON); // sisi BELAKANG
		glColor3ub(12, 15, 36);
		glVertex3f(10.8,-18,-18.0);
		glVertex3f(23,-18,-18.0);
		glVertex3f(23,16,-18.0);
		glVertex3f(10.8,16,-18.0);
		glEnd();
		glBegin(GL_POLYGON); // sisi BAWAH
		glColor3ub(122, 15, 36);
		glVertex3f(10.8,-18,-5.0);
		glVertex3f(23,-18,-5.0);
		glVertex3f(23,-18,-18.0);
		glVertex3f(10.8,-18,-18.0);
		glEnd();

		glBegin(GL_POLYGON); // sisi KIRI
		glColor3ub(122, 15, 36);
		glVertex3f(10.8,16,-18.0);
		glVertex3f(10.8,16,-5.0);
		glVertex3f(10.8,-18,-5.0);
		glVertex3f(10.8,-18,-18.0);
		glEnd();

		glBegin(GL_POLYGON); // sisi KANAN
		glColor3ub(122, 15, 36);
		glVertex3f(23,16,-18.0);
		glVertex3f(23,16,-5.0);
		glVertex3f(23,-18,-5.0);
		glVertex3f(23,-18,-18.0);
		glEnd();

		glBegin(GL_POLYGON); // sisi ATAS
		glColor3ub(122, 15, 36);
		glVertex3f(10.8,16,-5.0);
		glVertex3f(23,16,-5.0);
		glVertex3f(23,16,-18.0);
		glVertex3f(10.8,16,-18.0);
		glEnd();

		glBegin(GL_POLYGON); // sisi DEPAN
		glColor3ub(12, 15, 36);
		glVertex3f(10.8,-18,-5.0);
		glVertex3f(23,-18,-5.0);
		glVertex3f(23,16,-5.0);
		glVertex3f(10.8,16,-5.0);
		glEnd();
		//------------------------------------
		//kastil atas
		glBegin(GL_LINE_LOOP); // sisi ATAS
		glColor3ub(8,8,8);
		glVertex3f(10.8,16,-5.0);
		glVertex3f(23,16,-5.0);
		glVertex3f(23,16,-18.0);
		glVertex3f(10.8,16,-18.0);
		glEnd();
				glPushMatrix();
				glTranslatef(71.5,-2,-5); //depan
				castil();
				glPopMatrix();
        }

    void bangun6(){

    glBegin(GL_POLYGON); // BAWAH
		glColor3ub(2, 145, 36);
		glVertex3f(65.8,-18,-11.0);
		glVertex3f(22.8,-18,-11.0);
		glVertex3f(22.8,-18,-25.0);
		glVertex3f(65.8,-18,-25);
		glEnd();

		glBegin(GL_POLYGON); // ATAS
		glColor3ub(2, 145, 36);
		glVertex3f(65.8,3,-11.0);
		glVertex3f(22.8,3,-11.0);
		glVertex3f(22.8,3,-25.0);
		glVertex3f(65.8,3,-25);
		glEnd();

		glBegin(GL_POLYGON); // KANAN
		glColor3ub(2, 145, 36);
		glVertex3f(65.8,-18,-11.0);
		glVertex3f(22.8,-18,-25.0);
		glVertex3f(22.8,3,-25.0);
		glVertex3f(65.8,3,-11.0);
		glEnd();

		glBegin(GL_POLYGON); // KIRI
		glColor3ub(2, 145, 36);
		glVertex3f(65.8,-18,-11.0);
		glVertex3f(65.8,-18,-25.0);
		glVertex3f(65.8,3,-25.0);
		glVertex3f(65.8,3,-11.0);
		glEnd();

		glBegin(GL_POLYGON); // DEPAN
		glColor3ub(152, 125, 36);
		glVertex3f(65.8,-18,-11.0);
		glVertex3f(22.8,-18,-11.0);
		glVertex3f(22.8,3,-11.0);
		glVertex3f(65.8,3,-11.0);
		glEnd();



		//------------------------------------
		//kastil atas

			glPushMatrix();
			glTranslatef(83,-15.2,-25); //belakang
			castil();
			glPopMatrix();

			glPushMatrix();
			glTranslatef(93,-15.2,-25); //belakang
			castil();
			glPopMatrix();

			glPushMatrix();
			glTranslatef(103,-15.2,-25); //belakang
			castil();
			glPopMatrix();

			glPushMatrix();
			glTranslatef(113,-15.2,-25); //belakang
			castil();
			glPopMatrix();
			glPushMatrix();
			glTranslatef(115,-15.2,-25); //belakang
			castil();
			glPopMatrix();

				glPopMatrix();
				glPushMatrix();
				glTranslatef(83,-15.2,-11); //depan
				castil();
				glPopMatrix();

				glPushMatrix();
				glTranslatef(93,-15.2,-11); //depan
				castil();
				glPopMatrix();

				glPushMatrix();
				glTranslatef(103,-15.2,-11); //depan
				castil();
				glPopMatrix();

				glPushMatrix();
				glTranslatef(113,-15.2,-11); //depan
				castil();
				glPopMatrix();

				glPushMatrix();
				glTranslatef(121,-15.2,-11); //depan
				castil2();
				glPopMatrix();

    }

 void bangun5(){
		glBegin(GL_POLYGON); // bawah
		glColor3ub(255, 145, 36);
		glVertex3f(10.8,-18,-18.0);
		glVertex3f(26,-18,-18);
		glVertex3f(26,-18,-30);
		glVertex3f(10.8,-18,-30);
		glEnd();

		glBegin(GL_POLYGON); // atas
		glColor3ub(255, 145, 36);
		glVertex3f(10.8,24,-18.0);
		glVertex3f(26,24,-18);
		glVertex3f(26,24,-30);
		glVertex3f(10.8,24,-30);
		glEnd();

		glBegin(GL_POLYGON); // depan
		glColor3ub(255, 145, 36);
		glVertex3f(10.8,-18,-18.0);
		glVertex3f(26,-18,-18);
		glVertex3f(26,24,-18);
		glVertex3f(10.8,24,-18.0);
		glEnd();

		glBegin(GL_POLYGON); // belakang
		glColor3ub(255, 145, 36);
		glVertex3f(10.8,-18,-30.0);
		glVertex3f(26,-18,-30);
		glVertex3f(26,24,-30);
		glVertex3f(10.8,24,-30.0);
		glEnd();

		glBegin(GL_POLYGON); // kiri
		glColor3ub(255, 145, 36);
		glVertex3f(10.8,-18,-30);
		glVertex3f(10.8,-18,-18);
		glVertex3f(10.8,24,-18);
		glVertex3f(10.8,24,-30);
		glEnd();

		glBegin(GL_POLYGON); // kanan
		glColor3ub(255, 145, 36);
		glVertex3f(26,-18,-30);
		glVertex3f(26,-18,-18);
		glVertex3f(26,24,-18);
		glVertex3f(26,24,-30);
		glEnd();

		//kastil atas
		glBegin(GL_LINE_LOOP); // atas
		glColor3ub(8, 8, 8);
		glVertex3f(10.8,24,-18.0);
		glVertex3f(26,24,-18);
		glVertex3f(26,24,-30);
		glVertex3f(10.8,24,-30);
		glEnd();

			//depan
				glPushMatrix();
				glTranslatef(71,6,-18); //1
				castil2();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(71,6,-18); //2
				castil1();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(81,6,-18); //3
				castil2();
				glPopMatrix();
			//belakang
				glPushMatrix();
				glTranslatef(71,6,-30); //1
				castil2();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(71,6,-30); //2
				castil1();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(81,6,-30); //3
				castil2();
				glPopMatrix();
	}

	void bangun7(){
        glBegin(GL_POLYGON); // bawah
		glColor3ub(255, 145, 36);
		glVertex3f(65.8,-18,-18.0);
		glVertex3f(40,-18,-18);
		glVertex3f(40,-18,-30);
		glVertex3f(65.8,-18,-30);
		glEnd();

		glBegin(GL_POLYGON); // atas
		glColor3ub(255, 145, 36);
		glVertex3f(65.8,24,-18.0);
		glVertex3f(40,24,-18);
		glVertex3f(40,24,-30);
		glVertex3f(65.8,24,-30);
		glEnd();

		glBegin(GL_POLYGON); // depan
		glColor3ub(255, 145, 36);
		glVertex3f(65.8,-18,-18.0);
		glVertex3f(40,-18,-18);
		glVertex3f(40,24,-18);
		glVertex3f(65.8,24,-18.0);
		glEnd();

		glBegin(GL_POLYGON); // belakang
		glColor3ub(255, 145, 36);
		glVertex3f(65.8,-18,-30.0);
		glVertex3f(40,-18,-30);
		glVertex3f(40,24,-30);
		glVertex3f(65.8,24,-30.0);
		glEnd();

		glBegin(GL_POLYGON); // kiri
		glColor3ub(255, 145, 36);
		glVertex3f(65.8,-18,-30);
		glVertex3f(65.8,-18,-18);
		glVertex3f(65.8,24,-18);
		glVertex3f(65.8,24,-30);
		glEnd();

		glBegin(GL_POLYGON); // kanan
		glColor3ub(255, 145, 36);
		glVertex3f(40,-18,-30);
		glVertex3f(40,-18,-18);
		glVertex3f(40,24,-18);
		glVertex3f(40,24,-30);
		glEnd();

		//kastil atas
		glBegin(GL_LINE_LOOP); // atas
		glColor3ub(8, 8, 8);
		glVertex3f(65.8,24,-18.0);
		glVertex3f(40,24,-18);
		glVertex3f(40,24,-30);
		glVertex3f(65.8,24,-30);
		glEnd();

			//depan
				glPushMatrix();
				glTranslatef(100,6,-18); //1
				castil2();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(100,6,-18); //2
				castil1();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(110,6,-18); //3
				castil2();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(110,6,-18); //1
				castil2();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(110,6,-18); //2
				castil1();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(120,6,-18); //3
				castil2();
				glPopMatrix();
			//belakang
				glPushMatrix();
				glTranslatef(100,6,-30); //1
				castil2();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(100,6,-30); //2
				castil1();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(110,6,-30); //3
				castil2();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(110,6,-30); //1
				castil2();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(110,6,-30); //2
				castil1();
				glPopMatrix();
				glPushMatrix();
				glTranslatef(120,6,-30); //3
				castil2();
				glPopMatrix();

	}
void tampil(void)
{
	if (is_depth)
        glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT);
    else
    glClear(GL_COLOR_BUFFER_BIT);

	//----------------------------------------
	bangun1();
	bangun2();
	bangun3();
	bangun4();
	bangun6();
	bangun5();
	bangun7();
	//----------------------------------------


    glutSwapBuffers();

}
void idle(){
	if(!mouseDown){
		xrot += 0.3f;
		yrot += 0.4f;
	}
	glutPostRedisplay();
}

void mouse (int button, int state, int x, int y){
	if (button == GLUT_LEFT_BUTTON && state == GLUT_DOWN){
		mouseDown = true;
		xdiff = x - yrot;
		ydiff = -y + xrot;
	} else {
		mouseDown = false;
	}
}

void mouseMotion(int x, int y){
	if(mouseDown){
		yrot = x - xdiff;
		xrot = y + xdiff;
		glLoadIdentity();
		glutPostRedisplay();
	}
}
void keyboard(unsigned char key, int x, int y)
{
    switch (key)
    {
	case 'w':
    case 'W':
        glTranslatef(0.0, 0.0, 3.0);
        break;
    case 'd':
    case 'D':
        glTranslatef(3.0, 0.0, 0.0);
        break;
	case 's':
    case 'S':
        glTranslatef(0.0, 0.0, -3.0);
        break;
    case 'a':
    case 'A':
        glTranslatef(-3.0, 0.0, 0.0);
        break;
	case '7':
        glTranslatef(0.0, 3.0, 0.0);
        break;
	case '9':
        glTranslatef(0.0, -3.0, 0.0);
        break;
    case '2':
        glRotatef(2.0, 1.0, 0.0, 0.0);
        break;
    case '8':
        glRotatef(-2.0, 1.0, 0.0, 0.0);
        break;
    case '6':
        glRotatef(2.0, 0.0, 1.0, 0.0);
        break;
    case '4':
        glRotatef(-2.0, 0.0, 1.0, 0.0);
        break;
    case '1':
        glRotatef(2.0, 0.0, 0.0, 1.0);
        break;
    case '3':
        glRotatef(-2.0, 0.0, 0.0, 1.0);
        break;
    case '5':
        if (is_depth)
        {
            is_depth = 0;
            glDisable(GL_DEPTH_TEST);
        }
        else
        {
            is_depth = 1;
            glEnable(GL_DEPTH_TEST);
        }
    }
    tampil();
}

void ukuran(int lebar, int tinggi)
{
    if (tinggi == 0) tinggi = 1;

    glMatrixMode(GL_PROJECTION);
    glLoadIdentity();
    gluPerspective(50.0, lebar / tinggi, 5.0, 500.0);
    glTranslatef(0.0, -5.0, -150.0);
    glMatrixMode(GL_MODELVIEW);
}
