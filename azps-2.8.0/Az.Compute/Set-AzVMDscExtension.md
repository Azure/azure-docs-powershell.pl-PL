---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 6bc953f88b94cfd917eeff4d531d3137b25c6222
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706178"
---
# <span data-ttu-id="8da33-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8da33-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="8da33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8da33-102">SYNOPSIS</span></span>
<span data-ttu-id="8da33-103">Konfiguruje rozszerzenie DSC na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8da33-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="8da33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8da33-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da33-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8da33-105">DESCRIPTION</span></span>
<span data-ttu-id="8da33-106">Polecenie cmdlet **Set-AzVMDscExtension** konfiguruje rozszerzenie konfiguracji stanu wymaganego programu Windows PowerShell na maszynie wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8da33-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="8da33-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8da33-107">EXAMPLES</span></span>

### <span data-ttu-id="8da33-108">Przykład 1: Ustawianie rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="8da33-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="8da33-109">To polecenie ustawia rozszerzenie DSC na maszynie wirtualnej o nazwie VM07, aby pobrać Sample.ps1.zip z konta magazynu o nazwie STG i domyślnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="8da33-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="8da33-110">Polecenie wywoła konfigurację o nazwie configname.</span><span class="sxs-lookup"><span data-stu-id="8da33-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="8da33-111">Plik Sample.ps1.zip został przekazany wcześniej za pomocą polecenia **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8da33-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="8da33-112">Przykład 2: Ustawianie rozszerzenia DSC przy użyciu danych konfiguracji</span><span class="sxs-lookup"><span data-stu-id="8da33-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="8da33-113">To polecenie ustawia rozszerzenie na maszynie wirtualnej o nazwie VM13, aby pobrać Sample.ps1.zip z konta magazynu o nazwie STG i kontenera o nazwie WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="8da33-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="8da33-114">Polecenie o konfiguracji o nazwie configname i określające dane konfiguracji oraz argumenty.</span><span class="sxs-lookup"><span data-stu-id="8da33-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="8da33-115">Plik Sample.ps1.zip został przekazany wcześniej za pomocą polecenia **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8da33-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="8da33-116">Przykład 3: Ustawianie rozszerzenia DSC z danymi konfiguracji, które zawierają funkcję autoaktualizacji</span><span class="sxs-lookup"><span data-stu-id="8da33-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="8da33-117">To polecenie ustawia rozszerzenie na maszynie wirtualnej o nazwie VM22, aby pobrać Sample.ps1.zip z konta magazynu o nazwie STG i kontenera o nazwie WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="8da33-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="8da33-118">Polecenie umożliwia wywołanie konfiguracji o nazwie configname oraz określenie danych i argumentów konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8da33-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="8da33-119">To polecenie umożliwia również automatyczne aktualizowanie obsługi rozszerzeń do najnowszej wersji.</span><span class="sxs-lookup"><span data-stu-id="8da33-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="8da33-120">Sample.ps1.zip został przekazany wcześniej za pomocą polecenia **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8da33-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="8da33-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8da33-121">PARAMETERS</span></span>

