---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: 2a3b643a9ad9d9c588589003e5edb24ceddc4ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181803"
---
# <span data-ttu-id="abe78-101">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="abe78-101">Get-AzCloudServicePublicIPAddress</span></span>

## <span data-ttu-id="abe78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abe78-102">SYNOPSIS</span></span>
<span data-ttu-id="abe78-103">Uzyskaj publiczny adres IP usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-103">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="abe78-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="abe78-104">SYNTAX</span></span>

### <span data-ttu-id="abe78-105">CloudServiceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="abe78-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### <span data-ttu-id="abe78-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="abe78-106">CloudService</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="abe78-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="abe78-107">DESCRIPTION</span></span>
<span data-ttu-id="abe78-108">Uzyskaj publiczny adres IP usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-108">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="abe78-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="abe78-109">EXAMPLES</span></span>

### <span data-ttu-id="abe78-110">Przykład 1. Uzyskiwanie publicznych adresów IP na poziomie wystąpienia dla danej nazwy usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-110">Example 1: Get instance level public IP addresses for a given cloud service name.</span></span>
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="abe78-111">Pobiera publiczne adresy IP na poziomie wystąpienia dla danej nazwy usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-111">Gets the instance level public IP addresses for a given cloud service name.</span></span>

### <span data-ttu-id="abe78-112">Przykład 2. Uzyskaj publiczne adresy IP na poziomie wystąpienia dla danego obiektu usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-112">Example 2: Get instance level public IP addresses for a given cloud service object.</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

<span data-ttu-id="abe78-113">Pobiera publiczne adresy IP na poziomie wystąpienia dla danego obiektu usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-113">Gets the instance level public IP addresses for a given cloud service object.</span></span>

## <span data-ttu-id="abe78-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abe78-114">PARAMETERS</span></span>

### <span data-ttu-id="abe78-115">— CloudService</span><span class="sxs-lookup"><span data-stu-id="abe78-115">-CloudService</span></span>
<span data-ttu-id="abe78-116">Wystąpienie usługi CloudService.</span><span class="sxs-lookup"><span data-stu-id="abe78-116">CloudService instance.</span></span>
<span data-ttu-id="abe78-117">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach usługi CLOUDSERVICE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="abe78-117">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abe78-118">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="abe78-118">-CloudServiceName</span></span>
<span data-ttu-id="abe78-119">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="abe78-119">CloudServiceName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abe78-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abe78-120">-ResourceGroupName</span></span>
<span data-ttu-id="abe78-121">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="abe78-121">ResourceGroupName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abe78-122">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="abe78-122">-SubscriptionId</span></span>
<span data-ttu-id="abe78-123">Subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="abe78-123">Subscription.</span></span>

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

### <span data-ttu-id="abe78-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe78-124">CommonParameters</span></span>
<span data-ttu-id="abe78-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abe78-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe78-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abe78-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe78-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abe78-127">INPUTS</span></span>

## <span data-ttu-id="abe78-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="abe78-128">OUTPUTS</span></span>

## <span data-ttu-id="abe78-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="abe78-129">NOTES</span></span>

<span data-ttu-id="abe78-130">ALIASY</span><span class="sxs-lookup"><span data-stu-id="abe78-130">ALIASES</span></span>

