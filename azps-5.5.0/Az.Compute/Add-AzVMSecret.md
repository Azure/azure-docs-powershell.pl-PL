---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199362"
---
# <span data-ttu-id="11e60-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="11e60-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="11e60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11e60-102">SYNOPSIS</span></span>
<span data-ttu-id="11e60-103">Dodaje klucz tajny do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="11e60-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="11e60-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11e60-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11e60-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="11e60-105">DESCRIPTION</span></span>
<span data-ttu-id="11e60-106">Polecenie **cmdlet Add-AzVMSecret** dodaje klucz tajny do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="11e60-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="11e60-107">Ta wartość umożliwia dodanie certyfikatu do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="11e60-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="11e60-108">Klucz tajny musi być przechowywany w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="11e60-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="11e60-109">Aby uzyskać więcej informacji na temat magazynu kluczy, zobacz [Co to jest magazyn kluczy platformy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="11e60-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="11e60-110">Aby uzyskać więcej informacji o poleceniach cmdlet, zobacz polecenia [cmdlet](/powershell/module/az.keyvault) magazynu kluczy platformy Azure lub polecenie cmdlet [Set-AzKeyVaultSecret.](/powershell/module/az.keyvault/set-azkeyvaultsecret)</span><span class="sxs-lookup"><span data-stu-id="11e60-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="11e60-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11e60-111">EXAMPLES</span></span>

### <span data-ttu-id="11e60-112">Przykład 1. Dodawanie tajemnicy do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="11e60-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="11e60-113">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="11e60-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="11e60-114">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="11e60-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="11e60-115">Drugie polecenie tworzy obiekt poświadczeń przy użyciu Get-Credential cmdlet, a następnie zapisuje wynik w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="11e60-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="11e60-116">Polecenie monituje o nazwę użytkownika i hasło.</span><span class="sxs-lookup"><span data-stu-id="11e60-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="11e60-117">Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="11e60-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="11e60-118">Trzecie polecenie używa **polecenia cmdlet Set-AzVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="11e60-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="11e60-119">Czwarte polecenie przypisuje identyfikator magazynu źródłowego do zmiennej $SourceVaultId do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="11e60-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="11e60-120">W tym poleceniu założono, że $SubscriptionId zmienna ma odpowiednią wartość.</span><span class="sxs-lookup"><span data-stu-id="11e60-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="11e60-121">Piąte polecenie przypisuje wartość do zmiennej $CertificateStore 01 do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="11e60-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="11e60-122">Szóste polecenie przypisuje adres URL magazynu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="11e60-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="11e60-123">Siódme polecenie dodaje klucz tajny do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="11e60-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="11e60-124">Parametr SourceVaultId określa magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="11e60-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="11e60-125">To polecenie określa nazwę magazynu certyfikatów i adres URL certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="11e60-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="11e60-126">Dodatek **AzVMSecret można wielokrotnie uruchamiać** w celu dodania sekretów innych certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="11e60-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="11e60-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11e60-127">PARAMETERS</span></span>

### <span data-ttu-id="11e60-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="11e60-128">-CertificateStore</span></span>
<span data-ttu-id="11e60-129">Określa nazwę magazynu certyfikatów na maszyny wirtualnej, na których działa system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="11e60-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="11e60-130">To polecenie cmdlet dodaje certyfikat do magazynu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="11e60-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="11e60-131">Ten parametr można określić tylko dla maszyn wirtualnych, na których działa system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="11e60-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="11e60-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="11e60-132">-CertificateUrl</span></span>
<span data-ttu-id="11e60-133">Określa adres URL, który wskazuje klucz tajny magazynu kluczy, który zawiera certyfikat.</span><span class="sxs-lookup"><span data-stu-id="11e60-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="11e60-134">Certyfikat jest kodowaniem Base64 następującego obiektu JavaScript Object Notation (JSON), który jest kodowany w formacie UTF-8: { "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", ","password": " } Obecnie typ danych akceptuje tylko pliki \<pfx-file-password\> pfx.</span><span class="sxs-lookup"><span data-stu-id="11e60-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="11e60-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e60-135">-DefaultProfile</span></span>
<span data-ttu-id="11e60-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11e60-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11e60-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="11e60-137">-SourceVaultId</span></span>
<span data-ttu-id="11e60-138">Określa identyfikator zasobu magazynu kluczy zawierający certyfikaty, które można dodać do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="11e60-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="11e60-139">Ta wartość jest również kluczem do dodawania wielu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="11e60-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="11e60-140">Oznacza to, że można użyć tej samej wartości dla wartości *SourceVaultId* podczas dodawania wielu certyfikatów z tego samego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="11e60-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="11e60-141">- MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="11e60-141">-VM</span></span>
<span data-ttu-id="11e60-142">Określa obiekt maszyny wirtualnej, który zostanie zmodyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e60-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="11e60-143">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="11e60-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="11e60-144">Aby utworzyć obiekt maszyny wirtualnej, możesz użyć polecenia cmdlet [New-AzVMConfig.](./New-AzVMConfig.md)</span><span class="sxs-lookup"><span data-stu-id="11e60-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="11e60-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e60-145">CommonParameters</span></span>
<span data-ttu-id="11e60-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e60-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e60-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11e60-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e60-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11e60-148">INPUTS</span></span>

### <span data-ttu-id="11e60-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="11e60-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="11e60-150">System.String</span><span class="sxs-lookup"><span data-stu-id="11e60-150">System.String</span></span>

## <span data-ttu-id="11e60-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11e60-151">OUTPUTS</span></span>

### <span data-ttu-id="11e60-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="11e60-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="11e60-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11e60-153">NOTES</span></span>

## <span data-ttu-id="11e60-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11e60-154">RELATED LINKS</span></span>

[<span data-ttu-id="11e60-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="11e60-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="11e60-156">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="11e60-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="11e60-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="11e60-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
