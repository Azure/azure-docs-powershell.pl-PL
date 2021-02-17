---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188571"
---
# <span data-ttu-id="cd97d-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="cd97d-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="cd97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd97d-102">SYNOPSIS</span></span>
<span data-ttu-id="cd97d-103">Tworzy mapowanie zestawu danych dla subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="cd97d-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="cd97d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd97d-104">SYNTAX</span></span>

### <span data-ttu-id="cd97d-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="cd97d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd97d-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="cd97d-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd97d-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd97d-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd97d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd97d-108">DESCRIPTION</span></span>
<span data-ttu-id="cd97d-109">Polecenie **cmdlet New-AzDataShareDataSetMapping** tworzy mapowanie zestawu danych między źródłowymi zestawami danych a kontem magazynu w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="cd97d-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="cd97d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd97d-110">EXAMPLES</span></span>

### <span data-ttu-id="cd97d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd97d-111">Example 1</span></span>
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

<span data-ttu-id="cd97d-112">To polecenie tworzy mapowanie zestawu danych AdsDataSetMapping na konto magazynu AdsStorage dla subskrypcji udostępniania AdsShareSubscription w koncie udostępniania danych WikiAdsAccount.</span><span class="sxs-lookup"><span data-stu-id="cd97d-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="cd97d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd97d-113">PARAMETERS</span></span>

### <span data-ttu-id="cd97d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cd97d-114">-AccountName</span></span>
<span data-ttu-id="cd97d-115">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd97d-115">Azure data share account name</span></span>

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

### <span data-ttu-id="cd97d-116">— Kontener</span><span class="sxs-lookup"><span data-stu-id="cd97d-116">-Container</span></span>
<span data-ttu-id="cd97d-117">Nazwa kontenera konta magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd97d-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="cd97d-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="cd97d-118">-DataSetId</span></span>
<span data-ttu-id="cd97d-119">Identyfikator zestawu danych konsumentów</span><span class="sxs-lookup"><span data-stu-id="cd97d-119">Consumer data set id</span></span>

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

### <span data-ttu-id="cd97d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd97d-120">-DefaultProfile</span></span>
<span data-ttu-id="cd97d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd97d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd97d-122">- FilePath</span><span class="sxs-lookup"><span data-stu-id="cd97d-122">-FilePath</span></span>
<span data-ttu-id="cd97d-123">Ścieżka pliku magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd97d-123">Azure storage file path</span></span>

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

### <span data-ttu-id="cd97d-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="cd97d-124">-FileSystem</span></span>
<span data-ttu-id="cd97d-125">Nazwa systemu plików w usłudze Azure ADLS (gen2)</span><span class="sxs-lookup"><span data-stu-id="cd97d-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="cd97d-126">- FolderPath</span><span class="sxs-lookup"><span data-stu-id="cd97d-126">-FolderPath</span></span>
<span data-ttu-id="cd97d-127">Ścieżka folderu magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd97d-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="cd97d-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cd97d-128">-Name</span></span>
<span data-ttu-id="cd97d-129">Nazwa mapowania zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd97d-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="cd97d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd97d-130">-ResourceGroupName</span></span>
<span data-ttu-id="cd97d-131">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="cd97d-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="cd97d-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cd97d-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="cd97d-133">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd97d-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="cd97d-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cd97d-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="cd97d-135">Azure Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd97d-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="cd97d-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd97d-136">-Confirm</span></span>
<span data-ttu-id="cd97d-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd97d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd97d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd97d-138">-WhatIf</span></span>
<span data-ttu-id="cd97d-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd97d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd97d-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd97d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd97d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd97d-141">CommonParameters</span></span>
<span data-ttu-id="cd97d-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd97d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd97d-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd97d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd97d-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd97d-144">INPUTS</span></span>

### <span data-ttu-id="cd97d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="cd97d-145">System.String</span></span>

## <span data-ttu-id="cd97d-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd97d-146">OUTPUTS</span></span>

### <span data-ttu-id="cd97d-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="cd97d-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="cd97d-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd97d-148">NOTES</span></span>

## <span data-ttu-id="cd97d-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd97d-149">RELATED LINKS</span></span>
