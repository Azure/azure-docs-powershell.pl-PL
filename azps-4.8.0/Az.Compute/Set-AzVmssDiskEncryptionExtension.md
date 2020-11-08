---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220130"
---
# <span data-ttu-id="af24d-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="af24d-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="af24d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af24d-102">SYNOPSIS</span></span>
<span data-ttu-id="af24d-103">Umożliwia szyfrowanie dysków na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af24d-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="af24d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af24d-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af24d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af24d-105">DESCRIPTION</span></span>
<span data-ttu-id="af24d-106">Polecenie cmdlet **Set-AzVmssDiskEncryptionExtension** umożliwia szyfrowanie w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af24d-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="af24d-107">To polecenie cmdlet umożliwia szyfrowanie przez zainstalowanie rozszerzenia szyfrowanie dysku w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af24d-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="af24d-108">W przypadku maszyn wirtualnych systemu Linux parametr *volumetype* musi być obecny i musi mieć wartość "dane"</span><span class="sxs-lookup"><span data-stu-id="af24d-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="af24d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af24d-109">EXAMPLES</span></span>

### <span data-ttu-id="af24d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af24d-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="af24d-111">To polecenie umożliwia włączenie szyfrowania na wszystkich dyskach wszystkich maszyn wirtualnych systemu Windows w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af24d-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="af24d-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="af24d-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="af24d-113">To polecenie umożliwia włączenie szyfrowania na dyskach z danymi wszystkich maszyn wirtualnych systemu Linux w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af24d-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="af24d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af24d-114">PARAMETERS</span></span>

### <span data-ttu-id="af24d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af24d-115">-DefaultProfile</span></span>
<span data-ttu-id="af24d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af24d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af24d-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="af24d-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="af24d-118">Wyłącz automatyczne uaktualnianie wersji pomocniczej</span><span class="sxs-lookup"><span data-stu-id="af24d-118">Disable auto-upgrade of minor version</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af24d-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="af24d-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="af24d-120">Identyfikator zasobu magazynu kluczy, w którym ma zostać umieszczony wygenerowany klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="af24d-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="af24d-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="af24d-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="af24d-122">Adres URL magazynu kluczy, w którym zostanie umieszczony klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="af24d-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="af24d-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="af24d-123">-ExtensionName</span></span>
<span data-ttu-id="af24d-124">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="af24d-124">The extension name.</span></span>
<span data-ttu-id="af24d-125">Jeśli ten parametr nie jest określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="af24d-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="af24d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="af24d-126">-Force</span></span>
<span data-ttu-id="af24d-127">Aby wymusić włączenie szyfrowania na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af24d-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="af24d-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="af24d-128">-ForceUpdate</span></span>
<span data-ttu-id="af24d-129">Generowanie znacznika dla wymuszenia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="af24d-129">Generate a tag for force update.</span></span>  <span data-ttu-id="af24d-130">Należy to podać w celu wykonania powtarzających się operacji szyfrowania na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af24d-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af24d-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="af24d-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="af24d-132">Algorytm szyfrowania kluczy używany do szyfrowania klucza szyfrowania woluminu</span><span class="sxs-lookup"><span data-stu-id="af24d-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af24d-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="af24d-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="af24d-134">Adres URL magazynu kluczy z wersją KeyEncryptionKey, służący do szyfrowania klucza szyfrowania dysku</span><span class="sxs-lookup"><span data-stu-id="af24d-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="af24d-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="af24d-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="af24d-136">Identyfikator zasobu magazynu kluczy zawierający KeyEncryptionKey służący do szyfrowania klucza szyfrowania dysku</span><span class="sxs-lookup"><span data-stu-id="af24d-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="af24d-137">— Hasło</span><span class="sxs-lookup"><span data-stu-id="af24d-137">-Passphrase</span></span>
<span data-ttu-id="af24d-138">Hasło określone w parametrach.</span><span class="sxs-lookup"><span data-stu-id="af24d-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="af24d-139">Ten parametr działa tylko w przypadku maszyny wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="af24d-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="af24d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af24d-140">-ResourceGroupName</span></span>
<span data-ttu-id="af24d-141">Nazwa grupy zasobów, do której należy zestaw skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="af24d-141">The resource group name to which the VM Scale Set belongs to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af24d-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="af24d-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="af24d-143">Wersja programu obsługi typu.</span><span class="sxs-lookup"><span data-stu-id="af24d-143">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af24d-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="af24d-144">-VMScaleSetName</span></span>
<span data-ttu-id="af24d-145">Nazwa zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="af24d-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af24d-146">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="af24d-146">-VolumeType</span></span>
<span data-ttu-id="af24d-147">Określa typ woluminów maszyny wirtualnej, na których ma zostać wykonana operacja szyfrowania: system operacyjny, dane lub wszystko.</span><span class="sxs-lookup"><span data-stu-id="af24d-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="af24d-148">Linux: parametr **volumetype** musi być obecny i musi być ustawiony na dane.</span><span class="sxs-lookup"><span data-stu-id="af24d-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="af24d-149">Windows: parametr **volumetype** (jeśli jest obecny) musi mieć wartość All lub OS.</span><span class="sxs-lookup"><span data-stu-id="af24d-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="af24d-150">Jeśli parametr **nazwa_woluminu** jest pominięty, jego wartość domyślna to "wszystko".</span><span class="sxs-lookup"><span data-stu-id="af24d-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af24d-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af24d-151">-Confirm</span></span>
<span data-ttu-id="af24d-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af24d-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af24d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af24d-153">-WhatIf</span></span>
<span data-ttu-id="af24d-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af24d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af24d-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af24d-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af24d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af24d-156">CommonParameters</span></span>
<span data-ttu-id="af24d-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af24d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af24d-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af24d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af24d-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af24d-159">INPUTS</span></span>

### <span data-ttu-id="af24d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="af24d-160">System.String</span></span>

### <span data-ttu-id="af24d-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af24d-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="af24d-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af24d-162">OUTPUTS</span></span>

### <span data-ttu-id="af24d-163">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="af24d-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="af24d-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af24d-164">NOTES</span></span>

## <span data-ttu-id="af24d-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af24d-165">RELATED LINKS</span></span>