<span data-ttu-id="abe78-131">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abe78-131">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="abe78-132">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="abe78-132">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="abe78-133">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="abe78-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="abe78-134"><CloudService>CLOUDSERVICE: wystąpienie usługi CloudService.</span><span class="sxs-lookup"><span data-stu-id="abe78-134">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="abe78-135">`Location <String>`: lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="abe78-135">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="abe78-136">`[Configuration <String>]`: określa konfigurację usługi XML (cscfg) dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-136">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="abe78-137">`[ConfigurationUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji konfiguracji usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="abe78-137">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="abe78-138">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="abe78-138">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="abe78-139">Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="abe78-139">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="abe78-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: w tym artykule opisano profil rozszerzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="abe78-141">`[Extension <IExtension[]>]`: Lista rozszerzeń dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-141">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="abe78-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Jawnie określ, czy platforma może automatycznie uaktualniać typHandlerVersion do wyższych wersji pomocniczych, gdy staną się dostępne.</span><span class="sxs-lookup"><span data-stu-id="abe78-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="abe78-143">`[ForceUpdateTag <String>]`: Tag wymusza zastosowanie podanych ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="abe78-143">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="abe78-144">Zmiana wartości tagu umożliwia ponowne uruchomienie rozszerzenia bez zmieniania jakichkolwiek ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="abe78-144">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="abe78-145">Jeśli forceUpdateTag nie zostanie zmieniony, program obsługi nadal będzie stosować aktualizacje ustawień publicznych lub chronionych.</span><span class="sxs-lookup"><span data-stu-id="abe78-145">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="abe78-146">Jeśli ani forceUpdateTag, ani żadne ustawienia publiczne lub chronione nie ujdą, rozszerzenie przepływa do wystąpienia roli z tym samym numerem sekwencji, a implementacja programu obsługi może być uruchamiana ponownie, czy nie.</span><span class="sxs-lookup"><span data-stu-id="abe78-146">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="abe78-147">`[Name <String>]`: nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-147">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="abe78-148">`[ProtectedSetting <String>]`: ustawienia chronione rozszerzenia, które są szyfrowane przed wysłaniem do wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="abe78-148">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="abe78-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="abe78-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="abe78-150">`[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-150">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="abe78-151">`[RolesAppliedTo <String[]>]`: Opcjonalna lista ról do zastosowania tego rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-151">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="abe78-152">Jeśli nie określono właściwości lub określono wartość "\*", rozszerzenie jest stosowane do wszystkich ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-152">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="abe78-153">`[Setting <String>]`: ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-153">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="abe78-154">W przypadku rozszerzeń JSON są to ustawienia JSON rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-154">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="abe78-155">W przypadku rozszerzenia XML (takiego jak RDP) jest to ustawienie XML rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-155">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="abe78-156">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="abe78-156">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="abe78-157">`[Type <String>]`: określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-157">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="abe78-158">`[TypeHandlerVersion <String>]`: określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-158">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="abe78-159">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-159">Specifies the version of the extension.</span></span> <span data-ttu-id="abe78-160">Jeśli ten element nie jest określony lub jako wartość zostanie użyta gwiazdka (\*), zostanie użyta najnowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-160">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="abe78-161">Jeśli wartość jest określona z głównym numerem wersji i gwiazdką jako pomocniczy numer wersji (X.), wybrana jest najnowsza wersja pomocnicza określonej wersji głównych.</span><span class="sxs-lookup"><span data-stu-id="abe78-161">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="abe78-162">Jeśli podano główny numer wersji i numer wersji pomocniczej (X.Y), wybrana jest określona wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="abe78-162">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="abe78-163">Jeśli jest określona wersja, w wystąpieniu roli jest wykonywane automatyczne uaktualnianie.</span><span class="sxs-lookup"><span data-stu-id="abe78-163">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="abe78-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Profil sieciowy usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="abe78-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: lista konfiguracji równoważenia obciążenia dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="abe78-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: lista adresów IP</span><span class="sxs-lookup"><span data-stu-id="abe78-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="abe78-167">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="abe78-167">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="abe78-168">`[PrivateIPAddress <String>]`: prywatny adres IP, do których odwołuje się usługa w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-168">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="abe78-169">`[PublicIPAddressId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="abe78-169">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="abe78-170">`[SubnetId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="abe78-170">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="abe78-171">`[Name <String>]`: Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="abe78-171">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="abe78-172">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="abe78-172">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="abe78-173">`[Id <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="abe78-173">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="abe78-174">`[OSProfile <ICloudServiceOSProfile>]`: w tym artykule opisano profil systemu operacyjnego usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-174">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="abe78-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Określa zestaw certyfikatów, które powinny być instalowane w wystąpieniach ról.</span><span class="sxs-lookup"><span data-stu-id="abe78-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="abe78-176">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="abe78-176">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="abe78-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: lista odwołań do magazynu kluczy w u źródłach SourceVault, które zawierają certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="abe78-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="abe78-178">`[CertificateUrl <String>]`: jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako tajny.</span><span class="sxs-lookup"><span data-stu-id="abe78-178">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="abe78-179">`[PackageUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji pakietu usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="abe78-179">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="abe78-180">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="abe78-180">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="abe78-181">Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="abe78-181">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="abe78-182">`[RoleProfile <ICloudServiceRoleProfile>]`: opis profilu roli dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="abe78-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: lista ról dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="abe78-184">`[Name <String>]`: nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="abe78-184">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="abe78-185">`[SkuCapacity <Int64?>]`: określa liczbę wystąpień ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-185">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="abe78-186">`[SkuName <String>]`: nazwa sKU.</span><span class="sxs-lookup"><span data-stu-id="abe78-186">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="abe78-187">UWAGA: Jeśli nowa wersja SKU nie jest obsługiwana na sprzęcie, na który obecnie działa usługa w chmurze, musisz usunąć i ponownie utworzyć usługę w chmurze lub wrócić do starej.</span><span class="sxs-lookup"><span data-stu-id="abe78-187">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="abe78-188">`[SkuTier <String>]`: określa warstwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-188">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="abe78-189">Dopuszczalne wartości to</span><span class="sxs-lookup"><span data-stu-id="abe78-189">Possible Values are</span></span> <br /><br /> <span data-ttu-id="abe78-190">**Standardowe**</span><span class="sxs-lookup"><span data-stu-id="abe78-190">**Standard**</span></span> <br /><br /> <span data-ttu-id="abe78-191">**Podstawowe**</span><span class="sxs-lookup"><span data-stu-id="abe78-191">**Basic**</span></span>
  - <span data-ttu-id="abe78-192">`[StartCloudService <Boolean?>]`: (Opcjonalnie) Wskazuje, czy usługa w chmurze ma być uruchamiana natychmiast po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="abe78-192">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="abe78-193">Wartość domyślna `true` to.</span><span class="sxs-lookup"><span data-stu-id="abe78-193">The default value is `true`.</span></span>         <span data-ttu-id="abe78-194">Jeśli wartość jest fałszywa, model usługi jest nadal wdrażany, ale kod nie jest uruchamiany natychmiast.</span><span class="sxs-lookup"><span data-stu-id="abe78-194">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="abe78-195">Zamiast tego usługa będzie się uruchamiać do momentu wywołania startowego, o której usługa zostanie uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="abe78-195">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="abe78-196">Wdrożona usługa nadal ponosi opłaty, nawet jeśli zostanie wyłączony.</span><span class="sxs-lookup"><span data-stu-id="abe78-196">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="abe78-197">`[Tag <ICloudServiceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="abe78-197">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="abe78-198">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="abe78-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="abe78-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: tryb aktualizacji dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="abe78-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="abe78-200">Wystąpienia ról są przydzielane do aktualizowania domen podczas wdrażania usługi.</span><span class="sxs-lookup"><span data-stu-id="abe78-200">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="abe78-201">Aktualizacje mogą być inicjowane ręcznie w każdej domenie aktualizacji lub inicjowane automatycznie we wszystkich domenach aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="abe78-201">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="abe78-202">Dopuszczalne wartości to</span><span class="sxs-lookup"><span data-stu-id="abe78-202">Possible Values are</span></span> <br /><br /><span data-ttu-id="abe78-203">**Automatycznie**</span><span class="sxs-lookup"><span data-stu-id="abe78-203">**Auto**</span></span><br /><br /><span data-ttu-id="abe78-204">**Ręcznie**</span><span class="sxs-lookup"><span data-stu-id="abe78-204">**Manual**</span></span> <br /><br /><span data-ttu-id="abe78-205">**Jednoczesne**</span><span class="sxs-lookup"><span data-stu-id="abe78-205">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="abe78-206">Jeśli nie zostanie określona, wartością domyślną jest Auto. Jeśli ta wartość jest ustawiona na Ręcznie, aby zastosować aktualizację, musi zostać wywołana nazwa PUT UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="abe78-206">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="abe78-207">Jeśli ta opcja jest ustawiona na Automatyczne, aktualizacja jest automatycznie stosowana do każdej domeny aktualizacji w sekwencji.</span><span class="sxs-lookup"><span data-stu-id="abe78-207">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="abe78-208">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abe78-208">RELATED LINKS</span></span>

