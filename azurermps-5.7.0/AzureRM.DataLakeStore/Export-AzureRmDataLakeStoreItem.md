---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 907e4e92b511349011b27cb8aaf7588b8e495220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716844"
---
# <span data-ttu-id="27808-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="27808-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="27808-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27808-102">SYNOPSIS</span></span>
<span data-ttu-id="27808-103">Pobiera plik z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="27808-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27808-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27808-104">SYNTAX</span></span>

### <span data-ttu-id="27808-105">NoDiagnosticLogging (domyślny)</span><span class="sxs-lookup"><span data-stu-id="27808-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27808-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="27808-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27808-107">Opis</span><span class="sxs-lookup"><span data-stu-id="27808-107">DESCRIPTION</span></span>
<span data-ttu-id="27808-108">Polecenie cmdlet **Export-AzureRmDataLakeStoreItem** pobiera plik z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="27808-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="27808-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27808-109">EXAMPLES</span></span>

### <span data-ttu-id="27808-110">Przykład 1: pobieranie elementu z usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="27808-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="27808-111">To polecenie pobiera plik TestSource.csv z usługi Data Lake Store, aby C:\Test.csv z współbieżnością liczby 4.</span><span class="sxs-lookup"><span data-stu-id="27808-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="27808-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27808-112">PARAMETERS</span></span>

### <span data-ttu-id="27808-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="27808-113">-Account</span></span>
<span data-ttu-id="27808-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="27808-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="27808-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="27808-115">-Concurrency</span></span>
<span data-ttu-id="27808-116">Wskazuje liczbę plików lub fragmentów, które mają zostać pobrane równolegle.</span><span class="sxs-lookup"><span data-stu-id="27808-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="27808-117">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemowych.</span><span class="sxs-lookup"><span data-stu-id="27808-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27808-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="27808-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="27808-119">Wskazuje maksymalną liczbę plików do pobrania równolegle w celu pobrania folderu.</span><span class="sxs-lookup"><span data-stu-id="27808-119">Indicates the maximum number of files to download in parallel for a folder download.</span></span>  <span data-ttu-id="27808-120">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie rozmiaru folderu i pliku</span><span class="sxs-lookup"><span data-stu-id="27808-120">Default will be computed as a best effort based on folder and file size</span></span>

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

### <span data-ttu-id="27808-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27808-121">-DefaultProfile</span></span>
<span data-ttu-id="27808-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27808-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27808-123">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="27808-123">-Destination</span></span>
<span data-ttu-id="27808-124">Określa ścieżkę pliku lokalnego, do którego ma zostać pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="27808-124">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27808-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="27808-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="27808-126">Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="27808-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="27808-127">Błąd domyślny.</span><span class="sxs-lookup"><span data-stu-id="27808-127">Default is Error.</span></span>

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

### <span data-ttu-id="27808-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="27808-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="27808-129">Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="27808-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="27808-130">-Force</span><span class="sxs-lookup"><span data-stu-id="27808-130">-Force</span></span>
<span data-ttu-id="27808-131">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="27808-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27808-132">-Path</span><span class="sxs-lookup"><span data-stu-id="27808-132">-Path</span></span>
<span data-ttu-id="27808-133">Określa ścieżkę elementu, który należy pobrać z usługi Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="27808-133">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27808-134">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="27808-134">-PerFileThreadCount</span></span>
<span data-ttu-id="27808-135">Wskazuje maksymalną liczbę wątków, które mają być używane dla pliku.</span><span class="sxs-lookup"><span data-stu-id="27808-135">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="27808-136">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie rozmiaru folderu i pliku</span><span class="sxs-lookup"><span data-stu-id="27808-136">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27808-137">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="27808-137">-Recurse</span></span>
<span data-ttu-id="27808-138">Wskazuje, że pobieranie folderu jest cykliczne.</span><span class="sxs-lookup"><span data-stu-id="27808-138">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="27808-139">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="27808-139">-Resume</span></span>
<span data-ttu-id="27808-140">Wskazuje, że kopiowane pliki są kontynuacją wcześniejszego pobrania.</span><span class="sxs-lookup"><span data-stu-id="27808-140">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="27808-141">Spowoduje to, że system będzie próbował wznowić pracę z ostatniego pliku, który nie został w pełni pobrany.</span><span class="sxs-lookup"><span data-stu-id="27808-141">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="27808-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27808-142">-Confirm</span></span>
<span data-ttu-id="27808-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27808-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27808-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27808-144">-WhatIf</span></span>
<span data-ttu-id="27808-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27808-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27808-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="27808-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27808-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27808-147">CommonParameters</span></span>
<span data-ttu-id="27808-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27808-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27808-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27808-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27808-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27808-150">INPUTS</span></span>

### <span data-ttu-id="27808-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="27808-151">None</span></span>
<span data-ttu-id="27808-152">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="27808-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27808-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27808-153">OUTPUTS</span></span>

### <span data-ttu-id="27808-154">ciąg</span><span class="sxs-lookup"><span data-stu-id="27808-154">string</span></span>
<span data-ttu-id="27808-155">Ścieżka do pliku lub folderu, do którego został pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="27808-155">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="27808-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27808-156">NOTES</span></span>

## <span data-ttu-id="27808-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27808-157">RELATED LINKS</span></span>

[<span data-ttu-id="27808-158">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="27808-158">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="27808-159">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="27808-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="27808-160">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="27808-160">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="27808-161">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="27808-161">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="27808-162">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="27808-162">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="27808-163">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="27808-163">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="27808-164">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="27808-164">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