### <span data-ttu-id="8da33-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="8da33-122">-ArchiveBlobName</span></span>
<span data-ttu-id="8da33-123">Określa nazwę pliku konfiguracji, który został wcześniej przekazany za pomocą polecenia cmdlet Publish-AzVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8da33-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="8da33-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="8da33-124">-ArchiveContainerName</span></span>
<span data-ttu-id="8da33-125">Nazwa gatunku kontenera usługi Azure Storage, w którym znajduje się archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8da33-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="8da33-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da33-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="8da33-127">Określa nazwę grupy zasobów zawierającej konto magazynu zawierające archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8da33-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="8da33-128">Ten parametr jest opcjonalny, jeśli konto magazynu i maszyna wirtualna są w tej samej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8da33-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="8da33-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8da33-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="8da33-130">Określa nazwę konta usługi Azure Storage, która jest używana do pobierania ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="8da33-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="8da33-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8da33-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="8da33-132">Określa sufiks punktu końcowego składowania.</span><span class="sxs-lookup"><span data-stu-id="8da33-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="8da33-133">-Aktualizacje automatyczne</span><span class="sxs-lookup"><span data-stu-id="8da33-133">-AutoUpdate</span></span>
<span data-ttu-id="8da33-134">Określa wersję obsługi rozszerzeń określoną przez parametr *Version* .</span><span class="sxs-lookup"><span data-stu-id="8da33-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="8da33-135">Domyślnie obsługa rozszerzeń nie jest aktualizowana.</span><span class="sxs-lookup"><span data-stu-id="8da33-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="8da33-136">Użyj parametru *AutoUpdate* , aby włączyć automatyczną aktualizację programu obsługi rozszerzeń do najnowszej wersji, gdy jest ona dostępna.</span><span class="sxs-lookup"><span data-stu-id="8da33-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="8da33-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="8da33-137">-ConfigurationArgument</span></span>
<span data-ttu-id="8da33-138">Określa tabelę skrótów zawierającą argumenty funkcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8da33-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="8da33-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="8da33-139">-ConfigurationData</span></span>
<span data-ttu-id="8da33-140">Określa ścieżkę pliku psd1, który określa dane konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8da33-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="8da33-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8da33-141">-ConfigurationName</span></span>
<span data-ttu-id="8da33-142">Określa nazwę konfiguracji, jaką wywoła rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="8da33-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="8da33-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="8da33-143">-DataCollection</span></span>
<span data-ttu-id="8da33-144">Określa typ zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="8da33-144">Specifies the data collection type.</span></span>
<span data-ttu-id="8da33-145">Dopuszczalne wartości tego parametru to: enable i Disable.</span><span class="sxs-lookup"><span data-stu-id="8da33-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="8da33-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da33-146">-DefaultProfile</span></span>
<span data-ttu-id="8da33-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8da33-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8da33-148">-Force</span><span class="sxs-lookup"><span data-stu-id="8da33-148">-Force</span></span>
<span data-ttu-id="8da33-149">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8da33-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8da33-150">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8da33-150">-Location</span></span>
<span data-ttu-id="8da33-151">Określa ścieżkę rozszerzenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="8da33-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="8da33-152">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8da33-152">-Name</span></span>
<span data-ttu-id="8da33-153">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="8da33-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="8da33-154">Wartość domyślna to Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="8da33-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="8da33-155">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8da33-155">-NoWait</span></span>
<span data-ttu-id="8da33-156">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="8da33-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8da33-157">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="8da33-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8da33-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da33-158">-ResourceGroupName</span></span>
<span data-ttu-id="8da33-159">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8da33-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8da33-160">-Version</span><span class="sxs-lookup"><span data-stu-id="8da33-160">-Version</span></span>
<span data-ttu-id="8da33-161">Określa wersję rozszerzenia DSC, do którego Set-AzVMDscExtension zastosować ustawienia.</span><span class="sxs-lookup"><span data-stu-id="8da33-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="8da33-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="8da33-162">-VMName</span></span>
<span data-ttu-id="8da33-163">Określa nazwę maszyny wirtualnej, w której jest zainstalowany program obsługi rozszerzeń DSC.</span><span class="sxs-lookup"><span data-stu-id="8da33-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="8da33-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="8da33-164">-WmfVersion</span></span>
<span data-ttu-id="8da33-165">Określa wersję WMF.</span><span class="sxs-lookup"><span data-stu-id="8da33-165">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="8da33-166">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8da33-166">-Confirm</span></span>
<span data-ttu-id="8da33-167">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da33-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da33-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da33-168">-WhatIf</span></span>
<span data-ttu-id="8da33-169">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da33-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8da33-170">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8da33-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da33-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da33-171">CommonParameters</span></span>
<span data-ttu-id="8da33-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da33-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da33-173">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8da33-173">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da33-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8da33-174">INPUTS</span></span>

### <span data-ttu-id="8da33-175">System. String</span><span class="sxs-lookup"><span data-stu-id="8da33-175">System.String</span></span>

### <span data-ttu-id="8da33-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8da33-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8da33-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8da33-177">OUTPUTS</span></span>

### <span data-ttu-id="8da33-178">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8da33-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8da33-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8da33-179">NOTES</span></span>

## <span data-ttu-id="8da33-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8da33-180">RELATED LINKS</span></span>

[<span data-ttu-id="8da33-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8da33-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="8da33-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8da33-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="8da33-183">Publikowanie — AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da33-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


