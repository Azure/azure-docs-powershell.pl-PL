---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 3cf556bce81a2e77250e597b428aa23c6eabe496
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050802"
---
# <span data-ttu-id="ea346-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="ea346-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="ea346-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea346-102">SYNOPSIS</span></span>
<span data-ttu-id="ea346-103">Tworzenie mapowania zestawu danych dla subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="ea346-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="ea346-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea346-104">SYNTAX</span></span>

### <span data-ttu-id="ea346-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea346-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea346-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="ea346-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea346-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea346-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea346-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea346-108">DESCRIPTION</span></span>
<span data-ttu-id="ea346-109">Polecenie cmdlet **New-AzDataShareDataSetMapping** umożliwia utworzenie mapowania zestawu danych między zestawami danych źródłowych a kontem magazynu obiektów sink w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="ea346-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="ea346-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea346-110">EXAMPLES</span></span>

### <span data-ttu-id="ea346-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ea346-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="ea346-112">To polecenie tworzy mapowanie zestawu danych AdsDataSetMapping do konta magazynu AdsStorage na potrzeby udostępniania subskrypcji AdsShareSubscription w koncie udziału danych WikiAdsAccount.</span><span class="sxs-lookup"><span data-stu-id="ea346-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="ea346-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea346-113">PARAMETERS</span></span>

### <span data-ttu-id="ea346-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea346-114">-AccountName</span></span>
<span data-ttu-id="ea346-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="ea346-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-116">-Kontener</span><span class="sxs-lookup"><span data-stu-id="ea346-116">-Container</span></span>
<span data-ttu-id="ea346-117">Nazwa kontenera konta magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ea346-117">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="ea346-118">-DataSetId</span></span>
<span data-ttu-id="ea346-119">Identyfikator zestawu danych odbiorcy</span><span class="sxs-lookup"><span data-stu-id="ea346-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea346-120">-DefaultProfile</span></span>
<span data-ttu-id="ea346-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea346-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea346-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="ea346-122">-FilePath</span></span>
<span data-ttu-id="ea346-123">Ścieżka do pliku magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ea346-123">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-124">— System plików</span><span class="sxs-lookup"><span data-stu-id="ea346-124">-FileSystem</span></span>
<span data-ttu-id="ea346-125">Nazwa systemu plików usługi Azure ADLS Gen2</span><span class="sxs-lookup"><span data-stu-id="ea346-125">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="ea346-126">-FolderPath</span></span>
<span data-ttu-id="ea346-127">Ścieżka folderu magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ea346-127">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea346-128">-Name</span></span>
<span data-ttu-id="ea346-129">Nazwa mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ea346-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea346-130">-ResourceGroupName</span></span>
<span data-ttu-id="ea346-131">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="ea346-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ea346-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="ea346-133">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="ea346-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ea346-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="ea346-135">Identyfikator zasobu konta usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="ea346-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea346-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea346-136">-Confirm</span></span>
<span data-ttu-id="ea346-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea346-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea346-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea346-138">-WhatIf</span></span>
<span data-ttu-id="ea346-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea346-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea346-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea346-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea346-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea346-141">CommonParameters</span></span>
<span data-ttu-id="ea346-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea346-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea346-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea346-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea346-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea346-144">INPUTS</span></span>

### <span data-ttu-id="ea346-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ea346-145">System.String</span></span>

## <span data-ttu-id="ea346-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea346-146">OUTPUTS</span></span>

### <span data-ttu-id="ea346-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="ea346-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="ea346-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea346-148">NOTES</span></span>

## <span data-ttu-id="ea346-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea346-149">RELATED LINKS</span></span>
