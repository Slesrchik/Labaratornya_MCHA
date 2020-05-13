package lab5;

public class Gradient {

	public static void main(String[] args) {
		double [][] Q ={{500.1, 11.2, 11.1, -13.1}, {-3.3, 500.1, 30.1, -20.1}, {7.5, 1.3, 500.1, 10}, {1.7, 7.5, -1.8, 500.1}};
		double [] p={1.3, 1.1, 20, 1.1};
		double [] x0={0, 0, 0, 0};
		double [] x1={0, 0, 0, 0};
		double [] r = new double [4];
		double [] r1 = new double [4];
		double s, s1=0;
		int k=0;
		do
		{
		for(int i=0; i<4; i++)
		{
		r[i]=p[i];
		for (int j=0; j<4; j++)
		{
		r[i]-=Q[i][j]*x0[j];
		}
		}
		s=0;
		for(int i=0; i<4; i++)
		{
		s+=r[i]*r[i];
		}
		for(int i=0; i<4; i++)
		{
		r1[i]=0;
		for(int j=0; j<4; j++)
		{
		r1[i]+=Q[i][j]*r[j];
		}
		}
		s1=0;
		for(int i=0; i<4; i++)
		{
		s1+=r[i]*r1[i];
		}
		s/=s1;
		for(int i=0; i<4; i++)
		x1[i]+=s*r[i];
		s=0;
		for(int i=0; i<4; i++)
		{
		s+=(x0[i]-x1[i])*(x0[i]-x1[i]);
		x0[i]=x1[i];
		}
		k++;
		}
		while(k<50000 && Math.sqrt(s)>0.000001);
		System.out.println(x1[0]+" "+x1[1]+" "+x1[2]+" "+x1[3]);
		System.out.println(k);

	}

}
