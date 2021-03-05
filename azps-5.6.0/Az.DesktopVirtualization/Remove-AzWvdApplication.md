---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: 0d8f3f3fa1f89c2045b10e07a5f7b11358222234
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966049"
---
# <span data-ttu-id="55c59-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="55c59-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="55c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55c59-102">SYNOPSIS</span></span>
<span data-ttu-id="55c59-103">Usuwanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="55c59-103">Remove an application.</span></span>

## <span data-ttu-id="55c59-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="55c59-104">SYNTAX</span></span>

### <span data-ttu-id="55c59-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="55c59-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="55c59-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="55c59-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55c59-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="55c59-107">DESCRIPTION</span></span>
<span data-ttu-id="55c59-108">Usuwanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="55c59-108">Remove an application.</span></span>

## <span data-ttu-id="55c59-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="55c59-109">EXAMPLES</span></span>

### <span data-ttu-id="55c59-110">Przykład 1. Usuwanie aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="55c59-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="55c59-111">To polecenie usuwa aplikację pulpitu wirtualnego systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="55c59-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="55c59-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55c59-112">PARAMETERS</span></span>

### <span data-ttu-id="55c59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c59-113">-DefaultProfile</span></span>
<span data-ttu-id="55c59-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="55c59-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55c59-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="55c59-115">-GroupName</span></span>
<span data-ttu-id="55c59-116">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="55c59-116">The name of the application group</span></span>

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

### <span data-ttu-id="55c59-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55c59-117">-InputObject</span></span>
<span data-ttu-id="55c59-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="55c59-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="55c59-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="55c59-119">-Name</span></span>
<span data-ttu-id="55c59-120">Nazwa aplikacji w obrębie określonej grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="55c59-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c59-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55c59-121">-PassThru</span></span>
<span data-ttu-id="55c59-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="55c59-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="55c59-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c59-123">-ResourceGroupName</span></span>
<span data-ttu-id="55c59-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55c59-124">The name of the resource group.</span></span>
<span data-ttu-id="55c59-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="55c59-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="55c59-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55c59-126">-SubscriptionId</span></span>
<span data-ttu-id="55c59-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="55c59-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="55c59-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55c59-128">-Confirm</span></span>
<span data-ttu-id="55c59-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="55c59-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55c59-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55c59-130">-WhatIf</span></span>
<span data-ttu-id="55c59-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c59-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55c59-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="55c59-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55c59-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c59-133">CommonParameters</span></span>
<span data-ttu-id="55c59-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55c59-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c59-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55c59-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c59-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55c59-136">INPUTS</span></span>

### <span data-ttu-id="55c59-137">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="55c59-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="55c59-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55c59-138">OUTPUTS</span></span>

### <span data-ttu-id="55c59-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55c59-139">System.Boolean</span></span>

## <span data-ttu-id="55c59-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="55c59-140">NOTES</span></span>

<span data-ttu-id="55c59-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="55c59-141">ALIASES</span></span>

<span data-ttu-id="55c59-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55c59-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55c59-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="55c59-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55c59-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55c59-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55c59-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="55c59-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55c59-146">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="55c59-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="55c59-147">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="55c59-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="55c59-148">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="55c59-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="55c59-149">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55c59-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="55c59-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="55c59-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55c59-151">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="55c59-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="55c59-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55c59-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="55c59-153">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="55c59-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="55c59-154">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="55c59-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="55c59-155">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="55c59-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="55c59-156">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="55c59-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="55c59-157">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="55c59-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="55c59-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55c59-158">RELATED LINKS</span></span>

