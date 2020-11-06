---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 54969735bad877592abd17327c53e22a765b69fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549027"
---
# <span data-ttu-id="4d3e4-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d3e4-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="4d3e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3e4-103">Umożliwia przekazywanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d3e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d3e4-104">SYNTAX</span></span>

### <span data-ttu-id="4d3e4-105">NoDiagnosticLogging (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4d3e4-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d3e4-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="4d3e4-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d3e4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4d3e4-107">DESCRIPTION</span></span>
<span data-ttu-id="4d3e4-108">Polecenie cmdlet **Import-AzureRmDataLakeStoreItem** umożliwia przekazanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="4d3e4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d3e4-109">EXAMPLES</span></span>

### <span data-ttu-id="4d3e4-110">Przykład 1: przekazywanie pliku</span><span class="sxs-lookup"><span data-stu-id="4d3e4-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="4d3e4-111">To polecenie umożliwia przekazywanie pliku SrcFile.csv i dodanie go do folderu Moje pliki w usłudze Data Lake Store jako File.csv z współbieżnością równą 4.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="4d3e4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d3e4-112">PARAMETERS</span></span>

### <span data-ttu-id="4d3e4-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="4d3e4-113">-Account</span></span>
<span data-ttu-id="4d3e4-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="4d3e4-115">-Concurrency</span></span>
<span data-ttu-id="4d3e4-116">Wskazuje liczbę plików lub fragmentów, które mają być przekazywane równolegle.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="4d3e4-117">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemowych.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="4d3e4-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="4d3e4-119">Wskazuje maksymalną liczbę plików do przesłania równolegle w celu przekazania folderu.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-119">Indicates the maximum number of files to upload in parallel for a folder upload.</span></span>  <span data-ttu-id="4d3e4-120">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie rozmiaru folderu i pliku</span><span class="sxs-lookup"><span data-stu-id="4d3e4-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3e4-121">-DefaultProfile</span></span>
<span data-ttu-id="4d3e4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-123">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="4d3e4-123">-Destination</span></span>
<span data-ttu-id="4d3e4-124">Określa ścieżkę usługi Data Lake Store, do której ma zostać przekazany plik lub folder, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="4d3e4-124">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="4d3e4-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="4d3e4-126">Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="4d3e4-127">Błąd domyślny.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="4d3e4-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="4d3e4-129">Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="4d3e4-130">-Force</span></span>
<span data-ttu-id="4d3e4-131">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-132">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="4d3e4-132">-ForceBinary</span></span>
<span data-ttu-id="4d3e4-133">Wskazuje, że kopiowane pliki powinny być kopiowane bez obawy o zachowanie nowych wierszy po dołączaniu.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-133">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-134">-Path</span><span class="sxs-lookup"><span data-stu-id="4d3e4-134">-Path</span></span>
<span data-ttu-id="4d3e4-135">Określa ścieżkę lokalną pliku lub folderu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-135">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-136">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="4d3e4-136">-PerFileThreadCount</span></span>
<span data-ttu-id="4d3e4-137">Wskazuje maksymalną liczbę wątków, które mają być używane dla pliku.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-137">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="4d3e4-138">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie rozmiaru folderu i pliku</span><span class="sxs-lookup"><span data-stu-id="4d3e4-138">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-139">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="4d3e4-139">-Recurse</span></span>
<span data-ttu-id="4d3e4-140">Wskazuje, że ta operacja powinna przekazać wszystkie elementy we wszystkich podfolderach.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-140">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-141">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="4d3e4-141">-Resume</span></span>
<span data-ttu-id="4d3e4-142">Wskazuje, że kopiowane pliki są kontynuacją wcześniejszego przekazania.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-142">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="4d3e4-143">Spowoduje to, że system będzie próbował wznowić pracę z ostatniego pliku, który nie został w pełni przekazany.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-143">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d3e4-144">-Confirm</span></span>
<span data-ttu-id="4d3e4-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d3e4-146">-WhatIf</span></span>
<span data-ttu-id="4d3e4-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d3e4-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3e4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3e4-149">CommonParameters</span></span>
<span data-ttu-id="4d3e4-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3e4-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d3e4-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3e4-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d3e4-152">INPUTS</span></span>

### <span data-ttu-id="4d3e4-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4d3e4-153">None</span></span>
<span data-ttu-id="4d3e4-154">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d3e4-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d3e4-155">OUTPUTS</span></span>

### <span data-ttu-id="4d3e4-156">ciąg</span><span class="sxs-lookup"><span data-stu-id="4d3e4-156">string</span></span>
<span data-ttu-id="4d3e4-157">Pełna ścieżka konta usługi Data Lake Store do przekazanego pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="4d3e4-157">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="4d3e4-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d3e4-158">NOTES</span></span>

## <span data-ttu-id="4d3e4-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d3e4-159">RELATED LINKS</span></span>

[<span data-ttu-id="4d3e4-160">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d3e4-160">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4d3e4-161">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d3e4-161">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4d3e4-162">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d3e4-162">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4d3e4-163">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d3e4-163">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4d3e4-164">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d3e4-164">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4d3e4-165">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d3e4-165">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4d3e4-166">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d3e4-166">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


