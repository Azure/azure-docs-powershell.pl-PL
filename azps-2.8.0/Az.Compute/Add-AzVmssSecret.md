---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: d61374be31ef8b403c3ba823cb4b3b4d010c5a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706466"
---
# <span data-ttu-id="e1ebc-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="e1ebc-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="e1ebc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ebc-103">Dodaje klucz tajny do VMSS.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="e1ebc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1ebc-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ebc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ebc-106">Polecenie cmdlet **Add-AzVmssSecret** umożliwia dodanie klucza tajnego do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e1ebc-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e1ebc-107">Klucz tajny musi być przechowywany w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="e1ebc-108">Aby uzyskać więcej informacji dotyczących magazynu kluczy, zobacz [co to jest magazyn kluczy platformy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="e1ebc-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="e1ebc-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="e1ebc-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="e1ebc-110">Aby uzyskać więcej informacji na temat poleceń cmdlet, zobacz [polecenia cmdlet magazynu kluczy platformy Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) w bibliotece Microsoft Developer Network lub [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="e1ebc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1ebc-111">EXAMPLES</span></span>

### <span data-ttu-id="e1ebc-112">Przykład 1. Dodaj klucz tajny do VMSS</span><span class="sxs-lookup"><span data-stu-id="e1ebc-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="e1ebc-113">W tym przykładzie jest dodawany klucz tajny do VMSS.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="e1ebc-114">W pierwszym poleceniu użyto polecenia cmdlet Get-AzKeyVault, aby uzyskać tajemnicę magazynu z magazynu o nazwie ContosoVault i przechowywać wynik w zmiennej o nazwie $Vault.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="e1ebc-115">W drugim poleceniu użyto polecenia cmdlet **New-AzVmssVaultCertificateConfig** w celu utworzenia konfiguracji certyfikatu magazynu kluczy przy użyciu określonego adresu URL certyfikatu z magazynu certyfikatów o nazwie Certificates i zapisanie wyników w zmiennej o nazwie $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="e1ebc-116">W trzecim poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="e1ebc-117">Czwarte polecenie dodaje klucz tajny do VMSS przy użyciu klucza tajnego magazynu przy użyciu identyfikatora zasobu kluczy oraz certyfikatu magazynu przechowywanego w $Vault i $CertConfig zmiennych.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="e1ebc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1ebc-118">PARAMETERS</span></span>

### <span data-ttu-id="e1ebc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ebc-119">-DefaultProfile</span></span>
<span data-ttu-id="e1ebc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ebc-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e1ebc-121">-SourceVaultId</span></span>
<span data-ttu-id="e1ebc-122">Określa identyfikator zasobu magazynu kluczy zawierającego certyfikaty, które można dodać do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="e1ebc-123">Ta wartość działa także jako klucz do dodawania wielu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="e1ebc-124">Oznacza to, że w przypadku dodawania wielu certyfikatów z tego samego magazynu kluczy można użyć tej samej wartości parametru *SourceVaultId* .</span><span class="sxs-lookup"><span data-stu-id="e1ebc-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="e1ebc-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e1ebc-125">-VaultCertificate</span></span>
<span data-ttu-id="e1ebc-126">Określa obiekt **certyfikatu** magazynu zawierający adres URL i nazwę certyfikatu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="e1ebc-127">Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ebc-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="e1ebc-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e1ebc-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e1ebc-129">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="e1ebc-130">Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ebc-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="e1ebc-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1ebc-131">-Confirm</span></span>
<span data-ttu-id="e1ebc-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ebc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ebc-133">-WhatIf</span></span>
<span data-ttu-id="e1ebc-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1ebc-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ebc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ebc-136">CommonParameters</span></span>
<span data-ttu-id="e1ebc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ebc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ebc-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1ebc-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ebc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1ebc-139">INPUTS</span></span>

### <span data-ttu-id="e1ebc-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e1ebc-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e1ebc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ebc-141">System.String</span></span>

### <span data-ttu-id="e1ebc-142">Microsoft. Azure. Management. COMPUTE. MODELES. VaultCertificate []</span><span class="sxs-lookup"><span data-stu-id="e1ebc-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="e1ebc-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1ebc-143">OUTPUTS</span></span>

### <span data-ttu-id="e1ebc-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e1ebc-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e1ebc-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1ebc-145">NOTES</span></span>

## <span data-ttu-id="e1ebc-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1ebc-146">RELATED LINKS</span></span>

[<span data-ttu-id="e1ebc-147">Nowe — AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="e1ebc-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="e1ebc-148">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e1ebc-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)