---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: dbea608c24d8da8fa292316653b3e16953aed8b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242962"
---
# <span data-ttu-id="87e16-101">Update-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="87e16-101">Update-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="87e16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87e16-102">SYNOPSIS</span></span>
<span data-ttu-id="87e16-103">Aktualizowanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="87e16-103">Update a private cloud</span></span>

## <span data-ttu-id="87e16-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87e16-104">SYNTAX</span></span>

### <span data-ttu-id="87e16-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="87e16-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="87e16-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="87e16-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87e16-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="87e16-107">DESCRIPTION</span></span>
<span data-ttu-id="87e16-108">Aktualizowanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="87e16-108">Update a private cloud</span></span>

## <span data-ttu-id="87e16-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87e16-109">EXAMPLES</span></span>

### <span data-ttu-id="87e16-110">Przykład 1. Aktualizowanie rozmiaru chmury prywatnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="87e16-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="87e16-111">Aktualizowanie rozmiaru chmury prywatnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="87e16-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="87e16-112">Przykład 2. Aktualizowanie rozmiaru chmury prywatnej według obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="87e16-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMwarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="87e16-113">Aktualizowanie rozmiaru chmury prywatnej według obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="87e16-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="87e16-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87e16-114">PARAMETERS</span></span>

### <span data-ttu-id="87e16-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="87e16-115">-AsJob</span></span>
<span data-ttu-id="87e16-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="87e16-116">Run the command as a job</span></span>

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

### <span data-ttu-id="87e16-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e16-117">-DefaultProfile</span></span>
<span data-ttu-id="87e16-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="87e16-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e16-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="87e16-119">-IdentitySource</span></span>
<span data-ttu-id="87e16-120">VCenter Single Sign on Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="87e16-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e16-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87e16-121">-InputObject</span></span>
<span data-ttu-id="87e16-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="87e16-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87e16-123">— Internet</span><span class="sxs-lookup"><span data-stu-id="87e16-123">-Internet</span></span>
<span data-ttu-id="87e16-124">Łączność z Internetem jest włączona lub wyłączona</span><span class="sxs-lookup"><span data-stu-id="87e16-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e16-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="87e16-125">-ManagementClusterSize</span></span>
<span data-ttu-id="87e16-126">Rozmiar klastrów</span><span class="sxs-lookup"><span data-stu-id="87e16-126">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e16-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="87e16-127">-Name</span></span>
<span data-ttu-id="87e16-128">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="87e16-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e16-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="87e16-129">-NoWait</span></span>
<span data-ttu-id="87e16-130">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="87e16-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="87e16-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e16-131">-ResourceGroupName</span></span>
<span data-ttu-id="87e16-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87e16-132">The name of the resource group.</span></span>
<span data-ttu-id="87e16-133">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="87e16-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e16-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87e16-134">-SubscriptionId</span></span>
<span data-ttu-id="87e16-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="87e16-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e16-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="87e16-136">-Tag</span></span>
<span data-ttu-id="87e16-137">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="87e16-137">Resource tags.</span></span>

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

### <span data-ttu-id="87e16-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87e16-138">-Confirm</span></span>
<span data-ttu-id="87e16-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="87e16-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87e16-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87e16-140">-WhatIf</span></span>
<span data-ttu-id="87e16-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87e16-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87e16-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="87e16-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87e16-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e16-143">CommonParameters</span></span>
<span data-ttu-id="87e16-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e16-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e16-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87e16-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e16-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87e16-146">INPUTS</span></span>

### <span data-ttu-id="87e16-147">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.IVDentIdentity</span><span class="sxs-lookup"><span data-stu-id="87e16-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="87e16-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87e16-148">OUTPUTS</span></span>

### <span data-ttu-id="87e16-149">Microsoft.Azure.PowerShell.cmdlet.v Jak.model.api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="87e16-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="87e16-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87e16-150">NOTES</span></span>

<span data-ttu-id="87e16-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="87e16-151">ALIASES</span></span>

<span data-ttu-id="87e16-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="87e16-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87e16-153">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="87e16-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87e16-154">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87e16-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87e16-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span><span class="sxs-lookup"><span data-stu-id="87e16-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="87e16-156">`[Alias <String>]`: nazwa domeny NetBIOS</span><span class="sxs-lookup"><span data-stu-id="87e16-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="87e16-157">`[BaseGroupDn <String>]`: podstawowa nazwa wyróżniająa grup</span><span class="sxs-lookup"><span data-stu-id="87e16-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="87e16-158">`[BaseUserDn <String>]`: podstawowa nazwa wyróżniająa użytkowników</span><span class="sxs-lookup"><span data-stu-id="87e16-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="87e16-159">`[Domain <String>]`: nazwa DNS domeny</span><span class="sxs-lookup"><span data-stu-id="87e16-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="87e16-160">`[Name <String>]`: nazwa źródła tożsamości</span><span class="sxs-lookup"><span data-stu-id="87e16-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="87e16-161">`[Password <String>]`: hasło użytkownika usługi Active Directory z minimalnym dostępem tylko do odczytu do podstawowej nazwy dn dla użytkowników i grup.</span><span class="sxs-lookup"><span data-stu-id="87e16-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="87e16-162">`[PrimaryServer <String>]`: adres URL serwera podstawowego</span><span class="sxs-lookup"><span data-stu-id="87e16-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="87e16-163">`[SecondaryServer <String>]`: adres URL serwera pomocniczego</span><span class="sxs-lookup"><span data-stu-id="87e16-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="87e16-164">`[Ssl <SslEnum?>]`: ochrona komunikacji LDAP przy użyciu certyfikatu SSL (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="87e16-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="87e16-165">`[Username <String>]`: Identyfikator użytkownika usługi Active Directory z minimalnym dostępem tylko do odczytu do podstawowej nazwy dn dla użytkowników i grup</span><span class="sxs-lookup"><span data-stu-id="87e16-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="87e16-166">INPUTOBJECT: <IVMwareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="87e16-166">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87e16-167">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="87e16-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="87e16-168">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="87e16-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="87e16-169">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="87e16-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="87e16-170">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="87e16-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87e16-171">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="87e16-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="87e16-172">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="87e16-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="87e16-173">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87e16-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="87e16-174">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="87e16-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="87e16-175">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="87e16-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="87e16-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87e16-176">RELATED LINKS</span></span>

