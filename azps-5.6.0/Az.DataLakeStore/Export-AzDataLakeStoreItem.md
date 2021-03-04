---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: 72fcb1ecd78b2682fe678af8b75b36032ff58b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957306"
---
# <span data-ttu-id="e0dfb-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e0dfb-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="e0dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dfb-103">Pobiera plik ze sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="e0dfb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0dfb-104">SYNTAX</span></span>

### <span data-ttu-id="e0dfb-105">NoDiagnosticLogging (Default)</span><span class="sxs-lookup"><span data-stu-id="e0dfb-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0dfb-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="e0dfb-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0dfb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0dfb-107">DESCRIPTION</span></span>
<span data-ttu-id="e0dfb-108">Polecenie **cmdlet Export-AzDataLakeStoreItem** pobiera plik z magazynu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="e0dfb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0dfb-109">EXAMPLES</span></span>

### <span data-ttu-id="e0dfb-110">Przykład 1. Pobieranie elementu ze sklepu Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e0dfb-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="e0dfb-111">To polecenie pobiera plik TestSource.csv ze sklepu Data Lake Store w celu C:\Test.csv z współbieżnością 4.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="e0dfb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0dfb-112">PARAMETERS</span></span>

### <span data-ttu-id="e0dfb-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="e0dfb-113">-Account</span></span>
<span data-ttu-id="e0dfb-114">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-115">— współbieżność</span><span class="sxs-lookup"><span data-stu-id="e0dfb-115">-Concurrency</span></span>
<span data-ttu-id="e0dfb-116">Wskazuje liczbę plików lub fragmentów do pobrania równolegle.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="e0dfb-117">Wartość domyślna zostanie obliczona według najlepszych starań, na podstawie specyfikacji systemowych.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dfb-118">-DefaultProfile</span></span>
<span data-ttu-id="e0dfb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0dfb-120">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="e0dfb-120">-Destination</span></span>
<span data-ttu-id="e0dfb-121">Określa ścieżkę lokalnego pliku, do której należy pobrać plik.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-121">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-122">- DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="e0dfb-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="e0dfb-123">Opcjonalnie określa poziom dziennika diagnostycznego, na którym mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="e0dfb-124">Wartość domyślna to Błąd.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-125">- DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="e0dfb-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="e0dfb-126">Określa ścieżkę dziennika diagnostycznego do nagrywania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e0dfb-127">-Force</span></span>
<span data-ttu-id="e0dfb-128">Oznacza, że ta operacja może zastąpić plik docelowy, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-129">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="e0dfb-129">-Path</span></span>
<span data-ttu-id="e0dfb-130">Określa ścieżkę elementu do pobrania ze sklepu Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="e0dfb-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-131">- Rekurencie</span><span class="sxs-lookup"><span data-stu-id="e0dfb-131">-Recurse</span></span>
<span data-ttu-id="e0dfb-132">Wskazuje, że pobieranie folderu jest cykliczne.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-132">Indicates that a folder download is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-133">— Wznów</span><span class="sxs-lookup"><span data-stu-id="e0dfb-133">-Resume</span></span>
<span data-ttu-id="e0dfb-134">Wskazuje, że kopiowane pliki są kontynuacją poprzedniego pobierania.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="e0dfb-135">Spowoduje to, że system spróbuje wznowić pracę od ostatniego pliku, który nie został w pełni pobrany.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0dfb-136">-Confirm</span></span>
<span data-ttu-id="e0dfb-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0dfb-138">-WhatIf</span></span>
<span data-ttu-id="e0dfb-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0dfb-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dfb-141">CommonParameters</span></span>
<span data-ttu-id="e0dfb-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dfb-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0dfb-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dfb-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0dfb-144">INPUTS</span></span>

### <span data-ttu-id="e0dfb-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e0dfb-145">System.String</span></span>

### <span data-ttu-id="e0dfb-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e0dfb-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e0dfb-147">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e0dfb-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e0dfb-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e0dfb-148">System.Int32</span></span>

### <span data-ttu-id="e0dfb-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="e0dfb-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="e0dfb-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0dfb-150">OUTPUTS</span></span>

### <span data-ttu-id="e0dfb-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e0dfb-151">System.String</span></span>

## <span data-ttu-id="e0dfb-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0dfb-152">NOTES</span></span>

## <span data-ttu-id="e0dfb-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0dfb-153">RELATED LINKS</span></span>

[<span data-ttu-id="e0dfb-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e0dfb-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="e0dfb-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e0dfb-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="e0dfb-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e0dfb-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="e0dfb-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e0dfb-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="e0dfb-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e0dfb-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="e0dfb-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e0dfb-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="e0dfb-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e0dfb-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


