---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: a15dc7c72f2f7ef321f05f51d5b90c936f0406e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980522"
---
# <span data-ttu-id="94d99-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="94d99-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="94d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d99-102">SYNOPSIS</span></span>
<span data-ttu-id="94d99-103">Usuwanie sesji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="94d99-103">Remove a userSession.</span></span>

## <span data-ttu-id="94d99-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94d99-104">SYNTAX</span></span>

### <span data-ttu-id="94d99-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="94d99-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94d99-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94d99-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94d99-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="94d99-107">DESCRIPTION</span></span>
<span data-ttu-id="94d99-108">Usuwanie sesji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="94d99-108">Remove a userSession.</span></span>

## <span data-ttu-id="94d99-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94d99-109">EXAMPLES</span></span>

### <span data-ttu-id="94d99-110">Przykład 1. Usunięcie użytkownika pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="94d99-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="94d99-111">To polecenie usuwa polecenie UserSession (Użytkownik pulpitu wirtualnego systemu Windows) na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="94d99-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="94d99-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94d99-112">PARAMETERS</span></span>

### <span data-ttu-id="94d99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d99-113">-DefaultProfile</span></span>
<span data-ttu-id="94d99-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94d99-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94d99-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="94d99-115">-Force</span></span>
<span data-ttu-id="94d99-116">Wymusz flagę w celu zalogowania się poza userSession.</span><span class="sxs-lookup"><span data-stu-id="94d99-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="94d99-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="94d99-117">-HostPoolName</span></span>
<span data-ttu-id="94d99-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="94d99-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="94d99-119">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="94d99-119">-Id</span></span>
<span data-ttu-id="94d99-120">Nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="94d99-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d99-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94d99-121">-InputObject</span></span>
<span data-ttu-id="94d99-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="94d99-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94d99-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94d99-123">-PassThru</span></span>
<span data-ttu-id="94d99-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="94d99-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="94d99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d99-125">-ResourceGroupName</span></span>
<span data-ttu-id="94d99-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94d99-126">The name of the resource group.</span></span>
<span data-ttu-id="94d99-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="94d99-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="94d99-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="94d99-128">-SessionHostName</span></span>
<span data-ttu-id="94d99-129">Nazwa hosta sesji w określonej puli hosta</span><span class="sxs-lookup"><span data-stu-id="94d99-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="94d99-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94d99-130">-SubscriptionId</span></span>
<span data-ttu-id="94d99-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="94d99-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="94d99-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94d99-132">-Confirm</span></span>
<span data-ttu-id="94d99-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94d99-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94d99-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d99-134">-WhatIf</span></span>
<span data-ttu-id="94d99-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94d99-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94d99-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94d99-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94d99-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d99-137">CommonParameters</span></span>
<span data-ttu-id="94d99-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d99-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d99-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94d99-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d99-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94d99-140">INPUTS</span></span>

### <span data-ttu-id="94d99-141">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="94d99-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="94d99-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94d99-142">OUTPUTS</span></span>

### <span data-ttu-id="94d99-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94d99-143">System.Boolean</span></span>

## <span data-ttu-id="94d99-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94d99-144">NOTES</span></span>

<span data-ttu-id="94d99-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="94d99-145">ALIASES</span></span>

<span data-ttu-id="94d99-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94d99-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94d99-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="94d99-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94d99-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94d99-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94d99-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="94d99-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94d99-150">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="94d99-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="94d99-151">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="94d99-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="94d99-152">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="94d99-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="94d99-153">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94d99-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="94d99-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="94d99-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94d99-155">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="94d99-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="94d99-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94d99-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="94d99-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="94d99-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="94d99-158">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="94d99-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="94d99-159">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="94d99-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="94d99-160">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="94d99-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="94d99-161">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="94d99-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="94d99-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94d99-162">RELATED LINKS</span></span>

