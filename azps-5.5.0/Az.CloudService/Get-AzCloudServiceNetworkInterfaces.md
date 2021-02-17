---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServiceNetworkInterfaces
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
ms.openlocfilehash: 7f8a51c518bd034e51d8c25d5029bb57b3e38caf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196987"
---
# <span data-ttu-id="ad650-101">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="ad650-101">Get-AzCloudServiceNetworkInterfaces</span></span>

## <span data-ttu-id="ad650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad650-102">SYNOPSIS</span></span>
<span data-ttu-id="ad650-103">Uzyskiwanie interfejsów sieciowych usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-103">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="ad650-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad650-104">SYNTAX</span></span>

### <span data-ttu-id="ad650-105">CloudServiceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="ad650-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ad650-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="ad650-106">CloudService</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## <span data-ttu-id="ad650-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad650-107">DESCRIPTION</span></span>
<span data-ttu-id="ad650-108">Uzyskiwanie interfejsów sieciowych usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-108">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="ad650-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad650-109">EXAMPLES</span></span>

### <span data-ttu-id="ad650-110">Przykład 1. Uzyskiwanie interfejsów sieciowych według nazwy usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="ad650-110">Example 1: Get network interfaces by a cloud service name</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="ad650-111">Pobiera wszystkie interfejsy sieciowe dla danej nazwy usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-111">Gets all the network interfaces for a given cloud service name.</span></span>

### <span data-ttu-id="ad650-112">Przykład 2. Uzyskiwanie interfejsów sieciowych za pomocą obiektu usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="ad650-112">Example 2: Get network interfaces by a cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

<span data-ttu-id="ad650-113">Pobiera wszystkie interfejsy sieciowe dla danego obiektu usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-113">Gets all the network interfaces for a given cloud service object.</span></span>

### <span data-ttu-id="ad650-114">Przykład 3. Uzyskiwanie interfejsów sieciowych według obiektu usługi w chmurze i nazwy wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="ad650-114">Example 3: Get network interfaces by a cloud service object and role instance name.</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

<span data-ttu-id="ad650-115">Pobiera wszystkie interfejsy sieciowe dla danego obiektu usługi w chmurze i nazwy wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="ad650-115">Gets all the network interfaces for a given cloud service object and role instance name.</span></span>

## <span data-ttu-id="ad650-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad650-116">PARAMETERS</span></span>

### <span data-ttu-id="ad650-117">— CloudService</span><span class="sxs-lookup"><span data-stu-id="ad650-117">-CloudService</span></span>
<span data-ttu-id="ad650-118">Wystąpienie usługi CloudService.</span><span class="sxs-lookup"><span data-stu-id="ad650-118">CloudService instance.</span></span>
<span data-ttu-id="ad650-119">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach usługi CLOUDSERVICE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="ad650-119">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad650-120">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="ad650-120">-CloudServiceName</span></span>
<span data-ttu-id="ad650-121">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="ad650-121">CloudServiceName.</span></span>

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

### <span data-ttu-id="ad650-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad650-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad650-123">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ad650-123">ResourceGroupName.</span></span>

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

### <span data-ttu-id="ad650-124">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="ad650-124">-RoleInstanceName</span></span>
<span data-ttu-id="ad650-125">RoleInstanceName.</span><span class="sxs-lookup"><span data-stu-id="ad650-125">RoleInstanceName.</span></span>

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

### <span data-ttu-id="ad650-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad650-126">-SubscriptionId</span></span>
<span data-ttu-id="ad650-127">Subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="ad650-127">Subscription.</span></span>

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

### <span data-ttu-id="ad650-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad650-128">CommonParameters</span></span>
<span data-ttu-id="ad650-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad650-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad650-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad650-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad650-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad650-131">INPUTS</span></span>

## <span data-ttu-id="ad650-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad650-132">OUTPUTS</span></span>

## <span data-ttu-id="ad650-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad650-133">NOTES</span></span>

<span data-ttu-id="ad650-134">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ad650-134">ALIASES</span></span>

