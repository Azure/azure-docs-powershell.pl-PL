---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 5bd0e525607180659365c81825d6ad6899578fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706179"
---
# <span data-ttu-id="35e27-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="35e27-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="35e27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35e27-102">SYNOPSIS</span></span>
<span data-ttu-id="35e27-103">Włączenie szyfrowania na działającej maszynie wirtualnej IaaS na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="35e27-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="35e27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35e27-104">SYNTAX</span></span>

### <span data-ttu-id="35e27-105">SinglePassParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35e27-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35e27-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="35e27-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35e27-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="35e27-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35e27-108">Opis</span><span class="sxs-lookup"><span data-stu-id="35e27-108">DESCRIPTION</span></span>
<span data-ttu-id="35e27-109">Polecenie cmdlet **Set-AzVMDiskEncryptionExtension** umożliwia szyfrowanie uruchomionej infrastruktury jako maszyny wirtualnej usługi (IaaS) na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="35e27-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="35e27-110">Umożliwia szyfrowanie przez zainstalowanie rozszerzenia szyfrowanie dysków na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="35e27-111">To polecenie cmdlet wymaga potwierdzenia od użytkowników, ponieważ jedna z kroków umożliwiających włączenie szyfrowania wymaga ponownego uruchomienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="35e27-112">Przed uruchomieniem tego polecenia cmdlet zaleca się zapisanie pracy na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="35e27-113">Linux: parametr **volumetype** jest wymagany podczas szyfrowania maszyn wirtualnych systemu Linux i musi być ustawiony na wartość ("OS", "dane" lub "All") obsługiwanych przez dystrybucję Linux.</span><span class="sxs-lookup"><span data-stu-id="35e27-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="35e27-114">Windows: parametr **volumetype** może być pominięty, a w takim przypadku operacja jest domyślnie ustawiona na wartość wszystkie; Jeśli dla maszyny wirtualnej systemu Windows jest obecny parametr nazwa_woluminu, musi on mieć ustawioną wartość wszystko lub system operacyjny.</span><span class="sxs-lookup"><span data-stu-id="35e27-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="35e27-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35e27-115">EXAMPLES</span></span>

### <span data-ttu-id="35e27-116">Przykład 1: Włączanie szyfrowania</span><span class="sxs-lookup"><span data-stu-id="35e27-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="35e27-117">Ten przykład umożliwia włączenie szyfrowania na maszynie wirtualnej bez określania poświadczeń usługi AD.</span><span class="sxs-lookup"><span data-stu-id="35e27-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="35e27-118">Przykład 2: Włączanie szyfrowania przy użyciu danych wejściowych potokowych</span><span class="sxs-lookup"><span data-stu-id="35e27-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="35e27-119">W tym przykładzie są przesyłane parametry przy użyciu danych wejściowych potokowych w celu włączenia szyfrowania na maszynie wirtualnej bez określania poświadczeń usługi AD.</span><span class="sxs-lookup"><span data-stu-id="35e27-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="35e27-120">Przykład 3: Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i klucza tajnego klienta</span><span class="sxs-lookup"><span data-stu-id="35e27-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="35e27-121">W tym przykładzie użyto identyfikatora klienta usługi Azure AD i klucza tajnego klienta w celu włączenia szyfrowania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="35e27-122">Przykład 4: Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i odcisk palca certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="35e27-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="35e27-123">W tym przykładzie użyto odcisków palców identyfikatora klienta usługi Azure AD i certyfikatu klienta w celu włączenia szyfrowania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="35e27-124">Przykład 5: Włączanie szyfrowania za pomocą identyfikatora klienta usługi Azure AD, klucza tajnego klienta i Zawijanie klucza szyfrowania dysku przy użyciu klucza szyfrowania kluczy</span><span class="sxs-lookup"><span data-stu-id="35e27-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="35e27-125">W tym przykładzie użyto identyfikatora klienta usługi Azure AD i klucza tajnego klienta w celu włączenia szyfrowania na maszynie wirtualnej i oblewanie klucza szyfrowania dysku przy użyciu klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="35e27-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="35e27-126">Przykład 6: Włączanie szyfrowania za pomocą identyfikatora klienta usługi Azure AD, odcisku palca certyfikatu klienta i Zawijanie EncryptionKey dysków przy użyciu klucza szyfrowania kluczy</span><span class="sxs-lookup"><span data-stu-id="35e27-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="35e27-127">W tym przykładzie użyto identyfikatora klienta usługi Azure AD i odcisku palca certyfikatu klienta w celu włączenia szyfrowania na maszynie wirtualnej i oblewanie klucza szyfrowania dysku przy użyciu klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="35e27-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="35e27-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35e27-128">PARAMETERS</span></span>

