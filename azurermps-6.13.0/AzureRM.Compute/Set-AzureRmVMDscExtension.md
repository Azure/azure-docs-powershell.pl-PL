---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDscExtension.md
ms.openlocfilehash: 49c2250fa8a3746862b7ba17c9268fc82a8bf834
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545459"
---
# <span data-ttu-id="e7eac-101">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e7eac-101">Set-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="e7eac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7eac-102">SYNOPSIS</span></span>
<span data-ttu-id="e7eac-103">Konfiguruje rozszerzenie DSC na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7eac-103">Configures the DSC extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7eac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7eac-104">SYNTAX</span></span>

```
Set-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7eac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7eac-105">DESCRIPTION</span></span>
<span data-ttu-id="e7eac-106">Polecenie cmdlet **Set-AzureRmVMDscExtension** konfiguruje rozszerzenie konfiguracji stanu wymaganego programu Windows PowerShell na maszynie wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7eac-106">The **Set-AzureRmVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="e7eac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7eac-107">EXAMPLES</span></span>

### <span data-ttu-id="e7eac-108">Przykład 1: Ustawianie rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="e7eac-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="e7eac-109">To polecenie ustawia rozszerzenie DSC na maszynie wirtualnej o nazwie VM07, aby pobrać Sample.ps1.zip z konta magazynu o nazwie STG i domyślnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="e7eac-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="e7eac-110">Polecenie wywoła konfigurację o nazwie configname.</span><span class="sxs-lookup"><span data-stu-id="e7eac-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="e7eac-111">Plik Sample.ps1.zip został przekazany wcześniej za pomocą polecenia **Publish-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e7eac-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="e7eac-112">Przykład 2: Ustawianie rozszerzenia DSC przy użyciu danych konfiguracji</span><span class="sxs-lookup"><span data-stu-id="e7eac-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="e7eac-113">To polecenie ustawia rozszerzenie na maszynie wirtualnej o nazwie VM13, aby pobrać Sample.ps1.zip z konta magazynu o nazwie STG i kontenera o nazwie WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="e7eac-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="e7eac-114">Polecenie o konfiguracji o nazwie configname i określające dane konfiguracji oraz argumenty.</span><span class="sxs-lookup"><span data-stu-id="e7eac-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="e7eac-115">Plik Sample.ps1.zip został przekazany wcześniej za pomocą polecenia **Publish-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e7eac-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="e7eac-116">Przykład 3: Ustawianie rozszerzenia DSC z danymi konfiguracji, które zawierają funkcję autoaktualizacji</span><span class="sxs-lookup"><span data-stu-id="e7eac-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="e7eac-117">To polecenie ustawia rozszerzenie na maszynie wirtualnej o nazwie VM22, aby pobrać Sample.ps1.zip z konta magazynu o nazwie STG i kontenera o nazwie WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="e7eac-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="e7eac-118">Polecenie umożliwia wywołanie konfiguracji o nazwie configname oraz określenie danych i argumentów konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e7eac-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="e7eac-119">To polecenie umożliwia również automatyczne aktualizowanie obsługi rozszerzeń do najnowszej wersji.</span><span class="sxs-lookup"><span data-stu-id="e7eac-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="e7eac-120">Sample.ps1.zip został przekazany wcześniej za pomocą polecenia **Publish-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e7eac-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

## <span data-ttu-id="e7eac-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7eac-121">PARAMETERS</span></span>

### <span data-ttu-id="e7eac-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="e7eac-122">-ArchiveBlobName</span></span>
<span data-ttu-id="e7eac-123">Określa nazwę pliku konfiguracji, który został wcześniej przekazany za pomocą polecenia cmdlet Publish-AzureRmVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e7eac-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzureRmVMDscConfiguration cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="e7eac-124">-ArchiveContainerName</span></span>
<span data-ttu-id="e7eac-125">Nazwa gatunku kontenera usługi Azure Storage, w którym znajduje się archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e7eac-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7eac-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="e7eac-127">Określa nazwę grupy zasobów zawierającej konto magazynu zawierające archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e7eac-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="e7eac-128">Ten parametr jest opcjonalny, jeśli konto magazynu i maszyna wirtualna są w tej samej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7eac-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e7eac-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="e7eac-130">Określa nazwę konta usługi Azure Storage, która jest używana do pobierania ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="e7eac-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e7eac-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="e7eac-132">Określa sufiks punktu końcowego składowania.</span><span class="sxs-lookup"><span data-stu-id="e7eac-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-133">-Aktualizacje automatyczne</span><span class="sxs-lookup"><span data-stu-id="e7eac-133">-AutoUpdate</span></span>
<span data-ttu-id="e7eac-134">Określa wersję obsługi rozszerzeń określoną przez parametr *Version* .</span><span class="sxs-lookup"><span data-stu-id="e7eac-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="e7eac-135">Domyślnie obsługa rozszerzeń nie jest aktualizowana.</span><span class="sxs-lookup"><span data-stu-id="e7eac-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="e7eac-136">Użyj parametru *AutoUpdate* , aby włączyć automatyczną aktualizację programu obsługi rozszerzeń do najnowszej wersji, gdy jest ona dostępna.</span><span class="sxs-lookup"><span data-stu-id="e7eac-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="e7eac-137">-ConfigurationArgument</span></span>
<span data-ttu-id="e7eac-138">Określa tabelę skrótów zawierającą argumenty funkcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e7eac-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="e7eac-139">-ConfigurationData</span></span>
<span data-ttu-id="e7eac-140">Określa ścieżkę pliku psd1, który określa dane konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e7eac-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e7eac-141">-ConfigurationName</span></span>
<span data-ttu-id="e7eac-142">Określa nazwę konfiguracji, jaką wywoła rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="e7eac-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="e7eac-143">-DataCollection</span></span>
<span data-ttu-id="e7eac-144">Określa typ zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="e7eac-144">Specifies the data collection type.</span></span>
<span data-ttu-id="e7eac-145">Dopuszczalne wartości tego parametru to: enable i Disable.</span><span class="sxs-lookup"><span data-stu-id="e7eac-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7eac-146">-DefaultProfile</span></span>
<span data-ttu-id="e7eac-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7eac-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7eac-148">-Force</span><span class="sxs-lookup"><span data-stu-id="e7eac-148">-Force</span></span>
<span data-ttu-id="e7eac-149">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e7eac-149">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-150">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e7eac-150">-Location</span></span>
<span data-ttu-id="e7eac-151">Określa ścieżkę rozszerzenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7eac-151">Specifies the path of the resource extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-152">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7eac-152">-Name</span></span>
<span data-ttu-id="e7eac-153">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="e7eac-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e7eac-154">Wartość domyślna to Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="e7eac-154">The default value is Microsoft.Powershell.DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7eac-155">-ResourceGroupName</span></span>
<span data-ttu-id="e7eac-156">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7eac-156">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e7eac-157">-Version</span><span class="sxs-lookup"><span data-stu-id="e7eac-157">-Version</span></span>
<span data-ttu-id="e7eac-158">Określa wersję rozszerzenia DSC, do którego Set-AzureRmVMDscExtension zastosować ustawienia.</span><span class="sxs-lookup"><span data-stu-id="e7eac-158">Specifies the version of the DSC extension that Set-AzureRmVMDscExtension applies the settings to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-159">-VMName</span><span class="sxs-lookup"><span data-stu-id="e7eac-159">-VMName</span></span>
<span data-ttu-id="e7eac-160">Określa nazwę maszyny wirtualnej, w której jest zainstalowany program obsługi rozszerzeń DSC.</span><span class="sxs-lookup"><span data-stu-id="e7eac-160">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-161">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="e7eac-161">-WmfVersion</span></span>
<span data-ttu-id="e7eac-162">Określa wersję WMF.</span><span class="sxs-lookup"><span data-stu-id="e7eac-162">Specifies the WMF version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eac-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7eac-163">-Confirm</span></span>
<span data-ttu-id="e7eac-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7eac-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7eac-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7eac-165">-WhatIf</span></span>
<span data-ttu-id="e7eac-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7eac-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7eac-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7eac-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7eac-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7eac-168">CommonParameters</span></span>
<span data-ttu-id="e7eac-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7eac-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7eac-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7eac-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7eac-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7eac-171">INPUTS</span></span>

### <span data-ttu-id="e7eac-172">System. String</span><span class="sxs-lookup"><span data-stu-id="e7eac-172">System.String</span></span>

### <span data-ttu-id="e7eac-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e7eac-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e7eac-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7eac-174">OUTPUTS</span></span>

### <span data-ttu-id="e7eac-175">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e7eac-175">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e7eac-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7eac-176">NOTES</span></span>

## <span data-ttu-id="e7eac-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7eac-177">RELATED LINKS</span></span>

[<span data-ttu-id="e7eac-178">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e7eac-178">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="e7eac-179">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e7eac-179">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="e7eac-180">Publikowanie — AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7eac-180">Publish-AzureRmVMDscConfiguration</span></span>](./Publish-AzureRmVMDscConfiguration.md)


