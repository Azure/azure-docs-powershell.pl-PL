---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223129"
---
# <span data-ttu-id="6745f-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6745f-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="6745f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6745f-102">SYNOPSIS</span></span>
<span data-ttu-id="6745f-103">Umożliwia przekazywanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6745f-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="6745f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6745f-104">SYNTAX</span></span>

### <span data-ttu-id="6745f-105">NoDiagnosticLogging (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6745f-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6745f-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="6745f-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6745f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6745f-107">DESCRIPTION</span></span>
<span data-ttu-id="6745f-108">Polecenie cmdlet **Import-AzDataLakeStoreItem** umożliwia przekazanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6745f-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="6745f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6745f-109">EXAMPLES</span></span>

### <span data-ttu-id="6745f-110">Przykład 1: przekazywanie pliku</span><span class="sxs-lookup"><span data-stu-id="6745f-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="6745f-111">To polecenie umożliwia przekazywanie pliku SrcFile.csv i dodanie go do folderu Moje pliki w usłudze Data Lake Store jako File.csv z współbieżnością równą 4.</span><span class="sxs-lookup"><span data-stu-id="6745f-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="6745f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6745f-112">PARAMETERS</span></span>

### <span data-ttu-id="6745f-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="6745f-113">-Account</span></span>
<span data-ttu-id="6745f-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6745f-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6745f-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="6745f-115">-Concurrency</span></span>
<span data-ttu-id="6745f-116">Wskazuje liczbę plików lub fragmentów, które mają być przekazywane równolegle.</span><span class="sxs-lookup"><span data-stu-id="6745f-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="6745f-117">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemowych.</span><span class="sxs-lookup"><span data-stu-id="6745f-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="6745f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6745f-118">-DefaultProfile</span></span>
<span data-ttu-id="6745f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6745f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6745f-120">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="6745f-120">-Destination</span></span>
<span data-ttu-id="6745f-121">Określa ścieżkę usługi Data Lake Store, do której ma zostać przekazany plik lub folder, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="6745f-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6745f-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="6745f-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="6745f-123">Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="6745f-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="6745f-124">Błąd domyślny.</span><span class="sxs-lookup"><span data-stu-id="6745f-124">Default is Error.</span></span>

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

### <span data-ttu-id="6745f-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="6745f-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="6745f-126">Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="6745f-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="6745f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="6745f-127">-Force</span></span>
<span data-ttu-id="6745f-128">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="6745f-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="6745f-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="6745f-129">-ForceBinary</span></span>
<span data-ttu-id="6745f-130">Wskazuje, że kopiowane pliki powinny być kopiowane bez obawy o zachowanie nowych wierszy po dołączaniu.</span><span class="sxs-lookup"><span data-stu-id="6745f-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="6745f-131">-Path</span><span class="sxs-lookup"><span data-stu-id="6745f-131">-Path</span></span>
<span data-ttu-id="6745f-132">Określa ścieżkę lokalną pliku lub folderu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="6745f-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="6745f-133">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="6745f-133">-Recurse</span></span>
<span data-ttu-id="6745f-134">Wskazuje, że ta operacja powinna przekazać wszystkie elementy we wszystkich podfolderach.</span><span class="sxs-lookup"><span data-stu-id="6745f-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="6745f-135">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="6745f-135">-Resume</span></span>
<span data-ttu-id="6745f-136">Wskazuje, że kopiowane pliki są kontynuacją wcześniejszego przekazania.</span><span class="sxs-lookup"><span data-stu-id="6745f-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="6745f-137">Spowoduje to, że system będzie próbował wznowić pracę z ostatniego pliku, który nie został w pełni przekazany.</span><span class="sxs-lookup"><span data-stu-id="6745f-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="6745f-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6745f-138">-Confirm</span></span>
<span data-ttu-id="6745f-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6745f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6745f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6745f-140">-WhatIf</span></span>
<span data-ttu-id="6745f-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6745f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6745f-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6745f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6745f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6745f-143">CommonParameters</span></span>
<span data-ttu-id="6745f-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6745f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6745f-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6745f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6745f-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6745f-146">INPUTS</span></span>

### <span data-ttu-id="6745f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6745f-147">System.String</span></span>

### <span data-ttu-id="6745f-148">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6745f-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6745f-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6745f-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6745f-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6745f-150">System.Int32</span></span>

### <span data-ttu-id="6745f-151">Microsoft. Azure. Commands. DataLakeStore. models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="6745f-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="6745f-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6745f-152">OUTPUTS</span></span>

### <span data-ttu-id="6745f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="6745f-153">System.String</span></span>

## <span data-ttu-id="6745f-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6745f-154">NOTES</span></span>

## <span data-ttu-id="6745f-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6745f-155">RELATED LINKS</span></span>

[<span data-ttu-id="6745f-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6745f-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="6745f-157">Eksportowanie — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6745f-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="6745f-158">Dołącz do AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6745f-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="6745f-159">Przenieś — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6745f-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="6745f-160">Nowe — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6745f-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="6745f-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6745f-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="6745f-162">Test — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6745f-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


