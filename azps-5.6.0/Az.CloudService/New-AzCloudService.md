---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 607ac4e9854f3871c4a9a0f2859c6f1fe555f392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983402"
---
# <span data-ttu-id="12d38-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="12d38-101">New-AzCloudService</span></span>

## <span data-ttu-id="12d38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12d38-102">SYNOPSIS</span></span>
<span data-ttu-id="12d38-103">Tworzenie lub aktualizowanie usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-103">Create or update a cloud service.</span></span>
<span data-ttu-id="12d38-104">Niektóre właściwości można ustawić tylko podczas tworzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="12d38-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="12d38-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="12d38-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="12d38-106">DESCRIPTION</span></span>
<span data-ttu-id="12d38-107">Tworzenie lub aktualizowanie usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-107">Create or update a cloud service.</span></span>
<span data-ttu-id="12d38-108">Niektóre właściwości można ustawić tylko podczas tworzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="12d38-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="12d38-109">EXAMPLES</span></span>

### <span data-ttu-id="12d38-110">Przykład 1. Tworzenie nowej usługi w chmurze z jedną rolą</span><span class="sxs-lookup"><span data-stu-id="12d38-110">Example 1: Create new cloud service with single role</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

<span data-ttu-id="12d38-111">Powyższy zestaw poleceń tworzy usługę w chmurze z jedną rolą</span><span class="sxs-lookup"><span data-stu-id="12d38-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="12d38-112">Przykład 2. Tworzenie nowej usługi w chmurze z jedną rolą i rozszerzeniem RDP</span><span class="sxs-lookup"><span data-stu-id="12d38-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

<span data-ttu-id="12d38-113">Powyższy zestaw poleceń tworzy usługę w chmurze z jedną rolą i rozszerzeniem RDP</span><span class="sxs-lookup"><span data-stu-id="12d38-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="12d38-114">Przykład 3. Tworzenie nowej usługi w chmurze z jedną rolą i certyfikatem z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="12d38-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

<span data-ttu-id="12d38-115">Powyższy zestaw poleceń tworzy usługę w chmurze z pojedynczą rolą i certyfikatem z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="12d38-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="12d38-116">Przykład 4. Tworzenie nowej usługi w chmurze z wieloma rolami i rozszerzeniami</span><span class="sxs-lookup"><span data-stu-id="12d38-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

<span data-ttu-id="12d38-117">Powyższy zestaw poleceń tworzy usługę w chmurze z pojedynczą rolą i certyfikatem z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="12d38-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="12d38-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12d38-118">PARAMETERS</span></span>

### <span data-ttu-id="12d38-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="12d38-119">-AsJob</span></span>
<span data-ttu-id="12d38-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="12d38-120">Run the command as a job</span></span>

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

### <span data-ttu-id="12d38-121">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="12d38-121">-Configuration</span></span>
<span data-ttu-id="12d38-122">Określa konfigurację usługi XML (cscfg) dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-123">- ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="12d38-123">-ConfigurationUrl</span></span>
<span data-ttu-id="12d38-124">Określa adres URL, który odwołuje się do lokalizacji konfiguracji usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="12d38-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="12d38-125">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu. Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="12d38-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d38-126">-DefaultProfile</span></span>
<span data-ttu-id="12d38-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="12d38-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="12d38-128">-ExtensionProfile</span></span>
<span data-ttu-id="12d38-129">W tym artykule opisano profil rozszerzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="12d38-130">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach EXTENSIONPROFILE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="12d38-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="12d38-131">-Location</span></span>
<span data-ttu-id="12d38-132">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="12d38-132">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="12d38-133">-Name</span></span>
<span data-ttu-id="12d38-134">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-134">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-135">- NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="12d38-135">-NetworkProfile</span></span>
<span data-ttu-id="12d38-136">Profil sieciowy usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="12d38-137">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach NETWORKPROFILE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="12d38-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="12d38-138">-NoWait</span></span>
<span data-ttu-id="12d38-139">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="12d38-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12d38-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="12d38-140">-OSProfile</span></span>
<span data-ttu-id="12d38-141">W tym artykule opisano profil systemu operacyjnego usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="12d38-142">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach pliku OSPROFILE i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="12d38-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="12d38-143">-PackageUrl</span></span>
<span data-ttu-id="12d38-144">Określa adres URL, który odwołuje się do lokalizacji pakietu usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="12d38-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="12d38-145">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu. Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="12d38-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d38-146">-ResourceGroupName</span></span>
<span data-ttu-id="12d38-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12d38-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="12d38-148">-RoleProfile</span></span>
<span data-ttu-id="12d38-149">W tym artykule opisano profil roli dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="12d38-150">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach ROLEPROFILE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="12d38-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="12d38-151">-StartCloudService</span></span>
<span data-ttu-id="12d38-152">(Opcjonalnie) Wskazuje, czy usługa w chmurze ma być uruchamiana natychmiast po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="12d38-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="12d38-153">Wartość domyślna `true` to. Jeśli wartość jest fałszywa, model usługi jest nadal wdrażany, ale kod nie jest uruchamiany natychmiast.</span><span class="sxs-lookup"><span data-stu-id="12d38-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="12d38-154">Zamiast tego usługa będzie się uruchamiać do momentu wywołania startowego, o której usługa zostanie uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="12d38-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="12d38-155">Wdrożona usługa nadal wiąże się z opłatami, nawet jeśli zostanie wyłączony.</span><span class="sxs-lookup"><span data-stu-id="12d38-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

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

