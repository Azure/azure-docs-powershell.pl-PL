---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370890"
---
# <span data-ttu-id="2a8ee-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="2a8ee-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="2a8ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8ee-103">Usuwa pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="2a8ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a8ee-104">SYNTAX</span></span>

### <span data-ttu-id="2a8ee-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2a8ee-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2a8ee-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2a8ee-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2a8ee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2a8ee-107">DESCRIPTION</span></span>
<span data-ttu-id="2a8ee-108">Usuwa pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="2a8ee-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a8ee-109">EXAMPLES</span></span>

### <span data-ttu-id="2a8ee-110">Przykład 1. Usuń pulpit nawigacyjny</span><span class="sxs-lookup"><span data-stu-id="2a8ee-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="2a8ee-111">Usuń dashbaord, używając nazwy grupy zasobów i nazwy pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="2a8ee-112">Przykład 2: usuwanie pulpitu nawigacyjnego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="2a8ee-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="2a8ee-113">Usuń pulpit nawigacyjny zwrócony przez Get-AzDashboard połączenie.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="2a8ee-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a8ee-114">PARAMETERS</span></span>

### <span data-ttu-id="2a8ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8ee-115">-DefaultProfile</span></span>
<span data-ttu-id="2a8ee-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a8ee-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a8ee-117">-InputObject</span></span>
<span data-ttu-id="2a8ee-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a8ee-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a8ee-119">-Name</span></span>
<span data-ttu-id="2a8ee-120">Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-120">The name of the dashboard.</span></span>

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

### <span data-ttu-id="2a8ee-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a8ee-121">-PassThru</span></span>
<span data-ttu-id="2a8ee-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2a8ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a8ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="2a8ee-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a8ee-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2a8ee-125">-SubscriptionId</span></span>
<span data-ttu-id="2a8ee-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-126">The Azure subscription ID.</span></span>
<span data-ttu-id="2a8ee-127">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="2a8ee-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="2a8ee-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a8ee-128">-Confirm</span></span>
<span data-ttu-id="2a8ee-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a8ee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a8ee-130">-WhatIf</span></span>
<span data-ttu-id="2a8ee-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a8ee-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a8ee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8ee-133">CommonParameters</span></span>
<span data-ttu-id="2a8ee-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8ee-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a8ee-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8ee-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a8ee-136">INPUTS</span></span>

### <span data-ttu-id="2a8ee-137">Microsoft. Azure. PowerShell. polecenia cmdlet. Portal. models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="2a8ee-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="2a8ee-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a8ee-138">OUTPUTS</span></span>

### <span data-ttu-id="2a8ee-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a8ee-139">System.Boolean</span></span>

## <span data-ttu-id="2a8ee-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a8ee-140">NOTES</span></span>

<span data-ttu-id="2a8ee-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2a8ee-141">ALIASES</span></span>

<span data-ttu-id="2a8ee-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a8ee-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a8ee-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a8ee-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a8ee-145">INPUTobject <IPortalIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2a8ee-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2a8ee-146">`[DashboardName <String>]`: Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="2a8ee-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2a8ee-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2a8ee-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2a8ee-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8ee-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="2a8ee-150">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="2a8ee-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="2a8ee-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a8ee-151">RELATED LINKS</span></span>

