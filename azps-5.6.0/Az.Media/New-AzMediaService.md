---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: 9ad314046ec9a1f1769042a2e36c64ddb0af0666
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006618"
---
# <span data-ttu-id="f2f2f-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f2f2f-101">New-AzMediaService</span></span>

## <span data-ttu-id="f2f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f2f-103">Tworzy usługę multimediów, jeśli usługa multimediów już istnieje, wszystkie jej właściwości są aktualizowane przy użyciu podanych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="f2f2f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2f2f-104">SYNTAX</span></span>

### <span data-ttu-id="f2f2f-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="f2f2f-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2f2f-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="f2f2f-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2f2f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2f2f-107">DESCRIPTION</span></span>
<span data-ttu-id="f2f2f-108">Polecenie **cmdlet New-AzMediaService** tworzy usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="f2f2f-109">Jeśli usługa multimediów już istnieje, to polecenie cmdlet zaktualizuj jego właściwości.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="f2f2f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2f2f-110">EXAMPLES</span></span>

### <span data-ttu-id="f2f2f-111">Przykład1. Tworzenie usługi multimediów tylko z podstawowym kontem magazynu</span><span class="sxs-lookup"><span data-stu-id="f2f2f-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="f2f2f-112">W tym przykładzie pokazano, jak utworzyć usługę multimediów z określeniem tylko podstawowego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="f2f2f-113">W tym skrypcie jest używane kilka innych cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="f2f2f-114">Przykład 2. Tworzenie usługi multimediów z wieloma magazynami</span><span class="sxs-lookup"><span data-stu-id="f2f2f-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="f2f2f-115">W tym przykładzie pokazano, jak utworzyć usługę multimediów z wieloma kontami magazynu.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="f2f2f-116">W tym skrypcie jest używane kilka innych cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="f2f2f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2f2f-117">PARAMETERS</span></span>

### <span data-ttu-id="f2f2f-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2f2f-118">-AccountName</span></span>
<span data-ttu-id="f2f2f-119">Określa nazwę usługi multimediów, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f2f-120">-DefaultProfile</span></span>
<span data-ttu-id="f2f2f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f2f2f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2f2f-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f2f2f-122">-Location</span></span>
<span data-ttu-id="f2f2f-123">Określa region, w który to polecenie cmdlet tworzy usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-123">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f2f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2f2f-125">Określa nazwę grupy zasobów, do których jest przypisana usługa multimediów.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-126">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f2f2f-126">-StorageAccountId</span></span>
<span data-ttu-id="f2f2f-127">Określa konto magazynu skojarzone z kontem usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-128">— StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f2f2f-128">-StorageAccounts</span></span>
<span data-ttu-id="f2f2f-129">Określa tablicę kont magazynu do skojarzenia z usługą multimedialną.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="f2f2f-130">-Tag</span></span>
<span data-ttu-id="f2f2f-131">Tagi skojarzone z kontem usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-131">The tags associated with the media service account.</span></span>

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

### <span data-ttu-id="f2f2f-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2f2f-132">-Confirm</span></span>
<span data-ttu-id="f2f2f-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2f2f-134">-WhatIf</span></span>
<span data-ttu-id="f2f2f-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2f2f-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f2f-137">CommonParameters</span></span>
<span data-ttu-id="f2f2f-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f2f-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2f2f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f2f-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2f2f-140">INPUTS</span></span>

### <span data-ttu-id="f2f2f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f2f2f-141">System.String</span></span>

### <span data-ttu-id="f2f2f-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="f2f2f-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="f2f2f-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2f2f-143">OUTPUTS</span></span>

### <span data-ttu-id="f2f2f-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="f2f2f-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="f2f2f-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2f2f-145">NOTES</span></span>

## <span data-ttu-id="f2f2f-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2f2f-146">RELATED LINKS</span></span>

[<span data-ttu-id="f2f2f-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f2f2f-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="f2f2f-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f2f2f-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="f2f2f-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f2f2f-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


