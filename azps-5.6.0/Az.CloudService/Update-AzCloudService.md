---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: bb67420e3fbb4479a79c7a837aad3b9a65635d88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007178"
---
# <span data-ttu-id="73dec-101">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="73dec-101">Update-AzCloudService</span></span>

## <span data-ttu-id="73dec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73dec-102">SYNOPSIS</span></span>
<span data-ttu-id="73dec-103">Tworzenie lub aktualizowanie usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-103">Create or update a cloud service.</span></span>
<span data-ttu-id="73dec-104">Niektóre właściwości można ustawić tylko podczas tworzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="73dec-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73dec-105">SYNTAX</span></span>

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="73dec-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="73dec-106">DESCRIPTION</span></span>
<span data-ttu-id="73dec-107">Tworzenie lub aktualizowanie usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-107">Create or update a cloud service.</span></span>
<span data-ttu-id="73dec-108">Niektóre właściwości można ustawić tylko podczas tworzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="73dec-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73dec-109">EXAMPLES</span></span>

### <span data-ttu-id="73dec-110">Przykład 1. Dodawanie rozszerzenia RDP do istniejącej usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="73dec-110">Example 1: Add RDP extension to existing cloud service</span></span>
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="73dec-111">Powyższy zestaw poleceń dodaje rozszerzenie RDP do istniejącej już usługi w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="73dec-111">Above set of commands adds a RDP extension to already existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="73dec-112">Przykład 2. Usuwanie wszystkich rozszerzeń z usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="73dec-112">Example 2: Remove all extensions from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="73dec-113">Powyższy zestaw poleceń usuwa wszystkie rozszerzenia istniejącej usługi w chmurze o nazwie ContosoCS, które należą do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="73dec-113">Above set of commands removes all extensions from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="73dec-114">Przykład 3. Usuwanie rozszerzenia RDP z usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="73dec-114">Example 3: Remove RDP extension from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="73dec-115">Powyższy zestaw poleceń usuwa rozszerzenie RDP istniejącej usługi w chmurze o nazwie ContosoCS, które należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="73dec-115">Above set of commands removes RDP extension from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="73dec-116">Przykład 4. Scale-Out / Scale-In wystąpień ról</span><span class="sxs-lookup"><span data-stu-id="73dec-116">Example 4: Scale-Out / Scale-In role instances</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="73dec-117">Powyżej zestawu poleceń pokazano, jak przeskalować i skalować wystąpienia ról dla usługi w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="73dec-117">Above set of commands shows how to scale-out and scale-in role instance count for cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="73dec-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73dec-118">PARAMETERS</span></span>

### <span data-ttu-id="73dec-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="73dec-119">-AsJob</span></span>
<span data-ttu-id="73dec-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="73dec-120">Run the command as a job</span></span>

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

### <span data-ttu-id="73dec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73dec-121">-DefaultProfile</span></span>
<span data-ttu-id="73dec-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73dec-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73dec-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73dec-123">-InputObject</span></span>
<span data-ttu-id="73dec-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="73dec-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73dec-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="73dec-125">-NoWait</span></span>
<span data-ttu-id="73dec-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="73dec-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="73dec-127">- Parametr</span><span class="sxs-lookup"><span data-stu-id="73dec-127">-Parameter</span></span>
<span data-ttu-id="73dec-128">W tym artykule opisano usługę w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-128">Describes the cloud service.</span></span>
<span data-ttu-id="73dec-129">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach PARAMETRu i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="73dec-129">To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73dec-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73dec-130">-Confirm</span></span>
<span data-ttu-id="73dec-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="73dec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73dec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73dec-132">-WhatIf</span></span>
<span data-ttu-id="73dec-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73dec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73dec-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="73dec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73dec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73dec-135">CommonParameters</span></span>
<span data-ttu-id="73dec-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73dec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73dec-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73dec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73dec-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73dec-138">INPUTS</span></span>

### <span data-ttu-id="73dec-139">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.iCloudService</span><span class="sxs-lookup"><span data-stu-id="73dec-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

### <span data-ttu-id="73dec-140">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="73dec-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="73dec-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73dec-141">OUTPUTS</span></span>

### <span data-ttu-id="73dec-142">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.iCloudService</span><span class="sxs-lookup"><span data-stu-id="73dec-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="73dec-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73dec-143">NOTES</span></span>

<span data-ttu-id="73dec-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="73dec-144">ALIASES</span></span>

<span data-ttu-id="73dec-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73dec-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73dec-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="73dec-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73dec-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73dec-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73dec-148">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="73dec-148">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73dec-149">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="73dec-149">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="73dec-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="73dec-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73dec-151">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="73dec-151">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="73dec-152">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="73dec-152">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="73dec-153">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="73dec-153">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="73dec-154">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="73dec-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="73dec-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="73dec-155">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="73dec-156">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="73dec-156">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="73dec-157">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="73dec-157">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

