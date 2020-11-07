---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718215"
---
# <span data-ttu-id="12fcc-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="12fcc-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="12fcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="12fcc-103">Umożliwia przekazywanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="12fcc-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12fcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12fcc-104">SYNTAX</span></span>

### <span data-ttu-id="12fcc-105">Brak rejestrowania diagnostycznego (domyślne)</span><span class="sxs-lookup"><span data-stu-id="12fcc-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fcc-106">Uwzględnij rejestrowanie diagnostyczne</span><span class="sxs-lookup"><span data-stu-id="12fcc-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12fcc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="12fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="12fcc-108">Polecenie cmdlet **Import-AzureRmDataLakeStoreItem** umożliwia przekazanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="12fcc-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="12fcc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12fcc-109">EXAMPLES</span></span>

### <span data-ttu-id="12fcc-110">Przykład 1: przekazywanie pliku</span><span class="sxs-lookup"><span data-stu-id="12fcc-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="12fcc-111">To polecenie umożliwia przekazywanie pliku SrcFile.csv i dodanie go do folderu Moje pliki w usłudze Data Lake Store jako File.csv.</span><span class="sxs-lookup"><span data-stu-id="12fcc-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="12fcc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12fcc-112">PARAMETERS</span></span>

### <span data-ttu-id="12fcc-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="12fcc-113">-Account</span></span>
<span data-ttu-id="12fcc-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="12fcc-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="12fcc-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="12fcc-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="12fcc-116">Umożliwia określenie maksymalnej liczby plików do przekazania równolegle w celu przekazania folderu.</span><span class="sxs-lookup"><span data-stu-id="12fcc-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="12fcc-117">Wartość domyślna to pięć (5).</span><span class="sxs-lookup"><span data-stu-id="12fcc-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12fcc-118">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="12fcc-118">-Destination</span></span>
<span data-ttu-id="12fcc-119">Określa ścieżkę usługi Data Lake Store, do której ma zostać przekazany plik lub folder, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="12fcc-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="12fcc-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="12fcc-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="12fcc-121">Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="12fcc-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="12fcc-122">Błąd domyślny.</span><span class="sxs-lookup"><span data-stu-id="12fcc-122">Default is Error.</span></span>

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

### <span data-ttu-id="12fcc-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="12fcc-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="12fcc-124">Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="12fcc-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="12fcc-125">-Force</span><span class="sxs-lookup"><span data-stu-id="12fcc-125">-Force</span></span>
<span data-ttu-id="12fcc-126">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="12fcc-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="12fcc-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="12fcc-127">-ForceBinary</span></span>
<span data-ttu-id="12fcc-128">Wskazuje, że ta operacja przekazuje plik jako plik binarny.</span><span class="sxs-lookup"><span data-stu-id="12fcc-128">Indicates that this operation uploads the file as a binary file.</span></span>

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

### <span data-ttu-id="12fcc-129">-Path</span><span class="sxs-lookup"><span data-stu-id="12fcc-129">-Path</span></span>
<span data-ttu-id="12fcc-130">Określa ścieżkę lokalną pliku lub folderu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="12fcc-130">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="12fcc-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="12fcc-131">-PerFileThreadCount</span></span>
<span data-ttu-id="12fcc-132">Określa maksymalną liczbę wątków, które mają być używane dla pliku.</span><span class="sxs-lookup"><span data-stu-id="12fcc-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="12fcc-133">Wartość domyślna to dziesięć (10).</span><span class="sxs-lookup"><span data-stu-id="12fcc-133">The default value is ten (10).</span></span>

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

### <span data-ttu-id="12fcc-134">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="12fcc-134">-Recurse</span></span>
<span data-ttu-id="12fcc-135">Wskazuje, że ta operacja powinna przekazać wszystkie elementy we wszystkich podfolderach.</span><span class="sxs-lookup"><span data-stu-id="12fcc-135">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="12fcc-136">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="12fcc-136">-Resume</span></span>
<span data-ttu-id="12fcc-137">Wskazuje, że ta operacja powinna wznowić anulowaną wcześniej operację przekazywania lub nieudaną.</span><span class="sxs-lookup"><span data-stu-id="12fcc-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

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

### <span data-ttu-id="12fcc-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12fcc-138">-Confirm</span></span>
<span data-ttu-id="12fcc-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fcc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12fcc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fcc-140">-WhatIf</span></span>
<span data-ttu-id="12fcc-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fcc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12fcc-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12fcc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12fcc-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fcc-143">-DefaultProfile</span></span>
<span data-ttu-id="12fcc-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12fcc-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12fcc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fcc-145">CommonParameters</span></span>
<span data-ttu-id="12fcc-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12fcc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fcc-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12fcc-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fcc-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12fcc-148">INPUTS</span></span>

## <span data-ttu-id="12fcc-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12fcc-149">OUTPUTS</span></span>

### <span data-ttu-id="12fcc-150">ciąg</span><span class="sxs-lookup"><span data-stu-id="12fcc-150">string</span></span>
<span data-ttu-id="12fcc-151">Pełna ścieżka konta usługi Data Lake Store do przekazanego pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="12fcc-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="12fcc-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12fcc-152">NOTES</span></span>

## <span data-ttu-id="12fcc-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12fcc-153">RELATED LINKS</span></span>

[<span data-ttu-id="12fcc-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="12fcc-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="12fcc-155">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="12fcc-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="12fcc-156">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="12fcc-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="12fcc-157">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="12fcc-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="12fcc-158">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="12fcc-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="12fcc-159">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="12fcc-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="12fcc-160">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="12fcc-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


