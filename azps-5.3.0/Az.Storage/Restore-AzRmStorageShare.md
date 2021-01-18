---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502699"
---
# <span data-ttu-id="f7ba1-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f7ba1-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="f7ba1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ba1-103">Przywraca usunięty udział pliku.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="f7ba1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7ba1-104">SYNTAX</span></span>

### <span data-ttu-id="f7ba1-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f7ba1-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7ba1-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="f7ba1-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7ba1-107">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="f7ba1-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7ba1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f7ba1-108">DESCRIPTION</span></span>
<span data-ttu-id="f7ba1-109">Polecenie cmdlet **Restore-AzRmStorageShare** przywraca usunięty udział pliku w prawidłowych dniach przechowywania, jeśli jest włączone usuwanie nietrwałe.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="f7ba1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7ba1-110">EXAMPLES</span></span>

### <span data-ttu-id="f7ba1-111">Przykład 1: usuwanie i przywracanie udziału</span><span class="sxs-lookup"><span data-stu-id="f7ba1-111">Example 1: Remove and restore a share</span></span>
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

<span data-ttu-id="f7ba1-112">To polecenie najpierw usuwa udział plików, a następnie wyświetla listę udziałów i wyświetla wersję usuniętego udziału, a następnie przywraca jej normalny udział.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="f7ba1-113">Przed usunięciem udziału należy włączyć funkcję udostępniania trwałego Usuń, aktualizując-AzStorageFileServiceProperty.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="f7ba1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7ba1-114">PARAMETERS</span></span>

### <span data-ttu-id="f7ba1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ba1-115">-DefaultProfile</span></span>
<span data-ttu-id="f7ba1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7ba1-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="f7ba1-117">-DeletedShareVersion</span></span>
<span data-ttu-id="f7ba1-118">Usunięta wersja udziału, do której zostanie przywrócony.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="f7ba1-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f7ba1-119">-InputObject</span></span>
<span data-ttu-id="f7ba1-120">Usunięto obiekt Share</span><span class="sxs-lookup"><span data-stu-id="f7ba1-120">Deleted Share object</span></span>

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

### <span data-ttu-id="f7ba1-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7ba1-121">-Name</span></span>
<span data-ttu-id="f7ba1-122">Nazwa usuniętego udziału, która zostanie przywrócona.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="f7ba1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ba1-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7ba1-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7ba1-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7ba1-125">-StorageAccount</span></span>
<span data-ttu-id="f7ba1-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f7ba1-126">Storage account object</span></span>

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

### <span data-ttu-id="f7ba1-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f7ba1-127">-StorageAccountName</span></span>
<span data-ttu-id="f7ba1-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="f7ba1-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7ba1-129">-Confirm</span></span>
<span data-ttu-id="f7ba1-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7ba1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7ba1-131">-WhatIf</span></span>
<span data-ttu-id="f7ba1-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7ba1-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7ba1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ba1-134">CommonParameters</span></span>
<span data-ttu-id="f7ba1-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ba1-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ba1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ba1-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7ba1-137">INPUTS</span></span>

### <span data-ttu-id="f7ba1-138">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7ba1-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f7ba1-139">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="f7ba1-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f7ba1-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7ba1-140">OUTPUTS</span></span>

### <span data-ttu-id="f7ba1-141">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="f7ba1-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f7ba1-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7ba1-142">NOTES</span></span>

## <span data-ttu-id="f7ba1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7ba1-143">RELATED LINKS</span></span>
