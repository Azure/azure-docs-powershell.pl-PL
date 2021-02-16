---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197547"
---
# <span data-ttu-id="fcf47-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fcf47-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="fcf47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcf47-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf47-103">Tworzy udział plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="fcf47-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="fcf47-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fcf47-104">SYNTAX</span></span>

### <span data-ttu-id="fcf47-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="fcf47-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf47-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fcf47-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcf47-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fcf47-107">DESCRIPTION</span></span>
<span data-ttu-id="fcf47-108">Polecenie **cmdlet New-AzRmStorageShare** tworzy udział plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="fcf47-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="fcf47-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fcf47-109">EXAMPLES</span></span>

### <span data-ttu-id="fcf47-110">Przykład 1. Tworzenie udziału plików magazynu z nazwą konta magazynu i nazwą udostępniania z metadanymi i przydziałem udostępniania w rozmiarze 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="fcf47-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="fcf47-111">To polecenie tworzy udział plików magazynu z metadanymi i przydział udostępniania jako 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="fcf47-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="fcf47-112">Przykład 2. Tworzenie udziału plików magazynu przy użyciu obiektu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="fcf47-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="fcf47-113">To polecenie tworzy udział plików magazynu z obiektem konta magazynu i nazwą udostępniania.</span><span class="sxs-lookup"><span data-stu-id="fcf47-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="fcf47-114">Przykład 3. Tworzenie udziału plików magazynu jako hot</span><span class="sxs-lookup"><span data-stu-id="fcf47-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="fcf47-115">To polecenie powoduje utworzenie udziału plików magazynu z dostępną usługą Accesstier jako Hot.</span><span class="sxs-lookup"><span data-stu-id="fcf47-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="fcf47-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcf47-116">PARAMETERS</span></span>

### <span data-ttu-id="fcf47-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="fcf47-117">-AccessTier</span></span>
<span data-ttu-id="fcf47-118">Warstwa dostępu dla określonego udziału.</span><span class="sxs-lookup"><span data-stu-id="fcf47-118">Access tier for specific share.</span></span> <span data-ttu-id="fcf47-119">Konto StorageV2 może wybierać między opcjami TransactionOptimized (domyślne), Hot (Hot) i Cool (Cool).</span><span class="sxs-lookup"><span data-stu-id="fcf47-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="fcf47-120">Konto FileStorage może wybrać pozycję Premium.</span><span class="sxs-lookup"><span data-stu-id="fcf47-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="fcf47-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf47-121">-DefaultProfile</span></span>
<span data-ttu-id="fcf47-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf47-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcf47-123">— Metadane</span><span class="sxs-lookup"><span data-stu-id="fcf47-123">-Metadata</span></span>
<span data-ttu-id="fcf47-124">Udostępnianie metadanych</span><span class="sxs-lookup"><span data-stu-id="fcf47-124">Share Metadata</span></span>

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

### <span data-ttu-id="fcf47-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fcf47-125">-Name</span></span>
<span data-ttu-id="fcf47-126">Nazwa udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fcf47-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf47-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="fcf47-127">-QuotaGiB</span></span>
<span data-ttu-id="fcf47-128">Udostępnianie przydziału w gibibajcie.</span><span class="sxs-lookup"><span data-stu-id="fcf47-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="fcf47-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf47-129">-ResourceGroupName</span></span>
<span data-ttu-id="fcf47-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fcf47-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcf47-131">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcf47-131">-StorageAccount</span></span>
<span data-ttu-id="fcf47-132">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="fcf47-132">Storage account object</span></span>

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

### <span data-ttu-id="fcf47-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fcf47-133">-StorageAccountName</span></span>
<span data-ttu-id="fcf47-134">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fcf47-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="fcf47-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fcf47-135">-Confirm</span></span>
<span data-ttu-id="fcf47-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fcf47-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf47-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf47-137">-WhatIf</span></span>
<span data-ttu-id="fcf47-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf47-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcf47-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fcf47-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf47-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf47-140">CommonParameters</span></span>
<span data-ttu-id="fcf47-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf47-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf47-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf47-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf47-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcf47-143">INPUTS</span></span>

### <span data-ttu-id="fcf47-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fcf47-144">System.String</span></span>

### <span data-ttu-id="fcf47-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcf47-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fcf47-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fcf47-146">OUTPUTS</span></span>

### <span data-ttu-id="fcf47-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="fcf47-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="fcf47-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fcf47-148">NOTES</span></span>

## <span data-ttu-id="fcf47-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcf47-149">RELATED LINKS</span></span>
