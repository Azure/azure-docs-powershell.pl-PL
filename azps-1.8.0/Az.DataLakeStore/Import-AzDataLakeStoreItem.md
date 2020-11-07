---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ccb538446e7cb179e15f3af17d0cde03c4ab44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868524"
---
# <span data-ttu-id="c2468-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2468-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="c2468-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2468-102">SYNOPSIS</span></span>
<span data-ttu-id="c2468-103">Umożliwia przekazywanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c2468-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="c2468-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2468-104">SYNTAX</span></span>

### <span data-ttu-id="c2468-105">NoDiagnosticLogging (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2468-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2468-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="c2468-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2468-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2468-107">DESCRIPTION</span></span>
<span data-ttu-id="c2468-108">Polecenie cmdlet **Import-AzDataLakeStoreItem** umożliwia przekazanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c2468-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="c2468-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2468-109">EXAMPLES</span></span>

### <span data-ttu-id="c2468-110">Przykład 1: przekazywanie pliku</span><span class="sxs-lookup"><span data-stu-id="c2468-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="c2468-111">To polecenie umożliwia przekazywanie pliku SrcFile.csv i dodanie go do folderu Moje pliki w usłudze Data Lake Store jako File.csv z współbieżnością równą 4.</span><span class="sxs-lookup"><span data-stu-id="c2468-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="c2468-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2468-112">PARAMETERS</span></span>

### <span data-ttu-id="c2468-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="c2468-113">-Account</span></span>
<span data-ttu-id="c2468-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c2468-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c2468-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="c2468-115">-Concurrency</span></span>
<span data-ttu-id="c2468-116">Wskazuje liczbę plików lub fragmentów, które mają być przekazywane równolegle.</span><span class="sxs-lookup"><span data-stu-id="c2468-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="c2468-117">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemowych.</span><span class="sxs-lookup"><span data-stu-id="c2468-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="c2468-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2468-118">-DefaultProfile</span></span>
<span data-ttu-id="c2468-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2468-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2468-120">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="c2468-120">-Destination</span></span>
<span data-ttu-id="c2468-121">Określa ścieżkę usługi Data Lake Store, do której ma zostać przekazany plik lub folder, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="c2468-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c2468-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="c2468-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="c2468-123">Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="c2468-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="c2468-124">Błąd domyślny.</span><span class="sxs-lookup"><span data-stu-id="c2468-124">Default is Error.</span></span>

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

### <span data-ttu-id="c2468-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="c2468-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="c2468-126">Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="c2468-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="c2468-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c2468-127">-Force</span></span>
<span data-ttu-id="c2468-128">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="c2468-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="c2468-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="c2468-129">-ForceBinary</span></span>
<span data-ttu-id="c2468-130">Wskazuje, że kopiowane pliki powinny być kopiowane bez obawy o zachowanie nowych wierszy po dołączaniu.</span><span class="sxs-lookup"><span data-stu-id="c2468-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="c2468-131">-Path</span><span class="sxs-lookup"><span data-stu-id="c2468-131">-Path</span></span>
<span data-ttu-id="c2468-132">Określa ścieżkę lokalną pliku lub folderu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="c2468-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="c2468-133">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="c2468-133">-Recurse</span></span>
<span data-ttu-id="c2468-134">Wskazuje, że ta operacja powinna przekazać wszystkie elementy we wszystkich podfolderach.</span><span class="sxs-lookup"><span data-stu-id="c2468-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="c2468-135">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="c2468-135">-Resume</span></span>
<span data-ttu-id="c2468-136">Wskazuje, że kopiowane pliki są kontynuacją wcześniejszego przekazania.</span><span class="sxs-lookup"><span data-stu-id="c2468-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="c2468-137">Spowoduje to, że system będzie próbował wznowić pracę z ostatniego pliku, który nie został w pełni przekazany.</span><span class="sxs-lookup"><span data-stu-id="c2468-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="c2468-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2468-138">-Confirm</span></span>
<span data-ttu-id="c2468-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2468-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2468-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2468-140">-WhatIf</span></span>
<span data-ttu-id="c2468-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2468-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2468-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2468-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2468-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2468-143">CommonParameters</span></span>
<span data-ttu-id="c2468-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2468-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2468-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2468-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2468-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2468-146">INPUTS</span></span>

### <span data-ttu-id="c2468-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c2468-147">System.String</span></span>

### <span data-ttu-id="c2468-148">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c2468-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c2468-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2468-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c2468-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c2468-150">System.Int32</span></span>

### <span data-ttu-id="c2468-151">Microsoft. Azure. Commands. DataLakeStore. models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="c2468-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="c2468-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2468-152">OUTPUTS</span></span>

### <span data-ttu-id="c2468-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c2468-153">System.String</span></span>

## <span data-ttu-id="c2468-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2468-154">NOTES</span></span>

## <span data-ttu-id="c2468-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2468-155">RELATED LINKS</span></span>

[<span data-ttu-id="c2468-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2468-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2468-157">Eksportowanie — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2468-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2468-158">Dołącz do AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2468-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2468-159">Przenieś — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2468-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2468-160">Nowe — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2468-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2468-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2468-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2468-162">Test — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2468-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


