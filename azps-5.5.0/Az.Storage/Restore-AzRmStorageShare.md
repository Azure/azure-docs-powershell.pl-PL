---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188866"
---
# <span data-ttu-id="5fe9b-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5fe9b-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="5fe9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fe9b-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe9b-103">Przywraca usunięty udział plików.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="5fe9b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5fe9b-104">SYNTAX</span></span>

### <span data-ttu-id="5fe9b-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="5fe9b-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fe9b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5fe9b-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fe9b-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="5fe9b-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fe9b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5fe9b-108">DESCRIPTION</span></span>
<span data-ttu-id="5fe9b-109">Polecenie cmdlet **Restore-AzRmStorageShare** przywraca usunięty udział plików w ciągu prawidłowych dni przechowywania, jeśli opcja "miękkiego usunięcia" została włączona.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="5fe9b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5fe9b-110">EXAMPLES</span></span>

### <span data-ttu-id="5fe9b-111">Przykład 1. Usuwanie i przywracanie udziału</span><span class="sxs-lookup"><span data-stu-id="5fe9b-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="5fe9b-112">To polecenie pozwala najpierw usunąć udział plików, a następnie wyświetlić listę udziałów i wyświetlić wersję usuniętego udziału, a na koniec przywrócić go do normalnego udziału.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="5fe9b-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="5fe9b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fe9b-114">PARAMETERS</span></span>

### <span data-ttu-id="5fe9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe9b-115">-DefaultProfile</span></span>
<span data-ttu-id="5fe9b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe9b-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="5fe9b-117">-DeletedShareVersion</span></span>
<span data-ttu-id="5fe9b-118">Usunięto wersję udostępniania, z której zostanie przywrócona.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-118">Deleted Share Version, which will be restored from.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fe9b-119">-InputObject</span></span>
<span data-ttu-id="5fe9b-120">Usunięto obiekt Share</span><span class="sxs-lookup"><span data-stu-id="5fe9b-120">Deleted Share object</span></span>

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

### <span data-ttu-id="5fe9b-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5fe9b-121">-Name</span></span>
<span data-ttu-id="5fe9b-122">Usunięto nazwę udostępniania, która zostanie przywrócona.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="5fe9b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe9b-123">-ResourceGroupName</span></span>
<span data-ttu-id="5fe9b-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="5fe9b-125">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fe9b-125">-StorageAccount</span></span>
<span data-ttu-id="5fe9b-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5fe9b-126">Storage account object</span></span>

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

### <span data-ttu-id="5fe9b-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5fe9b-127">-StorageAccountName</span></span>
<span data-ttu-id="5fe9b-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="5fe9b-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5fe9b-129">-Confirm</span></span>
<span data-ttu-id="5fe9b-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fe9b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe9b-131">-WhatIf</span></span>
<span data-ttu-id="5fe9b-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe9b-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fe9b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe9b-134">CommonParameters</span></span>
<span data-ttu-id="5fe9b-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe9b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe9b-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe9b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe9b-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fe9b-137">INPUTS</span></span>

### <span data-ttu-id="5fe9b-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fe9b-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5fe9b-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="5fe9b-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="5fe9b-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fe9b-140">OUTPUTS</span></span>

### <span data-ttu-id="5fe9b-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="5fe9b-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="5fe9b-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5fe9b-142">NOTES</span></span>

## <span data-ttu-id="5fe9b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fe9b-143">RELATED LINKS</span></span>
