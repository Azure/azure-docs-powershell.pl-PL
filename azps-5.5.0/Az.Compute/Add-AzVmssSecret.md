---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 6f9f1f29f23906442d7c9c8187b9bab3bf41403b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238959"
---
# <span data-ttu-id="bdc00-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="bdc00-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="bdc00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdc00-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc00-103">Dodaje klucz tajny do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bdc00-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="bdc00-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bdc00-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdc00-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bdc00-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc00-106">Polecenie **cmdlet AzVmssSecret add-AzVmssSecret** dodaje klucz tajny do zestawu skal maszyny wirtualnej (VIRTUAL MACHINE Scale Set).</span><span class="sxs-lookup"><span data-stu-id="bdc00-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="bdc00-107">Klucz tajny musi być przechowywany w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc00-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="bdc00-108">Aby uzyskać więcej informacji dotyczących magazynu kluczy, zobacz [Co to jest magazyn kluczy platformy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="bdc00-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="bdc00-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="bdc00-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="bdc00-110">Aby uzyskać więcej informacji o poleceniach cmdlet, zobacz polecenia [cmdlet](/powershell/module/az.keyvault) magazynu kluczy platformy Azure lub polecenie cmdlet [Set-AzKeyVaultSecret.](/powershell/module/az.keyvault/set-azkeyvaultsecret)</span><span class="sxs-lookup"><span data-stu-id="bdc00-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="bdc00-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bdc00-111">EXAMPLES</span></span>

### <span data-ttu-id="bdc00-112">Przykład 1. Dodawanie tajemnicy do maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="bdc00-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="bdc00-113">W tym przykładzie do usługi maszyny wirtualnej jest dodano klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="bdc00-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="bdc00-114">Pierwsze polecenie używa Get-AzKeyVault cmdlet w celu uzyskania tajnego magazynu z magazynu o nazwie ContosoVault i przechowuje wynik w zmiennej o nazwie $Vault.</span><span class="sxs-lookup"><span data-stu-id="bdc00-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="bdc00-115">Drugie polecenie używa polecenia cmdlet **New-AzVmssVaultCertificateConfig** w celu utworzenia konfiguracji certyfikatu magazynu kluczy przy użyciu określonego adresu URL certyfikatu z magazynu certyfikatów o nazwie Certyfikaty i przechowuje wyniki w zmiennej o nazwie $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="bdc00-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="bdc00-116">Trzecie polecenie używa polecenia cmdlet **New-AzVmssConfig** w celu utworzenia obiektu konfiguracji maszyny WIRTUALNEJ i przechowuje wynik w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="bdc00-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="bdc00-117">Czwarte polecenie dodaje klucz tajny do maszyn wirtualnych wirtualnych przy użyciu klucza tajnego magazynu przy użyciu identyfikatora zasobu klucza i certyfikatu magazynu przechowywanego w $Vault i $CertConfig zmiennych.</span><span class="sxs-lookup"><span data-stu-id="bdc00-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="bdc00-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdc00-118">PARAMETERS</span></span>

### <span data-ttu-id="bdc00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc00-119">-DefaultProfile</span></span>
<span data-ttu-id="bdc00-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc00-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdc00-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="bdc00-121">-SourceVaultId</span></span>
<span data-ttu-id="bdc00-122">Określa identyfikator zasobu magazynu kluczy, który zawiera certyfikaty, które można dodać do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bdc00-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="bdc00-123">Ta wartość jest również kluczem do dodawania wielu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="bdc00-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="bdc00-124">Oznacza to, że można użyć tej samej wartości parametru *SourceVaultId* podczas dodawania wielu certyfikatów z tego samego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bdc00-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc00-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="bdc00-125">-VaultCertificate</span></span>
<span data-ttu-id="bdc00-126">Określa obiekt **certyfikat magazynu** zawierający adres URL certyfikatu i nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bdc00-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="bdc00-127">Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzVmssVaultCertificateConfig.](./New-AzVmssVaultCertificateConfig.md)</span><span class="sxs-lookup"><span data-stu-id="bdc00-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc00-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bdc00-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bdc00-129">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="bdc00-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="bdc00-130">Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="bdc00-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc00-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdc00-131">-Confirm</span></span>
<span data-ttu-id="bdc00-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bdc00-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc00-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc00-133">-WhatIf</span></span>
<span data-ttu-id="bdc00-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc00-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdc00-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bdc00-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc00-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc00-136">CommonParameters</span></span>
<span data-ttu-id="bdc00-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc00-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc00-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdc00-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc00-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdc00-139">INPUTS</span></span>

### <span data-ttu-id="bdc00-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bdc00-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="bdc00-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bdc00-141">System.String</span></span>

### <span data-ttu-id="bdc00-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span><span class="sxs-lookup"><span data-stu-id="bdc00-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="bdc00-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bdc00-143">OUTPUTS</span></span>

### <span data-ttu-id="bdc00-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bdc00-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bdc00-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bdc00-145">NOTES</span></span>

## <span data-ttu-id="bdc00-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdc00-146">RELATED LINKS</span></span>

[<span data-ttu-id="bdc00-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="bdc00-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="bdc00-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bdc00-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
