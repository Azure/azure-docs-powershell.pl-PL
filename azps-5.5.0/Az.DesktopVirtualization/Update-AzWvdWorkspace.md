---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 8a20777cfd6e28c3edc127117687b7aef801d94e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243778"
---
# <span data-ttu-id="d52bf-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="d52bf-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="d52bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d52bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d52bf-103">Aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d52bf-103">Update a workspace.</span></span>

## <span data-ttu-id="d52bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d52bf-104">SYNTAX</span></span>

### <span data-ttu-id="d52bf-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d52bf-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d52bf-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d52bf-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d52bf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d52bf-107">DESCRIPTION</span></span>
<span data-ttu-id="d52bf-108">Aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d52bf-108">Update a workspace.</span></span>

## <span data-ttu-id="d52bf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d52bf-109">EXAMPLES</span></span>

### <span data-ttu-id="d52bf-110">Przykład 1. Aktualizowanie obszaru roboczego pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="d52bf-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="d52bf-111">To polecenie aktualizuje obszar roboczy pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d52bf-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="d52bf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d52bf-112">PARAMETERS</span></span>

### <span data-ttu-id="d52bf-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="d52bf-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="d52bf-114">Lista linków applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="d52bf-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d52bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d52bf-115">-DefaultProfile</span></span>
<span data-ttu-id="d52bf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d52bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d52bf-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="d52bf-117">-Description</span></span>
<span data-ttu-id="d52bf-118">Opis obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d52bf-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="d52bf-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d52bf-119">-FriendlyName</span></span>
<span data-ttu-id="d52bf-120">Przyjazna nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d52bf-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="d52bf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d52bf-121">-InputObject</span></span>
<span data-ttu-id="d52bf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d52bf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d52bf-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d52bf-123">-Name</span></span>
<span data-ttu-id="d52bf-124">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="d52bf-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d52bf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d52bf-125">-ResourceGroupName</span></span>
<span data-ttu-id="d52bf-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d52bf-126">The name of the resource group.</span></span>
<span data-ttu-id="d52bf-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="d52bf-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d52bf-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d52bf-128">-SubscriptionId</span></span>
<span data-ttu-id="d52bf-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d52bf-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d52bf-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="d52bf-130">-Tag</span></span>
<span data-ttu-id="d52bf-131">tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="d52bf-131">tags to be updated</span></span>

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

### <span data-ttu-id="d52bf-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d52bf-132">-Confirm</span></span>
<span data-ttu-id="d52bf-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d52bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d52bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d52bf-134">-WhatIf</span></span>
<span data-ttu-id="d52bf-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d52bf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d52bf-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d52bf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d52bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d52bf-137">CommonParameters</span></span>
<span data-ttu-id="d52bf-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d52bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d52bf-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d52bf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d52bf-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d52bf-140">INPUTS</span></span>

### <span data-ttu-id="d52bf-141">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d52bf-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d52bf-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d52bf-142">OUTPUTS</span></span>

### <span data-ttu-id="d52bf-143">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="d52bf-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="d52bf-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d52bf-144">NOTES</span></span>

<span data-ttu-id="d52bf-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d52bf-145">ALIASES</span></span>

<span data-ttu-id="d52bf-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d52bf-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d52bf-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d52bf-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d52bf-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d52bf-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d52bf-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d52bf-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d52bf-150">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d52bf-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d52bf-151">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d52bf-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d52bf-152">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="d52bf-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d52bf-153">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d52bf-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d52bf-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d52bf-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d52bf-155">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="d52bf-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d52bf-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d52bf-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d52bf-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="d52bf-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="d52bf-158">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="d52bf-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d52bf-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d52bf-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d52bf-160">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="d52bf-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d52bf-161">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="d52bf-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d52bf-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d52bf-162">RELATED LINKS</span></span>

