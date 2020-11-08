---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054648"
---
# <span data-ttu-id="47f98-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="47f98-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="47f98-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47f98-102">SYNOPSIS</span></span>
<span data-ttu-id="47f98-103">Włącza diagnostykę aplikacji w witrynie usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="47f98-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="47f98-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47f98-104">SYNTAX</span></span>

### <span data-ttu-id="47f98-105">FileParameterSet</span><span class="sxs-lookup"><span data-stu-id="47f98-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="47f98-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="47f98-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="47f98-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="47f98-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47f98-108">Opis</span><span class="sxs-lookup"><span data-stu-id="47f98-108">DESCRIPTION</span></span>
<span data-ttu-id="47f98-109">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47f98-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="47f98-110">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="47f98-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="47f98-111">Włącza program Application Diagnostics w witrynie sieci Web platformy Azure i umożliwia konfigurowanie magazynu dzienników w systemie plików lub usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="47f98-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="47f98-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47f98-112">EXAMPLES</span></span>

### <span data-ttu-id="47f98-113">Przykład 1: Włączanie diagnostyki za pomocą systemu plików</span><span class="sxs-lookup"><span data-stu-id="47f98-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="47f98-114">W tym przykładzie można włączyć rejestrowanie aplikacji w systemie plików z pełnym poziomem szczegółowości.</span><span class="sxs-lookup"><span data-stu-id="47f98-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="47f98-115">Przykład 2: Włączanie rejestrowania za pomocą usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="47f98-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="47f98-116">W tym przykładzie można włączyć rejestrowanie aplikacji, korzystając z konta magazynu o nazwie Moje konto z ustawionym ustawieniem informacje.</span><span class="sxs-lookup"><span data-stu-id="47f98-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="47f98-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47f98-117">PARAMETERS</span></span>

### <span data-ttu-id="47f98-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="47f98-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-119">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="47f98-119">-File</span></span>
<span data-ttu-id="47f98-120">Określa, że chcesz używać systemu plików do przechowywania plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="47f98-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="47f98-121">-LogLevel</span></span>
<span data-ttu-id="47f98-122">Poziom dziennika do przechowywania.</span><span class="sxs-lookup"><span data-stu-id="47f98-122">The log level to store.</span></span>
<span data-ttu-id="47f98-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="47f98-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47f98-124">Błędów</span><span class="sxs-lookup"><span data-stu-id="47f98-124">Error</span></span>
- <span data-ttu-id="47f98-125">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="47f98-125">Warning</span></span>
- <span data-ttu-id="47f98-126">Dotyczących</span><span class="sxs-lookup"><span data-stu-id="47f98-126">Information</span></span>
- <span data-ttu-id="47f98-127">Pełne</span><span class="sxs-lookup"><span data-stu-id="47f98-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47f98-128">-Name</span></span>
<span data-ttu-id="47f98-129">Określa nazwę witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="47f98-129">Specifies the name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47f98-130">-PassThru</span></span>
<span data-ttu-id="47f98-131">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="47f98-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="47f98-132">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="47f98-132">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="47f98-133">-Profile</span></span>
<span data-ttu-id="47f98-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47f98-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="47f98-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="47f98-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="47f98-136">-Slot</span></span>
<span data-ttu-id="47f98-137">Określa nazwę gniazda.</span><span class="sxs-lookup"><span data-stu-id="47f98-137">Specifies the name of the slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="47f98-138">-StorageAccountName</span></span>
<span data-ttu-id="47f98-139">Konto magazynu, w którym mają być przechowywane dzienniki.</span><span class="sxs-lookup"><span data-stu-id="47f98-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="47f98-140">Jeśli nie określono tego parametru, używana jest CurrentStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="47f98-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="47f98-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="47f98-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-143">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="47f98-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f98-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f98-144">CommonParameters</span></span>
<span data-ttu-id="47f98-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47f98-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f98-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47f98-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f98-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47f98-147">INPUTS</span></span>

## <span data-ttu-id="47f98-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47f98-148">OUTPUTS</span></span>

## <span data-ttu-id="47f98-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47f98-149">NOTES</span></span>

## <span data-ttu-id="47f98-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47f98-150">RELATED LINKS</span></span>

[<span data-ttu-id="47f98-151">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="47f98-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="47f98-152">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="47f98-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="47f98-153">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="47f98-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="47f98-154">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="47f98-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="47f98-155">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="47f98-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


