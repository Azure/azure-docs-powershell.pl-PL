---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395445"
---
# <span data-ttu-id="b7884-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="b7884-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="b7884-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7884-102">SYNOPSIS</span></span>
<span data-ttu-id="b7884-103">Dodaje klucz tajny do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b7884-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="b7884-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7884-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7884-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7884-105">DESCRIPTION</span></span>
<span data-ttu-id="b7884-106">Polecenie cmdlet **Add-AzVMSecret** umożliwia dodanie klucza tajnego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b7884-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="b7884-107">Ta wartość umożliwia dodanie certyfikatu do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b7884-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="b7884-108">Klucz tajny musi być przechowywany w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7884-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="b7884-109">Aby uzyskać więcej informacji na temat magazynu kluczy, zobacz [co to jest magazyn kluczy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="b7884-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="b7884-110">Aby uzyskać więcej informacji na temat poleceń cmdlet, zobacz [polecenia cmdlet magazynu kluczy platformy Azure](/powershell/module/az.keyvault) lub polecenia cmdlet [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="b7884-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="b7884-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7884-111">EXAMPLES</span></span>

### <span data-ttu-id="b7884-112">Przykład 1: Dodawanie klucza tajnego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b7884-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="b7884-113">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b7884-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b7884-114">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b7884-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b7884-115">Drugie polecenie tworzy obiekt Credential, korzystając z polecenia cmdlet Get-Credential, a następnie zapisuje wynik w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="b7884-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="b7884-116">Polecenie monituje o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="b7884-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="b7884-117">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b7884-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="b7884-118">W trzecim poleceniu jest używana funkcja cmdlet **Set-AzVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b7884-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b7884-119">Czwarte polecenie przypisuje identyfikator magazynu źródłowego do zmiennej $SourceVaultId w celu późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="b7884-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="b7884-120">W poleceniu przyjęto założenie, że zmienna $SubscriptionId ma odpowiednią wartość.</span><span class="sxs-lookup"><span data-stu-id="b7884-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="b7884-121">Piąte polecenie przypisuje wartość zmiennej $CertificateStore 01 do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="b7884-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="b7884-122">Po szóstym poleceniu jest przypisywany adres URL magazynu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="b7884-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="b7884-123">Polecenie siódme powoduje dodanie klucza tajnego do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b7884-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b7884-124">Parametr SourceVaultId określa Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7884-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="b7884-125">Polecenie określa nazwę magazynu certyfikatów oraz adres URL certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b7884-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="b7884-126">Możesz wielokrotnie uruchamiać **dodatek Add-AzVMSecret** , aby dodać klucze tajne dla innych certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="b7884-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="b7884-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7884-127">PARAMETERS</span></span>

### <span data-ttu-id="b7884-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="b7884-128">-CertificateStore</span></span>
<span data-ttu-id="b7884-129">Określa nazwę magazynu certyfikatów na maszynie wirtualnej z uruchomionym systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="b7884-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="b7884-130">To polecenie cmdlet umożliwia dodanie certyfikatu do magazynu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b7884-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="b7884-131">Ten parametr można określić tylko dla maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="b7884-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7884-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b7884-132">-CertificateUrl</span></span>
<span data-ttu-id="b7884-133">Określa adres URL wskazujący klucz tajny magazynu kluczy zawierający certyfikat.</span><span class="sxs-lookup"><span data-stu-id="b7884-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="b7884-134">Certyfikat jest kodowaniem Base64 następującego obiektu notacji języka JavaScript (JSON), który jest zakodowany w formacie UTF-8: {"dane": " \<Base64-encoded-file\> ", "typ danych": " \<file-format\> ", "hasło" " \<pfx-file-password\> } obecnie typ danych akceptuje tylko pliki PFX.</span><span class="sxs-lookup"><span data-stu-id="b7884-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7884-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7884-135">-DefaultProfile</span></span>
<span data-ttu-id="b7884-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7884-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7884-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b7884-137">-SourceVaultId</span></span>
<span data-ttu-id="b7884-138">Określa identyfikator zasobu magazynu kluczy zawierającego certyfikaty, które można dodać do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b7884-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="b7884-139">Ta wartość działa także jako klucz do dodawania wielu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="b7884-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="b7884-140">Oznacza to, że przy dodawaniu wielu certyfikatów z tego samego magazynu kluczy można użyć tej samej wartości dla *SourceVaultId* .</span><span class="sxs-lookup"><span data-stu-id="b7884-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7884-141">-VM</span><span class="sxs-lookup"><span data-stu-id="b7884-141">-VM</span></span>
<span data-ttu-id="b7884-142">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7884-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="b7884-143">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="b7884-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="b7884-144">Za pomocą polecenia cmdlet [New-AzVMConfig](./New-AzVMConfig.md) można utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b7884-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7884-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7884-145">CommonParameters</span></span>
<span data-ttu-id="b7884-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7884-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7884-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7884-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7884-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7884-148">INPUTS</span></span>

### <span data-ttu-id="b7884-149">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b7884-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b7884-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b7884-150">System.String</span></span>

## <span data-ttu-id="b7884-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7884-151">OUTPUTS</span></span>

### <span data-ttu-id="b7884-152">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b7884-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b7884-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7884-153">NOTES</span></span>

## <span data-ttu-id="b7884-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7884-154">RELATED LINKS</span></span>

[<span data-ttu-id="b7884-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b7884-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b7884-156">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b7884-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="b7884-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b7884-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