### <span data-ttu-id="12d38-156">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12d38-156">-SubscriptionId</span></span>
<span data-ttu-id="12d38-157">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12d38-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="12d38-158">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="12d38-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-159">— Tag</span><span class="sxs-lookup"><span data-stu-id="12d38-159">-Tag</span></span>
<span data-ttu-id="12d38-160">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="12d38-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="12d38-161">-UpgradeMode</span></span>
<span data-ttu-id="12d38-162">Tryb aktualizacji dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="12d38-163">Wystąpienia ról są przydzielane do aktualizowania domen podczas wdrażania usługi.</span><span class="sxs-lookup"><span data-stu-id="12d38-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="12d38-164">Aktualizacje mogą być inicjowane ręcznie w każdej domenie aktualizacji lub inicjowane automatycznie we wszystkich domenach aktualizacji. Dopuszczalne wartości to \<br /\> \<br /\> **Automatyczne** \<br /\> \<br /\> **ręczne** \<br /\> \<br /\> **jednoczesne** \<br /\> \<br /\> (jeśli nie zostanie określone), wartością domyślną jest Auto. Jeśli ta wartość jest ustawiona na Ręcznie, aby zastosować aktualizację, musi zostać wywołana nazwa PUT UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="12d38-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="12d38-165">Jeśli ta opcja jest ustawiona na Automatyczne, aktualizacja jest automatycznie stosowana do każdej domeny aktualizacji w sekwencji.</span><span class="sxs-lookup"><span data-stu-id="12d38-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-166">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12d38-166">-Confirm</span></span>
<span data-ttu-id="12d38-167">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="12d38-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d38-168">-WhatIf</span></span>
<span data-ttu-id="12d38-169">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d38-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12d38-170">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="12d38-170">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d38-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d38-171">CommonParameters</span></span>
<span data-ttu-id="12d38-172">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d38-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d38-173">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12d38-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d38-174">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12d38-174">INPUTS</span></span>

## <span data-ttu-id="12d38-175">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12d38-175">OUTPUTS</span></span>

### <span data-ttu-id="12d38-176">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.iCloudService</span><span class="sxs-lookup"><span data-stu-id="12d38-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="12d38-177">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="12d38-177">NOTES</span></span>

<span data-ttu-id="12d38-178">ALIASY</span><span class="sxs-lookup"><span data-stu-id="12d38-178">ALIASES</span></span>

