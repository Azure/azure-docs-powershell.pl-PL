---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
ms.openlocfilehash: a7bffb3b1387c084ef3b29ad6feb3962c724278f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542692"
---
# <span data-ttu-id="e530b-101">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e530b-101">Set-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="e530b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e530b-102">SYNOPSIS</span></span>
<span data-ttu-id="e530b-103">Konfiguruje rozszerzenie DSC na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e530b-103">Configures the DSC extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e530b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e530b-104">SYNTAX</span></span>

```
Set-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e530b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e530b-105">DESCRIPTION</span></span>
<span data-ttu-id="e530b-106">Polecenie cmdlet **Set-AzureRmVMDscExtension** konfiguruje rozszerzenie konfiguracji stanu wymaganego programu Windows PowerShell na maszynie wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e530b-106">The **Set-AzureRmVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="e530b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e530b-107">EXAMPLES</span></span>

### <span data-ttu-id="e530b-108">Przykład 1: Ustawianie rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="e530b-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="e530b-109">To polecenie ustawia rozszerzenie DSC na maszynie wirtualnej o nazwie VM07, aby pobrać Sample.ps1.zip z konta magazynu o nazwie STG i domyślnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="e530b-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="e530b-110">Polecenie wywoła konfigurację o nazwie configname.</span><span class="sxs-lookup"><span data-stu-id="e530b-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="e530b-111">Plik Sample.ps1.zip został przekazany wcześniej za pomocą polecenia **Publish-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e530b-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="e530b-112">Przykład 2: Ustawianie rozszerzenia DSC przy użyciu danych konfiguracji</span><span class="sxs-lookup"><span data-stu-id="e530b-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="e530b-113">To polecenie ustawia rozszerzenie na maszynie wirtualnej o nazwie VM13, aby pobrać Sample.ps1.zip z konta magazynu o nazwie STG i kontenera o nazwie WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="e530b-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="e530b-114">Polecenie o konfiguracji o nazwie configname i określające dane konfiguracji oraz argumenty.</span><span class="sxs-lookup"><span data-stu-id="e530b-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="e530b-115">Plik Sample.ps1.zip został przekazany wcześniej za pomocą polecenia **Publish-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e530b-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="e530b-116">Przykład 3: Ustawianie rozszerzenia DSC z danymi konfiguracji, które zawierają funkcję autoaktualizacji</span><span class="sxs-lookup"><span data-stu-id="e530b-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="e530b-117">To polecenie ustawia rozszerzenie na maszynie wirtualnej o nazwie VM22, aby pobrać Sample.ps1.zip z konta magazynu o nazwie STG i kontenera o nazwie WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="e530b-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="e530b-118">Polecenie umożliwia wywołanie konfiguracji o nazwie configname oraz określenie danych i argumentów konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e530b-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="e530b-119">To polecenie umożliwia również automatyczne aktualizowanie obsługi rozszerzeń do najnowszej wersji.</span><span class="sxs-lookup"><span data-stu-id="e530b-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="e530b-120">Sample.ps1.zip został przekazany wcześniej za pomocą polecenia **Publish-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e530b-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

## <span data-ttu-id="e530b-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e530b-121">PARAMETERS</span></span>

### <span data-ttu-id="e530b-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="e530b-122">-ArchiveBlobName</span></span>
<span data-ttu-id="e530b-123">Określa nazwę pliku konfiguracji, który został wcześniej przekazany za pomocą polecenia cmdlet Publish-AzureRmVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e530b-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzureRmVMDscConfiguration cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e530b-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="e530b-124">-ArchiveContainerName</span></span>
<span data-ttu-id="e530b-125">Nazwa gatunku kontenera usługi Azure Storage, w którym znajduje się archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e530b-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e530b-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e530b-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="e530b-127">Określa nazwę grupy zasobów zawierającej konto magazynu zawierające archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e530b-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="e530b-128">Ten parametr jest opcjonalny, jeśli konto magazynu i maszyna wirtualna są w tej samej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e530b-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="e530b-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e530b-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="e530b-130">Określa nazwę konta usługi Azure Storage, która jest używana do pobierania ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="e530b-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e530b-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e530b-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="e530b-132">Określa sufiks punktu końcowego składowania.</span><span class="sxs-lookup"><span data-stu-id="e530b-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e530b-133">-Aktualizacje automatyczne</span><span class="sxs-lookup"><span data-stu-id="e530b-133">-AutoUpdate</span></span>
<span data-ttu-id="e530b-134">Określa wersję obsługi rozszerzeń określoną przez parametr *Version* .</span><span class="sxs-lookup"><span data-stu-id="e530b-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="e530b-135">Domyślnie obsługa rozszerzeń nie jest aktualizowana.</span><span class="sxs-lookup"><span data-stu-id="e530b-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="e530b-136">Użyj parametru *AutoUpdate* , aby włączyć automatyczną aktualizację programu obsługi rozszerzeń do najnowszej wersji, gdy jest ona dostępna.</span><span class="sxs-lookup"><span data-stu-id="e530b-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="e530b-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="e530b-137">-ConfigurationArgument</span></span>
<span data-ttu-id="e530b-138">Określa tabelę skrótów zawierającą argumenty funkcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e530b-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e530b-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="e530b-139">-ConfigurationData</span></span>
<span data-ttu-id="e530b-140">Określa ścieżkę pliku psd1, który określa dane konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e530b-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="e530b-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e530b-141">-ConfigurationName</span></span>
<span data-ttu-id="e530b-142">Określa nazwę konfiguracji, jaką wywoła rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="e530b-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="e530b-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="e530b-143">-DataCollection</span></span>
<span data-ttu-id="e530b-144">Określa typ zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="e530b-144">Specifies the data collection type.</span></span>
<span data-ttu-id="e530b-145">Dopuszczalne wartości tego parametru to: enable i Disable.</span><span class="sxs-lookup"><span data-stu-id="e530b-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e530b-146">-Force</span><span class="sxs-lookup"><span data-stu-id="e530b-146">-Force</span></span>
<span data-ttu-id="e530b-147">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e530b-147">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e530b-148">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e530b-148">-Location</span></span>
<span data-ttu-id="e530b-149">Określa ścieżkę rozszerzenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="e530b-149">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="e530b-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e530b-150">-Name</span></span>
<span data-ttu-id="e530b-151">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="e530b-151">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e530b-152">Wartość domyślna to Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="e530b-152">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="e530b-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e530b-153">-ResourceGroupName</span></span>
<span data-ttu-id="e530b-154">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e530b-154">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e530b-155">-Version</span><span class="sxs-lookup"><span data-stu-id="e530b-155">-Version</span></span>
<span data-ttu-id="e530b-156">Określa wersję rozszerzenia DSC, do którego Set-AzureRmVMDscExtension zastosować ustawienia.</span><span class="sxs-lookup"><span data-stu-id="e530b-156">Specifies the version of the DSC extension that Set-AzureRmVMDscExtension applies the settings to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e530b-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="e530b-157">-VMName</span></span>
<span data-ttu-id="e530b-158">Określa nazwę maszyny wirtualnej, w której jest zainstalowany program obsługi rozszerzeń DSC.</span><span class="sxs-lookup"><span data-stu-id="e530b-158">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e530b-159">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="e530b-159">-WmfVersion</span></span>
<span data-ttu-id="e530b-160">Określa wersję WMF.</span><span class="sxs-lookup"><span data-stu-id="e530b-160">Specifies the WMF version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e530b-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e530b-161">-Confirm</span></span>
<span data-ttu-id="e530b-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e530b-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e530b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e530b-163">-WhatIf</span></span>
<span data-ttu-id="e530b-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e530b-164">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e530b-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e530b-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e530b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e530b-166">CommonParameters</span></span>
<span data-ttu-id="e530b-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e530b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e530b-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e530b-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e530b-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e530b-169">INPUTS</span></span>

### <span data-ttu-id="e530b-170">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e530b-170">None</span></span>
<span data-ttu-id="e530b-171">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e530b-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e530b-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e530b-172">OUTPUTS</span></span>

## <span data-ttu-id="e530b-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e530b-173">NOTES</span></span>

## <span data-ttu-id="e530b-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e530b-174">RELATED LINKS</span></span>

[<span data-ttu-id="e530b-175">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e530b-175">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="e530b-176">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e530b-176">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="e530b-177">Publikowanie — AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e530b-177">Publish-AzureRmVMDscConfiguration</span></span>](./Publish-AzureRmVMDscConfiguration.md)