### <span data-ttu-id="35e27-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="35e27-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="35e27-130">Określa odcisk palca certyfikatu klienta aplikacji katalogu AzureActive (Azure AD), który ma uprawnienia do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="35e27-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="35e27-131">Jako warunek wstępny certyfikat klienta usługi Azure AD musi zostać wcześniej wdrożony w magazynie certyfikatów lokalnego komputera maszyny wirtualnej `my` .</span><span class="sxs-lookup"><span data-stu-id="35e27-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="35e27-132">Za pomocą polecenia cmdlet Add-AzVMSecret można wdrożyć certyfikat na maszynie wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="35e27-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="35e27-133">Aby uzyskać więcej informacji, zobacz Pomoc polecenia cmdlet **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="35e27-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="35e27-134">Certyfikat musi być wcześniej wdrożony na komputerze lokalnym maszyny wirtualnej mój magazyn certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="35e27-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="35e27-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="35e27-135">-AadClientID</span></span>
<span data-ttu-id="35e27-136">Określa identyfikator klienta aplikacji Azure AD z uprawnieniami do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="35e27-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="35e27-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="35e27-137">-AadClientSecret</span></span>
<span data-ttu-id="35e27-138">Określa klucz tajny klienta aplikacji usługi Azure AD z uprawnieniami do zapisywania kluczy tajnych w **magazynie** kluczy.</span><span class="sxs-lookup"><span data-stu-id="35e27-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="35e27-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e27-139">-DefaultProfile</span></span>
<span data-ttu-id="35e27-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35e27-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35e27-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="35e27-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="35e27-142">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="35e27-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="35e27-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="35e27-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="35e27-144">Określa identyfikator zasobu **magazynu** kluczy, do którego mają być przekazywane klucze szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="35e27-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="35e27-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="35e27-146">Określa adres URL **magazynu** kluczy, do którego mają być przekazywane klucze szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="35e27-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="35e27-147">-EncryptFormatAll</span></span>
<span data-ttu-id="35e27-148">Encrypt-Format wszystkich dysków danych, które nie są jeszcze zaszyfrowane</span><span class="sxs-lookup"><span data-stu-id="35e27-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="35e27-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="35e27-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="35e27-150">Nazwa wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="35e27-150">The extension publisher name.</span></span> <span data-ttu-id="35e27-151">Ten parametr można określić tylko w celu zastąpienia wartości domyślnej "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="35e27-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="35e27-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="35e27-152">-ExtensionType</span></span>
<span data-ttu-id="35e27-153">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="35e27-153">The extension type.</span></span> <span data-ttu-id="35e27-154">Określ ten parametr, aby zastąpić swoją domyślną wartość "AzureDiskEncryption" dla maszyn wirtualnych systemu Windows i "AzureDiskEncryptionForLinux" dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="35e27-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="35e27-155">-Force</span><span class="sxs-lookup"><span data-stu-id="35e27-155">-Force</span></span>
<span data-ttu-id="35e27-156">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="35e27-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35e27-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="35e27-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="35e27-158">Określa algorytm używany do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="35e27-159">Wartość domyślna to RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="35e27-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="35e27-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="35e27-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="35e27-161">Określa adres URL klucza szyfrowania klucza używanego do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="35e27-162">To musi być pełny adres URL w wersji.</span><span class="sxs-lookup"><span data-stu-id="35e27-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="35e27-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="35e27-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="35e27-164">Określa identyfikator zasobu **magazynu** kluczy zawierającego klucz szyfrowania klucza służący do zawijania i dezawijania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="35e27-165">To musi być pełny adres URL w wersji.</span><span class="sxs-lookup"><span data-stu-id="35e27-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="35e27-166">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35e27-166">-Name</span></span>
<span data-ttu-id="35e27-167">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="35e27-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="35e27-168">W przypadku pominięcia parametru *name* zainstalowane rozszerzenie będzie nazwane AzureDiskEncryption na maszynach wirtualnych systemu Windows i AzureDiskEncryptionForLinux na maszynach wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="35e27-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="35e27-169">— Hasło</span><span class="sxs-lookup"><span data-stu-id="35e27-169">-Passphrase</span></span>
<span data-ttu-id="35e27-170">Określa hasło używane do szyfrowania tylko maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="35e27-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="35e27-171">Ten parametr nie jest używany w przypadku maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="35e27-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="35e27-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e27-172">-ResourceGroupName</span></span>
<span data-ttu-id="35e27-173">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="35e27-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="35e27-174">-SequenceVersion</span></span>
<span data-ttu-id="35e27-175">Określa numer sekwencji operacji szyfrowania dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="35e27-176">Ta funkcja jest unikatowa dla każdej operacji szyfrowania wykonywanej na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="35e27-177">Za pomocą polecenia cmdlet Get-AzVMExtension można pobrać poprzedni numer sekwencyjny, którego użyto.</span><span class="sxs-lookup"><span data-stu-id="35e27-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="35e27-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="35e27-178">-SkipVmBackup</span></span>
<span data-ttu-id="35e27-179">Pomijanie tworzenia kopii zapasowych dla maszyn wirtualnych systemu Linux</span><span class="sxs-lookup"><span data-stu-id="35e27-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="35e27-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="35e27-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="35e27-181">Określa wersję rozszerzenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="35e27-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="35e27-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="35e27-182">-VMName</span></span>
<span data-ttu-id="35e27-183">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35e27-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="35e27-184">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="35e27-184">-VolumeType</span></span>
<span data-ttu-id="35e27-185">Określa typ woluminów maszyny wirtualnej, na których ma zostać wykonana operacja szyfrowania: system operacyjny, dane lub wszystko.</span><span class="sxs-lookup"><span data-stu-id="35e27-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="35e27-186">Linux: parametr **volumetype** jest wymagany podczas szyfrowania maszyn wirtualnych systemu Linux i musi być ustawiony na wartość ("OS", "dane" lub "All") obsługiwanych przez dystrybucję Linux.</span><span class="sxs-lookup"><span data-stu-id="35e27-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="35e27-187">Windows: parametr **volumetype** może być pominięty, a w takim przypadku operacja jest domyślnie ustawiona na wartość wszystkie; Jeśli dla maszyny wirtualnej systemu Windows jest obecny parametr nazwa_woluminu, musi on mieć ustawioną wartość wszystko lub system operacyjny.</span><span class="sxs-lookup"><span data-stu-id="35e27-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="35e27-188">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35e27-188">-Confirm</span></span>
<span data-ttu-id="35e27-189">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35e27-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35e27-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e27-190">-WhatIf</span></span>
<span data-ttu-id="35e27-191">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35e27-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35e27-192">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35e27-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35e27-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e27-193">CommonParameters</span></span>
<span data-ttu-id="35e27-194">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e27-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e27-195">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35e27-195">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e27-196">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35e27-196">INPUTS</span></span>

### <span data-ttu-id="35e27-197">System. String</span><span class="sxs-lookup"><span data-stu-id="35e27-197">System.String</span></span>

### <span data-ttu-id="35e27-198">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="35e27-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="35e27-199">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35e27-199">OUTPUTS</span></span>

### <span data-ttu-id="35e27-200">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="35e27-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="35e27-201">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35e27-201">NOTES</span></span>

## <span data-ttu-id="35e27-202">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35e27-202">RELATED LINKS</span></span>

[<span data-ttu-id="35e27-203">Dodaj-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="35e27-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="35e27-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="35e27-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="35e27-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="35e27-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