<span data-ttu-id="12d38-179">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12d38-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12d38-180">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="12d38-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12d38-181">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12d38-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12d38-182">EXTENSIONPROFILE: <ICloudServiceExtensionProfile> W tym artykule opisano profil rozszerzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="12d38-183">`[Extension <IExtension[]>]`: Lista rozszerzeń dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="12d38-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Jawnie określ, czy platforma może automatycznie uaktualniać typHandlerVersion do wyższych wersji pomocniczych, gdy staną się dostępne.</span><span class="sxs-lookup"><span data-stu-id="12d38-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="12d38-185">`[ForceUpdateTag <String>]`: Tag wymusza zastosowanie podanych ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="12d38-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="12d38-186">Zmiana wartości tagu umożliwia ponowne uruchomienie rozszerzenia bez zmieniania jakichkolwiek ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="12d38-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="12d38-187">Jeśli tag forceUpdate nie zostanie zmieniony, program obsługi nadal będzie stosować aktualizacje ustawień publicznych lub chronionych.</span><span class="sxs-lookup"><span data-stu-id="12d38-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="12d38-188">Jeśli ani forceUpdateTag, ani żadne ustawienia publiczne lub chronione nie ujdą, rozszerzenie przepływa do wystąpienia roli z tym samym numerem sekwencji, a implementacja programu obsługi może być uruchamiana ponownie, czy nie.</span><span class="sxs-lookup"><span data-stu-id="12d38-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="12d38-189">`[Name <String>]`: nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="12d38-190">`[ProtectedSetting <String>]`: ustawienia chronione rozszerzenia, które są szyfrowane przed wysłaniem do wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="12d38-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="12d38-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="12d38-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="12d38-192">`[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="12d38-193">`[RolesAppliedTo <String[]>]`: Opcjonalna lista ról do zastosowania tego rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="12d38-194">Jeśli nie określono właściwości lub określono wartość "\*", rozszerzenie jest stosowane do wszystkich ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="12d38-195">`[Setting <String>]`: ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="12d38-196">W przypadku rozszerzeń JSON są to ustawienia JSON rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="12d38-197">W przypadku rozszerzenia XML (takiego jak RDP) jest to ustawienie XML rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="12d38-198">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="12d38-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="12d38-199">`[Type <String>]`: określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="12d38-200">`[TypeHandlerVersion <String>]`: określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="12d38-201">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-201">Specifies the version of the extension.</span></span> <span data-ttu-id="12d38-202">Jeśli ten element nie jest określony lub jako wartość zostanie użyta gwiazdka (\*), zostanie użyta najnowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="12d38-203">Jeśli wartość zostanie określona z głównym numerem wersji i gwiazdką jako pomocniczy numer wersji (X),zostanie wybrana najnowsza wersja pomocnicza określonej wersji głównych.</span><span class="sxs-lookup"><span data-stu-id="12d38-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="12d38-204">Jeśli określono główny numer wersji i numer wersji pomocniczej (X.Y), wybrana jest określona wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12d38-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="12d38-205">Jeśli jest określona wersja, automatyczne uaktualnianie jest wykonywane w wystąpieniu roli.</span><span class="sxs-lookup"><span data-stu-id="12d38-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="12d38-206">NETWORKPROFILE: <ICloudServiceNetworkProfile> Profil sieciowy dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="12d38-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: lista konfiguracji równoważenia obciążenia dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="12d38-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: lista adresów IP</span><span class="sxs-lookup"><span data-stu-id="12d38-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="12d38-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="12d38-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="12d38-210">`[PrivateIPAddress <String>]`: prywatny adres IP, do których odwołuje się usługa w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="12d38-211">`[PublicIPAddressId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="12d38-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="12d38-212">`[SubnetId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="12d38-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="12d38-213">`[Name <String>]`: Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="12d38-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="12d38-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="12d38-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="12d38-215">`[Id <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="12d38-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="12d38-216">OSPROFILE: <ICloudServiceOSProfile> w tym artykule opisano profil systemu operacyjnego dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="12d38-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Określa zestaw certyfikatów, które powinny być instalowane w wystąpieniach ról.</span><span class="sxs-lookup"><span data-stu-id="12d38-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="12d38-218">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="12d38-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="12d38-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: lista odwołań do magazynu kluczy w u źródłach SourceVault, które zawierają certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="12d38-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="12d38-220">`[CertificateUrl <String>]`: jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako tajny.</span><span class="sxs-lookup"><span data-stu-id="12d38-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="12d38-221">ROLEPROFILE: <ICloudServiceRoleProfile> w tym artykule opisano profil roli usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="12d38-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: lista ról dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="12d38-223">`[Name <String>]`: nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="12d38-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="12d38-224">`[SkuCapacity <Int64?>]`: określa liczbę wystąpień ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="12d38-225">`[SkuName <String>]`: nazwa sKU.</span><span class="sxs-lookup"><span data-stu-id="12d38-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="12d38-226">UWAGA: Jeśli nowa wersja SKU nie jest obsługiwana na sprzęcie, na który obecnie działa usługa w chmurze, musisz usunąć i ponownie utworzyć usługę w chmurze lub wrócić do starej.</span><span class="sxs-lookup"><span data-stu-id="12d38-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="12d38-227">`[SkuTier <String>]`: określa warstwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="12d38-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="12d38-228">Dopuszczalne wartości to</span><span class="sxs-lookup"><span data-stu-id="12d38-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="12d38-229">**Standardowe**</span><span class="sxs-lookup"><span data-stu-id="12d38-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="12d38-230">**Podstawowe**</span><span class="sxs-lookup"><span data-stu-id="12d38-230">**Basic**</span></span>

## <span data-ttu-id="12d38-231">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12d38-231">RELATED LINKS</span></span>

