---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500621"
---
# <span data-ttu-id="547f2-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="547f2-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="547f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="547f2-102">SYNOPSIS</span></span>
<span data-ttu-id="547f2-103">Tworzy obiekt konfiguracji zapytania BLOB, który może być wykorzystywany w programie Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="547f2-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="547f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="547f2-104">SYNTAX</span></span>

### <span data-ttu-id="547f2-105">CSV (domyślny)</span><span class="sxs-lookup"><span data-stu-id="547f2-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="547f2-106">JSON</span><span class="sxs-lookup"><span data-stu-id="547f2-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="547f2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="547f2-107">DESCRIPTION</span></span>
<span data-ttu-id="547f2-108">Polecenie cmdlet **New-AzStorageBlobQueryConfig** tworzy obiekt konfiguracji zapytania BLOB, którego można użyć w polecenia Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="547f2-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="547f2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="547f2-109">EXAMPLES</span></span>

### <span data-ttu-id="547f2-110">Przykład 1: Konfigurowanie kwerendy obiektu BLOB oraz tworzenie zapytań do obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="547f2-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="547f2-111">To polecenie najpierw Utwórz obiekt konfiguracji wejściowej jako plik CSV, a następnie wyjściowy obiekt konfiguracji jako kod JSON, a następnie użyj 2 konfiguracji do zbadania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="547f2-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="547f2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="547f2-112">PARAMETERS</span></span>

### <span data-ttu-id="547f2-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="547f2-113">-AsCsv</span></span>
<span data-ttu-id="547f2-114">Wskaż, aby utworzyć konfigurację kwerendy obiektu BLOB dla pliku CSV.</span><span class="sxs-lookup"><span data-stu-id="547f2-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="547f2-115">-AsJob</span></span>
<span data-ttu-id="547f2-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="547f2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="547f2-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="547f2-117">-AsJson</span></span>
<span data-ttu-id="547f2-118">Wskaż, aby utworzyć konfigurację kwerendy obiektu BLOB dla notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="547f2-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f2-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="547f2-119">-ColumnSeparator</span></span>
<span data-ttu-id="547f2-120">Dodatkowych.</span><span class="sxs-lookup"><span data-stu-id="547f2-120">Optional.</span></span>
<span data-ttu-id="547f2-121">Ciąg służący do oddzielania kolumn.</span><span class="sxs-lookup"><span data-stu-id="547f2-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f2-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="547f2-122">-EscapeCharacter</span></span>
<span data-ttu-id="547f2-123">Dodatkowych.</span><span class="sxs-lookup"><span data-stu-id="547f2-123">Optional.</span></span>
<span data-ttu-id="547f2-124">Znak, którego użyto jako znaku ucieczki.</span><span class="sxs-lookup"><span data-stu-id="547f2-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f2-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="547f2-125">-HasHeader</span></span>
<span data-ttu-id="547f2-126">Dodatkowych.</span><span class="sxs-lookup"><span data-stu-id="547f2-126">Optional.</span></span>
<span data-ttu-id="547f2-127">Wskazać, że reprezentujący dane mają nagłówki.</span><span class="sxs-lookup"><span data-stu-id="547f2-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f2-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="547f2-128">-QuotationCharacter</span></span>
<span data-ttu-id="547f2-129">Dodatkowych.</span><span class="sxs-lookup"><span data-stu-id="547f2-129">Optional.</span></span>
<span data-ttu-id="547f2-130">Znak służący do cytowania określonego pola.</span><span class="sxs-lookup"><span data-stu-id="547f2-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f2-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="547f2-131">-RecordSeparator</span></span>
<span data-ttu-id="547f2-132">Dodatkowych.</span><span class="sxs-lookup"><span data-stu-id="547f2-132">Optional.</span></span>
<span data-ttu-id="547f2-133">Ciąg służący do oddzielania rekordów.</span><span class="sxs-lookup"><span data-stu-id="547f2-133">The string used to separate records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547f2-134">CommonParameters</span></span>
<span data-ttu-id="547f2-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547f2-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="547f2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547f2-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="547f2-137">INPUTS</span></span>

### <span data-ttu-id="547f2-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="547f2-138">None</span></span>

## <span data-ttu-id="547f2-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="547f2-139">OUTPUTS</span></span>

### <span data-ttu-id="547f2-140">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="547f2-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="547f2-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="547f2-141">NOTES</span></span>

## <span data-ttu-id="547f2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="547f2-142">RELATED LINKS</span></span>
