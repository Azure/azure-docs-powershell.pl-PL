---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 782ad8dbc5dc795503b314bfaf890a705774be4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525710"
---
# <span data-ttu-id="181b5-101">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="181b5-101">Add-AzureRmVMSecret</span></span>

## <span data-ttu-id="181b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="181b5-102">SYNOPSIS</span></span>
<span data-ttu-id="181b5-103">Dodaje klucz tajny do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="181b5-103">Adds a secret to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="181b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="181b5-104">SYNTAX</span></span>

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181b5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="181b5-105">DESCRIPTION</span></span>
<span data-ttu-id="181b5-106">Polecenie cmdlet **Add-AzureRmVMSecret** umożliwia dodanie klucza tajnego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="181b5-106">The **Add-AzureRmVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="181b5-107">Ta wartość umożliwia dodanie certyfikatu do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="181b5-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="181b5-108">Klucz tajny musi być przechowywany w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="181b5-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="181b5-109">Aby uzyskać więcej informacji na temat magazynu kluczy, zobacz [co to jest magazyn kluczy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="181b5-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="181b5-110">Aby uzyskać więcej informacji na temat poleceń cmdlet, zobacz [polecenia cmdlet magazynu kluczy platformy Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) w bibliotece sieci Microsoft Developer Network lub polecenia cmdlet [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="181b5-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="181b5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="181b5-111">EXAMPLES</span></span>

### <span data-ttu-id="181b5-112">Przykład 1: Dodawanie klucza tajnego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="181b5-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="181b5-113">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="181b5-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="181b5-114">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="181b5-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="181b5-115">Drugie polecenie tworzy obiekt Credential, korzystając z polecenia cmdlet Get-Credential, a następnie zapisuje wynik w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="181b5-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="181b5-116">Polecenie monituje o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="181b5-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="181b5-117">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="181b5-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="181b5-118">W trzecim poleceniu jest używana funkcja cmdlet **Set-AzureRmVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="181b5-118">The third command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="181b5-119">Czwarte polecenie przypisuje identyfikator magazynu źródłowego do zmiennej $SourceVaultId w celu późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="181b5-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="181b5-120">W poleceniu przyjęto założenie, że zmienna $SubscriptionId ma odpowiednią wartość.</span><span class="sxs-lookup"><span data-stu-id="181b5-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="181b5-121">Piąte polecenie przypisuje wartość zmiennej $CertificateStore 01 do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="181b5-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="181b5-122">Po szóstym poleceniu jest przypisywany adres URL magazynu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="181b5-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="181b5-123">Polecenie siódme powoduje dodanie klucza tajnego do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="181b5-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="181b5-124">Parametr SourceVaultId określa Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="181b5-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="181b5-125">Polecenie określa nazwę magazynu certyfikatów oraz adres URL certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="181b5-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="181b5-126">Możesz wielokrotnie uruchamiać **dodatek Add-AzureRmVMSecret** , aby dodać klucze tajne dla innych certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="181b5-126">You can run the **Add-AzureRmVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="181b5-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="181b5-127">PARAMETERS</span></span>

### <span data-ttu-id="181b5-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="181b5-128">-CertificateStore</span></span>
<span data-ttu-id="181b5-129">Określa nazwę magazynu certyfikatów na maszynie wirtualnej z uruchomionym systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="181b5-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="181b5-130">To polecenie cmdlet umożliwia dodanie certyfikatu do magazynu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="181b5-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="181b5-131">Ten parametr można określić tylko dla maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="181b5-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="181b5-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="181b5-132">-CertificateUrl</span></span>
<span data-ttu-id="181b5-133">Określa adres URL wskazujący klucz tajny magazynu kluczy zawierający certyfikat.</span><span class="sxs-lookup"><span data-stu-id="181b5-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="181b5-134">Certyfikat jest kodowaniem Base64 następującego obiektu notacji języka JavaScript (JSON), który jest kodowany w formacie UTF-8:</span><span class="sxs-lookup"><span data-stu-id="181b5-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="181b5-135">{"dane": " \<Base64-encoded-file\> ", "DataType": " \<file-format\> ", "hasło": "" \<pfx-file-password\> }</span><span class="sxs-lookup"><span data-stu-id="181b5-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="181b5-136">Obecnie typ danych akceptuje tylko pliki PFX.</span><span class="sxs-lookup"><span data-stu-id="181b5-136">Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="181b5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181b5-137">-DefaultProfile</span></span>
<span data-ttu-id="181b5-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="181b5-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="181b5-139">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="181b5-139">-SourceVaultId</span></span>
<span data-ttu-id="181b5-140">Określa identyfikator zasobu magazynu kluczy zawierającego certyfikaty, które można dodać do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="181b5-140">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="181b5-141">Ta wartość działa także jako klucz do dodawania wielu certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="181b5-141">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="181b5-142">Oznacza to, że przy dodawaniu wielu certyfikatów z tego samego magazynu kluczy można użyć tej samej wartości dla *SourceVaultId* .</span><span class="sxs-lookup"><span data-stu-id="181b5-142">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="181b5-143">-VM</span><span class="sxs-lookup"><span data-stu-id="181b5-143">-VM</span></span>
<span data-ttu-id="181b5-144">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="181b5-144">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="181b5-145">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="181b5-145">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="181b5-146">Za pomocą polecenia cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) można utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="181b5-146">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="181b5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181b5-147">CommonParameters</span></span>
<span data-ttu-id="181b5-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181b5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181b5-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181b5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181b5-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="181b5-150">INPUTS</span></span>

### <span data-ttu-id="181b5-151">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="181b5-151">PSVirtualMachine</span></span>
<span data-ttu-id="181b5-152">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="181b5-152">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="181b5-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="181b5-153">OUTPUTS</span></span>

### <span data-ttu-id="181b5-154">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="181b5-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="181b5-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="181b5-155">NOTES</span></span>

## <span data-ttu-id="181b5-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="181b5-156">RELATED LINKS</span></span>

[<span data-ttu-id="181b5-157">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="181b5-157">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="181b5-158">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="181b5-158">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="181b5-159">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="181b5-159">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)
