---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195114"
---
# <span data-ttu-id="0f2aa-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="0f2aa-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="0f2aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2aa-103">Zamienia punkty VIP między dwoma równoważeniem obciążenia usług w chmurze (wsparcie rozszerzone).</span><span class="sxs-lookup"><span data-stu-id="0f2aa-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="0f2aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f2aa-104">SYNTAX</span></span>

### <span data-ttu-id="0f2aa-105">CloudServiceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0f2aa-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0f2aa-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="0f2aa-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f2aa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f2aa-107">DESCRIPTION</span></span>
<span data-ttu-id="0f2aa-108">Zamienia punkty VIP między dwoma równoważeniem obciążenia usług w chmurze (wsparcie rozszerzone).</span><span class="sxs-lookup"><span data-stu-id="0f2aa-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="0f2aa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f2aa-109">EXAMPLES</span></span>

### <span data-ttu-id="0f2aa-110">Przykład 1. Przełączanie usługi w chmurze przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="0f2aa-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="0f2aa-111">Powyższe polecenie wywoła operację vipswap w usłudze w chmurze o nazwie "BService" i wykona operację, gdy użytkownik potwierdzi akcję w wierszu potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="0f2aa-112">Usługa "BService" zostanie zamieniona na usługę w chmurze, która można zamienić.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="0f2aa-113">Przykład 2. Przełączanie usługi w chmurze przy użyciu obiektu usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="0f2aa-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="0f2aa-114">Powyższe polecenie wywoła operację vipswap w usłudze w chmurze o nazwie "BService" i wykona operację, gdy użytkownik potwierdzi akcję w wierszu potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="0f2aa-115">Usługa "BService" zostanie zamieniona na usługę w chmurze, która można zamienić.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="0f2aa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f2aa-116">PARAMETERS</span></span>

### <span data-ttu-id="0f2aa-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0f2aa-117">-AsJob</span></span>
<span data-ttu-id="0f2aa-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0f2aa-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0f2aa-119">— Async</span><span class="sxs-lookup"><span data-stu-id="0f2aa-119">-Async</span></span>


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

### <span data-ttu-id="0f2aa-120">— CloudService</span><span class="sxs-lookup"><span data-stu-id="0f2aa-120">-CloudService</span></span>
<span data-ttu-id="0f2aa-121">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach usługi CLOUDSERVICE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="0f2aa-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="0f2aa-122">-CloudServiceName</span></span>


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

### <span data-ttu-id="0f2aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2aa-123">-DefaultProfile</span></span>
<span data-ttu-id="0f2aa-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f2aa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2aa-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="0f2aa-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f2aa-126">-SubscriptionId</span></span>
<span data-ttu-id="0f2aa-127">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0f2aa-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0f2aa-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f2aa-129">-Confirm</span></span>
<span data-ttu-id="0f2aa-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f2aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f2aa-131">-WhatIf</span></span>
<span data-ttu-id="0f2aa-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f2aa-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f2aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2aa-134">CommonParameters</span></span>
<span data-ttu-id="0f2aa-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2aa-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f2aa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2aa-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f2aa-137">INPUTS</span></span>

## <span data-ttu-id="0f2aa-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f2aa-138">OUTPUTS</span></span>

### <span data-ttu-id="0f2aa-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f2aa-139">System.Boolean</span></span>

## <span data-ttu-id="0f2aa-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f2aa-140">NOTES</span></span>

<span data-ttu-id="0f2aa-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0f2aa-141">ALIASES</span></span>

