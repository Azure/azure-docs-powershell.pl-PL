---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: 5422b416d7fc6bf16625625a991e17d65061339e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988975"
---
# <span data-ttu-id="fbcb1-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="fbcb1-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="fbcb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbcb1-102">SYNOPSIS</span></span>
<span data-ttu-id="fbcb1-103">Usuwa pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="fbcb1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbcb1-104">SYNTAX</span></span>

### <span data-ttu-id="fbcb1-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="fbcb1-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fbcb1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fbcb1-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fbcb1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbcb1-107">DESCRIPTION</span></span>
<span data-ttu-id="fbcb1-108">Usuwa pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="fbcb1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbcb1-109">EXAMPLES</span></span>

### <span data-ttu-id="fbcb1-110">Przykład 1. Usuwanie pulpitu nawigacyjnego</span><span class="sxs-lookup"><span data-stu-id="fbcb1-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="fbcb1-111">Usuń dashbaord, używając nazwy grupy zasobów i nazwy pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="fbcb1-112">Przykład 2. Usuwanie pulpitu nawigacyjnego przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="fbcb1-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="fbcb1-113">Usuń pulpit nawigacyjny zwrócony z Get-AzDashboard połączenia.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="fbcb1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbcb1-114">PARAMETERS</span></span>

### <span data-ttu-id="fbcb1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbcb1-115">-DefaultProfile</span></span>
<span data-ttu-id="fbcb1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbcb1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbcb1-117">-InputObject</span></span>
<span data-ttu-id="fbcb1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb1-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fbcb1-119">-Name</span></span>
<span data-ttu-id="fbcb1-120">Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbcb1-121">-PassThru</span></span>
<span data-ttu-id="fbcb1-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fbcb1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbcb1-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbcb1-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="fbcb1-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbcb1-125">-SubscriptionId</span></span>
<span data-ttu-id="fbcb1-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-126">The Azure subscription ID.</span></span>
<span data-ttu-id="fbcb1-127">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="fbcb1-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="fbcb1-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbcb1-128">-Confirm</span></span>
<span data-ttu-id="fbcb1-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbcb1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbcb1-130">-WhatIf</span></span>
<span data-ttu-id="fbcb1-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbcb1-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbcb1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbcb1-133">CommonParameters</span></span>
<span data-ttu-id="fbcb1-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbcb1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbcb1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbcb1-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbcb1-136">INPUTS</span></span>

### <span data-ttu-id="fbcb1-137">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="fbcb1-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="fbcb1-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbcb1-138">OUTPUTS</span></span>

### <span data-ttu-id="fbcb1-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbcb1-139">System.Boolean</span></span>

## <span data-ttu-id="fbcb1-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbcb1-140">NOTES</span></span>

<span data-ttu-id="fbcb1-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fbcb1-141">ALIASES</span></span>

<span data-ttu-id="fbcb1-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbcb1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fbcb1-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fbcb1-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fbcb1-145">INPUTOBJECT: <IPortalIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="fbcb1-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fbcb1-146">`[DashboardName <String>]`: nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="fbcb1-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fbcb1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fbcb1-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="fbcb1-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fbcb1-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="fbcb1-150">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="fbcb1-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="fbcb1-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbcb1-151">RELATED LINKS</span></span>

