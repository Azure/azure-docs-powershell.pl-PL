---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 31a9ecc324938ae3518887d58ac2a762b374328c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243795"
---
# <span data-ttu-id="3931f-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="3931f-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="3931f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3931f-102">SYNOPSIS</span></span>
<span data-ttu-id="3931f-103">Aktualizowanie pulpitu.</span><span class="sxs-lookup"><span data-stu-id="3931f-103">Update a desktop.</span></span>

## <span data-ttu-id="3931f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3931f-104">SYNTAX</span></span>

### <span data-ttu-id="3931f-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3931f-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3931f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3931f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3931f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3931f-107">DESCRIPTION</span></span>
<span data-ttu-id="3931f-108">Aktualizowanie pulpitu.</span><span class="sxs-lookup"><span data-stu-id="3931f-108">Update a desktop.</span></span>

## <span data-ttu-id="3931f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3931f-109">EXAMPLES</span></span>

### <span data-ttu-id="3931f-110">Przykład 1. Aktualizowanie pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="3931f-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
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

<span data-ttu-id="3931f-111">To polecenie aktualizuje pulpit wirtualny systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3931f-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="3931f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3931f-112">PARAMETERS</span></span>

### <span data-ttu-id="3931f-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="3931f-113">-ApplicationGroupName</span></span>
<span data-ttu-id="3931f-114">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3931f-114">The name of the application group</span></span>

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

### <span data-ttu-id="3931f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3931f-115">-DefaultProfile</span></span>
<span data-ttu-id="3931f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3931f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3931f-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="3931f-117">-Description</span></span>
<span data-ttu-id="3931f-118">Opis pulpitu.</span><span class="sxs-lookup"><span data-stu-id="3931f-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="3931f-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3931f-119">-FriendlyName</span></span>
<span data-ttu-id="3931f-120">Przyjazna nazwa pulpitu.</span><span class="sxs-lookup"><span data-stu-id="3931f-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="3931f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3931f-121">-InputObject</span></span>
<span data-ttu-id="3931f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3931f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3931f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3931f-123">-Name</span></span>
<span data-ttu-id="3931f-124">Nazwa pulpitu w określonej grupie pulpitu</span><span class="sxs-lookup"><span data-stu-id="3931f-124">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="3931f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3931f-125">-ResourceGroupName</span></span>
<span data-ttu-id="3931f-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3931f-126">The name of the resource group.</span></span>
<span data-ttu-id="3931f-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3931f-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3931f-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3931f-128">-SubscriptionId</span></span>
<span data-ttu-id="3931f-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3931f-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3931f-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="3931f-130">-Tag</span></span>
<span data-ttu-id="3931f-131">tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="3931f-131">tags to be updated</span></span>

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

### <span data-ttu-id="3931f-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3931f-132">-Confirm</span></span>
<span data-ttu-id="3931f-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3931f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3931f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3931f-134">-WhatIf</span></span>
<span data-ttu-id="3931f-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3931f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3931f-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3931f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3931f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3931f-137">CommonParameters</span></span>
<span data-ttu-id="3931f-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3931f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3931f-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3931f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3931f-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3931f-140">INPUTS</span></span>

### <span data-ttu-id="3931f-141">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3931f-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3931f-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3931f-142">OUTPUTS</span></span>

### <span data-ttu-id="3931f-143">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="3931f-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

## <span data-ttu-id="3931f-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3931f-144">NOTES</span></span>

<span data-ttu-id="3931f-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3931f-145">ALIASES</span></span>

<span data-ttu-id="3931f-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3931f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3931f-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3931f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3931f-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3931f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3931f-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3931f-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3931f-150">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3931f-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3931f-151">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3931f-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3931f-152">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="3931f-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3931f-153">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3931f-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3931f-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3931f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3931f-155">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="3931f-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3931f-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3931f-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3931f-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3931f-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="3931f-158">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="3931f-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3931f-159">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3931f-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3931f-160">`[UserSessionId <String>]`: nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="3931f-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3931f-161">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="3931f-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3931f-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3931f-162">RELATED LINKS</span></span>

