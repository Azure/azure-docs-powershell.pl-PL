---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 01871c63d9a734cba88da30032f8b1da21198160
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888009"
---
# <span data-ttu-id="e4aa5-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e4aa5-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="e4aa5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="e4aa5-103">Umożliwia utworzenie udziału plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="e4aa5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4aa5-104">SYNTAX</span></span>

### <span data-ttu-id="e4aa5-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e4aa5-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4aa5-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="e4aa5-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4aa5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e4aa5-107">DESCRIPTION</span></span>
<span data-ttu-id="e4aa5-108">Polecenie cmdlet **New-AzRmStorageShare** umożliwia utworzenie udziału plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="e4aa5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4aa5-109">EXAMPLES</span></span>

### <span data-ttu-id="e4aa5-110">Przykład 1. Utwórz udział plików magazynu z nazwą konta magazynu i nazwą udziału, a następnie Udostępnij przydział jako 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   
```

<span data-ttu-id="e4aa5-111">To polecenie tworzy udział plików magazynu z metadanymi i udostępnia przydział jako 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="e4aa5-112">Przykład 2: Tworzenie udziału plików magazynu za pomocą obiektu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e4aa5-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | New-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   
```

<span data-ttu-id="e4aa5-113">To polecenie tworzy udział plików magazynu z obiektem konta magazynu i nazwą udziału.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="e4aa5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4aa5-114">PARAMETERS</span></span>

### <span data-ttu-id="e4aa5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4aa5-115">-DefaultProfile</span></span>
<span data-ttu-id="e4aa5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4aa5-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e4aa5-117">-Metadata</span></span>
<span data-ttu-id="e4aa5-118">Udostępnianie metadanych</span><span class="sxs-lookup"><span data-stu-id="e4aa5-118">Share Metadata</span></span>

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

### <span data-ttu-id="e4aa5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4aa5-119">-Name</span></span>
<span data-ttu-id="e4aa5-120">Nazwa udziału plików Azure</span><span class="sxs-lookup"><span data-stu-id="e4aa5-120">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4aa5-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="e4aa5-121">-QuotaGiB</span></span>
<span data-ttu-id="e4aa5-122">Przydziel zasoby w Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-122">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4aa5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4aa5-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4aa5-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4aa5-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4aa5-125">-StorageAccount</span></span>
<span data-ttu-id="e4aa5-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e4aa5-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4aa5-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e4aa5-127">-StorageAccountName</span></span>
<span data-ttu-id="e4aa5-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4aa5-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4aa5-129">-Confirm</span></span>
<span data-ttu-id="e4aa5-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4aa5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4aa5-131">-WhatIf</span></span>
<span data-ttu-id="e4aa5-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4aa5-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4aa5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4aa5-134">CommonParameters</span></span>
<span data-ttu-id="e4aa5-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4aa5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4aa5-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4aa5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4aa5-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4aa5-137">INPUTS</span></span>

### <span data-ttu-id="e4aa5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e4aa5-138">System.String</span></span>

### <span data-ttu-id="e4aa5-139">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4aa5-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e4aa5-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4aa5-140">OUTPUTS</span></span>

### <span data-ttu-id="e4aa5-141">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="e4aa5-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="e4aa5-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4aa5-142">NOTES</span></span>

## <span data-ttu-id="e4aa5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4aa5-143">RELATED LINKS</span></span>