<span data-ttu-id="0f2aa-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0f2aa-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f2aa-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f2aa-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f2aa-145"><CloudService>CLOUDSERVICE:</span><span class="sxs-lookup"><span data-stu-id="0f2aa-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="0f2aa-146">`Location <String>`: lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="0f2aa-147">`[Configuration <String>]`: określa konfigurację usługi XML (cscfg) dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="0f2aa-148">`[ConfigurationUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji konfiguracji usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="0f2aa-149">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="0f2aa-150">Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="0f2aa-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: w tym artykule opisano profil rozszerzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="0f2aa-152">`[Extension <IExtension[]>]`: Lista rozszerzeń dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="0f2aa-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Jawnie określ, czy platforma może automatycznie uaktualniać typHandlerVersion do wyższych wersji pomocniczych, gdy staną się dostępne.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="0f2aa-154">`[ForceUpdateTag <String>]`: Tag wymusza zastosowanie podanych ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="0f2aa-155">Zmiana wartości tagu umożliwia ponowne uruchomienie rozszerzenia bez zmieniania jakichkolwiek ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="0f2aa-156">Jeśli forceUpdateTag nie zostanie zmieniony, program obsługi nadal będzie stosować aktualizacje ustawień publicznych lub chronionych.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="0f2aa-157">Jeśli ani forceUpdateTag, ani żadne ustawienia publiczne lub chronione nie ujdą, rozszerzenie przepływa do wystąpienia roli z tym samym numerem sekwencji, a implementacja programu obsługi może być uruchamiana ponownie, czy nie.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="0f2aa-158">`[Name <String>]`: nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="0f2aa-159">`[ProtectedSetting <String>]`: chronione ustawienia rozszerzenia, które są szyfrowane przed wysłaniem do wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="0f2aa-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="0f2aa-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="0f2aa-161">`[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="0f2aa-162">`[RolesAppliedTo <String[]>]`: Opcjonalna lista ról do zastosowania tego rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="0f2aa-163">Jeśli nie określono właściwości lub określono wartość "\*", rozszerzenie jest stosowane do wszystkich ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="0f2aa-164">`[Setting <String>]`: ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="0f2aa-165">W przypadku rozszerzeń JSON są to ustawienia JSON rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="0f2aa-166">W przypadku rozszerzenia XML (takiego jak RDP) jest to ustawienie XML rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="0f2aa-167">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="0f2aa-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="0f2aa-168">`[Type <String>]`: określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="0f2aa-169">`[TypeHandlerVersion <String>]`: określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="0f2aa-170">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-170">Specifies the version of the extension.</span></span> <span data-ttu-id="0f2aa-171">Jeśli ten element nie zostanie określony lub jako wartość zostanie użyta gwiazdka (\*), zostanie użyta najnowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="0f2aa-172">Jeśli wartość zostanie określona z głównym numerem wersji i gwiazdką jako pomocniczy numer wersji (X),zostanie wybrana najnowsza wersja pomocnicza określonej wersji głównych.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="0f2aa-173">Jeśli podano główny numer wersji i numer wersji pomocniczej (X.Y), wybrana jest określona wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="0f2aa-174">Jeśli jest określona wersja, w wystąpieniu roli jest wykonywane automatyczne uaktualnianie.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="0f2aa-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Profil sieciowy usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="0f2aa-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: lista konfiguracji równoważenia obciążenia dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="0f2aa-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: lista adresów IP</span><span class="sxs-lookup"><span data-stu-id="0f2aa-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="0f2aa-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="0f2aa-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="0f2aa-179">`[PrivateIPAddress <String>]`: prywatny adres IP, do których odwołuje się usługa w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="0f2aa-180">`[PublicIPAddressId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="0f2aa-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="0f2aa-181">`[SubnetId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="0f2aa-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="0f2aa-182">`[Name <String>]`: Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="0f2aa-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="0f2aa-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="0f2aa-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="0f2aa-184">`[Id <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="0f2aa-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="0f2aa-185">`[OSProfile <ICloudServiceOSProfile>]`: w tym artykule opisano profil systemu operacyjnego usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="0f2aa-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Określa zestaw certyfikatów, które powinny być instalowane w wystąpieniach ról.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="0f2aa-187">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="0f2aa-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="0f2aa-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: lista odwołań do magazynu kluczy w u źródłach SourceVault, które zawierają certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="0f2aa-189">`[CertificateUrl <String>]`: jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako tajny.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="0f2aa-190">`[PackageUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji pakietu usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="0f2aa-191">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="0f2aa-192">Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="0f2aa-193">`[RoleProfile <ICloudServiceRoleProfile>]`: opis profilu roli dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="0f2aa-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: lista ról dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="0f2aa-195">`[Name <String>]`: nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="0f2aa-196">`[SkuCapacity <Int64?>]`: określa liczbę wystąpień ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="0f2aa-197">`[SkuName <String>]`: nazwa sKU.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="0f2aa-198">UWAGA: Jeśli nowa wersja SKU nie jest obsługiwana na sprzęcie, na który obecnie działa usługa w chmurze, musisz usunąć i ponownie utworzyć usługę w chmurze lub wrócić do starej.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="0f2aa-199">`[SkuTier <String>]`: określa warstwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="0f2aa-200">Dopuszczalne wartości to</span><span class="sxs-lookup"><span data-stu-id="0f2aa-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="0f2aa-201">**Standardowe**</span><span class="sxs-lookup"><span data-stu-id="0f2aa-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="0f2aa-202">**Podstawowe**</span><span class="sxs-lookup"><span data-stu-id="0f2aa-202">**Basic**</span></span>
  - <span data-ttu-id="0f2aa-203">`[StartCloudService <Boolean?>]`: (Opcjonalnie) Wskazuje, czy usługa w chmurze ma być uruchamiana natychmiast po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="0f2aa-204">Wartość domyślna `true` to.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-204">The default value is `true`.</span></span>         <span data-ttu-id="0f2aa-205">Jeśli wartość jest fałszywa, model usługi jest nadal wdrażany, ale kod nie jest uruchamiany natychmiast.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="0f2aa-206">Zamiast tego usługa będzie się uruchamiać do momentu wywołania startowego, o której usługa zostanie uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="0f2aa-207">Wdrożona usługa nadal wiąże się z opłatami, nawet jeśli zostanie wyłączony.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="0f2aa-208">`[Tag <ICloudServiceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="0f2aa-209">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0f2aa-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: tryb aktualizacji dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="0f2aa-211">Wystąpienia ról są przydzielane do aktualizowania domen podczas wdrażania usługi.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="0f2aa-212">Aktualizacje mogą być inicjowane ręcznie w każdej domenie aktualizacji lub inicjowane automatycznie we wszystkich domenach aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="0f2aa-213">Dopuszczalne wartości to</span><span class="sxs-lookup"><span data-stu-id="0f2aa-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="0f2aa-214">**Automatycznie**</span><span class="sxs-lookup"><span data-stu-id="0f2aa-214">**Auto**</span></span><br /><br /><span data-ttu-id="0f2aa-215">**Ręcznie**</span><span class="sxs-lookup"><span data-stu-id="0f2aa-215">**Manual**</span></span> <br /><br /><span data-ttu-id="0f2aa-216">**Jednoczesne**</span><span class="sxs-lookup"><span data-stu-id="0f2aa-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="0f2aa-217">Jeśli nie zostanie określona, wartością domyślną jest Auto. Jeśli ta wartość jest ustawiona na Ręcznie, aby zastosować aktualizację, musi zostać wywołana nazwa PUT UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="0f2aa-218">Jeśli ta opcja jest ustawiona na Automatyczne, aktualizacja jest automatycznie stosowana do każdej domeny aktualizacji w sekwencji.</span><span class="sxs-lookup"><span data-stu-id="0f2aa-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="0f2aa-219">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f2aa-219">RELATED LINKS</span></span>

