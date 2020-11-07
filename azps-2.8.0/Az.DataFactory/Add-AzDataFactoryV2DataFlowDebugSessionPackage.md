---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: fdf8d4fefef434e503c0fc21c3036577e56b56c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706060"
---
# <span data-ttu-id="d3b37-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="d3b37-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="d3b37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3b37-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b37-103">Dodaj zasób przepływu danych i jego zależności do konkretnej sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="d3b37-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="d3b37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3b37-104">SYNTAX</span></span>

### <span data-ttu-id="d3b37-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d3b37-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3b37-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d3b37-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3b37-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3b37-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3b37-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d3b37-108">DESCRIPTION</span></span>
<span data-ttu-id="d3b37-109">To polecenie umożliwia dołączenie zasobu przepływu danych i jego zależności do konkretnej sesji debugowania sekwencja poleceń programu PowerShell dla przepływu pracy debugowania przepływu danych:</span><span class="sxs-lookup"><span data-stu-id="d3b37-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="d3b37-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3b37-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="d3b37-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="d3b37-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="d3b37-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (Powtórz ten krok dla różnych poleceń/obiektów docelowych) lub Powtórz krok 2-3 w celu zmiany pliku pakietu)</span><span class="sxs-lookup"><span data-stu-id="d3b37-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="d3b37-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3b37-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="d3b37-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3b37-114">EXAMPLES</span></span>

### <span data-ttu-id="d3b37-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3b37-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="d3b37-116">Dodaj pakiet przepływu danych do sesji debugowania "550effe4-93a3-485c-8525-eaf25259efbd" "WikiADF" fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d3b37-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="d3b37-117">Plik Pakcage zawiera zasób debugowania przepływu danych, listę funkcji debugowania zestawu danych Resouce, listę zasobów debugowania połączonej usługi, ustawienia debugowania i identyfikator sesji.</span><span class="sxs-lookup"><span data-stu-id="d3b37-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="d3b37-118">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="d3b37-118">For instance:</span></span>

<span data-ttu-id="d3b37-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName = Name; AccountKey = klucz; EndpointSuffix = Core. Windows. NET "}}}]," debugSettings ": {" sourceSettings ": [{" SourceName ":" source1 "," rowLimit ": 1000}]}," ":" 4f988caf-e765-47d2-82cd-430334a6b135 "}</span><span class="sxs-lookup"><span data-stu-id="d3b37-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="d3b37-120">Parametr SessionID służy do zamiany istniejącej właściwości sessionId w pliku pakietu.</span><span class="sxs-lookup"><span data-stu-id="d3b37-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="d3b37-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3b37-121">PARAMETERS</span></span>

### <span data-ttu-id="d3b37-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d3b37-122">-DataFactory</span></span>
<span data-ttu-id="d3b37-123">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d3b37-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b37-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d3b37-124">-DataFactoryName</span></span>
<span data-ttu-id="d3b37-125">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d3b37-125">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b37-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b37-126">-DefaultProfile</span></span>
<span data-ttu-id="d3b37-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3b37-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3b37-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="d3b37-128">-PackageFile</span></span>
<span data-ttu-id="d3b37-129">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="d3b37-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b37-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3b37-130">-PassThru</span></span>
<span data-ttu-id="d3b37-131">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="d3b37-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="d3b37-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d3b37-132">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b37-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b37-133">-ResourceGroupName</span></span>
<span data-ttu-id="d3b37-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3b37-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b37-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3b37-135">-ResourceId</span></span>
<span data-ttu-id="d3b37-136">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d3b37-136">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b37-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3b37-137">-Confirm</span></span>
<span data-ttu-id="d3b37-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3b37-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b37-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b37-139">-WhatIf</span></span>
<span data-ttu-id="d3b37-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3b37-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3b37-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d3b37-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3b37-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b37-142">CommonParameters</span></span>
<span data-ttu-id="d3b37-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3b37-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b37-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3b37-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b37-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3b37-145">INPUTS</span></span>

### <span data-ttu-id="d3b37-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d3b37-146">System.String</span></span>

### <span data-ttu-id="d3b37-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d3b37-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d3b37-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3b37-148">OUTPUTS</span></span>

### <span data-ttu-id="d3b37-149">System. void</span><span class="sxs-lookup"><span data-stu-id="d3b37-149">System.Void</span></span>

### <span data-ttu-id="d3b37-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3b37-150">System.Boolean</span></span>

## <span data-ttu-id="d3b37-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3b37-151">NOTES</span></span>
<span data-ttu-id="d3b37-152">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="d3b37-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d3b37-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3b37-153">RELATED LINKS</span></span>

[<span data-ttu-id="d3b37-154">Start — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3b37-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="d3b37-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3b37-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="d3b37-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="d3b37-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="d3b37-157">Zatrzymaj — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3b37-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)