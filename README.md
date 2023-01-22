# binary

class Solution {
public:
    int search(vector<int>& nums, int target) {
        int strt=0;
        int end=nums.size()-1;

        if(nums.size()==0){
            return -1;
        }
       
         while(strt<=end){
             int mid= strt+(end-strt)/2;
            if(nums[mid]==target){
                return mid;
            }   
            else if(target<nums[mid])
            {
               end=mid-1;
            }
            else{
                strt=mid+1;
            }

        }
        return -1;
        
    }
};
