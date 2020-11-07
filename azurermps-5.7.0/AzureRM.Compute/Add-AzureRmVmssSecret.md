---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 7fe1fd25801c2aa02ba6c1506f4792fda99d94de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716506"
---
# <span data-ttu-id="a93f3-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="a93f3-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="a93f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a93f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a93f3-103">Dodaje klucz tajny do VMSS.</span><span class="sxs-lookup"><span data-stu-id="a93f3-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a93f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a93f3-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a93f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a93f3-105">DESCRIPTION</span></span>
<span data-ttu-id="a93f3-106">Polecenie cmdlet **Add-AzureRmVmssSecret** umożliwia dodanie klucza tajnego do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a93f3-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a93f3-107">Klucz tajny musi być przechowywany w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a93f3-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="a93f3-108">Aby uzyskać więcej informacji dotyczących magazynu kluczy, zobacz [co to jest magazyn kluczy platformy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="a93f3-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="a93f3-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="a93f3-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="a93f3-110">Aby uzyskać więcej informacji na temat poleceń cmdlet, zobacz [polecenia cmdlet magazynu kluczy platformy Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) w bibliotece Microsoft Developer Network lub [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a93f3-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="a93f3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a93f3-111">EXAMPLES</span></span>

### <span data-ttu-id="a93f3-112">Przykład 1. Dodaj klucz tajny do VMSS</span><span class="sxs-lookup"><span data-stu-id="a93f3-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="a93f3-113">W tym przykładzie jest dodawany klucz tajny do VMSS.</span><span class="sxs-lookup"><span data-stu-id="a93f3-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="a93f3-114">W pierwszym poleceniu użyto polecenia cmdlet Get-AzureRmKeyVault, aby uzyskać tajemnicę magazynu z magazynu o nazwie ContosoVault i przechowywać wynik w zmiennej o nazwie $Vault.</span><span class="sxs-lookup"><span data-stu-id="a93f3-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="a93f3-115">W drugim poleceniu użyto polecenia cmdlet **New-AzureRmVmssVaultCertificateConfig** w celu utworzenia konfiguracji certyfikatu magazynu kluczy przy użyciu określonego adresu URL certyfikatu z magazynu certyfikatów o nazwie Certificates i zapisanie wyników w zmiennej o nazwie $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="a93f3-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="a93f3-116">W trzecim poleceniu użyto polecenia cmdlet **New-AzureRmVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="a93f3-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="a93f3-117">Czwarte polecenie dodaje klucz tajny do VMSS przy użyciu klucza tajnego magazynu przy użyciu identyfikatora zasobu kluczy oraz certyfikatu magazynu przechowywanego w $Vault i $CertConfig zmiennych.</span><span class="sxs-lookup"><span data-stu-id="a93f3-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="a93f3-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a93f3-118">PARAMETERS</span></span>

### <span data-ttu-id="a93f3-119">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a93f3-119">-SourceVaultId</span></span>
<span data-ttu-id="a93f3-120">Określa identyfikator zasobu magazynu kluczy zawierającego certyfikaty, które można dodać do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a93f3-120">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="a93f3-121">Ta wartość działa także jako klucz do dodawania wielu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="a93f3-121">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="a93f3-122">Oznacza to, że w przypadku dodawania wielu certyfikatów z tego samego magazynu kluczy można użyć tej samej wartości parametru *SourceVaultId* .</span><span class="sxs-lookup"><span data-stu-id="a93f3-122">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93f3-123">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a93f3-123">-VaultCertificate</span></span>
<span data-ttu-id="a93f3-124">Określa obiekt **certyfikatu** magazynu zawierający adres URL i nazwę certyfikatu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a93f3-124">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="a93f3-125">Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="a93f3-125">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93f3-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a93f3-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a93f3-127">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="a93f3-127">Specifies the VMSS object.</span></span>
<span data-ttu-id="a93f3-128">Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="a93f3-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a93f3-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a93f3-129">-Confirm</span></span>
<span data-ttu-id="a93f3-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a93f3-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a93f3-131">-WhatIf</span></span>
<span data-ttu-id="a93f3-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a93f3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a93f3-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a93f3-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93f3-134">CommonParameters</span></span>
<span data-ttu-id="a93f3-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93f3-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a93f3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93f3-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a93f3-137">INPUTS</span></span>

### <span data-ttu-id="a93f3-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a93f3-138">None</span></span>
<span data-ttu-id="a93f3-139">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a93f3-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a93f3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a93f3-140">OUTPUTS</span></span>

###  
<span data-ttu-id="a93f3-141">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a93f3-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a93f3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a93f3-142">NOTES</span></span>

## <span data-ttu-id="a93f3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a93f3-143">RELATED LINKS</span></span>

[<span data-ttu-id="a93f3-144">Nowe — AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="a93f3-144">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="a93f3-145">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a93f3-145">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
