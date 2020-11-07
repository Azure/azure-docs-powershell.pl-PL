---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
ms.openlocfilehash: fe4b965aa859388c2066dc759354a1651cb20123
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548340"
---
# <span data-ttu-id="bafe8-101">Set-AzureRmVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bafe8-101">Set-AzureRmVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="bafe8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bafe8-102">SYNOPSIS</span></span>
<span data-ttu-id="bafe8-103">Umożliwia szyfrowanie dysków na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bafe8-103">Enables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bafe8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bafe8-104">SYNTAX</span></span>

```
Set-AzureRmVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bafe8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bafe8-105">DESCRIPTION</span></span>
<span data-ttu-id="bafe8-106">Polecenie cmdlet **Set-AzureRmVmssDiskEncryptionExtension** umożliwia szyfrowanie w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bafe8-106">The **Set-AzureRmVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="bafe8-107">To polecenie cmdlet umożliwia szyfrowanie przez zainstalowanie rozszerzenia szyfrowanie dysku w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bafe8-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="bafe8-108">Jeśli nie podano parametru *name* , zainstalowane jest rozszerzenie o nazwie domyślnej AzureDiskEncryption dla maszyn wirtualnych z uruchomionym systemem operacyjnym Windows lub AzureDiskEncryptionForLinux dla komputerów wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="bafe8-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="bafe8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bafe8-109">EXAMPLES</span></span>

### <span data-ttu-id="bafe8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bafe8-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzureRmVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="bafe8-111">To polecenie umożliwia włączenie szyfrowania na wszystkich dyskach wszystkich maszyn wirtualnych w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bafe8-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="bafe8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bafe8-112">PARAMETERS</span></span>

### <span data-ttu-id="bafe8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafe8-113">-DefaultProfile</span></span>
<span data-ttu-id="bafe8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bafe8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bafe8-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bafe8-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bafe8-116">Wyłącz automatyczne uaktualnianie wersji pomocniczej</span><span class="sxs-lookup"><span data-stu-id="bafe8-116">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="bafe8-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="bafe8-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="bafe8-118">Identyfikator zasobu magazynu kluczy, w którym ma zostać umieszczony wygenerowany klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="bafe8-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="bafe8-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="bafe8-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="bafe8-120">Adres URL magazynu kluczy, w którym zostanie umieszczony klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="bafe8-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="bafe8-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="bafe8-121">-ExtensionName</span></span>
<span data-ttu-id="bafe8-122">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bafe8-122">The extension name.</span></span>
<span data-ttu-id="bafe8-123">Jeśli ten parametr nie jest określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="bafe8-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="bafe8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bafe8-124">-Force</span></span>
<span data-ttu-id="bafe8-125">Aby wymusić włączenie szyfrowania na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bafe8-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bafe8-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="bafe8-126">-ForceUpdate</span></span>
<span data-ttu-id="bafe8-127">Generowanie znacznika dla wymuszenia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="bafe8-127">Generate a tag for force update.</span></span>  <span data-ttu-id="bafe8-128">Należy to podać w celu wykonania powtarzających się operacji szyfrowania na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bafe8-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="bafe8-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="bafe8-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="bafe8-130">Algorytm szyfrowania kluczy używany do szyfrowania klucza szyfrowania woluminu</span><span class="sxs-lookup"><span data-stu-id="bafe8-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="bafe8-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="bafe8-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="bafe8-132">Adres URL magazynu kluczy z wersją KeyEncryptionKey, służący do szyfrowania klucza szyfrowania dysku</span><span class="sxs-lookup"><span data-stu-id="bafe8-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="bafe8-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="bafe8-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="bafe8-134">Identyfikator zasobu magazynu kluczy zawierający KeyEncryptionKey służący do szyfrowania klucza szyfrowania dysku</span><span class="sxs-lookup"><span data-stu-id="bafe8-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="bafe8-135">— Hasło</span><span class="sxs-lookup"><span data-stu-id="bafe8-135">-Passphrase</span></span>
<span data-ttu-id="bafe8-136">Hasło określone w parametrach.</span><span class="sxs-lookup"><span data-stu-id="bafe8-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="bafe8-137">Ten parametr działa tylko w przypadku maszyny wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="bafe8-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="bafe8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafe8-138">-ResourceGroupName</span></span>
<span data-ttu-id="bafe8-139">Nazwa grupy zasobów, do której należy zestaw skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="bafe8-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="bafe8-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bafe8-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="bafe8-141">Wersja programu obsługi typu.</span><span class="sxs-lookup"><span data-stu-id="bafe8-141">The type handler version.</span></span>

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

### <span data-ttu-id="bafe8-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bafe8-142">-VMScaleSetName</span></span>
<span data-ttu-id="bafe8-143">Nazwa zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="bafe8-143">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="bafe8-144">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="bafe8-144">-VolumeType</span></span>
<span data-ttu-id="bafe8-145">Typ woluminu (system operacyjny lub dane) do wykonania operacji szyfrowania</span><span class="sxs-lookup"><span data-stu-id="bafe8-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="bafe8-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bafe8-146">-Confirm</span></span>
<span data-ttu-id="bafe8-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafe8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bafe8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bafe8-148">-WhatIf</span></span>
<span data-ttu-id="bafe8-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafe8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bafe8-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bafe8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bafe8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafe8-151">CommonParameters</span></span>
<span data-ttu-id="bafe8-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bafe8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafe8-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bafe8-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafe8-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bafe8-154">INPUTS</span></span>

### <span data-ttu-id="bafe8-155">System. String</span><span class="sxs-lookup"><span data-stu-id="bafe8-155">System.String</span></span>
<span data-ttu-id="bafe8-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bafe8-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bafe8-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bafe8-157">OUTPUTS</span></span>

### <span data-ttu-id="bafe8-158">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="bafe8-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="bafe8-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bafe8-159">NOTES</span></span>

## <span data-ttu-id="bafe8-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bafe8-160">RELATED LINKS</span></span>
