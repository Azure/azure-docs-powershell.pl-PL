---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 76bdebc68f1fafef127863ef753c28fce7034fe0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898937"
---
# <span data-ttu-id="af8a1-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="af8a1-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="af8a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af8a1-102">SYNOPSIS</span></span>
<span data-ttu-id="af8a1-103">Włączenie szyfrowania na działającej maszynie wirtualnej IaaS na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="af8a1-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af8a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af8a1-104">SYNTAX</span></span>

### <span data-ttu-id="af8a1-105">AADClientSecretParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="af8a1-105">AADClientSecretParameterSet (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af8a1-106">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="af8a1-106">AADClientCertParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af8a1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="af8a1-107">DESCRIPTION</span></span>
<span data-ttu-id="af8a1-108">Polecenie cmdlet **Set-AzureRmVMDiskEncryptionExtension** umożliwia szyfrowanie uruchomionej infrastruktury jako maszyny wirtualnej usługi (IaaS) na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="af8a1-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="af8a1-109">To polecenie cmdlet umożliwia szyfrowanie przez zainstalowanie rozszerzenia szyfrowanie dysków na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="af8a1-110">Jeśli nie podano parametru *name* , zainstalowane jest rozszerzenie o nazwie domyślnej AzureDiskEncryption dla maszyn wirtualnych z uruchomionym systemem operacyjnym Windows lub AzureDiskEncryptionForLinux dla komputerów wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="af8a1-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="af8a1-111">To polecenie cmdlet wymaga potwierdzenia od użytkowników, ponieważ jedna z kroków umożliwiających włączenie szyfrowania wymaga ponownego uruchomienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="af8a1-112">Przed uruchomieniem tego polecenia cmdlet zaleca się zapisanie pracy na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="af8a1-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af8a1-113">EXAMPLES</span></span>

### <span data-ttu-id="af8a1-114">Przykład 1: Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i klucza tajnego klienta</span><span class="sxs-lookup"><span data-stu-id="af8a1-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="af8a1-115">W tym przykładzie funkcja szyfrowania jest włączana przy użyciu identyfikatora klienta usługi Azure AD i klucza tajnego klienta.</span><span class="sxs-lookup"><span data-stu-id="af8a1-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="af8a1-116">Przykład 2: Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i odcisk palca certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="af8a1-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="af8a1-117">W tym przykładzie funkcja szyfrowania jest włączana za pomocą palców o IDENTYFIKATORach klienta usługi Azure AD i certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="af8a1-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="af8a1-118">Przykład 3: Włączanie szyfrowania za pomocą identyfikatora klienta usługi Azure AD, klucza tajnego klienta i Zawijanie klucza szyfrowania dysku przy użyciu klucza szyfrowania kluczy</span><span class="sxs-lookup"><span data-stu-id="af8a1-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="af8a1-119">W tym przykładzie funkcja szyfrowania jest włączana przy użyciu identyfikatora klienta usługi Azure AD, klucza tajnego klienta i zawijania klucza szyfrowania dysku przy użyciu klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="af8a1-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="af8a1-120">Przykład 4: Włączanie szyfrowania za pomocą identyfikatora klienta usługi Azure AD, odcisku palca certyfikatu klienta i Zawijanie EncryptionKey dysków przy użyciu klucza szyfrowania kluczy</span><span class="sxs-lookup"><span data-stu-id="af8a1-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="af8a1-121">W tym przykładzie funkcja szyfrowania jest włączana przy użyciu identyfikatora klienta usługi Azure AD, odcisku palca certyfikatu klienta i zawijania klucza szyfrowania dysku przy użyciu klucza szyfrowania kluczy.</span><span class="sxs-lookup"><span data-stu-id="af8a1-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="af8a1-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af8a1-122">PARAMETERS</span></span>

