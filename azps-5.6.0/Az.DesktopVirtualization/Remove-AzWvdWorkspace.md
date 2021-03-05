---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 682f59c5c07643ecd93fd1ae051abc8e74c4e185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980481"
---
# <span data-ttu-id="adb02-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="adb02-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="adb02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb02-102">SYNOPSIS</span></span>
<span data-ttu-id="adb02-103">Usuwanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="adb02-103">Remove a workspace.</span></span>

## <span data-ttu-id="adb02-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="adb02-104">SYNTAX</span></span>

### <span data-ttu-id="adb02-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="adb02-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="adb02-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="adb02-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="adb02-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="adb02-107">DESCRIPTION</span></span>
<span data-ttu-id="adb02-108">Usuwanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="adb02-108">Remove a workspace.</span></span>

## <span data-ttu-id="adb02-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="adb02-109">EXAMPLES</span></span>

### <span data-ttu-id="adb02-110">Przykład 1. Usuwanie obszaru roboczego pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="adb02-110">Example 1: Delete a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="adb02-111">To polecenie usuwa obszar roboczy pulpitu wirtualnego systemu Windows z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="adb02-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="adb02-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adb02-112">PARAMETERS</span></span>

### <span data-ttu-id="adb02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb02-113">-DefaultProfile</span></span>
<span data-ttu-id="adb02-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="adb02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb02-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adb02-115">-InputObject</span></span>
<span data-ttu-id="adb02-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="adb02-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="adb02-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="adb02-117">-Name</span></span>
<span data-ttu-id="adb02-118">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="adb02-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adb02-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adb02-119">-PassThru</span></span>
<span data-ttu-id="adb02-120">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="adb02-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="adb02-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb02-121">-ResourceGroupName</span></span>
<span data-ttu-id="adb02-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="adb02-122">The name of the resource group.</span></span>
<span data-ttu-id="adb02-123">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="adb02-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="adb02-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="adb02-124">-SubscriptionId</span></span>
<span data-ttu-id="adb02-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="adb02-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="adb02-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="adb02-126">-Confirm</span></span>
<span data-ttu-id="adb02-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="adb02-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb02-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb02-128">-WhatIf</span></span>
<span data-ttu-id="adb02-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adb02-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adb02-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="adb02-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb02-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb02-131">CommonParameters</span></span>
<span data-ttu-id="adb02-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb02-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb02-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adb02-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb02-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adb02-134">INPUTS</span></span>

### <span data-ttu-id="adb02-135">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="adb02-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="adb02-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adb02-136">OUTPUTS</span></span>

### <span data-ttu-id="adb02-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="adb02-137">System.Boolean</span></span>

## <span data-ttu-id="adb02-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="adb02-138">NOTES</span></span>

<span data-ttu-id="adb02-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="adb02-139">ALIASES</span></span>

<span data-ttu-id="adb02-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="adb02-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="adb02-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="adb02-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="adb02-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="adb02-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="adb02-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="adb02-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="adb02-144">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="adb02-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="adb02-145">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="adb02-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="adb02-146">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="adb02-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="adb02-147">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="adb02-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="adb02-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="adb02-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="adb02-149">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="adb02-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="adb02-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="adb02-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="adb02-151">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="adb02-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="adb02-152">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="adb02-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="adb02-153">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="adb02-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="adb02-154">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="adb02-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="adb02-155">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="adb02-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="adb02-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adb02-156">RELATED LINKS</span></span>

