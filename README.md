# Quan_li_quan_cafe
#include <stdio.h>
#include <string.h>
#include <conio.h>

struct ThucUong{
    char ten[30];
    char loai[30];
    int giatien;
};

void nhap(ThucUong &TU){
	fflush(stdin);
	printf("\nTen thuc uong: ");
    gets(TU.ten);
    printf("Loai thuc uong: ");
    gets(TU.loai);
    printf("Nhap gia tien thuc uong: ");
    scanf("%d", &TU.giatien);
}

void xuat(ThucUong TU){
	printf("%-20s %-20s %-15d \n", TU.ten, TU.loai, TU.giatien);
}
void nhapDuLieu(ThucUong TU[], int &n){
    printf("Nhap so luong thuc uong: ");
    scanf("%d", &n);
    for(int i = 0; i<n; i++){
    	printf("Nhap thong tin thuc uong %d: \n", i);
    	nhap(TU[i]);
    }
}
void xuatDuLieu(ThucUong TU[], int n){
	printf("\n --------- Thong tin thuc uong -----\n");
    printf("%-20s %-20s %-20s\n", "Ten thuc uong", "Loai" , "Gia tien");
    for (int i=0; i<n; i++){
        xuat(TU[i]);
    }
}
