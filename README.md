{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Let's explore real payroll data of Chicago city. This data is available on kaggle website and can be downloaded using the provided link:https://www.kaggle.com/chicago/chicago-citywide-payroll-data"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Import pandas as pd"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Read City_of_Chicago_payroll_Data.csv as dataframe in pay"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [],
   "source": [
    "pay = pd.read_csv('City_of_Chicago_Payroll_Data.csv')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Show first five records in your data."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Name</th>\n",
       "      <th>Job Titles</th>\n",
       "      <th>Department</th>\n",
       "      <th>Full or Part-Time</th>\n",
       "      <th>Salary or Hourly</th>\n",
       "      <th>Typical Hours</th>\n",
       "      <th>Annual Salary</th>\n",
       "      <th>Hourly Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>ALLISON,  PAUL W</td>\n",
       "      <td>LIEUTENANT</td>\n",
       "      <td>FIRE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$107790.00</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>BRUNO,  KEVIN D</td>\n",
       "      <td>SERGEANT</td>\n",
       "      <td>POLICE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$104628.00</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>COOPER,  JOHN E</td>\n",
       "      <td>LIEUTENANT-EMT</td>\n",
       "      <td>FIRE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$114324.00</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>CRESPO,  VILMA I</td>\n",
       "      <td>STAFF ASST</td>\n",
       "      <td>LAW</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$76932.00</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>DOLAN,  ROBERT J</td>\n",
       "      <td>SERGEANT</td>\n",
       "      <td>POLICE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$111474.00</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "               Name      Job Titles Department Full or Part-Time  \\\n",
       "0  ALLISON,  PAUL W      LIEUTENANT       FIRE                 F   \n",
       "1   BRUNO,  KEVIN D        SERGEANT     POLICE                 F   \n",
       "2   COOPER,  JOHN E  LIEUTENANT-EMT       FIRE                 F   \n",
       "3  CRESPO,  VILMA I      STAFF ASST        LAW                 F   \n",
       "4  DOLAN,  ROBERT J        SERGEANT     POLICE                 F   \n",
       "\n",
       "  Salary or Hourly  Typical Hours Annual Salary Hourly Rate  \n",
       "0           Salary            NaN    $107790.00         NaN  \n",
       "1           Salary            NaN    $104628.00         NaN  \n",
       "2           Salary            NaN    $114324.00         NaN  \n",
       "3           Salary            NaN     $76932.00         NaN  \n",
       "4           Salary            NaN    $111474.00         NaN  "
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay.head()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Get the overview of your data."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "<class 'pandas.core.frame.DataFrame'>\n",
      "RangeIndex: 32658 entries, 0 to 32657\n",
      "Data columns (total 8 columns):\n",
      "Name                 32658 non-null object\n",
      "Job Titles           32658 non-null object\n",
      "Department           32658 non-null object\n",
      "Full or Part-Time    32658 non-null object\n",
      "Salary or Hourly     32658 non-null object\n",
      "Typical Hours        7883 non-null float64\n",
      "Annual Salary        24775 non-null object\n",
      "Hourly Rate          7883 non-null object\n",
      "dtypes: float64(1), object(7)\n",
      "memory usage: 2.0+ MB\n"
     ]
    }
   ],
   "source": [
    "pay.info()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### The number of 'NaN' we have in each column in our data"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Name                     0\n",
       "Job Titles               0\n",
       "Department               0\n",
       "Full or Part-Time        0\n",
       "Salary or Hourly         0\n",
       "Typical Hours        24775\n",
       "Annual Salary         7883\n",
       "Hourly Rate          24775\n",
       "dtype: int64"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay.isnull().sum()\n",
    "# If we need sorted values!\n",
    "#print(pay.isnull().sum().sort_values(ascending=False))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Output the statistics for your dataset."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Name</th>\n",
       "      <th>Job Titles</th>\n",
       "      <th>Department</th>\n",
       "      <th>Full or Part-Time</th>\n",
       "      <th>Salary or Hourly</th>\n",
       "      <th>Typical Hours</th>\n",
       "      <th>Annual Salary</th>\n",
       "      <th>Hourly Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>count</th>\n",
       "      <td>32658</td>\n",
       "      <td>32658</td>\n",
       "      <td>32658</td>\n",
       "      <td>32658</td>\n",
       "      <td>32658</td>\n",
       "      <td>7883.000000</td>\n",
       "      <td>24775</td>\n",
       "      <td>7883</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>unique</th>\n",
       "      <td>32350</td>\n",
       "      <td>1095</td>\n",
       "      <td>36</td>\n",
       "      <td>2</td>\n",
       "      <td>2</td>\n",
       "      <td>NaN</td>\n",
       "      <td>1038</td>\n",
       "      <td>167</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>top</th>\n",
       "      <td>HERNANDEZ,  JUAN C</td>\n",
       "      <td>POLICE OFFICER</td>\n",
       "      <td>POLICE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$90024.00</td>\n",
       "      <td>$35.60</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>freq</th>\n",
       "      <td>5</td>\n",
       "      <td>9393</td>\n",
       "      <td>12973</td>\n",
       "      <td>30676</td>\n",
       "      <td>24775</td>\n",
       "      <td>NaN</td>\n",
       "      <td>2368</td>\n",
       "      <td>1404</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mean</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>34.698719</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>std</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>9.145553</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>min</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>10.000000</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>25%</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>20.000000</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>50%</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>40.000000</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>75%</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>40.000000</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>max</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>40.000000</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                      Name      Job Titles Department Full or Part-Time  \\\n",
       "count                32658           32658      32658             32658   \n",
       "unique               32350            1095         36                 2   \n",
       "top     HERNANDEZ,  JUAN C  POLICE OFFICER     POLICE                 F   \n",
       "freq                     5            9393      12973             30676   \n",
       "mean                   NaN             NaN        NaN               NaN   \n",
       "std                    NaN             NaN        NaN               NaN   \n",
       "min                    NaN             NaN        NaN               NaN   \n",
       "25%                    NaN             NaN        NaN               NaN   \n",
       "50%                    NaN             NaN        NaN               NaN   \n",
       "75%                    NaN             NaN        NaN               NaN   \n",
       "max                    NaN             NaN        NaN               NaN   \n",
       "\n",
       "       Salary or Hourly  Typical Hours Annual Salary Hourly Rate  \n",
       "count             32658    7883.000000         24775        7883  \n",
       "unique                2            NaN          1038         167  \n",
       "top              Salary            NaN     $90024.00      $35.60  \n",
       "freq              24775            NaN          2368        1404  \n",
       "mean                NaN      34.698719           NaN         NaN  \n",
       "std                 NaN       9.145553           NaN         NaN  \n",
       "min                 NaN      10.000000           NaN         NaN  \n",
       "25%                 NaN      20.000000           NaN         NaN  \n",
       "50%                 NaN      40.000000           NaN         NaN  \n",
       "75%                 NaN      40.000000           NaN         NaN  \n",
       "max                 NaN      40.000000           NaN         NaN  "
      ]
     },
     "execution_count": 10,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay.describe(include = 'all')"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### What are the maximum, minimum and average Typical Hours? (use 'Typical Hours' column)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Max Typical Hours are :: 40.0\n",
      "Min Typical Hours are :: 10.0\n",
      "Mean/avg Typical Hours are :: 34.69871876189268\n"
     ]
    }
   ],
   "source": [
    "print('Max Typical Hours are ::', pay['Typical Hours'].max())\n",
    "print('Min Typical Hours are ::', pay['Typical Hours'].min())\n",
    "print('Mean/avg Typical Hours are ::', pay['Typical Hours'].mean())"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### How many employees are on salary and how many are working on hourly basis?\n",
    "Hint: Group the data on 'Salary or Hourly' column. Instead of whole dataset, you can take the single column as input as well."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Name</th>\n",
       "      <th>Job Titles</th>\n",
       "      <th>Department</th>\n",
       "      <th>Full or Part-Time</th>\n",
       "      <th>Typical Hours</th>\n",
       "      <th>Annual Salary</th>\n",
       "      <th>Hourly Rate</th>\n",
       "      <th>Salary</th>\n",
       "      <th>H_Rate</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Salary or Hourly</th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Hourly</th>\n",
       "      <td>7883</td>\n",
       "      <td>7883</td>\n",
       "      <td>7883</td>\n",
       "      <td>7883</td>\n",
       "      <td>7883</td>\n",
       "      <td>0</td>\n",
       "      <td>7883</td>\n",
       "      <td>0</td>\n",
       "      <td>7883</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Salary</th>\n",
       "      <td>24775</td>\n",
       "      <td>24775</td>\n",
       "      <td>24775</td>\n",
       "      <td>24775</td>\n",
       "      <td>0</td>\n",
       "      <td>24775</td>\n",
       "      <td>0</td>\n",
       "      <td>24775</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                   Name  Job Titles  Department  Full or Part-Time  \\\n",
       "Salary or Hourly                                                     \n",
       "Hourly             7883        7883        7883               7883   \n",
       "Salary            24775       24775       24775              24775   \n",
       "\n",
       "                  Typical Hours  Annual Salary  Hourly Rate  Salary  H_Rate  \n",
       "Salary or Hourly                                                             \n",
       "Hourly                     7883              0         7883       0    7883  \n",
       "Salary                        0          24775            0   24775       0  "
      ]
     },
     "execution_count": 44,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay.groupby('Salary or Hourly').count()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Department having maximum number of employees."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "POLICE    12973\n",
       "FIRE       4800\n",
       "Name: Department, dtype: int64"
      ]
     },
     "execution_count": 45,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay['Department'].value_counts().head(2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### The number of employees on Salary and  on Hourly in the Police department."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 46,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Salary or Hourly\n",
       "Hourly       32\n",
       "Salary    12941\n",
       "Name: Department, dtype: int64"
      ]
     },
     "execution_count": 46,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay[pay['Department'] == 'POLICE'].groupby('Salary or Hourly').count()['Department']"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### The mean, max and min salaries."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 47,
   "metadata": {},
   "outputs": [],
   "source": [
    "pay['Salary'] = pay['Annual Salary'].str.replace('$', '').astype(float)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 48,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "min: 0.96\n",
      "max: 300000.0\n",
      "mean: 87512.78024137241\n"
     ]
    }
   ],
   "source": [
    "print('min:', pay['Salary'].min())\n",
    "print('max:', pay['Salary'].max())\n",
    "print('mean:', pay['Salary'].mean())"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 49,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Name</th>\n",
       "      <th>Job Titles</th>\n",
       "      <th>Department</th>\n",
       "      <th>Full or Part-Time</th>\n",
       "      <th>Salary or Hourly</th>\n",
       "      <th>Typical Hours</th>\n",
       "      <th>Annual Salary</th>\n",
       "      <th>Hourly Rate</th>\n",
       "      <th>Salary</th>\n",
       "      <th>H_Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>ALLISON,  PAUL W</td>\n",
       "      <td>LIEUTENANT</td>\n",
       "      <td>FIRE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$107790.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>107790.0</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>BRUNO,  KEVIN D</td>\n",
       "      <td>SERGEANT</td>\n",
       "      <td>POLICE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$104628.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>104628.0</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "               Name  Job Titles Department Full or Part-Time Salary or Hourly  \\\n",
       "0  ALLISON,  PAUL W  LIEUTENANT       FIRE                 F           Salary   \n",
       "1   BRUNO,  KEVIN D    SERGEANT     POLICE                 F           Salary   \n",
       "\n",
       "   Typical Hours Annual Salary Hourly Rate    Salary  H_Rate  \n",
       "0            NaN    $107790.00         NaN  107790.0     NaN  \n",
       "1            NaN    $104628.00         NaN  104628.0     NaN  "
      ]
     },
     "execution_count": 49,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay.head(2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Employee who has the maximum salary. "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 50,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Name                         EVANS,  GINGER S\n",
       "Job Titles           COMMISSIONER OF AVIATION\n",
       "Department                           AVIATION\n",
       "Full or Part-Time                           F\n",
       "Salary or Hourly                       Salary\n",
       "Typical Hours                             NaN\n",
       "Annual Salary                      $300000.00\n",
       "Hourly Rate                               NaN\n",
       "Salary                                 300000\n",
       "H_Rate                                    NaN\n",
       "Name: 8310, dtype: object"
      ]
     },
     "execution_count": 50,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#pay[pay['Salary'] == pay['Salary'].max()]\n",
    "pay.loc[pay['Salary'].idxmax()]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Find an employee who has the minimum salary"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 51,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Name                           KOCH,  STEVEN \n",
       "Job Titles           ADMINISTRATIVE SECRETARY\n",
       "Department                     MAYOR'S OFFICE\n",
       "Full or Part-Time                           F\n",
       "Salary or Hourly                       Salary\n",
       "Typical Hours                             NaN\n",
       "Annual Salary                           $0.96\n",
       "Hourly Rate                               NaN\n",
       "Salary                                   0.96\n",
       "H_Rate                                    NaN\n",
       "Name: 15387, dtype: object"
      ]
     },
     "execution_count": 51,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay.loc[pay['Salary'].idxmin()]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### What are the mean, max and min Hourly Rate?"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "we will use .str and replace()\n",
    "we are going to create a new column name \"H_Rate\" and separate the number from dollar sign as float."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 52,
   "metadata": {},
   "outputs": [],
   "source": [
    "pay['H_Rate'] = pay['Hourly Rate'].str.replace('$', '').astype(float)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 53,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "min: 2.65\n",
      "max: 96.0\n",
      "mean: 32.86819231257292\n"
     ]
    }
   ],
   "source": [
    "print('min:', pay['H_Rate'].min())\n",
    "print('max:', pay['H_Rate'].max())\n",
    "print('mean:', pay['H_Rate'].mean())"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "metadata": {
    "scrolled": true
   },
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Name</th>\n",
       "      <th>Job Titles</th>\n",
       "      <th>Department</th>\n",
       "      <th>Full or Part-Time</th>\n",
       "      <th>Salary or Hourly</th>\n",
       "      <th>Typical Hours</th>\n",
       "      <th>Annual Salary</th>\n",
       "      <th>Hourly Rate</th>\n",
       "      <th>Salary</th>\n",
       "      <th>H_Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>ALLISON,  PAUL W</td>\n",
       "      <td>LIEUTENANT</td>\n",
       "      <td>FIRE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$107790.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>107790.0</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>BRUNO,  KEVIN D</td>\n",
       "      <td>SERGEANT</td>\n",
       "      <td>POLICE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$104628.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>104628.0</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>COOPER,  JOHN E</td>\n",
       "      <td>LIEUTENANT-EMT</td>\n",
       "      <td>FIRE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$114324.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>114324.0</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>CRESPO,  VILMA I</td>\n",
       "      <td>STAFF ASST</td>\n",
       "      <td>LAW</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$76932.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>76932.0</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>DOLAN,  ROBERT J</td>\n",
       "      <td>SERGEANT</td>\n",
       "      <td>POLICE</td>\n",
       "      <td>F</td>\n",
       "      <td>Salary</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$111474.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>111474.0</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "               Name      Job Titles Department Full or Part-Time  \\\n",
       "0  ALLISON,  PAUL W      LIEUTENANT       FIRE                 F   \n",
       "1   BRUNO,  KEVIN D        SERGEANT     POLICE                 F   \n",
       "2   COOPER,  JOHN E  LIEUTENANT-EMT       FIRE                 F   \n",
       "3  CRESPO,  VILMA I      STAFF ASST        LAW                 F   \n",
       "4  DOLAN,  ROBERT J        SERGEANT     POLICE                 F   \n",
       "\n",
       "  Salary or Hourly  Typical Hours Annual Salary Hourly Rate    Salary  H_Rate  \n",
       "0           Salary            NaN    $107790.00         NaN  107790.0     NaN  \n",
       "1           Salary            NaN    $104628.00         NaN  104628.0     NaN  \n",
       "2           Salary            NaN    $114324.00         NaN  114324.0     NaN  \n",
       "3           Salary            NaN     $76932.00         NaN   76932.0     NaN  \n",
       "4           Salary            NaN    $111474.00         NaN  111474.0     NaN  "
      ]
     },
     "execution_count": 30,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay.head()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### How many employees are getting max Hourly Rate?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 54,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Name                 1\n",
       "Job Titles           1\n",
       "Department           1\n",
       "Full or Part-Time    1\n",
       "Salary or Hourly     1\n",
       "Typical Hours        1\n",
       "Annual Salary        0\n",
       "Hourly Rate          1\n",
       "Salary               0\n",
       "H_Rate               1\n",
       "dtype: int64"
      ]
     },
     "execution_count": 54,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay[pay['H_Rate'] == pay['H_Rate'].max()].count()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Who is getting max Hourly Rate?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 55,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Name</th>\n",
       "      <th>Job Titles</th>\n",
       "      <th>Department</th>\n",
       "      <th>Full or Part-Time</th>\n",
       "      <th>Salary or Hourly</th>\n",
       "      <th>Typical Hours</th>\n",
       "      <th>Annual Salary</th>\n",
       "      <th>Hourly Rate</th>\n",
       "      <th>Salary</th>\n",
       "      <th>H_Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>14317</th>\n",
       "      <td>JONES,  JOHN W</td>\n",
       "      <td>PSYCHIATRIST</td>\n",
       "      <td>HEALTH</td>\n",
       "      <td>F</td>\n",
       "      <td>Hourly</td>\n",
       "      <td>35.0</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$96.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>96.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                 Name    Job Titles Department Full or Part-Time  \\\n",
       "14317  JONES,  JOHN W  PSYCHIATRIST     HEALTH                 F   \n",
       "\n",
       "      Salary or Hourly  Typical Hours Annual Salary Hourly Rate  Salary  \\\n",
       "14317           Hourly           35.0           NaN      $96.00     NaN   \n",
       "\n",
       "       H_Rate  \n",
       "14317    96.0  "
      ]
     },
     "execution_count": 55,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay[pay['H_Rate'] == pay['H_Rate'].max()]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### How many employees are earning less than the average Hourly Rate?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 56,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "2791"
      ]
     },
     "execution_count": 56,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay[pay['H_Rate'] < pay['H_Rate'].mean()].count()['H_Rate']"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "###  The number of employees paided hourly having a full-time job?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 57,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "5906"
      ]
     },
     "execution_count": 57,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay[(pay['Hourly Rate'].notnull()) & (pay['Full or Part-Time'] =='F')].count(0)['Full or Part-Time']"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Find the full-time employees who are working at hourly rate of $10.00?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 61,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Name</th>\n",
       "      <th>Job Titles</th>\n",
       "      <th>Department</th>\n",
       "      <th>Full or Part-Time</th>\n",
       "      <th>Salary or Hourly</th>\n",
       "      <th>Typical Hours</th>\n",
       "      <th>Annual Salary</th>\n",
       "      <th>Hourly Rate</th>\n",
       "      <th>Salary</th>\n",
       "      <th>H_Rate</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>1232</th>\n",
       "      <td>AYALA JR,  JESUS</td>\n",
       "      <td>STUDENT INTERN</td>\n",
       "      <td>HUMAN RESOURCES</td>\n",
       "      <td>F</td>\n",
       "      <td>Hourly</td>\n",
       "      <td>35.0</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$10.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>10.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4522</th>\n",
       "      <td>CERVANTES,  BIANCA A</td>\n",
       "      <td>STUDENT INTERN</td>\n",
       "      <td>BUDGET &amp; MGMT</td>\n",
       "      <td>F</td>\n",
       "      <td>Hourly</td>\n",
       "      <td>35.0</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$10.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>10.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>6476</th>\n",
       "      <td>DAVILA,  ROBERTO A</td>\n",
       "      <td>ALDERMANIC AIDE</td>\n",
       "      <td>CITY COUNCIL</td>\n",
       "      <td>F</td>\n",
       "      <td>Hourly</td>\n",
       "      <td>35.0</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$10.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>10.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>16474</th>\n",
       "      <td>LEVY,  ETHAN</td>\n",
       "      <td>CLERK CITY COUNCIL</td>\n",
       "      <td>CITY COUNCIL</td>\n",
       "      <td>F</td>\n",
       "      <td>Hourly</td>\n",
       "      <td>35.0</td>\n",
       "      <td>NaN</td>\n",
       "      <td>$10.00</td>\n",
       "      <td>NaN</td>\n",
       "      <td>10.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                       Name          Job Titles       Department  \\\n",
       "1232      AYALA JR,  JESUS       STUDENT INTERN  HUMAN RESOURCES   \n",
       "4522   CERVANTES,  BIANCA A      STUDENT INTERN    BUDGET & MGMT   \n",
       "6476     DAVILA,  ROBERTO A     ALDERMANIC AIDE     CITY COUNCIL   \n",
       "16474         LEVY,  ETHAN   CLERK CITY COUNCIL     CITY COUNCIL   \n",
       "\n",
       "      Full or Part-Time Salary or Hourly  Typical Hours Annual Salary  \\\n",
       "1232                  F           Hourly           35.0           NaN   \n",
       "4522                  F           Hourly           35.0           NaN   \n",
       "6476                  F           Hourly           35.0           NaN   \n",
       "16474                 F           Hourly           35.0           NaN   \n",
       "\n",
       "      Hourly Rate  Salary  H_Rate  \n",
       "1232       $10.00     NaN    10.0  \n",
       "4522       $10.00     NaN    10.0  \n",
       "6476       $10.00     NaN    10.0  \n",
       "16474      $10.00     NaN    10.0  "
      ]
     },
     "execution_count": 61,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay[(pay['Full or Part-Time']=='F') &(pay['H_Rate']==10)]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### How many unique Job Titles are there in the data?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 63,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1095"
      ]
     },
     "execution_count": 63,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay['Job Titles'].nunique()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### What was the average Salary of the employees in each department?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 66,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Department\n",
       "ADMIN HEARNG             78912.947368\n",
       "ANIMAL CONTRL            66089.684211\n",
       "AVIATION                 76140.018777\n",
       "BOARD OF ELECTION        56051.142857\n",
       "BOARD OF ETHICS          94552.500000\n",
       "BUDGET & MGMT            93925.395349\n",
       "BUILDINGS                98864.833534\n",
       "BUSINESS AFFAIRS         80446.425000\n",
       "CITY CLERK               69762.439024\n",
       "CITY COUNCIL             63577.172069\n",
       "COMMUNITY DEVELOPMENT    88363.257143\n",
       "COPA                     98784.705882\n",
       "CULTURAL AFFAIRS         87048.909091\n",
       "DISABILITIES             82431.724138\n",
       "DoIT                     99681.029703\n",
       "FAMILY & SUPPORT         79013.588785\n",
       "FINANCE                  73276.364662\n",
       "FIRE                     97762.348662\n",
       "GENERAL SERVICES         83095.528390\n",
       "HEALTH                   85488.210938\n",
       "HUMAN RELATIONS          93778.588235\n",
       "HUMAN RESOURCES          79851.761194\n",
       "INSPECTOR GEN            84030.666667\n",
       "IPRA                     94429.285714\n",
       "LAW                      84582.814404\n",
       "LICENSE APPL COMM        80568.000000\n",
       "MAYOR'S OFFICE           96165.512308\n",
       "OEMC                     73153.778221\n",
       "POLICE                   87836.025349\n",
       "POLICE BOARD             86136.000000\n",
       "PROCUREMENT              83278.243902\n",
       "PUBLIC LIBRARY           71273.288136\n",
       "STREETS & SAN            84347.775701\n",
       "TRANSPORTN               89976.896061\n",
       "TREASURER                88062.652174\n",
       "WATER MGMNT              89894.111803\n",
       "Name: Salary, dtype: float64"
      ]
     },
     "execution_count": 66,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay.groupby('Department').mean()['Salary']"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### The job title of 'AGAR, BULENT B'? There are two spaces between AGAR, and BULENT."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 73,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "230    CHIEF ENGINEER OF SEWERS\n",
       "Name: Job Titles, dtype: object"
      ]
     },
     "execution_count": 73,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay[pay['Name'] == 'AGAR,  BULENT B']['Job Titles']"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### What are the top most common job titles?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 74,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "POLICE OFFICER                            9393\n",
       "FIREFIGHTER-EMT                           1424\n",
       "SERGEANT                                  1118\n",
       "POOL MOTOR TRUCK DRIVER                    996\n",
       "POLICE OFFICER (ASSIGNED AS DETECTIVE)     845\n",
       "Name: Job Titles, dtype: int64"
      ]
     },
     "execution_count": 74,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pay['Job Titles'].value_counts().head()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### How many people have the word 'officer' in their job title?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 75,
   "metadata": {},
   "outputs": [],
   "source": [
    "def find_string(title):\n",
    "    if 'officer' in title.lower():\n",
    "        return True\n",
    "    else:\n",
    "        return False"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 76,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "11101"
      ]
     },
     "execution_count": 76,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "sum(pay['Job Titles'].apply(lambda x: find_string(x)))"
   ]
  }
 ],
 "metadata": {
  "gist": {
   "data": {
    "description": "Pandas_project_Chicago_Payroll",
    "public": true
   },
   "id": ""
  },
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.0"
  },
  "toc": {
   "base_numbering": 1,
   "nav_menu": {},
   "number_sections": true,
   "sideBar": true,
   "skip_h1_title": false,
   "title_cell": "Table of Contents",
   "title_sidebar": "Contents",
   "toc_cell": false,
   "toc_position": {},
   "toc_section_display": true,
   "toc_window_display": false
  },
  "varInspector": {
   "cols": {
    "lenName": 16,
    "lenType": 16,
    "lenVar": 40
   },
   "kernels_config": {
    "python": {
     "delete_cmd_postfix": "",
     "delete_cmd_prefix": "del ",
     "library": "var_list.py",
     "varRefreshCmd": "print(var_dic_list())"
    },
    "r": {
     "delete_cmd_postfix": ") ",
     "delete_cmd_prefix": "rm(",
     "library": "var_list.r",
     "varRefreshCmd": "cat(var_dic_list()) "
    }
   },
   "types_to_exclude": [
    "module",
    "function",
    "builtin_function_or_method",
    "instance",
    "_Feature"
   ],
   "window_display": false
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
