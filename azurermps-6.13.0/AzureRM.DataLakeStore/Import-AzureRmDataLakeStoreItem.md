---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 91e7969600f387a95f46cad02f87cf6466f2c642
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541720"
---
# <span data-ttu-id="4725a-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4725a-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="4725a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4725a-102">SYNOPSIS</span></span>
<span data-ttu-id="4725a-103">Umożliwia przekazywanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4725a-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4725a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4725a-104">SYNTAX</span></span>

### <span data-ttu-id="4725a-105">NoDiagnosticLogging (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4725a-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4725a-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="4725a-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4725a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4725a-107">DESCRIPTION</span></span>
<span data-ttu-id="4725a-108">Polecenie cmdlet **Import-AzureRmDataLakeStoreItem** umożliwia przekazanie lokalnego pliku lub katalogu do usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4725a-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="4725a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4725a-109">EXAMPLES</span></span>

### <span data-ttu-id="4725a-110">Przykład 1: przekazywanie pliku</span><span class="sxs-lookup"><span data-stu-id="4725a-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="4725a-111">To polecenie umożliwia przekazywanie pliku SrcFile.csv i dodanie go do folderu Moje pliki w usłudze Data Lake Store jako File.csv z współbieżnością równą 4.</span><span class="sxs-lookup"><span data-stu-id="4725a-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="4725a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4725a-112">PARAMETERS</span></span>

### <span data-ttu-id="4725a-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="4725a-113">-Account</span></span>
<span data-ttu-id="4725a-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4725a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4725a-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="4725a-115">-Concurrency</span></span>
<span data-ttu-id="4725a-116">Wskazuje liczbę plików lub fragmentów, które mają być przekazywane równolegle.</span><span class="sxs-lookup"><span data-stu-id="4725a-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="4725a-117">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemowych.</span><span class="sxs-lookup"><span data-stu-id="4725a-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="4725a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4725a-118">-DefaultProfile</span></span>
<span data-ttu-id="4725a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4725a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4725a-120">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="4725a-120">-Destination</span></span>
<span data-ttu-id="4725a-121">Określa ścieżkę usługi Data Lake Store, do której ma zostać przekazany plik lub folder, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="4725a-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4725a-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="4725a-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="4725a-123">Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="4725a-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="4725a-124">Błąd domyślny.</span><span class="sxs-lookup"><span data-stu-id="4725a-124">Default is Error.</span></span>

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

### <span data-ttu-id="4725a-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="4725a-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="4725a-126">Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="4725a-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="4725a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="4725a-127">-Force</span></span>
<span data-ttu-id="4725a-128">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="4725a-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="4725a-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="4725a-129">-ForceBinary</span></span>
<span data-ttu-id="4725a-130">Wskazuje, że kopiowane pliki powinny być kopiowane bez obawy o zachowanie nowych wierszy po dołączaniu.</span><span class="sxs-lookup"><span data-stu-id="4725a-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="4725a-131">-Path</span><span class="sxs-lookup"><span data-stu-id="4725a-131">-Path</span></span>
<span data-ttu-id="4725a-132">Określa ścieżkę lokalną pliku lub folderu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="4725a-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="4725a-133">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="4725a-133">-Recurse</span></span>
<span data-ttu-id="4725a-134">Wskazuje, że ta operacja powinna przekazać wszystkie elementy we wszystkich podfolderach.</span><span class="sxs-lookup"><span data-stu-id="4725a-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="4725a-135">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="4725a-135">-Resume</span></span>
<span data-ttu-id="4725a-136">Wskazuje, że kopiowane pliki są kontynuacją wcześniejszego przekazania.</span><span class="sxs-lookup"><span data-stu-id="4725a-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="4725a-137">Spowoduje to, że system będzie próbował wznowić pracę z ostatniego pliku, który nie został w pełni przekazany.</span><span class="sxs-lookup"><span data-stu-id="4725a-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="4725a-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4725a-138">-Confirm</span></span>
<span data-ttu-id="4725a-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4725a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4725a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4725a-140">-WhatIf</span></span>
<span data-ttu-id="4725a-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4725a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4725a-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4725a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4725a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4725a-143">CommonParameters</span></span>
<span data-ttu-id="4725a-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4725a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4725a-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4725a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4725a-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4725a-146">INPUTS</span></span>

### <span data-ttu-id="4725a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4725a-147">System.String</span></span>

### <span data-ttu-id="4725a-148">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4725a-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4725a-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4725a-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4725a-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4725a-150">System.Int32</span></span>

### <span data-ttu-id="4725a-151">Microsoft. Azure. Commands. DataLakeStore. models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="4725a-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="4725a-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4725a-152">OUTPUTS</span></span>

### <span data-ttu-id="4725a-153">System. String</span><span class="sxs-lookup"><span data-stu-id="4725a-153">System.String</span></span>
<span data-ttu-id="4725a-154">Pełna ścieżka konta usługi Data Lake Store do przekazanego pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="4725a-154">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="4725a-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4725a-155">NOTES</span></span>

## <span data-ttu-id="4725a-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4725a-156">RELATED LINKS</span></span>

[<span data-ttu-id="4725a-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4725a-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4725a-158">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4725a-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4725a-159">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4725a-159">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4725a-160">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4725a-160">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4725a-161">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4725a-161">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4725a-162">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4725a-162">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4725a-163">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4725a-163">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


