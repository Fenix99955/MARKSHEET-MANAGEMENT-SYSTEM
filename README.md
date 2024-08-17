# MARKSHEET-MANAGEMENT-SYSTEM
#A simple project for teachers to make it easy to keep the records of marks and print a marksheet when required







from tkinter import *
from tkinter import ttk
from tkinter import messagebox
import mysql.connector as con
root=Tk()





def true():
    root.destroy()
    root2=Tk()


    

    def system():

        
        def debo():
            
            rootye=Tk()
            rootye.configure(background="cyan")
            rootye.geometry("11000x11000")
            def fat():
                f=clad.get()
                print(f)

                
                if f =="SCIENCE"  :
                    aed1=Label(rootye,text="ENGLISH:",bg="cyan")
                    aed1.place(x=600,y=200)
                    aed2=Label(rootye,text="HINDI:",bg="cyan")
                    aed2.place(x=600,y=250)
                    aed3=Label(rootye,text="MATH:",bg="cyan")
                    aed3.place(x=600,y=300)
                    aed4=Label(rootye,text="PHYSICS:",bg="cyan")
                    aed4.place(x=600,y=350)
                    aed5=Label(rootye,text="CHEMISTRY:",bg="cyan")
                    aed5.place(x=600,y=400)
                    aed6=Label(rootye,text="BIOLOGY:",bg="cyan")
                    aed6.place(x=600,y=450)
                    aed7=Label(rootye,text="COM SCI:",bg="cyan")
                    aed7.place(x=600,y=500)
                    aed8=Label(rootye,text="PHY EDU:",bg="cyan")
                    aed8.place(x=600,y=550)


                
                if f =="HUMANITIES":
                    kaed=Label(rootye,text="english")
                    kaed.place(x=600,y=200)
                    kaed=Label(rootye,text="hindi")
                    kaed.place(x=600,y=250)
                    kaed=Label(rootye,text="history")
                    kaed.place(x=600,y=300)
                    kaed=Label(rootye,text="geography")
                    kaed.place(x=600,y=350)
                    kaed=Label(rootye,text="economics")
                    kaed.place(x=600,y=400)
                    kaed=Label(rootye,text="political science")
                    kaed.place(x=600,y=450)
                    kaed=Label(rootye,text="pHysical education")
                    kaed.place(x=600,y=500)
                






            
            def ed():
                
                aaa=ed1.get()
                bbb=ed2.get()
                ccc=ed3.get()
                ddd=ed4.get()
                eee=ed5.get()
                fff=ed6.get()
                ggg=ed7.get()
                hhh=ed8.get()
                addd=admisss.get()

                import mysql.connector
                edit=mysql.connector.connect(host="localhost",user="root", password="root",database="email")
                cursorr=edit.cursor()

                sql=("UPDATE `email`.`data` SET `sub1` = %s, `sub2` = %s, `sub3` = %s, `sub4` = %s, `sub5` = %s, `sub6` = %s, `sub7` = %s, `sub8` = %s WHERE `admissionid` = %s;")
                valuee=(aaa,bbb,ccc,ddd,eee,fff,ggg,hhh,addd)
                cursorr.execute(sql,valuee)



                edit.commit()
                



            ed1=Entry(rootye,)
            ed1.place(x=900,y=200)
            ed2=Entry(rootye,)
            ed2.place(x=900,y=250)
            ed3=Entry(rootye,)
            ed3.place(x=900,y=300)
            ed4=Entry(rootye,)
            ed4.place(x=900,y=350)
            ed5=Entry(rootye,)
            ed5.place(x=900,y=400)
            ed6=Entry(rootye,)
            ed6.place(x=900,y=450)
            ed7=Entry(rootye,)
            ed7.place(x=900,y=500)
            ed8=Entry(rootye,)
            ed8.place(x=900,y=550)




            admisss=Entry(rootye,)
            admisss.place(x=900,y=100)
            admiss=Label(rootye,text="admission ID")
            admiss.place(x=700,y=100)

            clad=Entry(rootye)
            clad.place(x=1000,y=100)
            cadl=Label(rootye,text="stream-HUMANITIES/SCIENCE ")
            cadl.place(x=1000,y=50)

            xxx=Button(rootye,text="fetch data",command=fat)
            xxx.place(x=900,y=150)


            final=Button(rootye,text="confirm",command=ed)
            final.place(x=900,y=600)







            rootye.mainloop()




            
        #get marksheet window
        def getmak():
            def MARKSHEET():
                if len(entry.get())==0:
                    messagebox.showerror("ERROR","ADMISSION NUMBER CANNOT BE EMPTY")
                    rootGM.destroy()
                if not len(entry.get())==0:
                        import mysql.connector
                        cnx = mysql.connector.connect(user='root', password='root',
                                                      host='localhost',
                                                      database='email')

                       
                        cursor = cnx.cursor()
                        dass=int(entry.get())

                        
                        cursor.execute("SELECT * FROM email.data where admissionid=%d;"%(dass))
                        
                        rows = cursor.fetchone()
                        print(rows)
                        admsid=(rows[0])
                        names=(rows[1])
                        fatnames=(rows[2])
                        matname=(rows[3])
                        clss=(rows[4])
                        sect=(rows[5])
                        dobs=(rows[6])
                        subs1=(rows[7])
                        subs2=(rows[8])
                        subs3=(rows[9])
                        subs4=(rows[10])
                        subs5=(rows[11])
                        subs6=(rows[12])
                        subs7=(rows[13])
                        subs8=(rows[14])
                        if sect=="SCIENCE":
                            rootp=Tk()
                            rootp.geometry("11000x11000")
                            zz=Label(rootp,text="NAME")
                            zz.place(x=30,y=10)
                            xx=Label(rootp,text="FATHER'NAME")
                            xx.place(x=190,y=10)
                            cc=Label(rootp,text="MOTHER'S NAME")
                            cc.place(x=480,y=10)
                            vv=Label(rootp,text="D.O.B")
                            vv.place(x=670,y=10)
                            bb=Label(rootp,text="CLASS")
                            bb.place(x=860,y=10)
                            nn=Label(rootp,text="STREAM")
                            nn.place(x=950,y=10)
                            mm=Label(rootp,text="ADMISSION NO")
                            mm.place(x=1140,y=10)
                            a=Label(rootp,text=names)
                            a.place(x=30,y=29)
                            b=Label(rootp,text=fatnames)
                            b.place(x=190,y=29)
                            c=Label(rootp,text=matname )
                            c.place(x=480,y=29)
                            d=Label(rootp,text=dobs)
                            d.place(x=670,y=29)
                            e=Label(rootp,text=clss)
                            e.place(x=860,y=29)
                            f=Label(rootp,text=sect)
                            f.place(x=950,y=29)
                            g=Label(rootp,text=admsid)
                            g.place(x=1140,y=29)


                            kk=Label(rootp,text=subs1,)
                            kk.place(x=900,y=200)
                            wwx=Label(rootp,text=subs2,)
                            wwx.place(x=900,y=250)
                            ecc=Label(rootp,text=subs3,)
                            ecc.place(x=900,y=300)
                            rvv=Label(rootp,text=subs4,)
                            rvv.place(x=900,y=350)
                            tbb=Label(rootp,text=subs5,)
                            tbb.place(x=900,y=400)
                            umm=Label(rootp,text=subs6,)
                            umm.place(x=900,y=450)
                            unn=Label(rootp,text=subs7,)
                            unn.place(x=900,y=500)
                            pmm=Label(rootp,text=subs8,)
                            pmm.place(x=900,y=550)
                            

                            qw=Label(rootp,text="english",font=('december',20))
                            qw.place(x=400,y=200)
                            er=Label(rootp,font=('december',20,),text="hindi")
                            er.place(x=400,y=250)
                            rt=Label(rootp,font=('december',20),text="maths")
                            rt.place(x=400,y=300)
                            yh=Label(rootp,font=('december',20),text="physics")
                            yh.place(x=400,y=350)
                            uy=Label(rootp,font=('december',20),text="chemistry")
                            uy.place(x=400,y=400)
                            yu=Label(rootp,font=('december',20),text="biology")
                            yu.place(x=400,y=450)
                            op=Label(rootp,font=('december',20),text="computerscience")
                            op.place(x=400,y=500)
                            wr=Label(rootp,font=('december',20),text="physical education")
                            wr.place(x=400,y=550)

                            rootp.mainloop()





                        if sect=="HUMANITIES":
                            asd=Tk()
                            asd.geometry("11000x11000")
                            zz=Label(asd,text="NAME",bg="cyan")
                            zz.place(x=30,y=10)
                            xx=Label(asd,text="FATHER'NAME",bg="cyan")
                            xx.place(x=190,y=10)
                            cc=Label(asd,text="MOTHER'S NAME",bg="cyan")
                            cc.place(x=480,y=10)
                            vv=Label(asd,text="D.O.B",bg="cyan")
                            vv.place(x=670,y=10)
                            bb=Label(asd,text="CLASS",bg="cyan")
                            bb.place(x=860,y=10)
                            nn=Label(asd,text="STREAM",bg="cyan")
                            nn.place(x=950,y=10)
                            mm=Label(asd,text="ADMISSION NO",bg="cyan")
                            mm.place(x=1140,y=10)
                            a=Label(asd,text=names)
                            a.place(x=30,y=29)
                            b=Label(asd,text=fatnames)
                            b.place(x=190,y=29)
                            c=Label(asd,text=matname )
                            c.place(x=480,y=29)
                            d=Label(asd,text=dobs)
                            d.place(x=670,y=29)
                            e=Label(asd,text=clss)
                            e.place(x=860,y=29)
                            f=Label(asd,text=sect)
                            f.place(x=950,y=29)
                            g=Label(asd,text=admsid)
                            g.place(x=1140,y=29)

                            kk=Label(asd,text=subs1,bg="cyan")
                            kk.place(x=900,y=200)
                            wwx=Label(asd,text=subs2,bg="cyan")
                            wwx.place(x=900,y=250)
                            ecc=Label(asd,text=subs3,bg="cyan")
                            ecc.place(x=900,y=300)
                            rvv=Label(asd,text=subs4,bg="cyan")
                            rvv.place(x=900,y=350)
                            tbb=Label(asd,text=subs5,bg="cyan")
                            tbb.place(x=900,y=400)
                            umm=Label(asd,text=subs6,bg="cyan")
                            umm.place(x=900,y=450)
                            unn=Label(asd,text=subs7,bg="cyan")
                            unn.place(x=900,y=500)
                            

                            qw=Label(asd,text="english",font=('december',20),bg="cyan")
                            qw.place(x=400,y=200)
                            er=Label(asd,font=('december',20,),text="hindi",bg="cyan")
                            er.place(x=400,y=250)
                            rt=Label(asd,font=('december',20),text="history",bg="cyan")
                            rt.place(x=400,y=300)
                            yh=Label(asd,font=('december',20),text="geography",bg="cyan")
                            yh.place(x=400,y=350)
                            uy=Label(asd,font=('december',20),text="economics",bg="cyan")
                            uy.place(x=400,y=400)
                            yu=Label(asd,font=('december',20),text="political science",bg="cyan")
                            yu.place(x=400,y=450)
                            op=Label(asd,font=('december',20),text="physical education",bg="cyan")
                            op.place(x=400,y=500)



                            asd.mainloop()

                        

                        cnx.close()
                        print("555")

            

            rootGM=Tk()
            rootGM.configure(background="cyan")
            rootGM.geometry("11000x11000")
            rootGM.title("GET MARKSHEET")
            enteradmnid=Label(rootGM,text="𝔼ℕ𝕋𝔼ℝ 𝔸𝔻𝔻𝕄𝕀𝕊𝕊𝕀𝕆ℕ ℕ𝕌𝕄𝔹𝔼ℝ:",font=("arial",40),fg="red",bg="cyan")
            enteradmnid.pack()
            
            entry=Entry(rootGM,font=('december',30),bg="silver")
            entry.place(x=500,y=250,)

            b1=Button(rootGM,text="GET",font=('december',12),width=50,height=2,command=MARKSHEET,bg="PURPLE")
            b1.place(x=500,y=400)

            o=Label(rootGM,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
            o.place(x=0,y=80)
            l=Label(rootGM,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
            l.place(x=0,y=700)

            rootGM.mainloop()
            #get marksheet window ends here



        import mysql.connector
        mydb = mysql.connector.connect(host="localhost",user="root", password="root",database="email")
        mycursor = mydb.cursor()
        query = "SELECT * FROM email.user WHERE id = %s and pas= %s "
        id = (email.get())
        pas=(password.get())
        mycursor.execute(query, (id,pas,))
        myresult = mycursor.fetchone()

        if myresult is not None:
            def stud():
                def mark():
                    #calling all the details and saving them in variables
                    na=NAME.get()
                    fa=FATHERNAME.get()
                    mo=MOTHERNAME.get()
                    do=DOB.get()
                    cl=grade.get()
                    se=sec.get()
                    fe=aid.get()
                    if len(na)==0:
                        messagebox.showwarning("WARNING","NAME CANNOT BE EMPTY ")
                        root4.destroy()
                    if len(fa)==0:
                        messagebox.showwarning("WARNING","FATHERNAME CANNOT BE EMPTY ")
                        root4.destroy()
                    if len(mo)==0:
                        messagebox.showwarning("WARNING","MOTHERNAME CANNOT BE EMPTY ")
                        root4.destroy()
                    if len(do)==0:
                        messagebox.showwarning("WARNING","DOB CANNOT BE EMPTY ")
                        root4.destroy()
                    if len(cl)==0:
                        messagebox.showwarning("WARNING","CLASS CANNOT BE EMPTY ")
                        root4.destroy()
                    if len(se)==0:
                        messagebox.showwarning("WARNING","STREAM CANNOT BE EMPTY ")
                        root4.destroy()
                    if len(fe)==0:
                        messagebox.showwarning("WARNING","ADMISSION ID CANNOT BE EMPTY ")
                        root4.destroy()


                    if not len(na and fa and mo and do and cl and se and fe)==0:


                        def confirm():
                            import mysql.connector
                            database = mysql.connector.connect(host="localhost",user="root", password="root",database="email")
                            cursorimp=database.cursor()
                            na=NAME.get()
                            fa=FATHERNAME.get()
                            mo=MOTHERNAME.get()
                            do=DOB.get()
                            cl=grade.get()
                            se=sec.get()
                            fe=aid.get()
                            


                            query=("INSERT INTO `email`.`data` (`admissionid`, `name`, `fathername`, `mothername`, `class`, `sec`, `dob`, `sub1`, `sub2`, `sub3`, `sub4`, `sub5`, `sub6`, `sub7`, `sub8`) VALUES (%s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s);")



                            #11sci
                           
                            
                            

                            if grade.get()=="XI" and sec.get()=="SCIENCE":
                                s1=mn.get()                            
                                s2=bv.get()                            
                                s3=vc.get()                           
                                s4=xz.get()                            
                                s5=lk.get()                            
                                s6=jh.get()                            
                                s7=hg.get()                            
                                s8=ll.get()
                            
                                val11b=(fe,na,fa,mo,cl,se,do,s1,s2,s3,s4,s5,s6,s7,s8)
                                cursorimp.execute(query,val11b)
                                NAME.delete(0,END)
                                FATHERNAME.delete(0,END)
                                MOTHERNAME.delete(0,END)
                                DOB.delete(0,END)
                                grade.delete(0,END)
                                sec.delete(0,END)
                                aid.delete(0,END)
                                NAME.focus_set()
                                '''

                                mobo=messagebox.askquestion("succesful","enter another data")
                                if mobo=="no":
                                    root5.destroy()

                                if mobo=="yes":
                                    root5.destroy()
                                '''


                            #for 11arts                                              
                            if grade.get()=="XI" and sec.get()=="HUMANITIES":
                                ss1=ass.get()
                                ss2=but.get()
                                ss3=fet.get()
                                ss4=diy.get()
                                ss5=lik.get()
                                ss6=sha.get()
                                ss7=hue.get()
                                ss8=0
                                val11a=(fe,na,fa,mo,cl,se,do,ss1,ss2,ss3,ss4,ss5,ss6,ss7,ss8)
                                cursorimp.execute(query,val11a)

                                NAME.delete(0,END)
                                FATHERNAME.delete(0,END)
                                MOTHERNAME.delete(0,END)
                                DOB.delete(0,END)
                                grade.delete(0,END)
                                sec.delete(0,END)
                                aid.delete(0,END)
                                NAME.focus_set()






                            #for 12sci

                            if grade.get()=="XII" and sec.get()=="SCIENCE":
                                sss1=qz.get()
                                sss2=wx.get()
                                sss3=ec.get()
                                sss4=rv.get()
                                sss5=tb.get()
                                sss6=um.get()
                                sss7=un.get()
                                sss8=pm.get()

                                val12b=(fe,na,fa,mo,cl,se,do,sss1,sss2,sss3,sss4,sss5,sss6,sss7,sss8)
                                cursorimp.execute(query,val12b)

                                NAME.delete(0,END)
                                FATHERNAME.delete(0,END)
                                MOTHERNAME.delete(0,END)
                                DOB.delete(0,END)
                                grade.delete(0,END)
                                sec.delete(0,END)
                                aid.delete(0,END)
                                NAME.focus_set()










                            #for 12arts

                            if grade.get()=="XII" and sec.get()=="HUMANITIES":
                                ssss1=mno.get()
                                ssss2=pqr.get()
                                ssss3=stu.get()
                                ssss4=vwx.get()
                                ssss5=yza.get()
                                ssss6=bcd.get()
                                ssss7=efg.get()
                                ssss8=0




                                val12a=(fe,na,fa,mo,cl,se,do,ssss1,ssss2,ssss3,ssss4,ssss5,ssss6,ssss7,ssss8)
                                cursorimp.execute(query,val12a)
                                NAME.delete(0,END)
                                FATHERNAME.delete(0,END)
                                MOTHERNAME.delete(0,END)
                                DOB.delete(0,END)
                                grade.delete(0,END)
                                sec.delete(0,END)
                                aid.delete(0,END)
                                NAME.focus_set()


                            






                            

                            database.commit()


                            print("success")


                        if grade.get()=="XI" and sec.get()=="SCIENCE":
                            na=NAME.get()
                            fa=FATHERNAME.get()
                            mo=MOTHERNAME.get()
                            do=DOB.get()
                            cl=grade.get()
                            se=sec.get()
                            fe=aid.get()
                            root5=Tk()
                            root5.configure(background="cyan")
                            root5.geometry("11000x11000")
                            AB=Label(root5,text="NAME:",font=('december',20),bg='cyan',fg="purple")
                            AB.place(x=0,y=10)
                            xx=Label(root5,text="FATHERNAME:",font=('december',20),bg='cyan',fg="purple")
                            xx.place(x=200,y=10)
                            cc=Label(root5,text="MOTHERNAME:",font=('december',20),bg='cyan',fg="purple")
                            cc.place(x=500,y=10)
                            vv=Label(root5,text="D.O.B:",font=('december',20),bg='cyan',fg="purple")
                            vv.place(x=800,y=10)
                            bb=Label(root5,text="CLASS:",font=('december',20),bg='cyan',fg="purple")
                            bb.place(x=990,y=10)
                            nn=Label(root5,text="STREAM:",font=('december',20),bg='cyan',fg="purple")
                            nn.place(x=1190,y=10)
                            mm=Label(root5,text="ADMs no:",font=('december',20),bg='cyan',fg="purple")
                            mm.place(x=1390,y=10)
                            a=Label(root5,text=na)
                            a.place(x=0,y=40)
                            b=Label(root5,text=fa)
                            b.place(x=200,y=40)
                            c=Label(root5,text=mo)
                            c.place(x=500,y=40)
                            d=Label(root5,text=do)
                            d.place(x=800,y=40)
                            e=Label(root5,text=cl)
                            e.place(x=990,y=40)
                            f=Label(root5,text=se)
                            f.place(x=1190,y=40)
                            g=Label(root5,text=fe)
                            g.place(x=1390,y=40)

                            mn=Entry(root5,)
                            mn.place(x=900,y=200)
                            bv=Entry(root5,)
                            bv.place(x=900,y=250)
                            vc=Entry(root5,)
                            vc.place(x=900,y=300)
                            xz=Entry(root5,)
                            xz.place(x=900,y=350)
                            lk=Entry(root5,)
                            lk.place(x=900,y=400)
                            jh=Entry(root5,)
                            jh.place(x=900,y=450)
                            hg=Entry(root5,)
                            hg.place(x=900,y=500)
                            ll=Entry(root5,)
                            ll.place(x=900,y=550)

                            qw=Label(root5,text="ENGLISH:",font=('december',20),bg='cyan')
                            qw.place(x=400,y=200)
                            er=Label(root5,font=('december',20,),text="HINDI:",bg='cyan')
                            er.place(x=400,y=250)
                            rt=Label(root5,font=('december',20),text="MATHS:",bg='cyan')
                            rt.place(x=400,y=300)
                            yh=Label(root5,font=('december',20),text="PHYSICS:",bg='cyan')
                            yh.place(x=400,y=350)
                            uy=Label(root5,font=('december',20),text="CHEMISTRY:",bg='cyan')
                            uy.place(x=400,y=400)
                            yu=Label(root5,font=('december',20),text="BIOLOGY:",bg='cyan')
                            yu.place(x=400,y=450)
                            op=Label(root5,font=('december',20),text="COM SCI:",bg='cyan')
                            op.place(x=400,y=500)
                            wr=Label(root5,font=('december',20),text="PHY EDU:",bg='cyan')
                            wr.place(x=400,y=550)









                            asd=Button(root5,text="confirm",width=50,height=2,command=confirm,bg="blue")
                            asd.place(x=550,y=600)
                            o=Label(root5,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
                            o.place(x=0,y=80)
                            l=Label(root5,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
                            l.place(x=0,y=700)                            

                            root5.mainloop()
                            

                        if grade.get()=="XII" and sec.get()=="SCIENCE":
                            na=NAME.get()
                            fa=FATHERNAME.get()
                            mo=MOTHERNAME.get()
                            do=DOB.get()
                            cl=grade.get()
                            se=sec.get()
                            fe=aid.get()
                            root6=Tk()
                            root6.configure(background="cyan")
                            root6.geometry("11000x11000")
                            zz=Label(root6,text="NAME:",font=('december',20),bg='cyan',fg="purple")
                            zz.place(x=0,y=10)
                            xx=Label(root6,text="FATHERNAME:",font=('december',20),bg='cyan',fg="purple")
                            xx.place(x=200,y=10)
                            cc=Label(root6,text="MOTHERNAME:",font=('december',20),bg='cyan',fg="purple")
                            cc.place(x=500,y=10)
                            vv=Label(root6,text="D.O.B:",font=('december',20),bg='cyan',fg="purple")
                            vv.place(x=800,y=10)
                            bb=Label(root6,text="CLASS:",font=('december',20),bg='cyan',fg="purple")
                            bb.place(x=990,y=10)
                            nn=Label(root6,text="STREAM:",font=('december',20),bg='cyan',fg="purple")
                            nn.place(x=1190,y=10)
                            mm=Label(root6,text="ADMs no:",font=('december',20),bg='cyan',fg="purple")
                            mm.place(x=1390,y=10)
                            a=Label(root6,text=na)
                            a.place(x=0,y=40)
                            b=Label(root6,text=fa)
                            b.place(x=200,y=40)
                            c=Label(root6,text=mo)
                            c.place(x=500,y=40)
                            d=Label(root6,text=do)
                            d.place(x=800,y=40)
                            e=Label(root6,text=cl)
                            e.place(x=990,y=40)
                            f=Label(root6,text=se)
                            f.place(x=1190,y=40)
                            g=Label(root6,text=fe)
                            g.place(x=1390,y=40)


                            qz=Entry(root6,)
                            qz.place(x=900,y=200)
                            wx=Entry(root6,)
                            wx.place(x=900,y=250)
                            ec=Entry(root6,)
                            ec.place(x=900,y=300)
                            rv=Entry(root6,)
                            rv.place(x=900,y=350)
                            tb=Entry(root6,)
                            tb.place(x=900,y=400)
                            um=Entry(root6,)
                            um.place(x=900,y=450)
                            un=Entry(root6,)
                            un.place(x=900,y=500)
                            pm=Entry(root6,)
                            pm.place(x=900,y=550)

                            qw=Label(root6,text="ENGLISH:",font=('december',20),bg='cyan')
                            qw.place(x=400,y=200)
                            er=Label(root6,font=('december',20,),text="HINDI:",bg='cyan')
                            er.place(x=400,y=250)
                            rt=Label(root6,font=('december',20),text="MATHS:",bg='cyan')
                            rt.place(x=400,y=300)
                            yh=Label(root6,font=('december',20),text="PHYSICS:",bg='cyan')
                            yh.place(x=400,y=350)
                            uy=Label(root6,font=('december',20),text="CHEMISTRY:",bg='cyan')
                            uy.place(x=400,y=400)
                            yu=Label(root6,font=('december',20),text="BIOLOGY:",bg='cyan')
                            yu.place(x=400,y=450)
                            op=Label(root6,font=('december',20),text="COM SCI:",bg='cyan')
                            op.place(x=400,y=500)
                            wr=Label(root6,font=('december',20),text="PHY EDU:",bg='cyan')
                            wr.place(x=400,y=550)









                            asd=Button(root6,text="confirm",width=50,height=2,command=confirm,bg="blue")
                            asd.place(x=550,y=600)
                            o=Label(root6,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
                            o.place(x=0,y=80)
                            l=Label(root6,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
                            l.place(x=0,y=700)                            

                            root6.mainloop()


                        if grade.get()=="XII" and sec.get()=="HUMANITIES":
                            na=NAME.get()
                            fa=FATHERNAME.get()
                            mo=MOTHERNAME.get()
                            do=DOB.get()
                            cl=grade.get()
                            se=sec.get()
                            fe=aid.get()

                            root7=Tk()
                            root7.configure(background="cyan")
                            root7.geometry("11000x11000")
                            zz=Label(root7,text="NAME:",font=('december',20),bg='cyan',fg="purple")
                            zz.place(x=0,y=10)
                            xx=Label(root7,text="FATHERNAME:",font=('december',20),bg='cyan',fg="purple")
                            xx.place(x=200,y=10)
                            cc=Label(root7,text="MOTHERNAME:",font=('december',20),bg='cyan',fg="purple")
                            cc.place(x=500,y=10)
                            vv=Label(root7,text="D.O.B:",font=('december',20),bg='cyan',fg="purple")
                            vv.place(x=800,y=10)
                            bb=Label(root7,text="CLASS:",font=('december',20),bg='cyan',fg="purple")
                            bb.place(x=990,y=10)
                            nn=Label(root7,text="STREAM:",font=('december',20),bg='cyan',fg="purple")
                            nn.place(x=1190,y=10)
                            mm=Label(root7,text="ADMS NO:",font=('december',20),bg='cyan',fg="purple")
                            mm.place(x=1390,y=10)
                            a=Label(root7,text=na)
                            a.place(x=0,y=40)
                            b=Label(root7,text=fa)
                            b.place(x=200,y=40)
                            c=Label(root7,text=mo)
                            c.place(x=500,y=40)
                            d=Label(root7,text=do)
                            d.place(x=800,y=40)
                            e=Label(root7,text=cl)
                            e.place(x=990,y=40)
                            f=Label(root7,text=se)
                            f.place(x=1190,y=40)
                            g=Label(root7,text=fe)
                            g.place(x=1390,y=40)


                            mno=Entry(root7,)
                            mno.place(x=900,y=200)
                            pqr=Entry(root7,)
                            pqr.place(x=900,y=250)
                            stu=Entry(root7,)
                            stu.place(x=900,y=300)
                            vwx=Entry(root7,)
                            vwx.place(x=900,y=350)
                            yza=Entry(root7,)
                            yza.place(x=900,y=400)
                            bcd=Entry(root7,)
                            bcd.place(x=900,y=450)
                            efg=Entry(root7,)
                            efg.place(x=900,y=500)
                            

                            qw=Label(root7,text="ENGLISH:",font=('december',20),bg='cyan')
                            qw.place(x=400,y=200)
                            er=Label(root7,font=('december',20,),text="HINDI:",bg='cyan')
                            er.place(x=400,y=250)
                            rt=Label(root7,font=('december',20),text="HISTORY:",bg='cyan')
                            rt.place(x=400,y=300)
                            yh=Label(root7,font=('december',20),text="GEOGRAPHY:",bg='cyan')
                            yh.place(x=400,y=350)
                            uy=Label(root7,font=('december',20),text="ECONOMICS:",bg='cyan')
                            uy.place(x=400,y=400)
                            yu=Label(root7,font=('december',20),text="POL SCI:",bg='cyan')
                            yu.place(x=400,y=450)
                            op=Label(root7,font=('december',20),text="PHY EDU:",bg='cyan')
                            op.place(x=400,y=500)
                            









                            asd=Button(root7,text="confirm",width=50,height=2,command=confirm,bg="blue")
                            asd.place(x=550,y=600)

                            o=Label(root7,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
                            o.place(x=0,y=80)
                            l=Label(root7,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
                            l.place(x=0,y=700)


                            root7.mainloop()

                        if grade.get()=="XI" and sec.get()=="HUMANITIES":
                            na=NAME.get()
                            fa=FATHERNAME.get()
                            mo=MOTHERNAME.get()
                            do=DOB.get()
                            cl=grade.get()
                            se=sec.get()
                            fe=aid.get()
                            root8=Tk()

                            root8.configure(background="cyan")
                            root8.geometry("11000x11000")
                            zz=Label(root8,text="NAME:",font=('december',20),bg='cyan',fg="purple")
                            zz.place(x=0,y=10)
                            xx=Label(root8,text="FATHERNAME:",font=('december',20),bg='cyan',fg="purple")
                            xx.place(x=200,y=10)
                            cc=Label(root8,text="MOTHERNAME:",font=('december',20),bg='cyan',fg="purple")
                            cc.place(x=500,y=10)
                            vv=Label(root8,text="D.O.B:",font=('december',20),bg='cyan',fg="purple")
                            vv.place(x=800,y=10)
                            bb=Label(root8,text="CLASS:",font=('december',20),bg='cyan',fg="purple")
                            bb.place(x=990,y=10)
                            nn=Label(root8,text="STREAM:",font=('december',20),bg='cyan',fg="purple")
                            nn.place(x=1190,y=10)
                            mm=Label(root8,text="ADMS NO:",font=('december',20),bg='cyan',fg="purple")
                            mm.place(x=1390,y=10)
                            a=Label(root8,text=na)
                            a.place(x=0,y=29)
                            b=Label(root8,text=fa)
                            b.place(x=200,y=29)
                            c=Label(root8,text=mo)
                            c.place(x=500,y=29)
                            d=Label(root8,text=do)
                            d.place(x=800,y=29)
                            e=Label(root8,text=cl)
                            e.place(x=990,y=29)
                            f=Label(root8,text=se)
                            f.place(x=1190,y=29)
                            g=Label(root8,text=fe)
                            g.place(x=1390,y=29)


                            ass=Entry(root8,)
                            ass.place(x=900,y=200)
                            but=Entry(root8,)
                            but.place(x=900,y=250)
                            fet=Entry(root8,)
                            fet.place(x=900,y=300)
                            diy=Entry(root8,)
                            diy.place(x=900,y=350)
                            lik=Entry(root8,)
                            lik.place(x=900,y=400)
                            sha=Entry(root8,)
                            sha.place(x=900,y=450)
                            hue=Entry(root8,)
                            hue.place(x=900,y=500)
                            

                            qw=Label(root8,text="ENGLISH:",font=('december',20),bg="cyan")
                            qw.place(x=400,y=200)
                            er=Label(root8,font=('december',20,),text="HINDI:",bg="cyan")
                            er.place(x=400,y=250)
                            rt=Label(root8,font=('december',20),text="HISTORY:",bg="cyan")
                            rt.place(x=400,y=300)
                            yh=Label(root8,font=('december',20),text="GEOGRAPHY:",bg="cyan")
                            yh.place(x=400,y=350)
                            uy=Label(root8,font=('december',20),text="ECONOMICS:",bg="cyan")
                            uy.place(x=400,y=400)
                            yu=Label(root8,font=('december',20),text="POL SCI:",bg="cyan")
                            yu.place(x=400,y=450)
                            op=Label(root8,font=('december',20),text="PHY EDU:",bg="cyan")
                            op.place(x=400,y=500)









                            asd=Button(root8,text="COMFIRM",width=50,height=2,command=confirm,bg="blue")
                            asd.place(x=550,y=600)
                            
                            o=Label(root8,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
                            o.place(x=0,y=80)
                            l=Label(root8,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
                            l.place(x=0,y=700)
                            

                            root8.mainloop()

                            


                root4=Tk()
                
                root4.configure(background="cyan")
                root4.geometry("1000000000x10000000")
                root4.title(" FILL STUDENT DETAILS ")
    
                head=Label(root4,text=" 𝕎𝔼𝕃ℂ𝕆𝕄𝔼 𝕋𝕆 𝕄𝔸𝔼𝕂𝕊ℍ𝔼𝔼𝕋 𝔾𝔼ℕ𝔼ℝ𝔸𝕋𝕆ℝ ",font=('december',40),fg='red',bg="cyan")
                head.pack()

                j=Label(root4,text=" 𝒫𝐿𝐸𝒜𝒮𝐸 𝐸𝒩𝒯𝐸𝑅 𝒯𝐻𝐸 𝒮𝒯𝒰𝒟𝐸𝒩𝒯 𝒟𝐸𝒯𝒜𝐼𝐿𝒮 ",font=('december',30),fg='dark blue',bg="cyan")
                j.pack()

                NAME=Entry(root4,font=('december',25),bg="silver")
                NAME.place(x=300,y=250)
                NM=Label(root4,text="STUDENT NAME:",font=('december',20),bg="cyan")
                NM.place(y=250,x=70)

                adid=Label(root4,text="STUDENT ADMISSION ID:",font=('december',20),bg="cyan")
                adid.place(y=250,x=698)
                aid=Entry(root4,font=('december',25),bg="silver")
                aid.place(y=250,x=1070)

                FATHERNAME=Entry(root4,font=('december',25),bg="silver")
                FATHERNAME.place(x=300,y=350)
                FN=Label(root4,text="FATHER NAME:",font=('december',20),bg="cyan")
                FN.place(y=350,x=80)

                MOTHERNAME=Entry(root4,font=('december',25),bg="silver")
                MOTHERNAME.place(x=300,y=450)
                MN=Label(root4,text="MOTHER NAME:",font=('december',20),bg="cyan")
                MN.place(y=450,x=80)
                DOB=Entry(root4,font=('december',25),bg="silver")
                DOB.place(x=300,y=550)
                DB=Label(root4,text="DATE OF BIRTH:",font=('december',20),bg="cyan")
                DB.place(y=550,x=80)
                lais=Label(root4,text="SELECT CLASS:",font=('december',12),bg='blue',fg="white")
                lais.pack()
                grade=ttk.Combobox(root4,values=("XI", "XII"),height=2,width=20)
                grade.pack()
                la=Label(root4,text="SELECT STEAM:",font=('december',12),bg='blue',fg="white")
                la.pack()
                sec=ttk.Combobox(root4,values=("SCIENCE", "HUMANITIES"),height=2,width=20)
                sec.pack()

               

                
                b=Button(root4,text="NEXT:",font=('december',15),width=39,height=1,bg="purple",command=mark)
                b.place(x=500,y=640)
                
                l=Label(root4,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
                l.place(x=0,y=700)

                root4.mainloop()





            
            root2.destroy()
            rootmf=Tk()
            rootmf.configure(background="cyan")
            rootmf.geometry("1000000000x10000000")
            rootmf.title("MAIN FRAME")
            lab=Label(rootmf,text="𝕄𝔸ℝ𝕂𝕊 𝕄𝔸𝕀ℕ𝔽ℝ𝔸𝕄𝔼 𝔻𝔹",font=('december',40),bg="cyan",fg='red')
            lab.pack()
            de=Button(rootmf,text="ENTER  STUDENTS DATA",font=('december',12),width=50,height=2,bg="darkblue",command=stud,fg="white")
            de.place(x=550,y=250)


            lol=Button(rootmf,text="EDIT  STUDENTS DATA",font=('december',12),width=50,height=2,bg="darkblue",fg="white",command=debo)
            lol.place(x=550,y=350)


            gm=Button(rootmf,text="GET MARKSHEET",font=('december',12),width=50,height=2,bg="violet",command=getmak,fg="white")
            gm.place(x=550,y=450)

            o=Label(rootmf,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
            o.pack()
            l=Label(rootmf,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
            l.place(x=0,y=750)



            rootmf.mainloop()
        else:
            lay=Label(root2,text="USER_ID or PASSWORD IS INVALID ",font=('december',20),fg="red",bg="cyan")
            lay.place(x=500,y=600)
        mydb.close()
        
        
                





                    
    root2.configure(background="cyan")
    root2.geometry("1000000000x10000000")
    root2.title(" LOGIN - PAGE ")
    head=Label(root2,text="𝕃𝕆𝔾-𝕀ℕ",font=('december',40),bg="cyan",fg='red')
    head.pack()

    email=Entry(root2,font=('december',30))
    email.place(x=500,y=250)
    em=Label(root2,text="USER_ID:",font=('december',25),bg="cyan")
    em.place(y=240,x=179)

    password=Entry(root2,font=('december',30))
    password.place(x=500,y=400)
    pas=Label(root2,text="PASSWORD:",font=('december',25),bg="cyan")
    pas.place(y=400,x=179)

    o=Label(root2,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
    o.pack()
    l=Label(root2,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
    l.place(x=0,y=700)


    b=Button(root2,text="LOGIN",bg="BLUE",command=system,font=('december',11),width=50,height=2)
    b.place(x=500,y=500)



    root2.mainloop()
    

def false():
    
    root3=Tk()
    def signp():
        abs=password1.get()
        bbs=email1.get()
        if len(bbs)==0:
            messagebox.showwarning("warning","user_id cannot be null")
        if len(abs)==0:
            messagebox.showwarning("warning","password cannot be null")
        
        else:
            import mysql.connector
            mydb = mysql.connector.connect(host="localhost",user="root", password="root",database="email")
            mycursor = mydb.cursor()
            query = "SELECT * FROM email.user WHERE id = %s and pas= %s "
            id = (email1.get())
            pas=(password1.get())
            mycursor.execute(query, (id,pas,))
            myresult = mycursor.fetchone()
            if myresult is not None:
                messagebox.showerror("error","this user_id is alreadyregistered")

            if myresult is  None:
                db=con.connect(host="localhost",user="root", password="root",database="email")
                cur=db.cursor()
                id=(email1.get())
                pas=(password1.get())
                sql=("insert into email.user (id,pas) values(%s,%s)")
                val=(id,pas)
                cur.execute(sql,val)
                db.commit()
                sup=Label(root3,text="𝙎𝙞𝙜𝙣-𝙪𝙥 𝙨𝙪𝙘𝙘𝙚𝙨𝙨𝙛𝙪𝙡𝙡𝙮 ✓",fg='blue',font=('december',30),bg="cyan")
                sup.place(x=550,y=600)

            
    


    root3.configure(background="cyan")
    root3.geometry("1000000000x10000000")
    root3.title(" SIGN-UP PAGE ")
    head=Label(root3,text="𝕊𝕀𝔾ℕ-𝕌ℙ",font=('december',40),bg="cyan",fg='red')
    head.pack()

    email1=Entry(root3,font=('december',30))
    email1.place(x=500,y=250)
    em=Label(root3,text="ENTER USER_ID:",font=('december',25),bg="cyan")
    em.place(y=230,x=179)

    password1=Entry(root3,font=('december',30))
    password1.place(x=500,y=400)
    pas=Label(root3,text="PASSWORD:",font=('december',25),bg="cyan")
    pas.place(y=400,x=179)

    o=Label(root3,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
    o.pack()
    l=Label(root3,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
    l.place(x=0,y=700)

    b=Button(root3,text="SIGNUP",bg="PURPLE",fg="white",font=('december',11),width=50,height=2,command=signp)
    b.place(x=500,y=500)

    root3.mainloop()



root.configure(background="cyan")
root.geometry("1000000000x10000000")
root.title("MARKSHEET MANAGEMENT SYSTEM")
h=Label(root,text="𝕄𝔸ℝ𝕂𝕊ℍ𝔼𝔼𝕋 𝕄𝔸ℕ𝔸𝔾𝔼𝕄𝔼ℕ𝕋 𝕊𝕐𝕊𝕋𝔼𝕄",font=('december',35),fg="red",background="cyan")
h.pack()







login=Button(root,text="LOGIN",font=('december',12),width=50,height=2,command=true,bg="BLUE",fg="white")
login.place(x=500,y=250)
signup=Button(root,text="SIGNUP",font=('december',12),width=50,height=2,command=false,bg="PURPLE",fg="white")
signup.place(x=500,y=400)

    
o=Label(root,text="",font=('december',34))
o.pack()

o=Label(root,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
o.place(x=0,y=80)
l=Label(root,text="-----------------------------------------------------------------------------------------------------",font=('december',34),bg="cyan")
l.place(x=0,y=700)
root.mainloop()
