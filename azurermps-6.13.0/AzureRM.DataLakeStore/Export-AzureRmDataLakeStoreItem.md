---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 508a7619374b7e245b8df99c929f161ce1966288
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548720"
---
# <span data-ttu-id="5ba6c-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ba6c-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5ba6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ba6c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba6c-103">Pobiera plik z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ba6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ba6c-104">SYNTAX</span></span>

### <span data-ttu-id="5ba6c-105">NoDiagnosticLogging (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ba6c-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ba6c-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="5ba6c-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ba6c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5ba6c-107">DESCRIPTION</span></span>
<span data-ttu-id="5ba6c-108">Polecenie cmdlet **Export-AzureRmDataLakeStoreItem** pobiera plik z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="5ba6c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ba6c-109">EXAMPLES</span></span>

### <span data-ttu-id="5ba6c-110">Przykład 1: pobieranie elementu z usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="5ba6c-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="5ba6c-111">To polecenie pobiera plik TestSource.csv z usługi Data Lake Store, aby C:\Test.csv z współbieżnością liczby 4.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="5ba6c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ba6c-112">PARAMETERS</span></span>

### <span data-ttu-id="5ba6c-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="5ba6c-113">-Account</span></span>
<span data-ttu-id="5ba6c-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5ba6c-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="5ba6c-115">-Concurrency</span></span>
<span data-ttu-id="5ba6c-116">Wskazuje liczbę plików lub fragmentów, które mają zostać pobrane równolegle.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="5ba6c-117">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemowych.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="5ba6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba6c-118">-DefaultProfile</span></span>
<span data-ttu-id="5ba6c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ba6c-120">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="5ba6c-120">-Destination</span></span>
<span data-ttu-id="5ba6c-121">Określa ścieżkę pliku lokalnego, do którego ma zostać pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="5ba6c-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="5ba6c-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="5ba6c-123">Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="5ba6c-124">Błąd domyślny.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-124">Default is Error.</span></span>

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

### <span data-ttu-id="5ba6c-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="5ba6c-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="5ba6c-126">Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="5ba6c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5ba6c-127">-Force</span></span>
<span data-ttu-id="5ba6c-128">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="5ba6c-129">-Path</span><span class="sxs-lookup"><span data-stu-id="5ba6c-129">-Path</span></span>
<span data-ttu-id="5ba6c-130">Określa ścieżkę elementu, który należy pobrać z usługi Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="5ba6c-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="5ba6c-131">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="5ba6c-131">-Recurse</span></span>
<span data-ttu-id="5ba6c-132">Wskazuje, że pobieranie folderu jest cykliczne.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="5ba6c-133">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="5ba6c-133">-Resume</span></span>
<span data-ttu-id="5ba6c-134">Wskazuje, że kopiowane pliki są kontynuacją wcześniejszego pobrania.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="5ba6c-135">Spowoduje to, że system będzie próbował wznowić pracę z ostatniego pliku, który nie został w pełni pobrany.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="5ba6c-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ba6c-136">-Confirm</span></span>
<span data-ttu-id="5ba6c-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ba6c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ba6c-138">-WhatIf</span></span>
<span data-ttu-id="5ba6c-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ba6c-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ba6c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba6c-141">CommonParameters</span></span>
<span data-ttu-id="5ba6c-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba6c-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba6c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba6c-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ba6c-144">INPUTS</span></span>

### <span data-ttu-id="5ba6c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5ba6c-145">System.String</span></span>

### <span data-ttu-id="5ba6c-146">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5ba6c-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5ba6c-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ba6c-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5ba6c-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5ba6c-148">System.Int32</span></span>

### <span data-ttu-id="5ba6c-149">Microsoft. Azure. Commands. DataLakeStore. models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="5ba6c-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="5ba6c-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ba6c-150">OUTPUTS</span></span>

### <span data-ttu-id="5ba6c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5ba6c-151">System.String</span></span>
<span data-ttu-id="5ba6c-152">Ścieżka do pliku lub folderu, do którego został pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="5ba6c-152">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="5ba6c-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ba6c-153">NOTES</span></span>

## <span data-ttu-id="5ba6c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ba6c-154">RELATED LINKS</span></span>

[<span data-ttu-id="5ba6c-155">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ba6c-155">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ba6c-156">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ba6c-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ba6c-157">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ba6c-157">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ba6c-158">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ba6c-158">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ba6c-159">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ba6c-159">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ba6c-160">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ba6c-160">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ba6c-161">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ba6c-161">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


