---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: e0bac2f22249b27442c75da7879f6a6cf85e7da7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049476"
---
# <span data-ttu-id="bb581-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bb581-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="bb581-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb581-102">SYNOPSIS</span></span>
<span data-ttu-id="bb581-103">Pobiera plik z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bb581-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="bb581-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb581-104">SYNTAX</span></span>

### <span data-ttu-id="bb581-105">NoDiagnosticLogging (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb581-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb581-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="bb581-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb581-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bb581-107">DESCRIPTION</span></span>
<span data-ttu-id="bb581-108">Polecenie cmdlet **Export-AzDataLakeStoreItem** pobiera plik z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bb581-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="bb581-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb581-109">EXAMPLES</span></span>

### <span data-ttu-id="bb581-110">Przykład 1: pobieranie elementu z usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bb581-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="bb581-111">To polecenie pobiera plik TestSource.csv z usługi Data Lake Store, aby C:\Test.csv z współbieżnością liczby 4.</span><span class="sxs-lookup"><span data-stu-id="bb581-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="bb581-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb581-112">PARAMETERS</span></span>

### <span data-ttu-id="bb581-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="bb581-113">-Account</span></span>
<span data-ttu-id="bb581-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bb581-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="bb581-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="bb581-115">-Concurrency</span></span>
<span data-ttu-id="bb581-116">Wskazuje liczbę plików lub fragmentów, które mają zostać pobrane równolegle.</span><span class="sxs-lookup"><span data-stu-id="bb581-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="bb581-117">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemowych.</span><span class="sxs-lookup"><span data-stu-id="bb581-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="bb581-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb581-118">-DefaultProfile</span></span>
<span data-ttu-id="bb581-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb581-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb581-120">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="bb581-120">-Destination</span></span>
<span data-ttu-id="bb581-121">Określa ścieżkę pliku lokalnego, do którego ma zostać pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="bb581-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="bb581-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="bb581-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="bb581-123">Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="bb581-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="bb581-124">Błąd domyślny.</span><span class="sxs-lookup"><span data-stu-id="bb581-124">Default is Error.</span></span>

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

### <span data-ttu-id="bb581-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="bb581-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="bb581-126">Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="bb581-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="bb581-127">-Force</span><span class="sxs-lookup"><span data-stu-id="bb581-127">-Force</span></span>
<span data-ttu-id="bb581-128">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="bb581-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="bb581-129">-Path</span><span class="sxs-lookup"><span data-stu-id="bb581-129">-Path</span></span>
<span data-ttu-id="bb581-130">Określa ścieżkę elementu, który należy pobrać z usługi Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="bb581-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="bb581-131">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="bb581-131">-Recurse</span></span>
<span data-ttu-id="bb581-132">Wskazuje, że pobieranie folderu jest cykliczne.</span><span class="sxs-lookup"><span data-stu-id="bb581-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="bb581-133">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="bb581-133">-Resume</span></span>
<span data-ttu-id="bb581-134">Wskazuje, że kopiowane pliki są kontynuacją wcześniejszego pobrania.</span><span class="sxs-lookup"><span data-stu-id="bb581-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="bb581-135">Spowoduje to, że system będzie próbował wznowić pracę z ostatniego pliku, który nie został w pełni pobrany.</span><span class="sxs-lookup"><span data-stu-id="bb581-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="bb581-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb581-136">-Confirm</span></span>
<span data-ttu-id="bb581-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb581-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb581-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb581-138">-WhatIf</span></span>
<span data-ttu-id="bb581-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb581-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb581-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb581-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb581-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb581-141">CommonParameters</span></span>
<span data-ttu-id="bb581-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb581-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb581-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb581-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb581-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb581-144">INPUTS</span></span>

### <span data-ttu-id="bb581-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bb581-145">System.String</span></span>

### <span data-ttu-id="bb581-146">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="bb581-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="bb581-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bb581-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bb581-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bb581-148">System.Int32</span></span>

### <span data-ttu-id="bb581-149">Microsoft. Azure. Commands. DataLakeStore. models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="bb581-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="bb581-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb581-150">OUTPUTS</span></span>

### <span data-ttu-id="bb581-151">System. String</span><span class="sxs-lookup"><span data-stu-id="bb581-151">System.String</span></span>

## <span data-ttu-id="bb581-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb581-152">NOTES</span></span>

## <span data-ttu-id="bb581-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb581-153">RELATED LINKS</span></span>

[<span data-ttu-id="bb581-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bb581-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="bb581-155">Import — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bb581-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="bb581-156">Dołącz do AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bb581-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="bb581-157">Przenieś — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bb581-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="bb581-158">Nowe — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bb581-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="bb581-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bb581-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="bb581-160">Test — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bb581-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


