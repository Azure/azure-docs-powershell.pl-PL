---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 517614e93510aab163f5d632705e4a5a3566186a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544516"
---
# <span data-ttu-id="167a9-101">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="167a9-101">Add-AzureRmVMSecret</span></span>

## <span data-ttu-id="167a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="167a9-102">SYNOPSIS</span></span>
<span data-ttu-id="167a9-103">Dodaje klucz tajny do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="167a9-103">Adds a secret to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="167a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="167a9-104">SYNTAX</span></span>

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [<CommonParameters>]
```

## <span data-ttu-id="167a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="167a9-105">DESCRIPTION</span></span>
<span data-ttu-id="167a9-106">Polecenie cmdlet **Add-AzureRmVMSecret** umożliwia dodanie klucza tajnego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="167a9-106">The **Add-AzureRmVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="167a9-107">Ta wartość umożliwia dodanie certyfikatu do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="167a9-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="167a9-108">Klucz tajny musi być przechowywany w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="167a9-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="167a9-109">Aby uzyskać więcej informacji na temat magazynu kluczy, zobacz [co to jest magazyn kluczy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="167a9-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="167a9-110">Aby uzyskać więcej informacji na temat poleceń cmdlet, zobacz [polecenia cmdlet magazynu kluczy platformy Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) w bibliotece sieci Microsoft Developer Network lub polecenia cmdlet [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="167a9-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="167a9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="167a9-111">EXAMPLES</span></span>

### <span data-ttu-id="167a9-112">Przykład 1: Dodawanie klucza tajnego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="167a9-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="167a9-113">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="167a9-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="167a9-114">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="167a9-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="167a9-115">Drugie polecenie tworzy obiekt Credential, korzystając z polecenia cmdlet Get-Credential, a następnie zapisuje wynik w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="167a9-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="167a9-116">Polecenie monituje o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="167a9-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="167a9-117">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="167a9-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="167a9-118">W trzecim poleceniu jest używana funkcja cmdlet **Set-AzureRmVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="167a9-118">The third command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="167a9-119">Czwarte polecenie przypisuje identyfikator magazynu źródłowego do zmiennej $SourceVaultId w celu późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="167a9-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="167a9-120">W poleceniu przyjęto założenie, że zmienna $SubscriptionId ma odpowiednią wartość.</span><span class="sxs-lookup"><span data-stu-id="167a9-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="167a9-121">Piąte polecenie przypisuje wartość zmiennej $CertificateStore 01 do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="167a9-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="167a9-122">Po szóstym poleceniu jest przypisywany adres URL magazynu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="167a9-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="167a9-123">Polecenie siódme powoduje dodanie klucza tajnego do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="167a9-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="167a9-124">Parametr SourceVaultId określa Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="167a9-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="167a9-125">Polecenie określa nazwę magazynu certyfikatów oraz adres URL certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="167a9-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="167a9-126">Możesz wielokrotnie uruchamiać **dodatek Add-AzureRmVMSecret** , aby dodać klucze tajne dla innych certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="167a9-126">You can run the **Add-AzureRmVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="167a9-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="167a9-127">PARAMETERS</span></span>

### <span data-ttu-id="167a9-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="167a9-128">-CertificateStore</span></span>
<span data-ttu-id="167a9-129">Określa nazwę magazynu certyfikatów na maszynie wirtualnej z uruchomionym systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="167a9-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="167a9-130">To polecenie cmdlet umożliwia dodanie certyfikatu do magazynu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="167a9-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="167a9-131">Ten parametr można określić tylko dla maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="167a9-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167a9-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="167a9-132">-CertificateUrl</span></span>
<span data-ttu-id="167a9-133">Określa adres URL wskazujący klucz tajny magazynu kluczy zawierający certyfikat.</span><span class="sxs-lookup"><span data-stu-id="167a9-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="167a9-134">Certyfikat jest kodowaniem Base64 następującego obiektu notacji języka JavaScript (JSON), który jest kodowany w formacie UTF-8:</span><span class="sxs-lookup"><span data-stu-id="167a9-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="167a9-135">{"dane": " \<Base64-encoded-file\> ", "DataType": " \<file-format\> ", "hasło": "" \<pfx-file-password\> }</span><span class="sxs-lookup"><span data-stu-id="167a9-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="167a9-136">Obecnie typ danych akceptuje tylko pliki PFX.</span><span class="sxs-lookup"><span data-stu-id="167a9-136">Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167a9-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="167a9-137">-SourceVaultId</span></span>
<span data-ttu-id="167a9-138">Określa identyfikator zasobu magazynu kluczy zawierającego certyfikaty, które można dodać do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="167a9-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="167a9-139">Ta wartość działa także jako klucz do dodawania wielu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="167a9-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="167a9-140">Oznacza to, że przy dodawaniu wielu certyfikatów z tego samego magazynu kluczy można użyć tej samej wartości dla *SourceVaultId* .</span><span class="sxs-lookup"><span data-stu-id="167a9-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167a9-141">-VM</span><span class="sxs-lookup"><span data-stu-id="167a9-141">-VM</span></span>
<span data-ttu-id="167a9-142">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="167a9-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="167a9-143">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="167a9-143">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="167a9-144">Za pomocą polecenia cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) można utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="167a9-144">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="167a9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167a9-145">CommonParameters</span></span>
<span data-ttu-id="167a9-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="167a9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167a9-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="167a9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167a9-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="167a9-148">INPUTS</span></span>

### <span data-ttu-id="167a9-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="167a9-149">None</span></span>
<span data-ttu-id="167a9-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="167a9-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="167a9-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="167a9-151">OUTPUTS</span></span>

## <span data-ttu-id="167a9-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="167a9-152">NOTES</span></span>

## <span data-ttu-id="167a9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="167a9-153">RELATED LINKS</span></span>

[<span data-ttu-id="167a9-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="167a9-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="167a9-155">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="167a9-155">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="167a9-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="167a9-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)
