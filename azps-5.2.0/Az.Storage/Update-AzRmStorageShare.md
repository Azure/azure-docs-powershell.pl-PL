---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335149"
---
# <span data-ttu-id="7ee18-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ee18-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="7ee18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ee18-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee18-103">Modyfikuje udział plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="7ee18-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="7ee18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ee18-104">SYNTAX</span></span>

### <span data-ttu-id="7ee18-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7ee18-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee18-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="7ee18-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ee18-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="7ee18-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee18-108">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="7ee18-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ee18-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7ee18-109">DESCRIPTION</span></span>
<span data-ttu-id="7ee18-110">Polecenie cmdlet **New-AzRmStorageShare** modyfikuje udział plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="7ee18-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="7ee18-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ee18-111">EXAMPLES</span></span>

### <span data-ttu-id="7ee18-112">Przykład 1: modyfikuje metadane udziału plików magazynu i udostępnia przydział z nazwą konta magazynu i nazwą udziału</span><span class="sxs-lookup"><span data-stu-id="7ee18-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="7ee18-113">To polecenie modyfikuje metadane udziału plików magazynu i udostępnia przydział z nazwą konta magazynu i nazwą udziału, a następnie Pokaż wynik modyfikacji z zwróconym obiektem udział pliku.</span><span class="sxs-lookup"><span data-stu-id="7ee18-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="7ee18-114">Przykład 2: modyfikuje metadane w udziale plików magazynu za pomocą obiektu konta magazynu i nazwy udziału</span><span class="sxs-lookup"><span data-stu-id="7ee18-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="7ee18-115">To polecenie modyfikuje metadane w udziale plików magazynu za pomocą obiektu konta magazynu i nazwy udziału.</span><span class="sxs-lookup"><span data-stu-id="7ee18-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="7ee18-116">Przykład 3: modyfikuje przydział udostępniania dla wszystkich udziałów plików magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="7ee18-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="7ee18-117">To polecenie modyfikuje przydział udostępniania jako 5000 GiB dla wszystkich udziałów plików magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="7ee18-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="7ee18-118">Przykład 4: modyfikowanie udziału plików magazynu przy użyciu accesstier jako schłodzenia</span><span class="sxs-lookup"><span data-stu-id="7ee18-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="7ee18-119">To polecenie modyfikuje udział plików magazynu przy użyciu accesstier jako schłodzenia.</span><span class="sxs-lookup"><span data-stu-id="7ee18-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="7ee18-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ee18-120">PARAMETERS</span></span>

### <span data-ttu-id="7ee18-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="7ee18-121">-AccessTier</span></span>
<span data-ttu-id="7ee18-122">Warstwa dostępu do określonego udziału.</span><span class="sxs-lookup"><span data-stu-id="7ee18-122">Access tier for specific share.</span></span> <span data-ttu-id="7ee18-123">StorageV2 konto może wybierać między TransactionOptimized (ustawienie domyślne), gorące i schłodzone.</span><span class="sxs-lookup"><span data-stu-id="7ee18-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="7ee18-124">FileStorage konto może wybrać opcję Premium.</span><span class="sxs-lookup"><span data-stu-id="7ee18-124">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee18-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee18-125">-DefaultProfile</span></span>
<span data-ttu-id="7ee18-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ee18-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ee18-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ee18-127">-InputObject</span></span>
<span data-ttu-id="7ee18-128">Obiekt udostępniania magazynu</span><span class="sxs-lookup"><span data-stu-id="7ee18-128">Storage Share object</span></span>

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

### <span data-ttu-id="7ee18-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7ee18-129">-Metadata</span></span>
<span data-ttu-id="7ee18-130">Udostępnianie metadanych</span><span class="sxs-lookup"><span data-stu-id="7ee18-130">Share Metadata</span></span>

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

### <span data-ttu-id="7ee18-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ee18-131">-Name</span></span>
<span data-ttu-id="7ee18-132">Nazwa udziału</span><span class="sxs-lookup"><span data-stu-id="7ee18-132">Share Name</span></span>

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

### <span data-ttu-id="7ee18-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="7ee18-133">-QuotaGiB</span></span>
<span data-ttu-id="7ee18-134">Przydziel zasoby w Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="7ee18-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="7ee18-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee18-135">-ResourceGroupName</span></span>
<span data-ttu-id="7ee18-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ee18-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="7ee18-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ee18-137">-ResourceId</span></span>
<span data-ttu-id="7ee18-138">Wprowadź identyfikator zasobu udziału pliku.</span><span class="sxs-lookup"><span data-stu-id="7ee18-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="7ee18-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ee18-139">-StorageAccount</span></span>
<span data-ttu-id="7ee18-140">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="7ee18-140">Storage account object</span></span>

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

### <span data-ttu-id="7ee18-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7ee18-141">-StorageAccountName</span></span>
<span data-ttu-id="7ee18-142">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7ee18-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="7ee18-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ee18-143">-Confirm</span></span>
<span data-ttu-id="7ee18-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ee18-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee18-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ee18-145">-WhatIf</span></span>
<span data-ttu-id="7ee18-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ee18-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ee18-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ee18-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee18-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee18-148">CommonParameters</span></span>
<span data-ttu-id="7ee18-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee18-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee18-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee18-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee18-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ee18-151">INPUTS</span></span>

### <span data-ttu-id="7ee18-152">System. String</span><span class="sxs-lookup"><span data-stu-id="7ee18-152">System.String</span></span>

### <span data-ttu-id="7ee18-153">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ee18-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7ee18-154">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="7ee18-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="7ee18-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ee18-155">OUTPUTS</span></span>

### <span data-ttu-id="7ee18-156">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="7ee18-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="7ee18-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ee18-157">NOTES</span></span>

## <span data-ttu-id="7ee18-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ee18-158">RELATED LINKS</span></span>
