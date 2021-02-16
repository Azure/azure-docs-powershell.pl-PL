---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 59ff3c3bd973e3b2189e7f06cd067eaca42870f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238039"
---
# <span data-ttu-id="206a0-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="206a0-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="206a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="206a0-102">SYNOPSIS</span></span>
<span data-ttu-id="206a0-103">Usuwanie grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="206a0-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="206a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="206a0-104">SYNTAX</span></span>

### <span data-ttu-id="206a0-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="206a0-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="206a0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="206a0-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="206a0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="206a0-107">DESCRIPTION</span></span>
<span data-ttu-id="206a0-108">Usuwanie grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="206a0-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="206a0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="206a0-109">EXAMPLES</span></span>

### <span data-ttu-id="206a0-110">Przykład 1. Usuwanie grupy aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="206a0-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="206a0-111">To polecenie usuwa grupę aplikacji pulpitu wirtualnego systemu Windows z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="206a0-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="206a0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="206a0-112">PARAMETERS</span></span>

### <span data-ttu-id="206a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="206a0-113">-DefaultProfile</span></span>
<span data-ttu-id="206a0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="206a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="206a0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="206a0-115">-InputObject</span></span>
<span data-ttu-id="206a0-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="206a0-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="206a0-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="206a0-117">-Name</span></span>
<span data-ttu-id="206a0-118">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="206a0-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206a0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="206a0-119">-PassThru</span></span>
<span data-ttu-id="206a0-120">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="206a0-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="206a0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="206a0-121">-ResourceGroupName</span></span>
<span data-ttu-id="206a0-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="206a0-122">The name of the resource group.</span></span>
<span data-ttu-id="206a0-123">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="206a0-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206a0-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="206a0-124">-SubscriptionId</span></span>
<span data-ttu-id="206a0-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="206a0-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206a0-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="206a0-126">-Confirm</span></span>
<span data-ttu-id="206a0-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="206a0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="206a0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="206a0-128">-WhatIf</span></span>
<span data-ttu-id="206a0-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="206a0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="206a0-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="206a0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="206a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206a0-131">CommonParameters</span></span>
<span data-ttu-id="206a0-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="206a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="206a0-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="206a0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206a0-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="206a0-134">INPUTS</span></span>

### <span data-ttu-id="206a0-135">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="206a0-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="206a0-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="206a0-136">OUTPUTS</span></span>

### <span data-ttu-id="206a0-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="206a0-137">System.Boolean</span></span>

## <span data-ttu-id="206a0-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="206a0-138">NOTES</span></span>

<span data-ttu-id="206a0-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="206a0-139">ALIASES</span></span>

<span data-ttu-id="206a0-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="206a0-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="206a0-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="206a0-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="206a0-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="206a0-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="206a0-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="206a0-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="206a0-144">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="206a0-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="206a0-145">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="206a0-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="206a0-146">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="206a0-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="206a0-147">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="206a0-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="206a0-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="206a0-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="206a0-149">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="206a0-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="206a0-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="206a0-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="206a0-151">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="206a0-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="206a0-152">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="206a0-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="206a0-153">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="206a0-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="206a0-154">`[UserSessionId <String>]`: nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="206a0-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="206a0-155">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="206a0-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="206a0-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="206a0-156">RELATED LINKS</span></span>

