---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: da50845ff5012d466eed0c68103cdbd0baea4e7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868887"
---
# <span data-ttu-id="0d55a-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0d55a-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="0d55a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d55a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d55a-103">Włączenie szyfrowania na działającej maszynie wirtualnej IaaS na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0d55a-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="0d55a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d55a-104">SYNTAX</span></span>

### <span data-ttu-id="0d55a-105">SinglePassParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0d55a-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d55a-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d55a-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d55a-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d55a-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d55a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0d55a-108">DESCRIPTION</span></span>
<span data-ttu-id="0d55a-109">Polecenie cmdlet **Set-AzVMDiskEncryptionExtension** umożliwia szyfrowanie uruchomionej infrastruktury jako maszyny wirtualnej usługi (IaaS) na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0d55a-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="0d55a-110">To polecenie cmdlet umożliwia szyfrowanie przez zainstalowanie rozszerzenia szyfrowanie dysków na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="0d55a-111">Jeśli nie podano parametru *name* , zainstalowane jest rozszerzenie o nazwie domyślnej AzureDiskEncryption dla maszyn wirtualnych z uruchomionym systemem operacyjnym Windows lub AzureDiskEncryptionForLinux dla komputerów wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="0d55a-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="0d55a-112">To polecenie cmdlet wymaga potwierdzenia od użytkowników, ponieważ jedna z kroków umożliwiających włączenie szyfrowania wymaga ponownego uruchomienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="0d55a-113">Przed uruchomieniem tego polecenia cmdlet zaleca się zapisanie pracy na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="0d55a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d55a-114">EXAMPLES</span></span>

### <span data-ttu-id="0d55a-115">Przykład 1: Włączanie szyfrowania</span><span class="sxs-lookup"><span data-stu-id="0d55a-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="0d55a-116">W tym przykładzie przedstawiono Włączanie szyfrowania bez określania poświadczeń usługi AD.</span><span class="sxs-lookup"><span data-stu-id="0d55a-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>   

### <span data-ttu-id="0d55a-117">Przykład 2: Włączanie szyfrowania przy użyciu danych wejściowych potokowych</span><span class="sxs-lookup"><span data-stu-id="0d55a-117">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="0d55a-118">W tym przykładzie pokazano, jak wysłać parametry za pomocą wejścia potokowego, aby włączyć szyfrowanie bez określania poświadczeń usługi AD.</span><span class="sxs-lookup"><span data-stu-id="0d55a-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>  

### <span data-ttu-id="0d55a-119">Przykład 3: Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i klucza tajnego klienta</span><span class="sxs-lookup"><span data-stu-id="0d55a-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="0d55a-120">W tym przykładzie funkcja szyfrowania jest włączana przy użyciu identyfikatora klienta usługi Azure AD i klucza tajnego klienta.</span><span class="sxs-lookup"><span data-stu-id="0d55a-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="0d55a-121">Przykład 4: Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i odcisk palca certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="0d55a-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="0d55a-122">W tym przykładzie funkcja szyfrowania jest włączana za pomocą palców o IDENTYFIKATORach klienta usługi Azure AD i certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="0d55a-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="0d55a-123">Przykład 5: Włączanie szyfrowania za pomocą identyfikatora klienta usługi Azure AD, klucza tajnego klienta i Zawijanie klucza szyfrowania dysku przy użyciu klucza szyfrowania kluczy</span><span class="sxs-lookup"><span data-stu-id="0d55a-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="0d55a-124">W tym przykładzie funkcja szyfrowania jest włączana przy użyciu identyfikatora klienta usługi Azure AD, klucza tajnego klienta i zawijania klucza szyfrowania dysku przy użyciu klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="0d55a-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="0d55a-125">Przykład 6: Włączanie szyfrowania za pomocą identyfikatora klienta usługi Azure AD, odcisku palca certyfikatu klienta i Zawijanie EncryptionKey dysków przy użyciu klucza szyfrowania kluczy</span><span class="sxs-lookup"><span data-stu-id="0d55a-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="0d55a-126">W tym przykładzie funkcja szyfrowania jest włączana przy użyciu identyfikatora klienta usługi Azure AD, odcisku palca certyfikatu klienta i zawijania klucza szyfrowania dysku przy użyciu klucza szyfrowania kluczy.</span><span class="sxs-lookup"><span data-stu-id="0d55a-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="0d55a-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d55a-127">PARAMETERS</span></span>

