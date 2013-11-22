

using namespace std;
#include <iostream>
#include <fstream>
#include <string>

#include <cmath>
#include "TRoot.h"
#include <TCanvas.h>
#include <TGraph.h>
#include <TFrame.h>
#include <TAxis.h>
#include <TEllipse.h>
#include <TPaveLabel.h>
#include <TH1F.h>
#include <RooEllipse.h>

#include <vector>
#include <stdlib.h>
#include <sstream>


typedef unsigned int uint ;
#define round(x) ((x)>=0?(double)((x)+0.5):(double)((x)-0.5))




//===================================================================
int main( ) {

	gROOT->SetStyle("Plain");
	

/*	
	//Draw ellipses
	//Author: Rene Brun
	{
		TCanvas * c1 = new TCanvas("c1");
		c1->Range(0,0,1,1);
		TPaveLabel pel(0.1,0.8,0.9,0.95,"Examples of Ellipses");
		pel.SetFillColor(42);
		pel.Draw();
		TEllipse el1(0.25,0.25,.1,.2);
		el1.Draw();
		TEllipse el2(0.25,0.6,.2,.1);
		el2.SetFillColor(6);
		el2.SetFillStyle(3008);
		el2.Draw();
		TEllipse el3(0.75,0.6,.2,.1,45,315);
		el3.SetFillColor(2);
		el3.SetFillStyle(1001);
		el3.SetLineColor(4);
		el3.Draw();
		TEllipse el4(0.75,0.25,.2,.15,45,315,62);
		el4.SetFillColor(5);
		el4.SetFillStyle(1001);
		el4.SetLineColor(4);
		el4.SetLineWidth(6);
		el4.Draw();
		c1->Update();
		//c1->Draw();
		return 1;
	}

 */
	
	
	
	// 1=BLACK  2=RED  4=BLUE    3=GREEN     5=YELLOW
	

	TCanvas *cv = new TCanvas( "ts", "ts" , 600,600);
	//TCanvas * cv = new TCanvas ;
	cv->Divide(1,2) ;
	
	cv->SetGrid();
	cv->GetFrame()->SetFillColor(21);
	cv->GetFrame()->SetBorderSize(12);
	cv->SetTitle("Lifetime comparison ");

	cv->cd(1) ;
	
	//TGraph gr( ENDYEAR-STARTYEAR+1, year, anomalyGHCN ) ;
	TGraph *gri = new TGraph("fftinput.txt") ;
	gri->SetTitle("input");
	//gri->SetMarkerStyle(1);
	//gri->SetMarkerColor(0);
	gri->SetLineWidth(2);	
	gri->SetLineColor(2);
	gri->Draw( "APL");
	//cv->Draw();	
	//cv->Update();

	cv->cd(2) ;

	//TGraph gr( ENDYEAR-STARTYEAR+1, year, anomalyGHCN ) ;
	TGraph *gr = new TGraph("fftresults.txt") ;
	gr->SetTitle("fft of input");
	//gr->SetMarkerStyle(1);
	//gr->SetMarkerColor(0);
	gr->SetLineWidth(2);	
	gr->SetLineColor(2);
	gr->Draw( "APL");

	
	cv->Draw();	
	cv->Update();

	
	 
	
}
