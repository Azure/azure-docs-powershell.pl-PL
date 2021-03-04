---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: facd5a3637dcb1a8a392171468dd890279ba0f74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957505"
---
# <span data-ttu-id="038fd-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="038fd-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="038fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="038fd-102">SYNOPSIS</span></span>
<span data-ttu-id="038fd-103">Konfiguruje rozszerzenie DSC na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="038fd-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="038fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="038fd-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="038fd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="038fd-105">DESCRIPTION</span></span>
<span data-ttu-id="038fd-106">Polecenie **cmdlet Set-AzVMDscExtension** konfiguruje rozszerzenie Windows PowerShell Desired State Configuration (DSC) na maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="038fd-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="038fd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="038fd-107">EXAMPLES</span></span>

### <span data-ttu-id="038fd-108">Przykład 1. Ustawianie rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="038fd-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="038fd-109">To polecenie ustawia rozszerzenie DSC na komputerze wirtualnym o nazwie MASZYNY WIRTUALNEJ07 w celu pobrania Sample.ps1.zip z konta magazynu o nazwie Stg i kontenera domyślnego.</span><span class="sxs-lookup"><span data-stu-id="038fd-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="038fd-110">To polecenie wywoła konfigurację o nazwie ConfigName.</span><span class="sxs-lookup"><span data-stu-id="038fd-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="038fd-111">Plik Sample.ps1.zip został wcześniej przekazany za pomocą **funkcji Publish-AzVMDscConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="038fd-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="038fd-112">Przykład 2. Ustawianie rozszerzenia dsC z danymi konfiguracji</span><span class="sxs-lookup"><span data-stu-id="038fd-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="038fd-113">To polecenie ustawia rozszerzenie na maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ13 w celu pobrania Sample.ps1.zip z konta magazynu o nazwie Stg i kontenera o nazwie WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="038fd-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="038fd-114">Polecenie konfiguracji o nazwie ConfigName oraz określenie danych i argumentów konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="038fd-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="038fd-115">Plik Sample.ps1.zip został wcześniej przekazany za pomocą **funkcji Publish-AzVMDscConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="038fd-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="038fd-116">Przykład 3. Ustawianie rozszerzenia dsC przy użyciu danych konfiguracji z automatyczną aktualizacją</span><span class="sxs-lookup"><span data-stu-id="038fd-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="038fd-117">To polecenie ustawia rozszerzenie na maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ22 w celu pobrania Sample.ps1.zip z konta magazynu o nazwie Stg i kontenera o nazwie WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="038fd-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="038fd-118">To polecenie wywołuje konfigurację o nazwie ConfigName oraz określa dane i argumenty konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="038fd-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="038fd-119">To polecenie umożliwia również automatyczną aktualizację programu obsługi rozszerzeń do najnowszej wersji.</span><span class="sxs-lookup"><span data-stu-id="038fd-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="038fd-120">Plik Sample.ps1.zip został wcześniej przekazany za pomocą **narzędzia Publish-AzVMDscConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="038fd-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="038fd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="038fd-121">PARAMETERS</span></span>

