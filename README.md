# 210629#!/usr/bin/env python
# coding: utf-8

# 
# 
# # Squeeze 예시

# In[1]:


import numpy as np


# In[2]:


ex=np.zeros((3,2,1,5,1))


# In[3]:


ex


# In[4]:


ex.shape #3개


# In[5]:


ex_i_data = np.squeeze(ex[2,:,:,:,:]) #2번째 값= 1 개, 지정해준 값.


# In[6]:


ex_i_data.shape #1개인 값 모두 소거


# V_md3와 동일한 값 지정

# In[7]:


adc_data_int=np.zeros((2,128,1,4,64))


# In[8]:


adc_data_int.shape


# In[9]:


i_data = np.squeeze(adc_data_int[0,:,:,:,:]) 
q_data = np.squeeze(adc_data_int[1,:,:,:,:]) 
adc_data_iq = i_data +1j*q_data


# In[10]:


adc_data_iq.shape


# In[11]:


adc_data_iq = np.transpose(adc_data_iq,(0, 2,1))
adc_data_iq.shape

