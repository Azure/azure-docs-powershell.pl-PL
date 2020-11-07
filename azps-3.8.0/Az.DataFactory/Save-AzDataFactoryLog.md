---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896310"
---
# <span data-ttu-id="d0f9c-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="d0f9c-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="d0f9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f9c-103">Pobiera pliki dziennika z przetwarzania usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="d0f9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0f9c-104">SYNTAX</span></span>

### <span data-ttu-id="d0f9c-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0f9c-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0f9c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d0f9c-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0f9c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d0f9c-107">DESCRIPTION</span></span>
<span data-ttu-id="d0f9c-108">Polecenie cmdlet **Save-AzDataFactoryLog** umożliwia pobieranie plików dziennika skojarzonych z przetwarzaniem usługi Azure HDInsight dla projektów świni lub Hive oraz dla niestandardowych aktywności na lokalnym dysku twardym.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="d0f9c-109">Uruchom polecenie cmdlet Get-AzDataFactoryRun, aby uzyskać identyfikator działania dla wycinka danych, a następnie użyj tego identyfikatora w celu pobrania plików dziennika z magazynu dużych obiektów binarnych (BLOB) skojarzonego z klastrem usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="d0f9c-110">Jeśli nie określisz parametru *DownloadLogs* , polecenie cmdlet zwróci tylko lokalizację plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="d0f9c-111">Jeśli określisz *DownloadLogs* bez określania katalogu wyjściowego (parametr *wyjściowy* ), pliki dziennika zostaną pobrane do domyślnego folderu dokumenty.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="d0f9c-112">Jeśli określisz *DownloadLogs* razem z folderem wyjściowym ( *wyjściem* ), pliki dziennika zostaną pobrane do określonego folderu.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="d0f9c-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0f9c-113">EXAMPLES</span></span>

### <span data-ttu-id="d0f9c-114">Przykład 1: zapisywanie plików dziennika w określonym folderze</span><span class="sxs-lookup"><span data-stu-id="d0f9c-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="d0f9c-115">To polecenie zapisuje pliki dziennika dla działania uruchomionego z IDENTYFIKATORem 841b77c9-d56c-48d1-99a3-8c16c3e77d39, w którym działanie należy do potoku w fabryce danych o nazwie LogProcessingFactory w grupie zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="d0f9c-116">Pliki dziennika są zapisywane w folderze C:\Test.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="d0f9c-117">Przykład 2: zapisywanie plików dziennika w folderze dokumenty domyślne</span><span class="sxs-lookup"><span data-stu-id="d0f9c-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="d0f9c-118">To polecenie zapisuje pliki dziennika w folderze dokumenty (ustawienie domyślne).</span><span class="sxs-lookup"><span data-stu-id="d0f9c-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="d0f9c-119">Przykład 3: Uzyskiwanie lokalizacji plików dziennika</span><span class="sxs-lookup"><span data-stu-id="d0f9c-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="d0f9c-120">To polecenie zwraca lokalizację plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-120">This command returns the location of log files.</span></span>
<span data-ttu-id="d0f9c-121">Zauważ, że nie podano *DownloadLogs* .</span><span class="sxs-lookup"><span data-stu-id="d0f9c-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="d0f9c-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0f9c-122">PARAMETERS</span></span>

### <span data-ttu-id="d0f9c-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d0f9c-123">-DataFactory</span></span>
<span data-ttu-id="d0f9c-124">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d0f9c-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="d0f9c-125">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d0f9c-125">-DataFactoryName</span></span>
<span data-ttu-id="d0f9c-126">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d0f9c-127">To polecenie cmdlet pobiera pliki dziennika dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d0f9c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f9c-128">-DefaultProfile</span></span>
<span data-ttu-id="d0f9c-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d0f9c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0f9c-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="d0f9c-130">-DownloadLogs</span></span>
<span data-ttu-id="d0f9c-131">Wskazuje, że to polecenie cmdlet pobiera pliki dziennika na komputer lokalny.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="d0f9c-132">Jeśli nie określono folderu *wyjściowego* , pliki są zapisywane w folderze dokumenty pod podfolderem.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="d0f9c-133">-ID</span><span class="sxs-lookup"><span data-stu-id="d0f9c-133">-Id</span></span>
<span data-ttu-id="d0f9c-134">Określa identyfikator działania dla wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="d0f9c-135">Użyj polecenia cmdlet Get-AzDataFactoryRun, aby uzyskać identyfikator.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="d0f9c-136">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="d0f9c-136">-Output</span></span>
<span data-ttu-id="d0f9c-137">Określa folder wyjściowy, w którym są zapisywane pobrane pliki dziennika.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="d0f9c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f9c-138">-ResourceGroupName</span></span>
<span data-ttu-id="d0f9c-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d0f9c-140">To polecenie cmdlet umożliwia utworzenie fabryki danych należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d0f9c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f9c-141">CommonParameters</span></span>
<span data-ttu-id="d0f9c-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f9c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f9c-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f9c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f9c-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0f9c-144">INPUTS</span></span>

### <span data-ttu-id="d0f9c-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d0f9c-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d0f9c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d0f9c-146">System.String</span></span>

## <span data-ttu-id="d0f9c-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0f9c-147">OUTPUTS</span></span>

### <span data-ttu-id="d0f9c-148">Microsoft. Azure. Commands. datafactors. models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="d0f9c-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="d0f9c-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0f9c-149">NOTES</span></span>
* <span data-ttu-id="d0f9c-150">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="d0f9c-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d0f9c-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0f9c-151">RELATED LINKS</span></span>

[<span data-ttu-id="d0f9c-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="d0f9c-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="d0f9c-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d0f9c-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="d0f9c-154">Nowe — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d0f9c-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="d0f9c-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d0f9c-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="d0f9c-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d0f9c-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="d0f9c-157">Suspend — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d0f9c-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


