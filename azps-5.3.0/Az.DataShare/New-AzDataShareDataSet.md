---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 5dbf797ffabdf42b1d30d9d709ba6bb3153d8696
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377265"
---
# <span data-ttu-id="ffe7e-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="ffe7e-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="ffe7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffe7e-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe7e-103">Umożliwia dodanie zestawów danych do usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="ffe7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffe7e-104">SYNTAX</span></span>

### <span data-ttu-id="ffe7e-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ffe7e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffe7e-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="ffe7e-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffe7e-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffe7e-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffe7e-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffe7e-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffe7e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="ffe7e-109">DESCRIPTION</span></span>
<span data-ttu-id="ffe7e-110">Polecenie cmdlet **New-AzDataShareDataSet** umożliwia dodanie zestawów danych w usłudze Azure Data Share dla konta udziału danych.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="ffe7e-111">Możesz dodać zestawy danych typu BLOB, ADLS Gen2 i ADLS Gen1.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="ffe7e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffe7e-112">EXAMPLES</span></span>

### <span data-ttu-id="ffe7e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ffe7e-113">Example 1</span></span>
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

<span data-ttu-id="ffe7e-114">To polecenie umożliwia dodanie zestawu danych o nazwie AdsDataSet w kontenerze typu BLOB do usługi Azure Data Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="ffe7e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffe7e-115">PARAMETERS</span></span>

### <span data-ttu-id="ffe7e-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ffe7e-116">-AccountName</span></span>
<span data-ttu-id="ffe7e-117">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="ffe7e-117">Azure data share account name</span></span>

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

### <span data-ttu-id="ffe7e-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="ffe7e-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="ffe7e-119">Ścieżka folderu usługi Azure Storage ADLS Gen1</span><span class="sxs-lookup"><span data-stu-id="ffe7e-119">Azure storage ADLS gen1 folder path</span></span>

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

### <span data-ttu-id="ffe7e-120">-Kontener</span><span class="sxs-lookup"><span data-stu-id="ffe7e-120">-Container</span></span>
<span data-ttu-id="ffe7e-121">Nazwa kontenera konta magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ffe7e-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="ffe7e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe7e-122">-DefaultProfile</span></span>
<span data-ttu-id="ffe7e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffe7e-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="ffe7e-124">-FileName</span></span>
<span data-ttu-id="ffe7e-125">Usługa Azure Storage ADLS Gen1 nazwa pliku</span><span class="sxs-lookup"><span data-stu-id="ffe7e-125">Azure storage ADLS gen1 file name</span></span>

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

### <span data-ttu-id="ffe7e-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="ffe7e-126">-FilePath</span></span>
<span data-ttu-id="ffe7e-127">Ścieżka do pliku magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ffe7e-127">Azure storage file path</span></span>

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

### <span data-ttu-id="ffe7e-128">— System plików</span><span class="sxs-lookup"><span data-stu-id="ffe7e-128">-FileSystem</span></span>
<span data-ttu-id="ffe7e-129">Nazwa systemu plików usługi Azure ADLS Gen2</span><span class="sxs-lookup"><span data-stu-id="ffe7e-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="ffe7e-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="ffe7e-130">-FolderPath</span></span>
<span data-ttu-id="ffe7e-131">Ścieżka folderu magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ffe7e-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="ffe7e-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ffe7e-132">-Name</span></span>
<span data-ttu-id="ffe7e-133">Nazwa zestawu danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ffe7e-133">Azure data set name</span></span>

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

### <span data-ttu-id="ffe7e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffe7e-134">-ResourceGroupName</span></span>
<span data-ttu-id="ffe7e-135">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="ffe7e-135">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ffe7e-136">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="ffe7e-136">-ShareName</span></span>
<span data-ttu-id="ffe7e-137">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ffe7e-137">Azure data share name</span></span>

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

### <span data-ttu-id="ffe7e-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ffe7e-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="ffe7e-139">Identyfikator zasobu konta usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="ffe7e-139">Azure storage account resourceId</span></span>

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

### <span data-ttu-id="ffe7e-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ffe7e-140">-Confirm</span></span>
<span data-ttu-id="ffe7e-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffe7e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffe7e-142">-WhatIf</span></span>
<span data-ttu-id="ffe7e-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffe7e-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffe7e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe7e-145">CommonParameters</span></span>
<span data-ttu-id="ffe7e-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe7e-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffe7e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe7e-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffe7e-148">INPUTS</span></span>

### <span data-ttu-id="ffe7e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ffe7e-149">System.String</span></span>

## <span data-ttu-id="ffe7e-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffe7e-150">OUTPUTS</span></span>

### <span data-ttu-id="ffe7e-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="ffe7e-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="ffe7e-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffe7e-152">NOTES</span></span>

## <span data-ttu-id="ffe7e-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffe7e-153">RELATED LINKS</span></span>