### <span data-ttu-id="0d55a-128">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="0d55a-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="0d55a-129">Określa odcisk palca certyfikatu klienta aplikacji katalogu AzureActive (Azure AD), który ma uprawnienia do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="0d55a-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="0d55a-130">Jako warunek wstępny certyfikat klienta usługi Azure AD musi zostać wcześniej wdrożony w magazynie certyfikatów lokalnego komputera maszyny wirtualnej `my` .</span><span class="sxs-lookup"><span data-stu-id="0d55a-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="0d55a-131">Za pomocą polecenia cmdlet Add-AzVMSecret można wdrożyć certyfikat na maszynie wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0d55a-131">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="0d55a-132">Aby uzyskać więcej informacji, zobacz Pomoc polecenia cmdlet **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="0d55a-132">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="0d55a-133">Certyfikat musi być wcześniej wdrożony na komputerze lokalnym maszyny wirtualnej mój magazyn certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="0d55a-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-134">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="0d55a-134">-AadClientID</span></span>
<span data-ttu-id="0d55a-135">Określa identyfikator klienta aplikacji Azure AD z uprawnieniami do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="0d55a-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="0d55a-136">-AadClientSecret</span></span>
<span data-ttu-id="0d55a-137">Określa klucz tajny klienta aplikacji usługi Azure AD z uprawnieniami do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="0d55a-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d55a-138">-DefaultProfile</span></span>
<span data-ttu-id="0d55a-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d55a-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d55a-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0d55a-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0d55a-141">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0d55a-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0d55a-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="0d55a-143">Określa identyfikator zasobu **magazynu** kluczy, do którego mają być przekazywane klucze szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="0d55a-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="0d55a-145">Określa adres URL **magazynu** kluczy, do którego mają być przekazywane klucze szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="0d55a-146">-EncryptFormatAll</span></span>
<span data-ttu-id="0d55a-147">Encrypt-Format wszystkich dysków danych, które nie są jeszcze zaszyfrowane</span><span class="sxs-lookup"><span data-stu-id="0d55a-147">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-148">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="0d55a-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="0d55a-149">Nazwa wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0d55a-149">The extension publisher name.</span></span> <span data-ttu-id="0d55a-150">Ten parametr można określić tylko w celu zastąpienia wartości domyślnej "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="0d55a-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="0d55a-151">-ExtensionType</span></span>
<span data-ttu-id="0d55a-152">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0d55a-152">The extension type.</span></span> <span data-ttu-id="0d55a-153">Określ ten parametr, aby zastąpić swoją domyślną wartość "AzureDiskEncryption" dla maszyn wirtualnych systemu Windows i "AzureDiskEncryptionForLinux" dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="0d55a-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-154">-Force</span><span class="sxs-lookup"><span data-stu-id="0d55a-154">-Force</span></span>
<span data-ttu-id="0d55a-155">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0d55a-155">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-156">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0d55a-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="0d55a-157">Określa algorytm używany do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="0d55a-158">Wartość domyślna to RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="0d55a-158">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="0d55a-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="0d55a-160">Określa adres URL klucza szyfrowania klucza używanego do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="0d55a-161">To musi być pełny adres URL w wersji.</span><span class="sxs-lookup"><span data-stu-id="0d55a-161">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0d55a-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="0d55a-163">Określa identyfikator zasobu **magazynu** kluczy zawierającego klucz szyfrowania klucza służący do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="0d55a-164">To musi być pełny adres URL w wersji.</span><span class="sxs-lookup"><span data-stu-id="0d55a-164">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-165">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d55a-165">-Name</span></span>
<span data-ttu-id="0d55a-166">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="0d55a-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="0d55a-167">Wartość domyślna to AzureDiskEncryption dla maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows lub AzureDiskEncryptionForLinux dla komputerów wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="0d55a-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-168">— Hasło</span><span class="sxs-lookup"><span data-stu-id="0d55a-168">-Passphrase</span></span>
<span data-ttu-id="0d55a-169">Określa hasło używane do szyfrowania tylko maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="0d55a-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="0d55a-170">Ten parametr nie jest używany w przypadku maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="0d55a-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d55a-171">-ResourceGroupName</span></span>
<span data-ttu-id="0d55a-172">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-172">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="0d55a-173">-SequenceVersion</span></span>
<span data-ttu-id="0d55a-174">Określa numer sekwencji operacji szyfrowania dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="0d55a-175">Ta funkcja jest unikatowa dla każdej operacji szyfrowania wykonywanej na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="0d55a-176">Za pomocą polecenia cmdlet Get-AzVMExtension można pobrać poprzedni numer sekwencyjny, którego użyto.</span><span class="sxs-lookup"><span data-stu-id="0d55a-176">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="0d55a-177">-SkipVmBackup</span></span>
<span data-ttu-id="0d55a-178">Pomijanie tworzenia kopii zapasowych dla maszyn wirtualnych systemu Linux</span><span class="sxs-lookup"><span data-stu-id="0d55a-178">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0d55a-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="0d55a-180">Określa wersję rozszerzenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="0d55a-180">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="0d55a-181">-VMName</span></span>
<span data-ttu-id="0d55a-182">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d55a-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-183">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="0d55a-183">-VolumeType</span></span>
<span data-ttu-id="0d55a-184">Określa typ woluminów maszyny wirtualnej, które mają wykonać operację szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="0d55a-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="0d55a-185">Dozwolone wartości dla maszyn wirtualnych z systemem operacyjnym Windows są następujące: wszystkie, system operacyjny i dane.</span><span class="sxs-lookup"><span data-stu-id="0d55a-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="0d55a-186">Dozwolone wartości dla maszyn wirtualnych systemu Linux są następujące: tylko dane.</span><span class="sxs-lookup"><span data-stu-id="0d55a-186">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-187">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d55a-187">-Confirm</span></span>
<span data-ttu-id="0d55a-188">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d55a-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d55a-189">-WhatIf</span></span>
<span data-ttu-id="0d55a-190">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d55a-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d55a-191">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d55a-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d55a-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d55a-192">CommonParameters</span></span>
<span data-ttu-id="0d55a-193">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d55a-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d55a-194">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d55a-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d55a-195">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d55a-195">INPUTS</span></span>

### <span data-ttu-id="0d55a-196">System. String</span><span class="sxs-lookup"><span data-stu-id="0d55a-196">System.String</span></span>

### <span data-ttu-id="0d55a-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0d55a-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0d55a-198">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d55a-198">OUTPUTS</span></span>

### <span data-ttu-id="0d55a-199">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0d55a-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0d55a-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d55a-200">NOTES</span></span>

## <span data-ttu-id="0d55a-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d55a-201">RELATED LINKS</span></span>

[<span data-ttu-id="0d55a-202">Dodaj-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="0d55a-202">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="0d55a-203">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="0d55a-203">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="0d55a-204">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0d55a-204">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