<span data-ttu-id="73dec-158">PARAMETR: <ICloudService> w tym artykule opisano usługę w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-158">PARAMETER <ICloudService>: Describes the cloud service.</span></span>
  - <span data-ttu-id="73dec-159">`Location <String>`: lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="73dec-159">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="73dec-160">`[Configuration <String>]`: określa konfigurację usługi XML (cscfg) dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-160">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="73dec-161">`[ConfigurationUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji konfiguracji usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="73dec-161">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="73dec-162">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="73dec-162">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="73dec-163">Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="73dec-163">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="73dec-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: w tym artykule opisano profil rozszerzenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="73dec-165">`[Extension <IExtension[]>]`: Lista rozszerzeń dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-165">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="73dec-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Jawnie określ, czy platforma może automatycznie uaktualniać typHandlerVersion do wyższych wersji pomocniczych, gdy staną się dostępne.</span><span class="sxs-lookup"><span data-stu-id="73dec-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="73dec-167">`[ForceUpdateTag <String>]`: Tag wymusza zastosowanie podanych ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="73dec-167">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="73dec-168">Zmiana wartości tagu umożliwia ponowne uruchomienie rozszerzenia bez zmieniania jakichkolwiek ustawień publicznych i chronionych.</span><span class="sxs-lookup"><span data-stu-id="73dec-168">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="73dec-169">Jeśli tag forceUpdate nie zostanie zmieniony, program obsługi nadal będzie stosować aktualizacje ustawień publicznych lub chronionych.</span><span class="sxs-lookup"><span data-stu-id="73dec-169">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="73dec-170">Jeśli ani forceUpdateTag, ani żadne ustawienia publiczne lub chronione nie ujdą, rozszerzenie przepływa do wystąpienia roli z tym samym numerem sekwencji, a implementacja programu obsługi może być uruchamiana ponownie, czy nie.</span><span class="sxs-lookup"><span data-stu-id="73dec-170">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="73dec-171">`[Name <String>]`: nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-171">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="73dec-172">`[ProtectedSetting <String>]`: ustawienia chronione rozszerzenia, które są szyfrowane przed wysłaniem do wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="73dec-172">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="73dec-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="73dec-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="73dec-174">`[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-174">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="73dec-175">`[RolesAppliedTo <String[]>]`: Opcjonalna lista ról do zastosowania tego rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-175">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="73dec-176">Jeśli nie określono właściwości lub określono wartość "\*", rozszerzenie jest stosowane do wszystkich ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-176">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="73dec-177">`[Setting <String>]`: ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-177">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="73dec-178">W przypadku rozszerzeń JSON są to ustawienia JSON rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-178">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="73dec-179">W przypadku rozszerzenia XML (takiego jak RDP) jest to ustawienie XML rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-179">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="73dec-180">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="73dec-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="73dec-181">`[Type <String>]`: określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-181">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="73dec-182">`[TypeHandlerVersion <String>]`: określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-182">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="73dec-183">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-183">Specifies the version of the extension.</span></span> <span data-ttu-id="73dec-184">Jeśli ten element nie jest określony lub jako wartość zostanie użyta gwiazdka (\*), zostanie użyta najnowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-184">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="73dec-185">Jeśli wartość zostanie określona z głównym numerem wersji i gwiazdką jako pomocniczy numer wersji (X),zostanie wybrana najnowsza wersja pomocnicza określonej wersji głównych.</span><span class="sxs-lookup"><span data-stu-id="73dec-185">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="73dec-186">Jeśli określono główny numer wersji i numer wersji pomocniczej (X.Y), wybrana jest określona wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73dec-186">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="73dec-187">Jeśli jest określona wersja, automatyczne uaktualnianie jest wykonywane w wystąpieniu roli.</span><span class="sxs-lookup"><span data-stu-id="73dec-187">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="73dec-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Profil sieciowy dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="73dec-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: lista konfiguracji równoważenia obciążenia dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="73dec-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: lista adresów IP</span><span class="sxs-lookup"><span data-stu-id="73dec-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="73dec-191">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="73dec-191">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="73dec-192">`[PrivateIPAddress <String>]`: prywatny adres IP, do których odwołuje się usługa w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-192">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="73dec-193">`[PublicIPAddressId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="73dec-193">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="73dec-194">`[SubnetId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="73dec-194">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="73dec-195">`[Name <String>]`: Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="73dec-195">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="73dec-196">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="73dec-196">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="73dec-197">`[Id <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="73dec-197">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="73dec-198">`[OSProfile <ICloudServiceOSProfile>]`: w tym artykule opisano profil systemu operacyjnego usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-198">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="73dec-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Określa zestaw certyfikatów, które powinny być instalowane w wystąpieniach ról.</span><span class="sxs-lookup"><span data-stu-id="73dec-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="73dec-200">`[SourceVaultId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="73dec-200">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="73dec-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: lista odwołań do magazynu kluczy w u źródłach SourceVault, które zawierają certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="73dec-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="73dec-202">`[CertificateUrl <String>]`: jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako tajny.</span><span class="sxs-lookup"><span data-stu-id="73dec-202">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="73dec-203">`[PackageUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji pakietu usługi w usłudze obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="73dec-203">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="73dec-204">Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="73dec-204">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="73dec-205">Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.</span><span class="sxs-lookup"><span data-stu-id="73dec-205">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="73dec-206">`[RoleProfile <ICloudServiceRoleProfile>]`: opis profilu roli dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="73dec-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: lista ról dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="73dec-208">`[Name <String>]`: nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="73dec-208">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="73dec-209">`[SkuCapacity <Int64?>]`: określa liczbę wystąpień ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-209">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="73dec-210">`[SkuName <String>]`: nazwa sKU.</span><span class="sxs-lookup"><span data-stu-id="73dec-210">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="73dec-211">UWAGA: Jeśli nowa wersja SKU nie jest obsługiwana na sprzęcie, na który obecnie działa usługa w chmurze, musisz usunąć i ponownie utworzyć usługę w chmurze lub wrócić do starej.</span><span class="sxs-lookup"><span data-stu-id="73dec-211">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="73dec-212">`[SkuTier <String>]`: określa warstwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-212">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="73dec-213">Dopuszczalne wartości to</span><span class="sxs-lookup"><span data-stu-id="73dec-213">Possible Values are</span></span> <br /><br /> <span data-ttu-id="73dec-214">**Standardowe**</span><span class="sxs-lookup"><span data-stu-id="73dec-214">**Standard**</span></span> <br /><br /> <span data-ttu-id="73dec-215">**Podstawowe**</span><span class="sxs-lookup"><span data-stu-id="73dec-215">**Basic**</span></span>
  - <span data-ttu-id="73dec-216">`[StartCloudService <Boolean?>]`: (Opcjonalnie) Wskazuje, czy usługa w chmurze ma być uruchamiana natychmiast po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="73dec-216">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="73dec-217">Wartość domyślna `true` to.</span><span class="sxs-lookup"><span data-stu-id="73dec-217">The default value is `true`.</span></span>         <span data-ttu-id="73dec-218">Jeśli wartość jest fałszywa, model usługi jest nadal wdrażany, ale kod nie jest uruchamiany natychmiast.</span><span class="sxs-lookup"><span data-stu-id="73dec-218">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="73dec-219">Zamiast tego usługa będzie się uruchamiać do momentu wywołania startowego, o której usługa zostanie uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="73dec-219">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="73dec-220">Wdrożona usługa nadal wiąże się z opłatami, nawet jeśli zostanie wyłączony.</span><span class="sxs-lookup"><span data-stu-id="73dec-220">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="73dec-221">`[Tag <ICloudServiceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="73dec-221">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="73dec-222">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="73dec-222">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="73dec-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: tryb aktualizacji dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="73dec-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="73dec-224">Wystąpienia ról są przydzielane do aktualizowania domen podczas wdrażania usługi.</span><span class="sxs-lookup"><span data-stu-id="73dec-224">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="73dec-225">Aktualizacje mogą być inicjowane ręcznie w każdej domenie aktualizacji lub inicjowane automatycznie we wszystkich domenach aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="73dec-225">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="73dec-226">Dopuszczalne wartości to</span><span class="sxs-lookup"><span data-stu-id="73dec-226">Possible Values are</span></span> <br /><br /><span data-ttu-id="73dec-227">**Automatycznie**</span><span class="sxs-lookup"><span data-stu-id="73dec-227">**Auto**</span></span><br /><br /><span data-ttu-id="73dec-228">**Ręcznie**</span><span class="sxs-lookup"><span data-stu-id="73dec-228">**Manual**</span></span> <br /><br /><span data-ttu-id="73dec-229">**Jednoczesne**</span><span class="sxs-lookup"><span data-stu-id="73dec-229">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="73dec-230">Jeśli nie zostanie określona, wartością domyślną jest Auto. Jeśli ta wartość jest ustawiona na Ręcznie, aby zastosować aktualizację, musi zostać wywołana nazwa PUT UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="73dec-230">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="73dec-231">Jeśli ta opcja jest ustawiona na Automatyczne, aktualizacja jest automatycznie stosowana do każdej domeny aktualizacji w sekwencji.</span><span class="sxs-lookup"><span data-stu-id="73dec-231">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="73dec-232">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73dec-232">RELATED LINKS</span></span>

