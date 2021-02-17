---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186026"
---
# <span data-ttu-id="b6bbf-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="b6bbf-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="b6bbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bbf-103">Zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="b6bbf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6bbf-104">SYNTAX</span></span>

### <span data-ttu-id="b6bbf-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="b6bbf-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6bbf-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b6bbf-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6bbf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6bbf-107">DESCRIPTION</span></span>
<span data-ttu-id="b6bbf-108">Zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="b6bbf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6bbf-109">EXAMPLES</span></span>

### <span data-ttu-id="b6bbf-110">Przykład 1. Aktualizowanie pakietu MSIX</span><span class="sxs-lookup"><span data-stu-id="b6bbf-110">Example 1: Update a MSIX Package</span></span> 
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

<span data-ttu-id="b6bbf-111">To polecenie aktualizuje pakiet MSIX w buforze hosta.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="b6bbf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6bbf-112">PARAMETERS</span></span>

### <span data-ttu-id="b6bbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bbf-113">-DefaultProfile</span></span>
<span data-ttu-id="b6bbf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6bbf-115">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="b6bbf-115">-DisplayName</span></span>
<span data-ttu-id="b6bbf-116">Nazwa wyświetlana pakietu MSIX.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="b6bbf-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="b6bbf-117">-FullName</span></span>
<span data-ttu-id="b6bbf-118">Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="b6bbf-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="b6bbf-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b6bbf-119">-HostPoolName</span></span>
<span data-ttu-id="b6bbf-120">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b6bbf-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="b6bbf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6bbf-121">-InputObject</span></span>
<span data-ttu-id="b6bbf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6bbf-123">—IsActive</span><span class="sxs-lookup"><span data-stu-id="b6bbf-123">-IsActive</span></span>
<span data-ttu-id="b6bbf-124">Ustaw wersję pakietu, aby pakiet był aktywny w całej buforze hosta.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="b6bbf-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="b6bbf-125">-IsRegularRegistration</span></span>
<span data-ttu-id="b6bbf-126">Ustaw tryb rejestracji.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-126">Set Registration mode.</span></span>
<span data-ttu-id="b6bbf-127">Zwykły lub Opóźniony.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="b6bbf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6bbf-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6bbf-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-129">The name of the resource group.</span></span>
<span data-ttu-id="b6bbf-130">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b6bbf-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6bbf-131">-SubscriptionId</span></span>
<span data-ttu-id="b6bbf-132">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b6bbf-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6bbf-133">-Confirm</span></span>
<span data-ttu-id="b6bbf-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6bbf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6bbf-135">-WhatIf</span></span>
<span data-ttu-id="b6bbf-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6bbf-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6bbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bbf-138">CommonParameters</span></span>
<span data-ttu-id="b6bbf-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bbf-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6bbf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bbf-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6bbf-141">INPUTS</span></span>

### <span data-ttu-id="b6bbf-142">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b6bbf-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b6bbf-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6bbf-143">OUTPUTS</span></span>

### <span data-ttu-id="b6bbf-144">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="b6bbf-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="b6bbf-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6bbf-145">NOTES</span></span>

<span data-ttu-id="b6bbf-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b6bbf-146">ALIASES</span></span>

<span data-ttu-id="b6bbf-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6bbf-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6bbf-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6bbf-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6bbf-150">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b6bbf-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6bbf-151">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b6bbf-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b6bbf-152">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b6bbf-153">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="b6bbf-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b6bbf-154">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b6bbf-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b6bbf-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6bbf-156">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="b6bbf-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b6bbf-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b6bbf-158">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="b6bbf-159">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="b6bbf-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b6bbf-160">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b6bbf-161">`[UserSessionId <String>]`: nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="b6bbf-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b6bbf-162">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="b6bbf-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b6bbf-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6bbf-163">RELATED LINKS</span></span>

