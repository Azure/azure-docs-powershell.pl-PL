---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
ms.openlocfilehash: 9c31442e1242114572540c23049f26715fc3099e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898090"
---
# <span data-ttu-id="010bc-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="010bc-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="010bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="010bc-102">SYNOPSIS</span></span>
<span data-ttu-id="010bc-103">Dodaje klucz tajny do VMSS.</span><span class="sxs-lookup"><span data-stu-id="010bc-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="010bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="010bc-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="010bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="010bc-105">DESCRIPTION</span></span>
<span data-ttu-id="010bc-106">Polecenie cmdlet **Add-AzureRmVmssSecret** umożliwia dodanie klucza tajnego do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="010bc-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="010bc-107">Klucz tajny musi być przechowywany w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="010bc-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="010bc-108">Aby uzyskać więcej informacji dotyczących magazynu kluczy, zobacz [co to jest magazyn kluczy platformy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="010bc-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="010bc-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="010bc-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="010bc-110">Aby uzyskać więcej informacji na temat poleceń cmdlet, zobacz [polecenia cmdlet magazynu kluczy platformy Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) w bibliotece Microsoft Developer Network lub [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010bc-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="010bc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="010bc-111">EXAMPLES</span></span>

### <span data-ttu-id="010bc-112">Przykład 1. Dodaj klucz tajny do VMSS</span><span class="sxs-lookup"><span data-stu-id="010bc-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="010bc-113">W tym przykładzie jest dodawany klucz tajny do VMSS.</span><span class="sxs-lookup"><span data-stu-id="010bc-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="010bc-114">W pierwszym poleceniu użyto polecenia cmdlet Get-AzureRmKeyVault, aby uzyskać tajemnicę magazynu z magazynu o nazwie ContosoVault i przechowywać wynik w zmiennej o nazwie $Vault.</span><span class="sxs-lookup"><span data-stu-id="010bc-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="010bc-115">W drugim poleceniu użyto polecenia cmdlet **New-AzureRmVmssVaultCertificateConfig** w celu utworzenia konfiguracji certyfikatu magazynu kluczy przy użyciu określonego adresu URL certyfikatu z magazynu certyfikatów o nazwie Certificates i zapisanie wyników w zmiennej o nazwie $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="010bc-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="010bc-116">W trzecim poleceniu użyto polecenia cmdlet **New-AzureRmVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="010bc-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="010bc-117">Czwarte polecenie dodaje klucz tajny do VMSS przy użyciu klucza tajnego magazynu przy użyciu identyfikatora zasobu kluczy oraz certyfikatu magazynu przechowywanego w $Vault i $CertConfig zmiennych.</span><span class="sxs-lookup"><span data-stu-id="010bc-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="010bc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="010bc-118">PARAMETERS</span></span>

### <span data-ttu-id="010bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="010bc-119">-DefaultProfile</span></span>
<span data-ttu-id="010bc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="010bc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="010bc-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="010bc-121">-SourceVaultId</span></span>
<span data-ttu-id="010bc-122">Określa identyfikator zasobu magazynu kluczy zawierającego certyfikaty, które można dodać do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="010bc-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="010bc-123">Ta wartość działa także jako klucz do dodawania wielu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="010bc-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="010bc-124">Oznacza to, że w przypadku dodawania wielu certyfikatów z tego samego magazynu kluczy można użyć tej samej wartości parametru *SourceVaultId* .</span><span class="sxs-lookup"><span data-stu-id="010bc-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="010bc-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="010bc-125">-VaultCertificate</span></span>
<span data-ttu-id="010bc-126">Określa obiekt **certyfikatu** magazynu zawierający adres URL i nazwę certyfikatu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="010bc-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="010bc-127">Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="010bc-127">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="010bc-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="010bc-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="010bc-129">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="010bc-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="010bc-130">Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="010bc-130">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="010bc-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="010bc-131">-Confirm</span></span>
<span data-ttu-id="010bc-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010bc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="010bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="010bc-133">-WhatIf</span></span>
<span data-ttu-id="010bc-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010bc-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="010bc-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="010bc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="010bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010bc-136">CommonParameters</span></span>
<span data-ttu-id="010bc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="010bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010bc-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="010bc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010bc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="010bc-139">INPUTS</span></span>

### <span data-ttu-id="010bc-140">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="010bc-140">VirtualMachineScaleSet</span></span>
<span data-ttu-id="010bc-141">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="010bc-141">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="010bc-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="010bc-142">OUTPUTS</span></span>

### <span data-ttu-id="010bc-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="010bc-143">None</span></span>
<span data-ttu-id="010bc-144">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="010bc-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="010bc-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="010bc-145">NOTES</span></span>

## <span data-ttu-id="010bc-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="010bc-146">RELATED LINKS</span></span>

[<span data-ttu-id="010bc-147">Nowe — AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="010bc-147">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="010bc-148">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="010bc-148">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
