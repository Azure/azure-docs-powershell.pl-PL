---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 8525333f2be148b59053c62fc4d0f95dda8949a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549228"
---
# <span data-ttu-id="eace3-101">Save-AzureRmDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="eace3-101">Save-AzureRmDataFactoryLog</span></span>

## <span data-ttu-id="eace3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eace3-102">SYNOPSIS</span></span>
<span data-ttu-id="eace3-103">Pobiera pliki dziennika z przetwarzania usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="eace3-103">Downloads log files from Azure HDInsight processing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eace3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eace3-104">SYNTAX</span></span>

### <span data-ttu-id="eace3-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eace3-105">ByFactoryName (Default)</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eace3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eace3-106">ByFactoryObject</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eace3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eace3-107">DESCRIPTION</span></span>
<span data-ttu-id="eace3-108">Polecenie cmdlet **Save-AzureRmDataFactoryLog** umożliwia pobieranie plików dziennika skojarzonych z przetwarzaniem usługi Azure HDInsight dla projektów świni lub Hive oraz dla niestandardowych aktywności na lokalnym dysku twardym.</span><span class="sxs-lookup"><span data-stu-id="eace3-108">The **Save-AzureRmDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="eace3-109">Uruchom polecenie cmdlet Get-AzureRmDataFactoryRun, aby uzyskać identyfikator działania dla wycinka danych, a następnie użyj tego identyfikatora w celu pobrania plików dziennika z magazynu dużych obiektów binarnych (BLOB) skojarzonego z klastrem usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="eace3-109">You first run the Get-AzureRmDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>

<span data-ttu-id="eace3-110">Jeśli nie określisz parametru *DownloadLogs* , polecenie cmdlet zwróci tylko lokalizację plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="eace3-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>

<span data-ttu-id="eace3-111">Jeśli określisz *DownloadLogs* bez określania katalogu wyjściowego (parametr *wyjściowy* ), pliki dziennika zostaną pobrane do domyślnego folderu dokumenty.</span><span class="sxs-lookup"><span data-stu-id="eace3-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>

<span data-ttu-id="eace3-112">Jeśli określisz *DownloadLogs* razem z folderem wyjściowym ( *wyjściem* ), pliki dziennika zostaną pobrane do określonego folderu.</span><span class="sxs-lookup"><span data-stu-id="eace3-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="eace3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eace3-113">EXAMPLES</span></span>

### <span data-ttu-id="eace3-114">Przykład 1: zapisywanie plików dziennika w określonym folderze</span><span class="sxs-lookup"><span data-stu-id="eace3-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="eace3-115">To polecenie zapisuje pliki dziennika dla działania uruchomionego z IDENTYFIKATORem 841b77c9-d56c-48d1-99a3-8c16c3e77d39, w którym działanie należy do potoku w fabryce danych o nazwie LogProcessingFactory w grupie zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="eace3-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="eace3-116">Pliki dziennika są zapisywane w folderze C:\Test.</span><span class="sxs-lookup"><span data-stu-id="eace3-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="eace3-117">Przykład 2: zapisywanie plików dziennika w folderze dokumenty domyślne</span><span class="sxs-lookup"><span data-stu-id="eace3-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="eace3-118">To polecenie zapisuje pliki dziennika w folderze dokumenty (ustawienie domyślne).</span><span class="sxs-lookup"><span data-stu-id="eace3-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="eace3-119">Przykład 3: Uzyskiwanie lokalizacji plików dziennika</span><span class="sxs-lookup"><span data-stu-id="eace3-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="eace3-120">To polecenie zwraca lokalizację plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="eace3-120">This command returns the location of log files.</span></span>
<span data-ttu-id="eace3-121">Zauważ, że nie podano *DownloadLogs* .</span><span class="sxs-lookup"><span data-stu-id="eace3-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="eace3-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eace3-122">PARAMETERS</span></span>

### <span data-ttu-id="eace3-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="eace3-123">-DataFactory</span></span>
<span data-ttu-id="eace3-124">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="eace3-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="eace3-125">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="eace3-125">-DataFactoryName</span></span>
<span data-ttu-id="eace3-126">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="eace3-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="eace3-127">To polecenie cmdlet pobiera pliki dziennika dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="eace3-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eace3-128">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="eace3-128">-DownloadLogs</span></span>
<span data-ttu-id="eace3-129">Wskazuje, że to polecenie cmdlet pobiera pliki dziennika na komputer lokalny.</span><span class="sxs-lookup"><span data-stu-id="eace3-129">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="eace3-130">Jeśli nie określono folderu *ouptut* , pliki są zapisywane w folderze dokumenty pod podfolderem.</span><span class="sxs-lookup"><span data-stu-id="eace3-130">If *Ouptut* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="eace3-131">-ID</span><span class="sxs-lookup"><span data-stu-id="eace3-131">-Id</span></span>
<span data-ttu-id="eace3-132">Określa identyfikator działania dla wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="eace3-132">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="eace3-133">Użyj polecenia cmdlet Get-AzureRmDataFactoryRun, aby uzyskać identyfikator.</span><span class="sxs-lookup"><span data-stu-id="eace3-133">Use the Get-AzureRmDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="eace3-134">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="eace3-134">-Output</span></span>
<span data-ttu-id="eace3-135">Określa folder wyjściowy, w którym są zapisywane pobrane pliki dziennika.</span><span class="sxs-lookup"><span data-stu-id="eace3-135">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="eace3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eace3-136">-ResourceGroupName</span></span>
<span data-ttu-id="eace3-137">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eace3-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="eace3-138">To polecenie cmdlet umożliwia utworzenie fabryki danych należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="eace3-138">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="eace3-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eace3-139">-DefaultProfile</span></span>
<span data-ttu-id="eace3-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eace3-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eace3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eace3-141">CommonParameters</span></span>
<span data-ttu-id="eace3-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eace3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eace3-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eace3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eace3-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eace3-144">INPUTS</span></span>

## <span data-ttu-id="eace3-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eace3-145">OUTPUTS</span></span>

### <span data-ttu-id="eace3-146">Microsoft. Azure. Commands. datafactors. models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="eace3-146">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="eace3-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eace3-147">NOTES</span></span>
* <span data-ttu-id="eace3-148">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="eace3-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="eace3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eace3-149">RELATED LINKS</span></span>

[<span data-ttu-id="eace3-150">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="eace3-150">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="eace3-151">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="eace3-151">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="eace3-152">Nowe — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="eace3-152">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="eace3-153">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="eace3-153">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="eace3-154">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="eace3-154">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="eace3-155">Suspend — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="eace3-155">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


