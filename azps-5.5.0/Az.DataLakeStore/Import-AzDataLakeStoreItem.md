---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238190"
---
# <span data-ttu-id="52237-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="52237-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="52237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52237-102">SYNOPSIS</span></span>
<span data-ttu-id="52237-103">Przekazanie lokalnego pliku lub katalogu do sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="52237-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="52237-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52237-104">SYNTAX</span></span>

### <span data-ttu-id="52237-105">NoDiagnosticLogging (Default)</span><span class="sxs-lookup"><span data-stu-id="52237-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52237-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="52237-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52237-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="52237-107">DESCRIPTION</span></span>
<span data-ttu-id="52237-108">Polecenie **cmdlet Import-AzDataLakeStoreItem** przekaże plik lub katalog lokalny do magazynu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="52237-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="52237-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52237-109">EXAMPLES</span></span>

### <span data-ttu-id="52237-110">Przykład 1. Przekazywanie pliku</span><span class="sxs-lookup"><span data-stu-id="52237-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="52237-111">To polecenie przekaże plik do SrcFile.csv i doda go do folderu MyFiles w magazynie Data Lake Store jako File.csv z współbieżnością 4.</span><span class="sxs-lookup"><span data-stu-id="52237-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="52237-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52237-112">PARAMETERS</span></span>

### <span data-ttu-id="52237-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="52237-113">-Account</span></span>
<span data-ttu-id="52237-114">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="52237-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="52237-115">— współbieżność</span><span class="sxs-lookup"><span data-stu-id="52237-115">-Concurrency</span></span>
<span data-ttu-id="52237-116">Wskazuje liczbę plików lub fragmentów do przekazania równolegle.</span><span class="sxs-lookup"><span data-stu-id="52237-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="52237-117">Wartość domyślna zostanie obliczona według najlepszych starań, na podstawie specyfikacji systemowych.</span><span class="sxs-lookup"><span data-stu-id="52237-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="52237-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52237-118">-DefaultProfile</span></span>
<span data-ttu-id="52237-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52237-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52237-120">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="52237-120">-Destination</span></span>
<span data-ttu-id="52237-121">Określa ścieżkę do usługi Data Lake Store, do której należy przekazać plik lub folder, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="52237-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52237-122">- DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="52237-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="52237-123">Opcjonalnie określa poziom dziennika diagnostycznego, na którym mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="52237-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="52237-124">Wartość domyślna to Błąd.</span><span class="sxs-lookup"><span data-stu-id="52237-124">Default is Error.</span></span>

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

### <span data-ttu-id="52237-125">- DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="52237-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="52237-126">Określa ścieżkę dziennika diagnostycznego do nagrywania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="52237-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="52237-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="52237-127">-Force</span></span>
<span data-ttu-id="52237-128">Oznacza, że ta operacja może zastąpić plik docelowy, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="52237-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52237-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="52237-129">-ForceBinary</span></span>
<span data-ttu-id="52237-130">Wskazuje, że kopiowane pliki powinny zostać skopiowane bez obaw o zachowywanie nowych linii przez dołączanie.</span><span class="sxs-lookup"><span data-stu-id="52237-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52237-131">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="52237-131">-Path</span></span>
<span data-ttu-id="52237-132">Określa ścieżkę lokalną pliku lub folderu do przekazania.</span><span class="sxs-lookup"><span data-stu-id="52237-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="52237-133">- Rekurencie</span><span class="sxs-lookup"><span data-stu-id="52237-133">-Recurse</span></span>
<span data-ttu-id="52237-134">Oznacza, że ta operacja powinna przekazywać wszystkie elementy ze wszystkich podfolderów.</span><span class="sxs-lookup"><span data-stu-id="52237-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="52237-135">— Wznów</span><span class="sxs-lookup"><span data-stu-id="52237-135">-Resume</span></span>
<span data-ttu-id="52237-136">Wskazuje, że kopiowane pliki są kontynuacją poprzedniego przekazania.</span><span class="sxs-lookup"><span data-stu-id="52237-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="52237-137">Spowoduje to, że system spróbuje wznowić od ostatniego pliku, który nie został w pełni przekazany.</span><span class="sxs-lookup"><span data-stu-id="52237-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="52237-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52237-138">-Confirm</span></span>
<span data-ttu-id="52237-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="52237-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52237-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52237-140">-WhatIf</span></span>
<span data-ttu-id="52237-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52237-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52237-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="52237-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52237-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52237-143">CommonParameters</span></span>
<span data-ttu-id="52237-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52237-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52237-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52237-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52237-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52237-146">INPUTS</span></span>

### <span data-ttu-id="52237-147">System.String</span><span class="sxs-lookup"><span data-stu-id="52237-147">System.String</span></span>

### <span data-ttu-id="52237-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="52237-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="52237-149">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="52237-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="52237-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="52237-150">System.Int32</span></span>

### <span data-ttu-id="52237-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="52237-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="52237-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52237-152">OUTPUTS</span></span>

### <span data-ttu-id="52237-153">System.String</span><span class="sxs-lookup"><span data-stu-id="52237-153">System.String</span></span>

## <span data-ttu-id="52237-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52237-154">NOTES</span></span>

## <span data-ttu-id="52237-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52237-155">RELATED LINKS</span></span>

[<span data-ttu-id="52237-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="52237-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="52237-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="52237-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="52237-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="52237-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="52237-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="52237-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="52237-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="52237-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="52237-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="52237-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="52237-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="52237-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


