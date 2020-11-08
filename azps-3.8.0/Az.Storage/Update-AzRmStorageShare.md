---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 6e3c71900e5fe4a4ac8e4f092691dcde3e759c2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050458"
---
# <span data-ttu-id="70c19-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="70c19-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="70c19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70c19-102">SYNOPSIS</span></span>
<span data-ttu-id="70c19-103">Modyfikuje udział plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="70c19-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="70c19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70c19-104">SYNTAX</span></span>

### <span data-ttu-id="70c19-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="70c19-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70c19-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="70c19-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c19-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="70c19-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c19-108">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="70c19-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70c19-109">Opis</span><span class="sxs-lookup"><span data-stu-id="70c19-109">DESCRIPTION</span></span>
<span data-ttu-id="70c19-110">Polecenie cmdlet **New-AzRmStorageShare** modyfikuje udział plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="70c19-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="70c19-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70c19-111">EXAMPLES</span></span>

### <span data-ttu-id="70c19-112">Przykład 1: modyfikuje metadane udziału plików magazynu i udostępnia przydział z nazwą konta magazynu i nazwą udziału</span><span class="sxs-lookup"><span data-stu-id="70c19-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup                       200     

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="70c19-113">To polecenie modyfikuje metadane udziału plików magazynu i udostępnia przydział z nazwą konta magazynu i nazwą udziału, a następnie Pokaż wynik modyfikacji z zwróconym obiektem udział pliku.</span><span class="sxs-lookup"><span data-stu-id="70c19-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="70c19-114">Przykład 2: modyfikuje metadane w udziale plików magazynu za pomocą obiektu konta magazynu i nazwy udziału</span><span class="sxs-lookup"><span data-stu-id="70c19-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="70c19-115">To polecenie modyfikuje metadane w udziale plików magazynu za pomocą obiektu konta magazynu i nazwy udziału.</span><span class="sxs-lookup"><span data-stu-id="70c19-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="70c19-116">Przykład 3: modyfikuje przydział udostępniania dla wszystkich udziałów plików magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="70c19-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Update-AzRmStorageShare -QuotaGiB 5000

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup                       5000
share2   myStorageAccount   myResourceGroup                       5000
```

<span data-ttu-id="70c19-117">To polecenie modyfikuje przydział udostępniania jako 5000 GiB dla wszystkich udziałów plików magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="70c19-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="70c19-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70c19-118">PARAMETERS</span></span>

### <span data-ttu-id="70c19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c19-119">-DefaultProfile</span></span>
<span data-ttu-id="70c19-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70c19-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="70c19-121">-InputObject</span></span>
<span data-ttu-id="70c19-122">Obiekt udostępniania magazynu</span><span class="sxs-lookup"><span data-stu-id="70c19-122">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="70c19-123">-Metadata</span></span>
<span data-ttu-id="70c19-124">Udostępnianie metadanych</span><span class="sxs-lookup"><span data-stu-id="70c19-124">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70c19-125">-Name</span></span>
<span data-ttu-id="70c19-126">Nazwa udziału</span><span class="sxs-lookup"><span data-stu-id="70c19-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="70c19-127">-QuotaGiB</span></span>
<span data-ttu-id="70c19-128">Przydziel zasoby w Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="70c19-128">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c19-129">-ResourceGroupName</span></span>
<span data-ttu-id="70c19-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70c19-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70c19-131">-ResourceId</span></span>
<span data-ttu-id="70c19-132">Wprowadź identyfikator zasobu udziału pliku.</span><span class="sxs-lookup"><span data-stu-id="70c19-132">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="70c19-133">-StorageAccount</span></span>
<span data-ttu-id="70c19-134">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="70c19-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="70c19-135">-StorageAccountName</span></span>
<span data-ttu-id="70c19-136">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="70c19-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70c19-137">-Confirm</span></span>
<span data-ttu-id="70c19-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c19-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c19-139">-WhatIf</span></span>
<span data-ttu-id="70c19-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c19-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c19-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70c19-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c19-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c19-142">CommonParameters</span></span>
<span data-ttu-id="70c19-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70c19-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c19-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c19-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c19-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70c19-145">INPUTS</span></span>

### <span data-ttu-id="70c19-146">System. String</span><span class="sxs-lookup"><span data-stu-id="70c19-146">System.String</span></span>

### <span data-ttu-id="70c19-147">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70c19-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="70c19-148">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="70c19-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="70c19-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70c19-149">OUTPUTS</span></span>

### <span data-ttu-id="70c19-150">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="70c19-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="70c19-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70c19-151">NOTES</span></span>

## <span data-ttu-id="70c19-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70c19-152">RELATED LINKS</span></span>