<span data-ttu-id="ad650-135">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ad650-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad650-136">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ad650-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad650-137">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad650-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad650-138"><CloudService>CLOUDSERVICE: wystąpienie usługi CloudService.</span><span class="sxs-lookup"><span data-stu-id="ad650-138">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="ad650-139">`Location <String>`: lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ad650-139">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="ad650-140">`[Configuration <String>]`: określa konfigurację usługi XML (cscfg) dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-140">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="ad650-141">`[ConfigurationUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji konfiguracji usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="ad650-141">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="ad650-142">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ad650-142">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="ad650-143">Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="ad650-143">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="ad650-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: w tym artykule opisano profil rozszerzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="ad650-145">`[Extension <IExtension[]>]`: Lista rozszerzeń dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-145">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="ad650-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Jawnie określ, czy platforma może automatycznie uaktualniać typHandlerVersion do wyższych wersji pomocniczych, gdy staną się dostępne.</span><span class="sxs-lookup"><span data-stu-id="ad650-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="ad650-147">`[ForceUpdateTag <String>]`: Tag wymusza zastosowanie podanych ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="ad650-147">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="ad650-148">Zmiana wartości tagu umożliwia ponowne uruchomienie rozszerzenia bez zmieniania jakichkolwiek ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="ad650-148">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="ad650-149">Jeśli forceUpdateTag nie zostanie zmieniony, program obsługi nadal będzie stosować aktualizacje ustawień publicznych lub chronionych.</span><span class="sxs-lookup"><span data-stu-id="ad650-149">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="ad650-150">Jeśli ani forceUpdateTag, ani żadne ustawienia publiczne lub chronione nie ujdą, rozszerzenie przepływa do wystąpienia roli z tym samym numerem sekwencji, a implementacja programu obsługi może być uruchamiana ponownie, czy nie.</span><span class="sxs-lookup"><span data-stu-id="ad650-150">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="ad650-151">`[Name <String>]`: nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-151">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="ad650-152">`[ProtectedSetting <String>]`: ustawienia chronione rozszerzenia, które są szyfrowane przed wysłaniem do wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="ad650-152">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="ad650-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ad650-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="ad650-154">`[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-154">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="ad650-155">`[RolesAppliedTo <String[]>]`: Opcjonalna lista ról do zastosowania tego rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-155">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="ad650-156">Jeśli nie określono właściwości lub określono wartość "\*", rozszerzenie jest stosowane do wszystkich ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-156">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="ad650-157">`[Setting <String>]`: ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-157">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="ad650-158">W przypadku rozszerzeń JSON są to ustawienia JSON rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-158">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="ad650-159">W przypadku rozszerzenia XML (takiego jak RDP) jest to ustawienie XML rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-159">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="ad650-160">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="ad650-160">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ad650-161">`[Type <String>]`: określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-161">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="ad650-162">`[TypeHandlerVersion <String>]`: określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-162">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="ad650-163">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-163">Specifies the version of the extension.</span></span> <span data-ttu-id="ad650-164">Jeśli ten element nie zostanie określony lub jako wartość zostanie użyta gwiazdka (\*), zostanie użyta najnowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-164">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="ad650-165">Jeśli wartość jest określona z głównym numerem wersji i gwiazdką jako pomocniczy numer wersji (X.), wybrana jest najnowsza wersja pomocnicza określonej wersji głównych.</span><span class="sxs-lookup"><span data-stu-id="ad650-165">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="ad650-166">Jeśli określono główny numer wersji i numer wersji pomocniczej (X.Y), wybrana jest określona wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad650-166">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="ad650-167">Jeśli jest określona wersja, automatyczne uaktualnianie jest wykonywane w wystąpieniu roli.</span><span class="sxs-lookup"><span data-stu-id="ad650-167">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="ad650-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Profil sieciowy usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="ad650-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: lista konfiguracji równoważenia obciążenia dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="ad650-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: lista adresów IP</span><span class="sxs-lookup"><span data-stu-id="ad650-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="ad650-171">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ad650-171">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="ad650-172">`[PrivateIPAddress <String>]`: prywatny adres IP, do których odwołuje się usługa w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-172">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="ad650-173">`[PublicIPAddressId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="ad650-173">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="ad650-174">`[SubnetId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="ad650-174">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ad650-175">`[Name <String>]`: Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="ad650-175">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="ad650-176">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="ad650-176">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="ad650-177">`[Id <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="ad650-177">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="ad650-178">`[OSProfile <ICloudServiceOSProfile>]`: w tym artykule opisano profil systemu operacyjnego usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-178">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="ad650-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Określa zestaw certyfikatów, które powinny być instalowane w wystąpieniach ról.</span><span class="sxs-lookup"><span data-stu-id="ad650-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="ad650-180">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="ad650-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ad650-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: lista odwołań do magazynu kluczy w u źródłach SourceVault, które zawierają certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="ad650-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="ad650-182">`[CertificateUrl <String>]`: jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako tajny.</span><span class="sxs-lookup"><span data-stu-id="ad650-182">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="ad650-183">`[PackageUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji pakietu usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="ad650-183">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="ad650-184">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ad650-184">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="ad650-185">Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="ad650-185">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="ad650-186">`[RoleProfile <ICloudServiceRoleProfile>]`: opis profilu roli dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="ad650-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: lista ról dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="ad650-188">`[Name <String>]`: nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ad650-188">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="ad650-189">`[SkuCapacity <Int64?>]`: określa liczbę wystąpień ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-189">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="ad650-190">`[SkuName <String>]`: nazwa sKU.</span><span class="sxs-lookup"><span data-stu-id="ad650-190">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="ad650-191">UWAGA: Jeśli nowa wersja SKU nie jest obsługiwana na sprzęcie, na który obecnie działa usługa w chmurze, musisz usunąć i ponownie utworzyć usługę w chmurze lub wrócić do starej.</span><span class="sxs-lookup"><span data-stu-id="ad650-191">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="ad650-192">`[SkuTier <String>]`: określa warstwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-192">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="ad650-193">Dopuszczalne wartości to</span><span class="sxs-lookup"><span data-stu-id="ad650-193">Possible Values are</span></span> <br /><br /> <span data-ttu-id="ad650-194">**Standardowe**</span><span class="sxs-lookup"><span data-stu-id="ad650-194">**Standard**</span></span> <br /><br /> <span data-ttu-id="ad650-195">**Podstawowe**</span><span class="sxs-lookup"><span data-stu-id="ad650-195">**Basic**</span></span>
  - <span data-ttu-id="ad650-196">`[StartCloudService <Boolean?>]`: (Opcjonalnie) Wskazuje, czy usługa w chmurze ma być uruchamiana natychmiast po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="ad650-196">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="ad650-197">Wartość domyślna `true` to.</span><span class="sxs-lookup"><span data-stu-id="ad650-197">The default value is `true`.</span></span>         <span data-ttu-id="ad650-198">Jeśli wartość jest fałszywa, model usługi jest nadal wdrażany, ale kod nie jest uruchamiany natychmiast.</span><span class="sxs-lookup"><span data-stu-id="ad650-198">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="ad650-199">Zamiast tego usługa będzie się uruchamiać do momentu wywołania startowego, o której usługa zostanie uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="ad650-199">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="ad650-200">Wdrożona usługa nadal wiąże się z opłatami, nawet jeśli zostanie wyłączony.</span><span class="sxs-lookup"><span data-stu-id="ad650-200">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="ad650-201">`[Tag <ICloudServiceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad650-201">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ad650-202">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ad650-202">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ad650-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: tryb aktualizacji dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ad650-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="ad650-204">Wystąpienia ról są przydzielane do aktualizowania domen podczas wdrażania usługi.</span><span class="sxs-lookup"><span data-stu-id="ad650-204">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="ad650-205">Aktualizacje mogą być inicjowane ręcznie w każdej domenie aktualizacji lub inicjowane automatycznie we wszystkich domenach aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ad650-205">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="ad650-206">Dopuszczalne wartości to</span><span class="sxs-lookup"><span data-stu-id="ad650-206">Possible Values are</span></span> <br /><br /><span data-ttu-id="ad650-207">**Automatycznie**</span><span class="sxs-lookup"><span data-stu-id="ad650-207">**Auto**</span></span><br /><br /><span data-ttu-id="ad650-208">**Ręcznie**</span><span class="sxs-lookup"><span data-stu-id="ad650-208">**Manual**</span></span> <br /><br /><span data-ttu-id="ad650-209">**Jednoczesne**</span><span class="sxs-lookup"><span data-stu-id="ad650-209">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="ad650-210">Jeśli nie zostanie określona, wartością domyślną jest Auto. Jeśli ta wartość jest ustawiona na Ręcznie, aby zastosować aktualizację, musi zostać wywołana nazwa PUT UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="ad650-210">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="ad650-211">Jeśli ta opcja jest ustawiona na Automatyczne, aktualizacja jest automatycznie stosowana do każdej domeny aktualizacji w sekwencji.</span><span class="sxs-lookup"><span data-stu-id="ad650-211">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="ad650-212">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad650-212">RELATED LINKS</span></span>

