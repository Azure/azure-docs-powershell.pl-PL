---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: ed18e7de10df5762309f3bcd4ddf6dcee7ee1b94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717220"
---
# <span data-ttu-id="1b148-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1b148-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="1b148-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b148-102">SYNOPSIS</span></span>
<span data-ttu-id="1b148-103">Włączenie szyfrowania na działającej maszynie wirtualnej IaaS na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1b148-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b148-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b148-104">SYNTAX</span></span>

### <span data-ttu-id="1b148-105">Parametry tajne klienta usługi AAD (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1b148-105">AAD Client Secret Parameters (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b148-106">Parametry certyfikatu klienta usługi AAD</span><span class="sxs-lookup"><span data-stu-id="1b148-106">AAD Client Cert Parameters</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b148-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1b148-107">DESCRIPTION</span></span>
<span data-ttu-id="1b148-108">Polecenie cmdlet **Set-AzureRmVMDiskEncryptionExtension** umożliwia szyfrowanie uruchomionej infrastruktury jako maszyny wirtualnej usługi (IaaS) na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1b148-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="1b148-109">To polecenie cmdlet umożliwia szyfrowanie przez zainstalowanie rozszerzenia szyfrowanie dysków na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="1b148-110">Jeśli nie podano parametru *name* , zainstalowane jest rozszerzenie o nazwie domyślnej AzureDiskEncryption dla maszyn wirtualnych z uruchomionym systemem operacyjnym Windows lub AzureDiskEncryptionForLinux dla komputerów wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="1b148-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="1b148-111">To polecenie cmdlet wymaga potwierdzenia od użytkowników, ponieważ jedna z kroków umożliwiających włączenie szyfrowania wymaga ponownego uruchomienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="1b148-112">Przed uruchomieniem tego polecenia cmdlet zaleca się zapisanie pracy na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="1b148-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b148-113">EXAMPLES</span></span>

### <span data-ttu-id="1b148-114">Przykład 1: Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i klucza tajnego klienta</span><span class="sxs-lookup"><span data-stu-id="1b148-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="1b148-115">W tym przykładzie funkcja szyfrowania jest włączana przy użyciu identyfikatora klienta usługi Azure AD i klucza tajnego klienta.</span><span class="sxs-lookup"><span data-stu-id="1b148-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="1b148-116">Przykład 2: Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i odcisk palca certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="1b148-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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

<span data-ttu-id="1b148-117">W tym przykładzie funkcja szyfrowania jest włączana za pomocą palców o IDENTYFIKATORach klienta usługi Azure AD i certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="1b148-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="1b148-118">Przykład 3: Włączanie szyfrowania za pomocą identyfikatora klienta usługi Azure AD, klucza tajnego klienta i Zawijanie klucza szyfrowania dysku przy użyciu klucza szyfrowania kluczy</span><span class="sxs-lookup"><span data-stu-id="1b148-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
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

<span data-ttu-id="1b148-119">W tym przykładzie funkcja szyfrowania jest włączana przy użyciu identyfikatora klienta usługi Azure AD, klucza tajnego klienta i zawijania klucza szyfrowania dysku przy użyciu klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="1b148-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="1b148-120">Przykład 4: Włączanie szyfrowania za pomocą identyfikatora klienta usługi Azure AD, odcisku palca certyfikatu klienta i Zawijanie EncryptionKey dysków przy użyciu klucza szyfrowania kluczy</span><span class="sxs-lookup"><span data-stu-id="1b148-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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

<span data-ttu-id="1b148-121">W tym przykładzie funkcja szyfrowania jest włączana przy użyciu identyfikatora klienta usługi Azure AD, odcisku palca certyfikatu klienta i zawijania klucza szyfrowania dysku przy użyciu klucza szyfrowania kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b148-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="1b148-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b148-122">PARAMETERS</span></span>

