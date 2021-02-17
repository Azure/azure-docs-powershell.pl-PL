---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238660"
---
# <span data-ttu-id="bffb4-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bffb4-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="bffb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bffb4-102">SYNOPSIS</span></span>
<span data-ttu-id="bffb4-103">Włącza szyfrowanie na uruchomionej maszynie wirtualnej IaaS na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="bffb4-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="bffb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bffb4-104">SYNTAX</span></span>

### <span data-ttu-id="bffb4-105">SinglePassParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bffb4-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bffb4-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="bffb4-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bffb4-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="bffb4-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bffb4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bffb4-108">DESCRIPTION</span></span>
<span data-ttu-id="bffb4-109">Polecenie **cmdlet Set-AzVMBlockEncryptionExtension** umożliwia szyfrowanie na uruchomionej infrastrukturze jako maszyny wirtualnej (IaaS) na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="bffb4-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="bffb4-110">Umożliwia on szyfrowanie, instalując rozszerzenie szyfrowania dysku na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="bffb4-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="bffb4-111">To polecenie cmdlet wymaga potwierdzenia od użytkowników jako jednego z kroków umożliwiających włączenie szyfrowania wymaga ponownego uruchomienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bffb4-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="bffb4-112">Zaleca się zapisanie pracy na komputerze wirtualnym przed uruchomieniem tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bffb4-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="bffb4-113">Linux: Parametr **VolumeType** jest wymagany podczas szyfrowania maszyn wirtualnych systemu Linux i musi mieć ustawioną wartość ("System operacyjny", "Dane" lub "Wszystkie") obsługiwaną przez dystrybucję Linuksa.</span><span class="sxs-lookup"><span data-stu-id="bffb4-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="bffb4-114">Windows: Parametr **VolumeType** może zostać pominięty — w takim przypadku operacja ma wartość domyślną All (Wszystko); Jeśli parametr VolumeType jest dostępny dla maszyny wirtualnej systemu Windows, musi mieć ustawioną wartość Wszystkie lub System operacyjny.</span><span class="sxs-lookup"><span data-stu-id="bffb4-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="bffb4-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bffb4-115">EXAMPLES</span></span>

### <span data-ttu-id="bffb4-116">Przykład 1. Włączanie szyfrowania</span><span class="sxs-lookup"><span data-stu-id="bffb4-116">Example 1: Enable encryption</span></span>
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

<span data-ttu-id="bffb4-117">W tym przykładzie szyfrowanie na maszyny wirtualnej jest włączane bez określania poświadczeń usługi AD.</span><span class="sxs-lookup"><span data-stu-id="bffb4-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="bffb4-118">Przykład 2. Włączanie szyfrowania za pomocą danych wejściowych potokowych</span><span class="sxs-lookup"><span data-stu-id="bffb4-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="bffb4-119">W tym przykładzie parametry są wysyłane przy użyciu danych wejściowych potokowych w celu włączenia szyfrowania maszyny wirtualnej bez określania poświadczeń usługi AD.</span><span class="sxs-lookup"><span data-stu-id="bffb4-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="bffb4-120">Przykład 3. Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i klucza tajnego klienta</span><span class="sxs-lookup"><span data-stu-id="bffb4-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="bffb4-121">W tym przykładzie do włączenia szyfrowania maszyny wirtualnej są używane identyfikator klienta usługi Azure AD i klucz tajny klienta.</span><span class="sxs-lookup"><span data-stu-id="bffb4-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="bffb4-122">Przykład 4. Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD i funkcji thumbprint certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="bffb4-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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

<span data-ttu-id="bffb4-123">W tym przykładzie zastosowano identyfikator klienta usługi Azure AD i kciuki certyfikacji klienta, aby włączyć szyfrowanie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bffb4-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="bffb4-124">Przykład 5. Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD, klucza tajnego klienta i klucza szyfrowania zawijania dysku przy użyciu klucza szyfrowania</span><span class="sxs-lookup"><span data-stu-id="bffb4-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
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

<span data-ttu-id="bffb4-125">W tym przykładzie do włączenia szyfrowania maszyny wirtualnej są używane identyfikatory klienta usługi Azure AD i klucz tajny klienta, a klucz szyfrowania dysku jest zawijany przy użyciu klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="bffb4-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="bffb4-126">Przykład 6. Włączanie szyfrowania przy użyciu identyfikatora klienta usługi Azure AD, identyfikatora usbprint certyfikatu klienta i klucza szyfrowania zawijania dysku przy użyciu klucza szyfrowania</span><span class="sxs-lookup"><span data-stu-id="bffb4-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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

