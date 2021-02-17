---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: b03fe0c62a446c9ed54c9330708f29737e18bd59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188547"
---
# <span data-ttu-id="c6338-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c6338-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c6338-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6338-102">SYNOPSIS</span></span>
<span data-ttu-id="c6338-103">Aktualizowanie grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c6338-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="c6338-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6338-104">SYNTAX</span></span>

### <span data-ttu-id="c6338-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="c6338-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c6338-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c6338-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c6338-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6338-107">DESCRIPTION</span></span>
<span data-ttu-id="c6338-108">Aktualizowanie grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c6338-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="c6338-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6338-109">EXAMPLES</span></span>

### <span data-ttu-id="c6338-110">Przykład 1. Tworzenie grupy aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="c6338-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="c6338-111">To polecenie tworzy grupę aplikacji pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6338-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="c6338-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6338-112">PARAMETERS</span></span>

### <span data-ttu-id="c6338-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6338-113">-DefaultProfile</span></span>
<span data-ttu-id="c6338-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6338-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6338-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="c6338-115">-Description</span></span>
<span data-ttu-id="c6338-116">Opis grupy ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="c6338-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="c6338-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c6338-117">-FriendlyName</span></span>
<span data-ttu-id="c6338-118">Przyjazna nazwa grupy ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="c6338-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="c6338-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6338-119">-InputObject</span></span>
<span data-ttu-id="c6338-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c6338-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6338-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c6338-121">-Name</span></span>
<span data-ttu-id="c6338-122">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c6338-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6338-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6338-123">-ResourceGroupName</span></span>
<span data-ttu-id="c6338-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6338-124">The name of the resource group.</span></span>
<span data-ttu-id="c6338-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="c6338-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c6338-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6338-126">-SubscriptionId</span></span>
<span data-ttu-id="c6338-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c6338-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c6338-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="c6338-128">-Tag</span></span>
<span data-ttu-id="c6338-129">tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="c6338-129">tags to be updated</span></span>

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

### <span data-ttu-id="c6338-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6338-130">-Confirm</span></span>
<span data-ttu-id="c6338-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c6338-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6338-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6338-132">-WhatIf</span></span>
<span data-ttu-id="c6338-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6338-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6338-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c6338-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6338-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6338-135">CommonParameters</span></span>
<span data-ttu-id="c6338-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6338-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6338-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6338-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6338-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6338-138">INPUTS</span></span>

### <span data-ttu-id="c6338-139">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c6338-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c6338-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6338-140">OUTPUTS</span></span>

### <span data-ttu-id="c6338-141">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c6338-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="c6338-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6338-142">NOTES</span></span>

<span data-ttu-id="c6338-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c6338-143">ALIASES</span></span>

<span data-ttu-id="c6338-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6338-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c6338-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c6338-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6338-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c6338-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c6338-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="c6338-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6338-148">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c6338-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c6338-149">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c6338-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c6338-150">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="c6338-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c6338-151">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6338-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c6338-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c6338-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6338-153">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="c6338-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c6338-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6338-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c6338-155">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="c6338-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="c6338-156">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="c6338-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c6338-157">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c6338-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c6338-158">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="c6338-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c6338-159">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="c6338-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c6338-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6338-160">RELATED LINKS</span></span>

