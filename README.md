if(idpResp!=null && idpResp.data !=null && idpResp.data.groups !=null){
    
    
    
    console.log("idpResp::",idpResp.data.groups);
    
    
    if (idpResp.data.groups.length >= 1) {
        // console.log("IDPResponse length >1", idpResp.data)
        let groups = idpResp.data.groups[0]
        
        let groupName = '';
        if(groups.group_name!=null){
            groupName = String(groups.group_name).toLowerCase()
        }
       
        return groupName
       
    }
    else {
        // console.log("IDPResponse empty", idpResp.data)
      return ''
    }
    
    }