<span data-ttu-id="bffb4-127">W tym przykładzie do włączenia szyfrowania maszyny wirtualnej jest używany identyfikator klienta usługi Azure AD i usbprint certyfikatu klienta, a klucz szyfrowania dysku jest zawijany przy użyciu klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="bffb4-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="bffb4-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bffb4-128">PARAMETERS</span></span>

### <span data-ttu-id="bffb4-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="bffb4-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="bffb4-130">Określa thumbprint certyfikatu klienta aplikacji usługi AzureActive Directory (Azure AD), który ma uprawnienia do pisania sekretów w **usłudze KeyVault.**</span><span class="sxs-lookup"><span data-stu-id="bffb4-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="bffb4-131">Wstępnie wymagane jest, aby certyfikat klienta usługi Azure AD był wcześniej wdrożony w magazynie certyfikatów komputera `my` lokalnego na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="bffb4-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="bffb4-132">Za Add-AzVMSecret cmdlet można wdrożyć certyfikat na komputerze wirtualnym na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="bffb4-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="bffb4-133">Aby uzyskać więcej szczegółowych informacji, zobacz pomoc polecenia **cmdlet Add-AzVMSecret.**</span><span class="sxs-lookup"><span data-stu-id="bffb4-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="bffb4-134">Certyfikat musi być wcześniej wdrożony na komputerze wirtualnym, na moim magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="bffb4-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="bffb4-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="bffb4-135">-AadClientID</span></span>
<span data-ttu-id="bffb4-136">Określa identyfikator klienta aplikacji usługi Azure AD, który ma uprawnienia do pisania sekretów w **usłudze KeyVault.**</span><span class="sxs-lookup"><span data-stu-id="bffb4-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="bffb4-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="bffb4-137">-AadClientSecret</span></span>
<span data-ttu-id="bffb4-138">Określa klucz tajny klienta aplikacji Usługi Azure AD, który ma uprawnienia do pisania sekretów w **usłudze KeyVault.**</span><span class="sxs-lookup"><span data-stu-id="bffb4-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="bffb4-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bffb4-139">-DefaultProfile</span></span>
<span data-ttu-id="bffb4-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bffb4-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bffb4-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bffb4-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bffb4-142">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie wersji pomocniczej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bffb4-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="bffb4-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="bffb4-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="bffb4-144">Określa identyfikator zasobu klucza **KeyVault,** do którego mają zostać przekazane klucze szyfrowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="bffb4-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="bffb4-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="bffb4-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="bffb4-146">Określa adres URL **KeyVault,** do którego należy przekazać klucze szyfrowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="bffb4-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="bffb4-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="bffb4-147">-EncryptFormatAll</span></span>
<span data-ttu-id="bffb4-148">Encrypt-Format wszystkich dysków danych, które nie są jeszcze zaszyfrowane</span><span class="sxs-lookup"><span data-stu-id="bffb4-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="bffb4-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="bffb4-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="bffb4-150">Nazwa wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bffb4-150">The extension publisher name.</span></span> <span data-ttu-id="bffb4-151">Określ ten parametr, aby zastąpić wartość domyślną "Microsoft.Azure.Security".</span><span class="sxs-lookup"><span data-stu-id="bffb4-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="bffb4-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="bffb4-152">-ExtensionType</span></span>
<span data-ttu-id="bffb4-153">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bffb4-153">The extension type.</span></span> <span data-ttu-id="bffb4-154">Określ ten parametr, aby zastąpić jego wartość domyślną "AzureUxEncryption" dla maszyn wirtualnych systemu Windows i "AzureCryptionForLinux" dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="bffb4-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="bffb4-155">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="bffb4-155">-Force</span></span>
<span data-ttu-id="bffb4-156">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bffb4-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bffb4-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="bffb4-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="bffb4-158">Określa algorytm używany do zawijania i cofania klucza szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bffb4-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="bffb4-159">Wartość domyślna to RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="bffb4-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="bffb4-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="bffb4-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="bffb4-161">Określa adres URL klucza szyfrowania używanego do zawijania i cofania szyfrowania klucza maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bffb4-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="bffb4-162">Musi to być pełny adres URL z pełną wersją.</span><span class="sxs-lookup"><span data-stu-id="bffb4-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="bffb4-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="bffb4-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="bffb4-164">Określa identyfikator zasobu klucza **KeyVault zawierający** klucz szyfrowania używany do zawijania i cofania szyfrowania klucza maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bffb4-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="bffb4-165">Musi to być adres URL z pełną wersją.</span><span class="sxs-lookup"><span data-stu-id="bffb4-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="bffb4-166">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bffb4-166">-Name</span></span>
<span data-ttu-id="bffb4-167">Określa nazwę zasobu usługi Azure Resource Manager reprezentującą to rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="bffb4-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="bffb4-168">Jeśli parametr *Name* zostanie pominięty, zainstalowane rozszerzenie będzie nosiło nazwę AzureCryption w komputerach wirtualnych systemu Windows i Azure PrzyszłaNacryptionForLinux na komputerach wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="bffb4-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="bffb4-169">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="bffb4-169">-Passphrase</span></span>
<span data-ttu-id="bffb4-170">Określa hasło używane tylko do szyfrowania maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="bffb4-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="bffb4-171">Ten parametr nie jest używany w przypadku maszyn wirtualnych, na których działa system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="bffb4-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="bffb4-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bffb4-172">-ResourceGroupName</span></span>
<span data-ttu-id="bffb4-173">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bffb4-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bffb4-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="bffb4-174">-SequenceVersion</span></span>
<span data-ttu-id="bffb4-175">Określa numer sekwencji operacji szyfrowania dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bffb4-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="bffb4-176">Jest to unikatowe dla każdej operacji szyfrowania wykonywanej na tej samej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bffb4-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="bffb4-177">To Get-AzVMExtension cmdlet może zostać użyte do pobrania poprzedniego numeru sekwencji, który był używany.</span><span class="sxs-lookup"><span data-stu-id="bffb4-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="bffb4-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="bffb4-178">-SkipVmBackup</span></span>
<span data-ttu-id="bffb4-179">Pomiń tworzenie kopii zapasowej dla maszyn wirtualnych systemu Linux</span><span class="sxs-lookup"><span data-stu-id="bffb4-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="bffb4-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bffb4-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="bffb4-181">Określa wersję rozszerzenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="bffb4-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="bffb4-182">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="bffb4-182">-VMName</span></span>
<span data-ttu-id="bffb4-183">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bffb4-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="bffb4-184">- VolumeType</span><span class="sxs-lookup"><span data-stu-id="bffb4-184">-VolumeType</span></span>
<span data-ttu-id="bffb4-185">Określa typ woluminów maszyn wirtualnych, na których ma być przetwarzana operacja szyfrowania: system operacyjny, dane lub wszystko.</span><span class="sxs-lookup"><span data-stu-id="bffb4-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="bffb4-186">Linux: Parametr **VolumeType** jest wymagany podczas szyfrowania maszyn wirtualnych systemu Linux i musi mieć ustawioną wartość ("System operacyjny", "Dane" lub "Wszystkie") obsługiwaną przez dystrybucję Linuksa.</span><span class="sxs-lookup"><span data-stu-id="bffb4-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="bffb4-187">Windows: Parametr **VolumeType** może zostać pominięty — w takim przypadku operacja ma wartość domyślną All (Wszystko); Jeśli parametr VolumeType jest dostępny dla maszyny wirtualnej systemu Windows, musi mieć ustawioną wartość Wszystkie lub System operacyjny.</span><span class="sxs-lookup"><span data-stu-id="bffb4-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="bffb4-188">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bffb4-188">-Confirm</span></span>
<span data-ttu-id="bffb4-189">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bffb4-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bffb4-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bffb4-190">-WhatIf</span></span>
<span data-ttu-id="bffb4-191">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bffb4-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bffb4-192">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bffb4-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bffb4-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffb4-193">CommonParameters</span></span>
<span data-ttu-id="bffb4-194">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bffb4-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffb4-195">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bffb4-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffb4-196">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bffb4-196">INPUTS</span></span>

### <span data-ttu-id="bffb4-197">System.String</span><span class="sxs-lookup"><span data-stu-id="bffb4-197">System.String</span></span>

### <span data-ttu-id="bffb4-198">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="bffb4-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bffb4-199">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bffb4-199">OUTPUTS</span></span>

### <span data-ttu-id="bffb4-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bffb4-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bffb4-201">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bffb4-201">NOTES</span></span>

## <span data-ttu-id="bffb4-202">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bffb4-202">RELATED LINKS</span></span>

[<span data-ttu-id="bffb4-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="bffb4-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="bffb4-204">Get-AzVM GdyszytEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="bffb4-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="bffb4-205">Remove-AzVMCryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bffb4-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