### <span data-ttu-id="af8a1-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="af8a1-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="af8a1-124">Określa odcisk palca certyfikatu klienta aplikacji katalogu AzureActive (Azure AD), który ma uprawnienia do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="af8a1-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="af8a1-125">Jako warunek wstępny certyfikat klienta usługi Azure AD musi zostać wcześniej wdrożony w magazynie certyfikatów lokalnego komputera maszyny wirtualnej `my` .</span><span class="sxs-lookup"><span data-stu-id="af8a1-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="af8a1-126">Za pomocą polecenia cmdlet Add-AzureRmVMSecret można wdrożyć certyfikat na maszynie wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="af8a1-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="af8a1-127">Aby uzyskać więcej informacji, zobacz Pomoc polecenia cmdlet **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="af8a1-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="af8a1-128">Certyfikat musi być wcześniej wdrożony na komputerze lokalnym maszyny wirtualnej mój magazyn certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="af8a1-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AADClientCertParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="af8a1-129">-AadClientID</span></span>
<span data-ttu-id="af8a1-130">Określa identyfikator klienta aplikacji Azure AD z uprawnieniami do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="af8a1-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="af8a1-131">-AadClientSecret</span></span>
<span data-ttu-id="af8a1-132">Określa klucz tajny klienta aplikacji usługi Azure AD z uprawnieniami do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="af8a1-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AADClientSecretParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af8a1-133">-DefaultProfile</span></span>
<span data-ttu-id="af8a1-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af8a1-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af8a1-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="af8a1-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="af8a1-136">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="af8a1-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="af8a1-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="af8a1-138">Określa identyfikator zasobu **magazynu** kluczy, do którego mają być przekazywane klucze szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="af8a1-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="af8a1-140">Określa adres URL **magazynu** kluczy, do którego mają być przekazywane klucze szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-141">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="af8a1-141">-EncryptFormatAll</span></span>
<span data-ttu-id="af8a1-142">Encrypt-Format wszystkich dysków danych, które nie są jeszcze zaszyfrowane</span><span class="sxs-lookup"><span data-stu-id="af8a1-142">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-143">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="af8a1-143">-ExtensionPublisherName</span></span>
<span data-ttu-id="af8a1-144">Nazwa wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="af8a1-144">The extension publisher name.</span></span> <span data-ttu-id="af8a1-145">Ten parametr można określić tylko w celu zastąpienia wartości domyślnej "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="af8a1-145">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-146">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="af8a1-146">-ExtensionType</span></span>
<span data-ttu-id="af8a1-147">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="af8a1-147">The extension type.</span></span> <span data-ttu-id="af8a1-148">Określ ten parametr, aby zastąpić swoją domyślną wartość "AzureDiskEncryption" dla maszyn wirtualnych systemu Windows i "AzureDiskEncryptionForLinux" dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="af8a1-148">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-149">-Force</span><span class="sxs-lookup"><span data-stu-id="af8a1-149">-Force</span></span>
<span data-ttu-id="af8a1-150">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="af8a1-150">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-151">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="af8a1-151">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="af8a1-152">Określa algorytm używany do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-152">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="af8a1-153">Wartość domyślna to RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="af8a1-153">The default value is RSA-OAEP.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-154">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="af8a1-154">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="af8a1-155">Określa adres URL klucza szyfrowania klucza używanego do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-155">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="af8a1-156">To musi być pełny adres URL w wersji.</span><span class="sxs-lookup"><span data-stu-id="af8a1-156">This must be the full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-157">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="af8a1-157">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="af8a1-158">Określa identyfikator zasobu **magazynu** kluczy zawierającego klucz szyfrowania klucza służący do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-158">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="af8a1-159">To musi być pełny adres URL w wersji.</span><span class="sxs-lookup"><span data-stu-id="af8a1-159">This must be a full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-160">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af8a1-160">-Name</span></span>
<span data-ttu-id="af8a1-161">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="af8a1-161">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="af8a1-162">Wartość domyślna to AzureDiskEncryption dla maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows lub AzureDiskEncryptionForLinux dla komputerów wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="af8a1-162">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-163">— Hasło</span><span class="sxs-lookup"><span data-stu-id="af8a1-163">-Passphrase</span></span>
<span data-ttu-id="af8a1-164">Określa hasło używane do szyfrowania tylko maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="af8a1-164">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="af8a1-165">Ten parametr nie jest używany w przypadku maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="af8a1-165">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af8a1-166">-ResourceGroupName</span></span>
<span data-ttu-id="af8a1-167">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-167">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-168">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="af8a1-168">-SequenceVersion</span></span>
<span data-ttu-id="af8a1-169">Określa numer sekwencji operacji szyfrowania dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-169">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="af8a1-170">Ta funkcja jest unikatowa dla każdej operacji szyfrowania wykonywanej na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-170">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="af8a1-171">Za pomocą polecenia cmdlet Get-AzureRmVMExtension można pobrać poprzedni numer sekwencyjny, którego użyto.</span><span class="sxs-lookup"><span data-stu-id="af8a1-171">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-172">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="af8a1-172">-SkipVmBackup</span></span>
<span data-ttu-id="af8a1-173">Pomijanie tworzenia kopii zapasowych dla maszyn wirtualnych systemu Linux</span><span class="sxs-lookup"><span data-stu-id="af8a1-173">Skip backup creation for Linux VMs</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-174">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="af8a1-174">-TypeHandlerVersion</span></span>
<span data-ttu-id="af8a1-175">Określa wersję rozszerzenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="af8a1-175">Specifies the version of the encryption extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-176">-VMName</span><span class="sxs-lookup"><span data-stu-id="af8a1-176">-VMName</span></span>
<span data-ttu-id="af8a1-177">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af8a1-177">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-178">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="af8a1-178">-VolumeType</span></span>
<span data-ttu-id="af8a1-179">Określa typ woluminów maszyny wirtualnej, które mają wykonać operację szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="af8a1-179">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="af8a1-180">Dozwolone wartości dla maszyn wirtualnych z systemem operacyjnym Windows są następujące: wszystkie, system operacyjny i dane.</span><span class="sxs-lookup"><span data-stu-id="af8a1-180">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="af8a1-181">Dozwolone wartości dla maszyn wirtualnych systemu Linux są następujące: tylko dane.</span><span class="sxs-lookup"><span data-stu-id="af8a1-181">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-182">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af8a1-182">-Confirm</span></span>
<span data-ttu-id="af8a1-183">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af8a1-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af8a1-184">-WhatIf</span></span>
<span data-ttu-id="af8a1-185">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af8a1-185">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="af8a1-186">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af8a1-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8a1-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af8a1-187">CommonParameters</span></span>
<span data-ttu-id="af8a1-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af8a1-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af8a1-189">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af8a1-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af8a1-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af8a1-190">INPUTS</span></span>

### <span data-ttu-id="af8a1-191">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="af8a1-191">None</span></span>
<span data-ttu-id="af8a1-192">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="af8a1-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af8a1-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af8a1-193">OUTPUTS</span></span>

### <span data-ttu-id="af8a1-194">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="af8a1-194">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="af8a1-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af8a1-195">NOTES</span></span>

## <span data-ttu-id="af8a1-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af8a1-196">RELATED LINKS</span></span>

[<span data-ttu-id="af8a1-197">Dodaj-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="af8a1-197">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="af8a1-198">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="af8a1-198">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="af8a1-199">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="af8a1-199">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


