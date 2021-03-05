---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: eb2e3c9acd93e8b20c7bdf6f4ee04ef2910a3cbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006970"
---
# <span data-ttu-id="50c7b-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="50c7b-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="50c7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="50c7b-103">Pobiera pliki dziennika z przetwarzania usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="50c7b-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="50c7b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50c7b-104">SYNTAX</span></span>

### <span data-ttu-id="50c7b-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="50c7b-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50c7b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="50c7b-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50c7b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="50c7b-107">DESCRIPTION</span></span>
<span data-ttu-id="50c7b-108">Polecenie cmdlet **Save-AzDataFactoryLog** pobiera pliki dziennika skojarzone z przetwarzaniem usługi Azure HDInsight w projektach Prosia lub Gałąź albo na niestandardowe działania na lokalnym dysku twardym.</span><span class="sxs-lookup"><span data-stu-id="50c7b-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="50c7b-109">Najpierw uruchom polecenie cmdlet Get-AzDataFactoryRun w celu uzyskania identyfikatora działania uruchomionego dla wycinka danych, a następnie użyj tego identyfikatora do pobrania plików dziennika z magazynu danych dużego obiektu binarnego (BLOB) skojarzonego z klasterem HDInsight.</span><span class="sxs-lookup"><span data-stu-id="50c7b-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="50c7b-110">Jeśli parametr *DownloadLogs* nie zostanie określony, polecenie cmdlet po prostu zwróci lokalizację plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="50c7b-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="50c7b-111">Jeśli określisz *wartości DownloadLogs* bez określenia katalogu wyjściowego (parametru *wyjściowego),* pliki dziennika zostaną pobrane do domyślnego folderu Dokumenty.</span><span class="sxs-lookup"><span data-stu-id="50c7b-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="50c7b-112">Jeśli oprócz folderu wyjściowego (Danychwyjściowych) określisz wartości *DownloadLogs,* pliki dziennika zostaną pobrane do określonego folderu.</span><span class="sxs-lookup"><span data-stu-id="50c7b-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="50c7b-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50c7b-113">EXAMPLES</span></span>

### <span data-ttu-id="50c7b-114">Przykład 1. Zapisywanie plików dziennika w określonym folderze</span><span class="sxs-lookup"><span data-stu-id="50c7b-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="50c7b-115">To polecenie zapisuje pliki dziennika dla działania uruchamianego z identyfikatorem 841b77c9-d56c-48d1-99a3-8c16c3e77d39, gdzie działanie należy do potoku w fabrycznej układzie danych o nazwie LogProcessingFactory w grupie zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="50c7b-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="50c7b-116">Pliki dziennika są zapisywane w folderze C:\Test.</span><span class="sxs-lookup"><span data-stu-id="50c7b-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="50c7b-117">Przykład 2. Zapisywanie plików dziennika w domyślnym folderze Dokumenty</span><span class="sxs-lookup"><span data-stu-id="50c7b-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="50c7b-118">To polecenie zapisuje pliki dziennika w folderze Dokumenty (domyślnie).</span><span class="sxs-lookup"><span data-stu-id="50c7b-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="50c7b-119">Przykład 3. Uzyskiwanie lokalizacji plików dziennika</span><span class="sxs-lookup"><span data-stu-id="50c7b-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="50c7b-120">To polecenie zwraca lokalizację plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="50c7b-120">This command returns the location of log files.</span></span>
<span data-ttu-id="50c7b-121">Pamiętaj, że nie określono *listy DownloadLogs.*</span><span class="sxs-lookup"><span data-stu-id="50c7b-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="50c7b-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50c7b-122">PARAMETERS</span></span>

### <span data-ttu-id="50c7b-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="50c7b-123">-DataFactory</span></span>
<span data-ttu-id="50c7b-124">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="50c7b-124">Specifies a **PSDataFactory** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c7b-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="50c7b-125">-DataFactoryName</span></span>
<span data-ttu-id="50c7b-126">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="50c7b-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="50c7b-127">To polecenie cmdlet pobiera pliki dziennika dla fabrycznych danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="50c7b-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="50c7b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c7b-128">-DefaultProfile</span></span>
<span data-ttu-id="50c7b-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="50c7b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50c7b-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="50c7b-130">-DownloadLogs</span></span>
<span data-ttu-id="50c7b-131">Wskazuje, że to polecenie cmdlet pobiera pliki dziennika na komputer lokalny.</span><span class="sxs-lookup"><span data-stu-id="50c7b-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="50c7b-132">Jeśli *nie* określono folderu wyjściowego, pliki są zapisywane w folderze Dokumenty w podfolderze.</span><span class="sxs-lookup"><span data-stu-id="50c7b-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="50c7b-133">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="50c7b-133">-Id</span></span>
<span data-ttu-id="50c7b-134">Określa identyfikator działania uruchamianego dla wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="50c7b-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="50c7b-135">Użyj Get-AzDataFactoryRun cmdlet, aby uzyskać identyfikator.</span><span class="sxs-lookup"><span data-stu-id="50c7b-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c7b-136">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="50c7b-136">-Output</span></span>
<span data-ttu-id="50c7b-137">Określa folder wyjściowy, w którym są zapisywane pobrane pliki dziennika.</span><span class="sxs-lookup"><span data-stu-id="50c7b-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50c7b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50c7b-138">-ResourceGroupName</span></span>
<span data-ttu-id="50c7b-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="50c7b-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="50c7b-140">To polecenie cmdlet tworzy grupę danych należącą do grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="50c7b-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="50c7b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c7b-141">CommonParameters</span></span>
<span data-ttu-id="50c7b-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c7b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c7b-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c7b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c7b-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50c7b-144">INPUTS</span></span>

### <span data-ttu-id="50c7b-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="50c7b-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="50c7b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="50c7b-146">System.String</span></span>

## <span data-ttu-id="50c7b-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50c7b-147">OUTPUTS</span></span>

### <span data-ttu-id="50c7b-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="50c7b-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="50c7b-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50c7b-149">NOTES</span></span>
* <span data-ttu-id="50c7b-150">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="50c7b-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="50c7b-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50c7b-151">RELATED LINKS</span></span>

[<span data-ttu-id="50c7b-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="50c7b-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="50c7b-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="50c7b-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="50c7b-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="50c7b-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="50c7b-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="50c7b-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="50c7b-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="50c7b-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="50c7b-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="50c7b-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


