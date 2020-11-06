---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551060"
---
# <span data-ttu-id="e2e53-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2e53-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="e2e53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2e53-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e53-103">Pobiera plik z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e2e53-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2e53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2e53-104">SYNTAX</span></span>

### <span data-ttu-id="e2e53-105">Brak rejestrowania diagnostycznego (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e2e53-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2e53-106">Uwzględnij rejestrowanie diagnostyczne</span><span class="sxs-lookup"><span data-stu-id="e2e53-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e53-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e2e53-107">DESCRIPTION</span></span>
<span data-ttu-id="e2e53-108">Polecenie cmdlet **Export-AzureRmDataLakeStoreItem** pobiera plik z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e2e53-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="e2e53-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2e53-109">EXAMPLES</span></span>

### <span data-ttu-id="e2e53-110">Przykład 1: pobieranie elementu z usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e2e53-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="e2e53-111">To polecenie umożliwia pobranie pliku TestSource.csv z usługi Data Lake Store w celu C:\Test.csv.</span><span class="sxs-lookup"><span data-stu-id="e2e53-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="e2e53-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2e53-112">PARAMETERS</span></span>

### <span data-ttu-id="e2e53-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="e2e53-113">-Account</span></span>
<span data-ttu-id="e2e53-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e2e53-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e2e53-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="e2e53-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="e2e53-116">Określa maksymalną liczbę plików do pobrania równolegle w celu pobrania folderu.</span><span class="sxs-lookup"><span data-stu-id="e2e53-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="e2e53-117">Wartość domyślna to pięć (5).</span><span class="sxs-lookup"><span data-stu-id="e2e53-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e53-118">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="e2e53-118">-Destination</span></span>
<span data-ttu-id="e2e53-119">Określa ścieżkę pliku lokalnego, do którego ma zostać pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="e2e53-119">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="e2e53-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="e2e53-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="e2e53-121">Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="e2e53-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="e2e53-122">Błąd domyślny.</span><span class="sxs-lookup"><span data-stu-id="e2e53-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e53-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="e2e53-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="e2e53-124">Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="e2e53-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e53-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e2e53-125">-Force</span></span>
<span data-ttu-id="e2e53-126">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="e2e53-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="e2e53-127">-Path</span><span class="sxs-lookup"><span data-stu-id="e2e53-127">-Path</span></span>
<span data-ttu-id="e2e53-128">Określa ścieżkę elementu, który należy pobrać z usługi Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="e2e53-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="e2e53-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="e2e53-129">-PerFileThreadCount</span></span>
<span data-ttu-id="e2e53-130">Określa maksymalną liczbę wątków, które mają być używane dla pliku.</span><span class="sxs-lookup"><span data-stu-id="e2e53-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="e2e53-131">Wartość domyślna to dziesięć (10).</span><span class="sxs-lookup"><span data-stu-id="e2e53-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e53-132">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="e2e53-132">-Recurse</span></span>
<span data-ttu-id="e2e53-133">Wskazuje, że pobieranie folderu jest cykliczne.</span><span class="sxs-lookup"><span data-stu-id="e2e53-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="e2e53-134">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="e2e53-134">-Resume</span></span>
<span data-ttu-id="e2e53-135">Wskazuje, że kopiowany plik lub pliki są kontynuacją wcześniejszego pobrania.</span><span class="sxs-lookup"><span data-stu-id="e2e53-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="e2e53-136">Pobieranie próbuje wznowić pracę z ostatniego pliku, który nie został w pełni pobrany.</span><span class="sxs-lookup"><span data-stu-id="e2e53-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="e2e53-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2e53-137">-Confirm</span></span>
<span data-ttu-id="e2e53-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2e53-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2e53-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e53-139">-WhatIf</span></span>
<span data-ttu-id="e2e53-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2e53-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2e53-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2e53-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2e53-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e53-142">-DefaultProfile</span></span>
<span data-ttu-id="e2e53-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e53-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2e53-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e53-144">CommonParameters</span></span>
<span data-ttu-id="e2e53-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e53-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e53-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e53-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e53-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2e53-147">INPUTS</span></span>

## <span data-ttu-id="e2e53-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2e53-148">OUTPUTS</span></span>

### <span data-ttu-id="e2e53-149">ciąg</span><span class="sxs-lookup"><span data-stu-id="e2e53-149">string</span></span>
<span data-ttu-id="e2e53-150">Ścieżka do pliku lub folderu, do którego został pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="e2e53-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="e2e53-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2e53-151">NOTES</span></span>

## <span data-ttu-id="e2e53-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2e53-152">RELATED LINKS</span></span>

[<span data-ttu-id="e2e53-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2e53-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2e53-154">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2e53-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2e53-155">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2e53-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2e53-156">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2e53-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2e53-157">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2e53-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2e53-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2e53-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2e53-159">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2e53-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


