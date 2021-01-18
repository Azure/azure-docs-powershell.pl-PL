---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498129"
---
# <span data-ttu-id="aae61-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="aae61-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="aae61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aae61-102">SYNOPSIS</span></span>
<span data-ttu-id="aae61-103">Aktualizowanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="aae61-103">Update a private cloud</span></span>

## <span data-ttu-id="aae61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aae61-104">SYNTAX</span></span>

### <span data-ttu-id="aae61-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aae61-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aae61-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aae61-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aae61-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aae61-107">DESCRIPTION</span></span>
<span data-ttu-id="aae61-108">Aktualizowanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="aae61-108">Update a private cloud</span></span>

## <span data-ttu-id="aae61-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aae61-109">EXAMPLES</span></span>

### <span data-ttu-id="aae61-110">Przykład 1: aktualizowanie rozmiaru chmury prywatnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="aae61-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="aae61-111">Aktualizowanie rozmiaru chmury prywatnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="aae61-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="aae61-112">Przykład 2: aktualizowanie rozmiaru chmury prywatnej przez obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="aae61-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="aae61-113">Aktualizowanie rozmiaru chmury prywatnej według obiektu wejścia</span><span class="sxs-lookup"><span data-stu-id="aae61-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="aae61-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aae61-114">PARAMETERS</span></span>

### <span data-ttu-id="aae61-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aae61-115">-AsJob</span></span>
<span data-ttu-id="aae61-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="aae61-116">Run the command as a job</span></span>

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

### <span data-ttu-id="aae61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae61-117">-DefaultProfile</span></span>
<span data-ttu-id="aae61-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aae61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aae61-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="aae61-119">-IdentitySource</span></span>
<span data-ttu-id="aae61-120">Aby utworzyć źródło tożsamości pojedynczego podpisu vCenter, zobacz sekcję notatki dla właściwości IDENTITYSOURCE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="aae61-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae61-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aae61-121">-InputObject</span></span>
<span data-ttu-id="aae61-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="aae61-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aae61-123">— Internet</span><span class="sxs-lookup"><span data-stu-id="aae61-123">-Internet</span></span>
<span data-ttu-id="aae61-124">Łączność z Internetem jest włączona lub wyłączona</span><span class="sxs-lookup"><span data-stu-id="aae61-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae61-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="aae61-125">-ManagementClusterSize</span></span>
<span data-ttu-id="aae61-126">Rozmiar klastra</span><span class="sxs-lookup"><span data-stu-id="aae61-126">The cluster size</span></span>

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

### <span data-ttu-id="aae61-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aae61-127">-Name</span></span>
<span data-ttu-id="aae61-128">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="aae61-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="aae61-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="aae61-129">-NoWait</span></span>
<span data-ttu-id="aae61-130">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="aae61-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aae61-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae61-131">-ResourceGroupName</span></span>
<span data-ttu-id="aae61-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aae61-132">The name of the resource group.</span></span>
<span data-ttu-id="aae61-133">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="aae61-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="aae61-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="aae61-134">-SubscriptionId</span></span>
<span data-ttu-id="aae61-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="aae61-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="aae61-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="aae61-136">-Tag</span></span>
<span data-ttu-id="aae61-137">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="aae61-137">Resource tags.</span></span>

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

### <span data-ttu-id="aae61-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aae61-138">-Confirm</span></span>
<span data-ttu-id="aae61-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aae61-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aae61-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aae61-140">-WhatIf</span></span>
<span data-ttu-id="aae61-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aae61-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aae61-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aae61-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aae61-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae61-143">CommonParameters</span></span>
<span data-ttu-id="aae61-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae61-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae61-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aae61-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae61-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aae61-146">INPUTS</span></span>

### <span data-ttu-id="aae61-147">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="aae61-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="aae61-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aae61-148">OUTPUTS</span></span>

### <span data-ttu-id="aae61-149">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="aae61-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="aae61-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aae61-150">NOTES</span></span>

<span data-ttu-id="aae61-151">PISUJE</span><span class="sxs-lookup"><span data-stu-id="aae61-151">ALIASES</span></span>

<span data-ttu-id="aae61-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aae61-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aae61-153">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="aae61-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aae61-154">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aae61-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aae61-155">IDENTITYSOURCE <IIdentitySource [] >: Logowanie jednokrotne w usłudze vCenter dla źródeł tożsamości</span><span class="sxs-lookup"><span data-stu-id="aae61-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="aae61-156">`[Alias <String>]`: Nazwa NetBIOS domeny</span><span class="sxs-lookup"><span data-stu-id="aae61-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="aae61-157">`[BaseGroupDn <String>]`: Podstawowa nazwa wyróżniająca dla grup</span><span class="sxs-lookup"><span data-stu-id="aae61-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="aae61-158">`[BaseUserDn <String>]`: Podstawowa nazwa wyróżniająca dla użytkowników</span><span class="sxs-lookup"><span data-stu-id="aae61-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="aae61-159">`[Domain <String>]`: Nazwa DNS domeny</span><span class="sxs-lookup"><span data-stu-id="aae61-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="aae61-160">`[Name <String>]`: Nazwa źródła tożsamości</span><span class="sxs-lookup"><span data-stu-id="aae61-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="aae61-161">`[Password <String>]`: Hasło użytkownika usługi Active Directory z minimalną opcją dostęp tylko do odczytu do podstawowej domeny DN dla użytkowników i grup.</span><span class="sxs-lookup"><span data-stu-id="aae61-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="aae61-162">`[PrimaryServer <String>]`: Podstawowy adres URL serwera</span><span class="sxs-lookup"><span data-stu-id="aae61-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="aae61-163">`[SecondaryServer <String>]`: Adres URL serwera pomocniczego</span><span class="sxs-lookup"><span data-stu-id="aae61-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="aae61-164">`[Ssl <SslEnum?>]`: Ochrona komunikacji przy użyciu protokołu LDAP za pomocą certyfikatu SSL (LDAPs)</span><span class="sxs-lookup"><span data-stu-id="aae61-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="aae61-165">`[Username <String>]`: Identyfikator użytkownika usługi Active Directory z co najmniej dostępem tylko do odczytu do podstawowej domeny DN dla użytkowników i grup</span><span class="sxs-lookup"><span data-stu-id="aae61-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="aae61-166">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="aae61-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aae61-167">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="aae61-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="aae61-168">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="aae61-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="aae61-169">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="aae61-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="aae61-170">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="aae61-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aae61-171">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="aae61-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="aae61-172">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="aae61-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="aae61-173">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aae61-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aae61-174">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="aae61-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="aae61-175">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="aae61-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="aae61-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aae61-176">RELATED LINKS</span></span>

