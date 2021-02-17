---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198482"
---
# <span data-ttu-id="6a1cd-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="6a1cd-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="6a1cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1cd-103">Tworzy obiekt konfiguracji zapytania blob, którego można użyć w pliku Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="6a1cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a1cd-104">SYNTAX</span></span>

### <span data-ttu-id="6a1cd-105">Csv (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6a1cd-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="6a1cd-106">Json</span><span class="sxs-lookup"><span data-stu-id="6a1cd-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="6a1cd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a1cd-107">DESCRIPTION</span></span>
<span data-ttu-id="6a1cd-108">Polecenie cmdlet **New-AzStorageBlobQueryConfig** tworzy obiekt konfiguracji zapytania obiektów blob, którego można używać w pliku Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="6a1cd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a1cd-109">EXAMPLES</span></span>

### <span data-ttu-id="6a1cd-110">Przykład 1. Tworzenie konfiguracji zapytania obiektów blob i tworzenie zapytania do obiektu blob</span><span class="sxs-lookup"><span data-stu-id="6a1cd-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="6a1cd-111">To polecenie najpierw tworzy obiekt konfiguracji danych wejściowych jako plik csv, a obiekt konfiguracji wyjściowej jako json, a następnie używa dwóch konfiguracji do tworzenia zapytań obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="6a1cd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a1cd-112">PARAMETERS</span></span>

### <span data-ttu-id="6a1cd-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="6a1cd-113">-AsCsv</span></span>
<span data-ttu-id="6a1cd-114">Wskaż, aby utworzyć konfigurację zapytania obiektów blob dla pliku CSV.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="6a1cd-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6a1cd-115">-AsJob</span></span>
<span data-ttu-id="6a1cd-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6a1cd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a1cd-117">- AsJson</span><span class="sxs-lookup"><span data-stu-id="6a1cd-117">-AsJson</span></span>
<span data-ttu-id="6a1cd-118">Wskaż, aby utworzyć konfigurację zapytania obiektów blob dla Jsna.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="6a1cd-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="6a1cd-119">-ColumnSeparator</span></span>
<span data-ttu-id="6a1cd-120">Argument opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-120">Optional.</span></span>
<span data-ttu-id="6a1cd-121">Ciąg używany do oddzielania kolumn.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="6a1cd-122">- EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="6a1cd-122">-EscapeCharacter</span></span>
<span data-ttu-id="6a1cd-123">Argument opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-123">Optional.</span></span>
<span data-ttu-id="6a1cd-124">Znak używany jako znak ucieczki.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="6a1cd-125">- HasHeader</span><span class="sxs-lookup"><span data-stu-id="6a1cd-125">-HasHeader</span></span>
<span data-ttu-id="6a1cd-126">Argument opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-126">Optional.</span></span>
<span data-ttu-id="6a1cd-127">Oznacza, że dane mają nagłówki.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="6a1cd-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="6a1cd-128">-QuotationCharacter</span></span>
<span data-ttu-id="6a1cd-129">Argument opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-129">Optional.</span></span>
<span data-ttu-id="6a1cd-130">Znak użyty do zacytowania określonego pola.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="6a1cd-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="6a1cd-131">-RecordSeparator</span></span>
<span data-ttu-id="6a1cd-132">Argument opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-132">Optional.</span></span>
<span data-ttu-id="6a1cd-133">Ciąg używany do oddzielania rekordów.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="6a1cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1cd-134">CommonParameters</span></span>
<span data-ttu-id="6a1cd-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a1cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1cd-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a1cd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1cd-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a1cd-137">INPUTS</span></span>

### <span data-ttu-id="6a1cd-138">Brak</span><span class="sxs-lookup"><span data-stu-id="6a1cd-138">None</span></span>

## <span data-ttu-id="6a1cd-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a1cd-139">OUTPUTS</span></span>

### <span data-ttu-id="6a1cd-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a1cd-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="6a1cd-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a1cd-141">NOTES</span></span>

## <span data-ttu-id="6a1cd-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a1cd-142">RELATED LINKS</span></span>
