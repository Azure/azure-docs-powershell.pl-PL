---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: fbc61ec485be94eacb0267a9698a861f962c61a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001594"
---
# <span data-ttu-id="cd7de-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="cd7de-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="cd7de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7de-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7de-103">Aktualizowanie pulpitu.</span><span class="sxs-lookup"><span data-stu-id="cd7de-103">Update a desktop.</span></span>

## <span data-ttu-id="cd7de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd7de-104">SYNTAX</span></span>

### <span data-ttu-id="cd7de-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="cd7de-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd7de-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cd7de-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cd7de-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd7de-107">DESCRIPTION</span></span>
<span data-ttu-id="cd7de-108">Aktualizowanie pulpitu.</span><span class="sxs-lookup"><span data-stu-id="cd7de-108">Update a desktop.</span></span>

## <span data-ttu-id="cd7de-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd7de-109">EXAMPLES</span></span>

### <span data-ttu-id="cd7de-110">Przykład 1. Aktualizowanie pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="cd7de-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="cd7de-111">To polecenie aktualizuje pulpit wirtualny systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd7de-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="cd7de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd7de-112">PARAMETERS</span></span>

### <span data-ttu-id="cd7de-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7de-113">-ApplicationGroupName</span></span>
<span data-ttu-id="cd7de-114">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="cd7de-114">The name of the application group</span></span>

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

### <span data-ttu-id="cd7de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7de-115">-DefaultProfile</span></span>
<span data-ttu-id="cd7de-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd7de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd7de-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="cd7de-117">-Description</span></span>
<span data-ttu-id="cd7de-118">Opis pulpitu.</span><span class="sxs-lookup"><span data-stu-id="cd7de-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="cd7de-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cd7de-119">-FriendlyName</span></span>
<span data-ttu-id="cd7de-120">Przyjazna nazwa pulpitu.</span><span class="sxs-lookup"><span data-stu-id="cd7de-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="cd7de-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd7de-121">-InputObject</span></span>
<span data-ttu-id="cd7de-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cd7de-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd7de-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cd7de-123">-Name</span></span>
<span data-ttu-id="cd7de-124">Nazwa pulpitu w określonej grupie pulpitu</span><span class="sxs-lookup"><span data-stu-id="cd7de-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7de-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd7de-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd7de-126">The name of the resource group.</span></span>
<span data-ttu-id="cd7de-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="cd7de-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cd7de-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd7de-128">-SubscriptionId</span></span>
<span data-ttu-id="cd7de-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="cd7de-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cd7de-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="cd7de-130">-Tag</span></span>
<span data-ttu-id="cd7de-131">tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="cd7de-131">tags to be updated</span></span>

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

### <span data-ttu-id="cd7de-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd7de-132">-Confirm</span></span>
<span data-ttu-id="cd7de-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd7de-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd7de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd7de-134">-WhatIf</span></span>
<span data-ttu-id="cd7de-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd7de-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd7de-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd7de-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd7de-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7de-137">CommonParameters</span></span>
<span data-ttu-id="cd7de-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd7de-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7de-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd7de-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7de-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd7de-140">INPUTS</span></span>

### <span data-ttu-id="cd7de-141">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cd7de-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cd7de-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd7de-142">OUTPUTS</span></span>

### <span data-ttu-id="cd7de-143">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="cd7de-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

## <span data-ttu-id="cd7de-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd7de-144">NOTES</span></span>

<span data-ttu-id="cd7de-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cd7de-145">ALIASES</span></span>

<span data-ttu-id="cd7de-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd7de-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd7de-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cd7de-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd7de-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd7de-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd7de-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="cd7de-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd7de-150">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="cd7de-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cd7de-151">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd7de-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cd7de-152">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="cd7de-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cd7de-153">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd7de-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cd7de-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cd7de-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd7de-155">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="cd7de-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="cd7de-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd7de-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cd7de-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="cd7de-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="cd7de-158">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="cd7de-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cd7de-159">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="cd7de-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cd7de-160">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="cd7de-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cd7de-161">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="cd7de-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cd7de-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd7de-162">RELATED LINKS</span></span>

