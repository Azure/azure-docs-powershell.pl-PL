---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: ee8334a233c35c2b834bfb89ddf20152d466367f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966001"
---
# <span data-ttu-id="ecd62-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="ecd62-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="ecd62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecd62-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd62-103">Usuń hosta SessionHost.</span><span class="sxs-lookup"><span data-stu-id="ecd62-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="ecd62-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ecd62-104">SYNTAX</span></span>

### <span data-ttu-id="ecd62-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="ecd62-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ecd62-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ecd62-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ecd62-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ecd62-107">DESCRIPTION</span></span>
<span data-ttu-id="ecd62-108">Usuń hosta SessionHost.</span><span class="sxs-lookup"><span data-stu-id="ecd62-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="ecd62-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ecd62-109">EXAMPLES</span></span>

### <span data-ttu-id="ecd62-110">Przykład 1. Usunięcie hosta SessionHost pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="ecd62-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="ecd62-111">To polecenie usuwa hosta SessionHost pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="ecd62-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="ecd62-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecd62-112">PARAMETERS</span></span>

### <span data-ttu-id="ecd62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd62-113">-DefaultProfile</span></span>
<span data-ttu-id="ecd62-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ecd62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecd62-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ecd62-115">-Force</span></span>
<span data-ttu-id="ecd62-116">Wymusz flagę, aby wymusić usunięcie sessionHost nawet wtedy, gdy istnieje userSession.</span><span class="sxs-lookup"><span data-stu-id="ecd62-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="ecd62-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ecd62-117">-HostPoolName</span></span>
<span data-ttu-id="ecd62-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ecd62-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ecd62-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecd62-119">-InputObject</span></span>
<span data-ttu-id="ecd62-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ecd62-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ecd62-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ecd62-121">-Name</span></span>
<span data-ttu-id="ecd62-122">Nazwa hosta sesji w określonej puli hosta</span><span class="sxs-lookup"><span data-stu-id="ecd62-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd62-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecd62-123">-PassThru</span></span>
<span data-ttu-id="ecd62-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ecd62-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ecd62-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd62-125">-ResourceGroupName</span></span>
<span data-ttu-id="ecd62-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ecd62-126">The name of the resource group.</span></span>
<span data-ttu-id="ecd62-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ecd62-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ecd62-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecd62-128">-SubscriptionId</span></span>
<span data-ttu-id="ecd62-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ecd62-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ecd62-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ecd62-130">-Confirm</span></span>
<span data-ttu-id="ecd62-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ecd62-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd62-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd62-132">-WhatIf</span></span>
<span data-ttu-id="ecd62-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecd62-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd62-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ecd62-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd62-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd62-135">CommonParameters</span></span>
<span data-ttu-id="ecd62-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd62-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd62-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecd62-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd62-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecd62-138">INPUTS</span></span>

### <span data-ttu-id="ecd62-139">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ecd62-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ecd62-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecd62-140">OUTPUTS</span></span>

### <span data-ttu-id="ecd62-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ecd62-141">System.Boolean</span></span>

## <span data-ttu-id="ecd62-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ecd62-142">NOTES</span></span>

<span data-ttu-id="ecd62-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ecd62-143">ALIASES</span></span>

<span data-ttu-id="ecd62-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ecd62-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ecd62-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ecd62-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ecd62-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ecd62-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ecd62-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ecd62-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ecd62-148">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ecd62-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ecd62-149">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ecd62-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ecd62-150">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="ecd62-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ecd62-151">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ecd62-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ecd62-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ecd62-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ecd62-153">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="ecd62-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ecd62-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ecd62-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ecd62-155">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ecd62-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="ecd62-156">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="ecd62-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ecd62-157">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ecd62-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ecd62-158">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="ecd62-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ecd62-159">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="ecd62-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ecd62-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecd62-160">RELATED LINKS</span></span>

