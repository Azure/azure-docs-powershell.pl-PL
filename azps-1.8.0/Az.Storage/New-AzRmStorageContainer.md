---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: efbdcc79bed4b7dd3dcca40f87db7fcef668405a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707599"
---
# <span data-ttu-id="612d6-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="612d6-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="612d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="612d6-102">SYNOPSIS</span></span>
<span data-ttu-id="612d6-103">Tworzy kontener obiektu blob magazynu</span><span class="sxs-lookup"><span data-stu-id="612d6-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="612d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="612d6-104">SYNTAX</span></span>

### <span data-ttu-id="612d6-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="612d6-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="612d6-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="612d6-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="612d6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="612d6-107">DESCRIPTION</span></span>
<span data-ttu-id="612d6-108">Polecenie cmdlet **New-AzRmStorageContainer** tworzy kontener obiektu BLOB magazynowania</span><span class="sxs-lookup"><span data-stu-id="612d6-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="612d6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="612d6-109">EXAMPLES</span></span>

### <span data-ttu-id="612d6-110">Przykład 1: Tworzenie kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera z metadanymi</span><span class="sxs-lookup"><span data-stu-id="612d6-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="612d6-111">To polecenie tworzy kontener obiektu BLOB przechowywania z nazwą konta magazynu i nazwą kontenera z metadanymi.</span><span class="sxs-lookup"><span data-stu-id="612d6-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="612d6-112">Przykład 2: Tworzenie kontenera obiektów BLOB magazynowania z obiektem konta magazynu i nazwą kontenera z dostępem publicznym jako obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="612d6-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="612d6-113">To polecenie tworzy kontener obiektu BLOB magazynowania z obiektem konta magazynu i nazwą kontenera z dostępem publicznym jako obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="612d6-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="612d6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="612d6-114">PARAMETERS</span></span>

### <span data-ttu-id="612d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="612d6-115">-DefaultProfile</span></span>
<span data-ttu-id="612d6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="612d6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="612d6-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="612d6-117">-Metadata</span></span>
<span data-ttu-id="612d6-118">Metadane kontenera</span><span class="sxs-lookup"><span data-stu-id="612d6-118">Container Metadata</span></span>

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

### <span data-ttu-id="612d6-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="612d6-119">-Name</span></span>
<span data-ttu-id="612d6-120">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="612d6-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="612d6-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="612d6-121">-PublicAccess</span></span>
<span data-ttu-id="612d6-122">Kontener PublicAccess</span><span class="sxs-lookup"><span data-stu-id="612d6-122">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="612d6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="612d6-123">-ResourceGroupName</span></span>
<span data-ttu-id="612d6-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="612d6-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="612d6-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="612d6-125">-StorageAccount</span></span>
<span data-ttu-id="612d6-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="612d6-126">Storage account object</span></span>

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

### <span data-ttu-id="612d6-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="612d6-127">-StorageAccountName</span></span>
<span data-ttu-id="612d6-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="612d6-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="612d6-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="612d6-129">-Confirm</span></span>
<span data-ttu-id="612d6-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="612d6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="612d6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="612d6-131">-WhatIf</span></span>
<span data-ttu-id="612d6-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="612d6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="612d6-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="612d6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="612d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612d6-134">CommonParameters</span></span>
<span data-ttu-id="612d6-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="612d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612d6-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="612d6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612d6-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="612d6-137">INPUTS</span></span>

### <span data-ttu-id="612d6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="612d6-138">System.String</span></span>

### <span data-ttu-id="612d6-139">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="612d6-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="612d6-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="612d6-140">OUTPUTS</span></span>

### <span data-ttu-id="612d6-141">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="612d6-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="612d6-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="612d6-142">NOTES</span></span>

## <span data-ttu-id="612d6-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="612d6-143">RELATED LINKS</span></span>