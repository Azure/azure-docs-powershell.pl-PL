---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 72e42153e46c02a3e721400c83b4cba886485db4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717509"
---
# <span data-ttu-id="e3897-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="e3897-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="e3897-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3897-102">SYNOPSIS</span></span>
<span data-ttu-id="e3897-103">Tworzy usługę multimediów, jeśli usługa multimedialna już istnieje, wszystkie jej właściwości są aktualizowane przy użyciu dostarczonych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e3897-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3897-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3897-104">SYNTAX</span></span>

### <span data-ttu-id="e3897-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="e3897-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3897-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="e3897-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3897-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e3897-107">DESCRIPTION</span></span>
<span data-ttu-id="e3897-108">Polecenie cmdlet **New-AzureRmMediaService** tworzy usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="e3897-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="e3897-109">Jeśli usługa multimedialna już istnieje, to polecenie cmdlet umożliwia zaktualizowanie jego właściwości.</span><span class="sxs-lookup"><span data-stu-id="e3897-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="e3897-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3897-110">EXAMPLES</span></span>

### <span data-ttu-id="e3897-111">Example1: Tworzenie usługi multimedialnej tylko przy użyciu podstawowego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e3897-111">Example1: Create a media service with the primary storage account only</span></span>
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
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="e3897-112">W tym przykładzie pokazano, jak utworzyć usługę multimedialną tylko z określeniem podstawowego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3897-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="e3897-113">Ten skrypt używa kilku innych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3897-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="e3897-114">Przykład 2: Tworzenie usługi multimedialnej z wieloma miejscami do magazynowania</span><span class="sxs-lookup"><span data-stu-id="e3897-114">Example 2: Create a media service with multiple storage</span></span>
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
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="e3897-115">W tym przykładzie pokazano, jak utworzyć usługę multimedialną z wieloma kontami magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3897-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="e3897-116">Ten skrypt używa kilku innych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3897-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="e3897-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3897-117">PARAMETERS</span></span>

### <span data-ttu-id="e3897-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e3897-118">-AccountName</span></span>
<span data-ttu-id="e3897-119">Określa nazwę usługi multimedialnej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3897-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3897-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3897-120">-DefaultProfile</span></span>
<span data-ttu-id="e3897-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e3897-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3897-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e3897-122">-Location</span></span>
<span data-ttu-id="e3897-123">Określa region, w którym to polecenie cmdlet tworzy usługę Media.</span><span class="sxs-lookup"><span data-stu-id="e3897-123">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3897-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3897-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3897-125">Określa nazwę grupy zasobów, do której przypisano usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="e3897-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3897-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e3897-126">-StorageAccountId</span></span>
<span data-ttu-id="e3897-127">Określa konto magazynu skojarzone z kontem usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="e3897-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3897-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e3897-128">-StorageAccounts</span></span>
<span data-ttu-id="e3897-129">Określa tablicę kont magazynu, które mają zostać skojarzone z usługą Media.</span><span class="sxs-lookup"><span data-stu-id="e3897-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3897-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3897-130">-Tag</span></span>
<span data-ttu-id="e3897-131">Tagi skojarzone z kontem usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="e3897-131">The tags associated with the media service account.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3897-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3897-132">-Confirm</span></span>
<span data-ttu-id="e3897-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3897-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3897-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3897-134">-WhatIf</span></span>
<span data-ttu-id="e3897-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3897-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3897-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3897-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3897-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3897-137">CommonParameters</span></span>
<span data-ttu-id="e3897-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3897-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3897-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3897-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3897-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3897-140">INPUTS</span></span>

### <span data-ttu-id="e3897-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e3897-141">None</span></span>
<span data-ttu-id="e3897-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e3897-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3897-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3897-143">OUTPUTS</span></span>

### <span data-ttu-id="e3897-144">Microsoft. Azure. Commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="e3897-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="e3897-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3897-145">NOTES</span></span>

## <span data-ttu-id="e3897-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3897-146">RELATED LINKS</span></span>

[<span data-ttu-id="e3897-147">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="e3897-147">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="e3897-148">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="e3897-148">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="e3897-149">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="e3897-149">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


