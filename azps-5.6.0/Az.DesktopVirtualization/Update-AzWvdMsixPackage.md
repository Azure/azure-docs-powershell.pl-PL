---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: f552c8e21703d64efa2ac65f47461daa963fc1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983578"
---
# <span data-ttu-id="f071a-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="f071a-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="f071a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f071a-102">SYNOPSIS</span></span>
<span data-ttu-id="f071a-103">Zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="f071a-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="f071a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f071a-104">SYNTAX</span></span>

### <span data-ttu-id="f071a-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="f071a-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f071a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f071a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f071a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f071a-107">DESCRIPTION</span></span>
<span data-ttu-id="f071a-108">Zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="f071a-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="f071a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f071a-109">EXAMPLES</span></span>

### <span data-ttu-id="f071a-110">Przykład 1. Aktualizowanie pakietu MSIX</span><span class="sxs-lookup"><span data-stu-id="f071a-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="f071a-111">To polecenie aktualizuje pakiet MSIX w buforze hosta.</span><span class="sxs-lookup"><span data-stu-id="f071a-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="f071a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f071a-112">PARAMETERS</span></span>

### <span data-ttu-id="f071a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f071a-113">-DefaultProfile</span></span>
<span data-ttu-id="f071a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f071a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f071a-115">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="f071a-115">-DisplayName</span></span>
<span data-ttu-id="f071a-116">Nazwa wyświetlana pakietu MSIX.</span><span class="sxs-lookup"><span data-stu-id="f071a-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="f071a-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="f071a-117">-FullName</span></span>
<span data-ttu-id="f071a-118">Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="f071a-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f071a-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f071a-119">-HostPoolName</span></span>
<span data-ttu-id="f071a-120">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="f071a-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="f071a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f071a-121">-InputObject</span></span>
<span data-ttu-id="f071a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f071a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f071a-123">—IsActive</span><span class="sxs-lookup"><span data-stu-id="f071a-123">-IsActive</span></span>
<span data-ttu-id="f071a-124">Ustaw wersję pakietu, aby pakiet był aktywny w całej buforze hosta.</span><span class="sxs-lookup"><span data-stu-id="f071a-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="f071a-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="f071a-125">-IsRegularRegistration</span></span>
<span data-ttu-id="f071a-126">Ustaw tryb rejestracji.</span><span class="sxs-lookup"><span data-stu-id="f071a-126">Set Registration mode.</span></span>
<span data-ttu-id="f071a-127">Zwykły lub Opóźniony.</span><span class="sxs-lookup"><span data-stu-id="f071a-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="f071a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f071a-128">-ResourceGroupName</span></span>
<span data-ttu-id="f071a-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f071a-129">The name of the resource group.</span></span>
<span data-ttu-id="f071a-130">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f071a-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f071a-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f071a-131">-SubscriptionId</span></span>
<span data-ttu-id="f071a-132">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f071a-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f071a-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f071a-133">-Confirm</span></span>
<span data-ttu-id="f071a-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f071a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f071a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f071a-135">-WhatIf</span></span>
<span data-ttu-id="f071a-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f071a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f071a-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f071a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f071a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f071a-138">CommonParameters</span></span>
<span data-ttu-id="f071a-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f071a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f071a-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f071a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f071a-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f071a-141">INPUTS</span></span>

### <span data-ttu-id="f071a-142">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f071a-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f071a-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f071a-143">OUTPUTS</span></span>

### <span data-ttu-id="f071a-144">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="f071a-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="f071a-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f071a-145">NOTES</span></span>

<span data-ttu-id="f071a-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f071a-146">ALIASES</span></span>

<span data-ttu-id="f071a-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f071a-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f071a-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f071a-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f071a-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f071a-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f071a-150">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f071a-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f071a-151">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="f071a-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f071a-152">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f071a-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f071a-153">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="f071a-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f071a-154">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f071a-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f071a-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f071a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f071a-156">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="f071a-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f071a-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f071a-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f071a-158">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f071a-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="f071a-159">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="f071a-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f071a-160">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f071a-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f071a-161">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="f071a-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f071a-162">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="f071a-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f071a-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f071a-163">RELATED LINKS</span></span>

