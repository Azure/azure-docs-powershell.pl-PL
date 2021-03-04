---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 12c0c4832d13e3e8637ab1cdb36a1f3fe3abb7d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969233"
---
# <span data-ttu-id="d84da-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="d84da-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="d84da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d84da-102">SYNOPSIS</span></span>
<span data-ttu-id="d84da-103">Dodaje zestawy danych do udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d84da-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="d84da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d84da-104">SYNTAX</span></span>

### <span data-ttu-id="d84da-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d84da-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d84da-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="d84da-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d84da-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="d84da-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d84da-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="d84da-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d84da-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d84da-109">DESCRIPTION</span></span>
<span data-ttu-id="d84da-110">Polecenie **cmdlet New-AzDataShareDataSet** umożliwia dodawanie zestawów danych w usłudze Azure Data Share Account.</span><span class="sxs-lookup"><span data-stu-id="d84da-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="d84da-111">Możesz dodać zestawy danych typu Obiekt blob, ADLS Gen2 i ADLS Gen1.</span><span class="sxs-lookup"><span data-stu-id="d84da-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="d84da-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d84da-112">EXAMPLES</span></span>

### <span data-ttu-id="d84da-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d84da-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="d84da-114">To polecenie dodaje zestaw danych o nazwie AdsDataSet typu kontener obiektów blob do usługi Azure Data Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="d84da-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="d84da-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d84da-115">PARAMETERS</span></span>

### <span data-ttu-id="d84da-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d84da-116">-AccountName</span></span>
<span data-ttu-id="d84da-117">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d84da-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84da-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="d84da-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="d84da-119">Ścieżka folderu usługi ADLS w usłudze Azure Storage</span><span class="sxs-lookup"><span data-stu-id="d84da-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84da-120">— Kontener</span><span class="sxs-lookup"><span data-stu-id="d84da-120">-Container</span></span>
<span data-ttu-id="d84da-121">Nazwa kontenera konta magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d84da-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="d84da-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84da-122">-DefaultProfile</span></span>
<span data-ttu-id="d84da-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d84da-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d84da-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="d84da-124">-FileName</span></span>
<span data-ttu-id="d84da-125">Nazwa pliku adls (1) magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d84da-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84da-126">- FilePath</span><span class="sxs-lookup"><span data-stu-id="d84da-126">-FilePath</span></span>
<span data-ttu-id="d84da-127">Ścieżka pliku magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d84da-127">Azure storage file path</span></span>

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

### <span data-ttu-id="d84da-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="d84da-128">-FileSystem</span></span>
<span data-ttu-id="d84da-129">Nazwa systemu plików w usłudze Azure ADLS (gen2)</span><span class="sxs-lookup"><span data-stu-id="d84da-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="d84da-130">- FolderPath</span><span class="sxs-lookup"><span data-stu-id="d84da-130">-FolderPath</span></span>
<span data-ttu-id="d84da-131">Ścieżka folderu magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d84da-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="d84da-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d84da-132">-Name</span></span>
<span data-ttu-id="d84da-133">Nazwa zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d84da-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84da-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84da-134">-ResourceGroupName</span></span>
<span data-ttu-id="d84da-135">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d84da-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84da-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d84da-136">-ShareName</span></span>
<span data-ttu-id="d84da-137">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d84da-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84da-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d84da-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="d84da-139">Azure storage account resourceId</span><span class="sxs-lookup"><span data-stu-id="d84da-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84da-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d84da-140">-Confirm</span></span>
<span data-ttu-id="d84da-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d84da-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d84da-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d84da-142">-WhatIf</span></span>
<span data-ttu-id="d84da-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d84da-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d84da-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d84da-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d84da-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84da-145">CommonParameters</span></span>
<span data-ttu-id="d84da-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d84da-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84da-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d84da-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84da-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d84da-148">INPUTS</span></span>

### <span data-ttu-id="d84da-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d84da-149">System.String</span></span>

## <span data-ttu-id="d84da-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d84da-150">OUTPUTS</span></span>

### <span data-ttu-id="d84da-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="d84da-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="d84da-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d84da-152">NOTES</span></span>

## <span data-ttu-id="d84da-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d84da-153">RELATED LINKS</span></span>