### <span data-ttu-id="1b148-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="1b148-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="1b148-124">Określa odcisk palca certyfikatu klienta aplikacji katalogu AzureActive (Azure AD), który ma uprawnienia do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b148-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="1b148-125">Jako warunek wstępny certyfikat klienta usługi Azure AD musi zostać wcześniej wdrożony w magazynie certyfikatów lokalnego komputera maszyny wirtualnej `my` .</span><span class="sxs-lookup"><span data-stu-id="1b148-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="1b148-126">Za pomocą polecenia cmdlet Add-AzureRmVMSecret można wdrożyć certyfikat na maszynie wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1b148-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="1b148-127">Aby uzyskać więcej informacji, zobacz Pomoc polecenia cmdlet **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="1b148-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="1b148-128">Certyfikat musi być wcześniej wdrożony na komputerze lokalnym maszyny wirtualnej mój magazyn certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="1b148-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AAD Client Cert Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b148-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="1b148-129">-AadClientID</span></span>
<span data-ttu-id="1b148-130">Określa identyfikator klienta aplikacji Azure AD z uprawnieniami do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b148-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="1b148-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="1b148-131">-AadClientSecret</span></span>
<span data-ttu-id="1b148-132">Określa klucz tajny klienta aplikacji usługi Azure AD z uprawnieniami do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b148-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AAD Client Secret Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b148-133">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1b148-133">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1b148-134">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1b148-134">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="1b148-135">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1b148-135">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="1b148-136">Określa identyfikator zasobu **magazynu** kluczy, do którego mają być przekazywane klucze szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-136">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="1b148-137">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="1b148-137">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="1b148-138">Określa adres URL **magazynu** kluczy, do którego mają być przekazywane klucze szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-138">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="1b148-139">-Force</span><span class="sxs-lookup"><span data-stu-id="1b148-139">-Force</span></span>
<span data-ttu-id="1b148-140">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1b148-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1b148-141">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1b148-141">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="1b148-142">Określa algorytm używany do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-142">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="1b148-143">Wartość domyślna to RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="1b148-143">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="1b148-144">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="1b148-144">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="1b148-145">Określa adres URL klucza szyfrowania klucza używanego do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-145">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="1b148-146">To musi być pełny adres URL w wersji.</span><span class="sxs-lookup"><span data-stu-id="1b148-146">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="1b148-147">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1b148-147">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="1b148-148">Określa identyfikator zasobu **magazynu** kluczy zawierającego klucz szyfrowania klucza służący do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-148">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="1b148-149">To musi być pełny adres URL w wersji.</span><span class="sxs-lookup"><span data-stu-id="1b148-149">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="1b148-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b148-150">-Name</span></span>
<span data-ttu-id="1b148-151">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="1b148-151">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="1b148-152">Wartość domyślna to AzureDiskEncryption dla maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows lub AzureDiskEncryptionForLinux dla komputerów wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="1b148-152">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

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

### <span data-ttu-id="1b148-153">— Hasło</span><span class="sxs-lookup"><span data-stu-id="1b148-153">-Passphrase</span></span>
<span data-ttu-id="1b148-154">Określa hasło używane do szyfrowania tylko maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="1b148-154">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="1b148-155">Ten parametr nie jest używany w przypadku maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="1b148-155">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="1b148-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b148-156">-ResourceGroupName</span></span>
<span data-ttu-id="1b148-157">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-157">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1b148-158">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="1b148-158">-SequenceVersion</span></span>
<span data-ttu-id="1b148-159">Określa numer sekwencji operacji szyfrowania dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-159">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="1b148-160">Ta funkcja jest unikatowa dla każdej operacji szyfrowania wykonywanej na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-160">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="1b148-161">Za pomocą polecenia cmdlet Get-AzureRmVMExtension można pobrać poprzedni numer sekwencyjny, którego użyto.</span><span class="sxs-lookup"><span data-stu-id="1b148-161">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="1b148-162">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="1b148-162">-SkipVmBackup</span></span>
<span data-ttu-id="1b148-163">Pomijanie tworzenia kopii zapasowych dla maszyn wirtualnych systemu Linux</span><span class="sxs-lookup"><span data-stu-id="1b148-163">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="1b148-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1b148-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="1b148-165">Określa wersję rozszerzenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="1b148-165">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="1b148-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="1b148-166">-VMName</span></span>
<span data-ttu-id="1b148-167">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b148-167">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="1b148-168">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="1b148-168">-VolumeType</span></span>
<span data-ttu-id="1b148-169">Określa typ woluminów maszyny wirtualnej, które mają wykonać operację szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="1b148-169">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="1b148-170">Dozwolone wartości dla maszyn wirtualnych z systemem operacyjnym Windows są następujące: wszystkie, system operacyjny i dane.</span><span class="sxs-lookup"><span data-stu-id="1b148-170">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="1b148-171">Dozwolone wartości dla maszyn wirtualnych systemu Linux są następujące: tylko dane.</span><span class="sxs-lookup"><span data-stu-id="1b148-171">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

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

### <span data-ttu-id="1b148-172">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b148-172">-Confirm</span></span>
<span data-ttu-id="1b148-173">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b148-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b148-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b148-174">-WhatIf</span></span>
<span data-ttu-id="1b148-175">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b148-175">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1b148-176">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b148-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b148-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b148-177">CommonParameters</span></span>
<span data-ttu-id="1b148-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b148-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b148-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b148-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b148-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b148-180">INPUTS</span></span>

### <span data-ttu-id="1b148-181">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1b148-181">None</span></span>
<span data-ttu-id="1b148-182">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1b148-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b148-183">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b148-183">OUTPUTS</span></span>

## <span data-ttu-id="1b148-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b148-184">NOTES</span></span>

## <span data-ttu-id="1b148-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b148-185">RELATED LINKS</span></span>

[<span data-ttu-id="1b148-186">Dodaj-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="1b148-186">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="1b148-187">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="1b148-187">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="1b148-188">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1b148-188">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