### <span data-ttu-id="038fd-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="038fd-122">-ArchiveBlobName</span></span>
<span data-ttu-id="038fd-123">Określa nazwę pliku konfiguracji, który został wcześniej przekazany przez Publish-AzVMDscConfiguration cmdlet.</span><span class="sxs-lookup"><span data-stu-id="038fd-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="038fd-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="038fd-124">-ArchiveContainerName</span></span>
<span data-ttu-id="038fd-125">Nazwa gatunek kontenera magazynu platformy Azure, w którym znajduje się archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="038fd-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="038fd-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="038fd-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="038fd-127">Określa nazwę grupy zasobów zawierającej konto magazynu zawierające archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="038fd-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="038fd-128">Ten parametr jest opcjonalny, jeśli konto magazynu i maszynę wirtualną znajdują się w tej samej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="038fd-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="038fd-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="038fd-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="038fd-130">Określa nazwę konta magazynu platformy Azure służącego do pobierania pliku ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="038fd-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="038fd-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="038fd-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="038fd-132">Określa sufiks punktu końcowego magazynu.</span><span class="sxs-lookup"><span data-stu-id="038fd-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="038fd-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="038fd-133">-AutoUpdate</span></span>
<span data-ttu-id="038fd-134">Określa wersję obsługi rozszerzenia określoną przez *parametr Version.*</span><span class="sxs-lookup"><span data-stu-id="038fd-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="038fd-135">Domyślnie program obsługi rozszerzeń nie jest automatycznie wysuany.</span><span class="sxs-lookup"><span data-stu-id="038fd-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="038fd-136">Użyj *parametru AutoUpdate,* aby włączyć automatyczną aktualizację programu obsługi rozszerzeń do najnowszej wersji w momencie, gdy jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="038fd-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="038fd-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="038fd-137">-ConfigurationArgument</span></span>
<span data-ttu-id="038fd-138">Określa tabelę skrótu zawierającą argumenty funkcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="038fd-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="038fd-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="038fd-139">-ConfigurationData</span></span>
<span data-ttu-id="038fd-140">Określa ścieżkę pliku psd1 określającą dane dla konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="038fd-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="038fd-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="038fd-141">-ConfigurationName</span></span>
<span data-ttu-id="038fd-142">Określa nazwę konfiguracji wywoływanej przez rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="038fd-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="038fd-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="038fd-143">-DataCollection</span></span>
<span data-ttu-id="038fd-144">Określa typ kolekcji danych.</span><span class="sxs-lookup"><span data-stu-id="038fd-144">Specifies the data collection type.</span></span>
<span data-ttu-id="038fd-145">Dopuszczalne wartości dla tego parametru to: Włącz i Wyłącz.</span><span class="sxs-lookup"><span data-stu-id="038fd-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="038fd-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038fd-146">-DefaultProfile</span></span>
<span data-ttu-id="038fd-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="038fd-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="038fd-148">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="038fd-148">-Force</span></span>
<span data-ttu-id="038fd-149">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="038fd-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="038fd-150">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="038fd-150">-Location</span></span>
<span data-ttu-id="038fd-151">Określa ścieżkę rozszerzenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="038fd-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="038fd-152">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="038fd-152">-Name</span></span>
<span data-ttu-id="038fd-153">Określa nazwę zasobu usługi Azure Resource Manager reprezentującą to rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="038fd-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="038fd-154">Wartość domyślna to Microsoft.Powershell.DSC.</span><span class="sxs-lookup"><span data-stu-id="038fd-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="038fd-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="038fd-155">-NoWait</span></span>
<span data-ttu-id="038fd-156">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="038fd-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="038fd-157">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="038fd-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="038fd-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="038fd-158">-ResourceGroupName</span></span>
<span data-ttu-id="038fd-159">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="038fd-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="038fd-160">— Wersja</span><span class="sxs-lookup"><span data-stu-id="038fd-160">-Version</span></span>
<span data-ttu-id="038fd-161">Określa wersję rozszerzenia DSC, do Set-AzVMDscExtension do których mają zastosowanie ustawienia.</span><span class="sxs-lookup"><span data-stu-id="038fd-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="038fd-162">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="038fd-162">-VMName</span></span>
<span data-ttu-id="038fd-163">Określa nazwę maszyny wirtualnej, na której jest zainstalowany program obsługi rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="038fd-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="038fd-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="038fd-164">-WmfVersion</span></span>
<span data-ttu-id="038fd-165">Określa wersję WMF.</span><span class="sxs-lookup"><span data-stu-id="038fd-165">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="038fd-166">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="038fd-166">-Confirm</span></span>
<span data-ttu-id="038fd-167">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="038fd-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="038fd-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="038fd-168">-WhatIf</span></span>
<span data-ttu-id="038fd-169">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="038fd-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="038fd-170">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="038fd-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="038fd-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038fd-171">CommonParameters</span></span>
<span data-ttu-id="038fd-172">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="038fd-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038fd-173">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="038fd-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038fd-174">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="038fd-174">INPUTS</span></span>

### <span data-ttu-id="038fd-175">System.String</span><span class="sxs-lookup"><span data-stu-id="038fd-175">System.String</span></span>

### <span data-ttu-id="038fd-176">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="038fd-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="038fd-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="038fd-177">OUTPUTS</span></span>

### <span data-ttu-id="038fd-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="038fd-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="038fd-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="038fd-179">NOTES</span></span>

## <span data-ttu-id="038fd-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="038fd-180">RELATED LINKS</span></span>

[<span data-ttu-id="038fd-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="038fd-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="038fd-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="038fd-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="038fd-183">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="038fd-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


