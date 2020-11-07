---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: 976f00f62cfda991e7d1aff349a0b04807dbbe1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705949"
---
# <span data-ttu-id="78a4f-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="78a4f-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="78a4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="78a4f-103">Pobiera pliki dziennika z przetwarzania usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="78a4f-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="78a4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78a4f-104">SYNTAX</span></span>

### <span data-ttu-id="78a4f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="78a4f-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a4f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="78a4f-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78a4f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="78a4f-107">DESCRIPTION</span></span>
<span data-ttu-id="78a4f-108">Polecenie cmdlet **Save-AzDataFactoryLog** umożliwia pobieranie plików dziennika skojarzonych z przetwarzaniem usługi Azure HDInsight dla projektów świni lub Hive oraz dla niestandardowych aktywności na lokalnym dysku twardym.</span><span class="sxs-lookup"><span data-stu-id="78a4f-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="78a4f-109">Uruchom polecenie cmdlet Get-AzDataFactoryRun, aby uzyskać identyfikator działania dla wycinka danych, a następnie użyj tego identyfikatora w celu pobrania plików dziennika z magazynu dużych obiektów binarnych (BLOB) skojarzonego z klastrem usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="78a4f-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="78a4f-110">Jeśli nie określisz parametru *DownloadLogs* , polecenie cmdlet zwróci tylko lokalizację plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="78a4f-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="78a4f-111">Jeśli określisz *DownloadLogs* bez określania katalogu wyjściowego (parametr *wyjściowy* ), pliki dziennika zostaną pobrane do domyślnego folderu dokumenty.</span><span class="sxs-lookup"><span data-stu-id="78a4f-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="78a4f-112">Jeśli określisz *DownloadLogs* razem z folderem wyjściowym ( *wyjściem* ), pliki dziennika zostaną pobrane do określonego folderu.</span><span class="sxs-lookup"><span data-stu-id="78a4f-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="78a4f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78a4f-113">EXAMPLES</span></span>

### <span data-ttu-id="78a4f-114">Przykład 1: zapisywanie plików dziennika w określonym folderze</span><span class="sxs-lookup"><span data-stu-id="78a4f-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="78a4f-115">To polecenie zapisuje pliki dziennika dla działania uruchomionego z IDENTYFIKATORem 841b77c9-d56c-48d1-99a3-8c16c3e77d39, w którym działanie należy do potoku w fabryce danych o nazwie LogProcessingFactory w grupie zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="78a4f-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="78a4f-116">Pliki dziennika są zapisywane w folderze C:\Test.</span><span class="sxs-lookup"><span data-stu-id="78a4f-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="78a4f-117">Przykład 2: zapisywanie plików dziennika w folderze dokumenty domyślne</span><span class="sxs-lookup"><span data-stu-id="78a4f-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="78a4f-118">To polecenie zapisuje pliki dziennika w folderze dokumenty (ustawienie domyślne).</span><span class="sxs-lookup"><span data-stu-id="78a4f-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="78a4f-119">Przykład 3: Uzyskiwanie lokalizacji plików dziennika</span><span class="sxs-lookup"><span data-stu-id="78a4f-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="78a4f-120">To polecenie zwraca lokalizację plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="78a4f-120">This command returns the location of log files.</span></span>
<span data-ttu-id="78a4f-121">Zauważ, że nie podano *DownloadLogs* .</span><span class="sxs-lookup"><span data-stu-id="78a4f-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="78a4f-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78a4f-122">PARAMETERS</span></span>

### <span data-ttu-id="78a4f-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="78a4f-123">-DataFactory</span></span>
<span data-ttu-id="78a4f-124">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="78a4f-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="78a4f-125">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="78a4f-125">-DataFactoryName</span></span>
<span data-ttu-id="78a4f-126">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="78a4f-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="78a4f-127">To polecenie cmdlet pobiera pliki dziennika dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="78a4f-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="78a4f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a4f-128">-DefaultProfile</span></span>
<span data-ttu-id="78a4f-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="78a4f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78a4f-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="78a4f-130">-DownloadLogs</span></span>
<span data-ttu-id="78a4f-131">Wskazuje, że to polecenie cmdlet pobiera pliki dziennika na komputer lokalny.</span><span class="sxs-lookup"><span data-stu-id="78a4f-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="78a4f-132">Jeśli nie określono folderu *wyjściowego* , pliki są zapisywane w folderze dokumenty pod podfolderem.</span><span class="sxs-lookup"><span data-stu-id="78a4f-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="78a4f-133">-ID</span><span class="sxs-lookup"><span data-stu-id="78a4f-133">-Id</span></span>
<span data-ttu-id="78a4f-134">Określa identyfikator działania dla wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="78a4f-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="78a4f-135">Użyj polecenia cmdlet Get-AzDataFactoryRun, aby uzyskać identyfikator.</span><span class="sxs-lookup"><span data-stu-id="78a4f-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="78a4f-136">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="78a4f-136">-Output</span></span>
<span data-ttu-id="78a4f-137">Określa folder wyjściowy, w którym są zapisywane pobrane pliki dziennika.</span><span class="sxs-lookup"><span data-stu-id="78a4f-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="78a4f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a4f-138">-ResourceGroupName</span></span>
<span data-ttu-id="78a4f-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="78a4f-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="78a4f-140">To polecenie cmdlet umożliwia utworzenie fabryki danych należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="78a4f-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="78a4f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a4f-141">CommonParameters</span></span>
<span data-ttu-id="78a4f-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a4f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a4f-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a4f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a4f-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78a4f-144">INPUTS</span></span>

### <span data-ttu-id="78a4f-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="78a4f-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="78a4f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="78a4f-146">System.String</span></span>

## <span data-ttu-id="78a4f-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78a4f-147">OUTPUTS</span></span>

### <span data-ttu-id="78a4f-148">Microsoft. Azure. Commands. datafactors. models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="78a4f-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="78a4f-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78a4f-149">NOTES</span></span>
* <span data-ttu-id="78a4f-150">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="78a4f-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="78a4f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78a4f-151">RELATED LINKS</span></span>

[<span data-ttu-id="78a4f-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="78a4f-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="78a4f-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="78a4f-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="78a4f-154">Nowe — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="78a4f-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="78a4f-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="78a4f-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="78a4f-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="78a4f-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="78a4f-157">Suspend — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="78a4f-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

