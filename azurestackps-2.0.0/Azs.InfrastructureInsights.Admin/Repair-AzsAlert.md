---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891714"
---
# <span data-ttu-id="23076-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="23076-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="23076-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23076-102">SYNOPSIS</span></span>
<span data-ttu-id="23076-103">Naprawianie alertu.</span><span class="sxs-lookup"><span data-stu-id="23076-103">Repairs an alert.</span></span>

## <span data-ttu-id="23076-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23076-104">SYNTAX</span></span>

### <span data-ttu-id="23076-105">Naprawianie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="23076-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="23076-106">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23076-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="23076-107">Opis</span><span class="sxs-lookup"><span data-stu-id="23076-107">DESCRIPTION</span></span>
<span data-ttu-id="23076-108">Naprawianie alertu.</span><span class="sxs-lookup"><span data-stu-id="23076-108">Repairs an alert.</span></span>

## <span data-ttu-id="23076-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23076-109">EXAMPLES</span></span>

### <span data-ttu-id="23076-110">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="23076-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="23076-111">Naprawianie alertu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="23076-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="23076-112">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="23076-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="23076-113">Naprawianie alertu za pośrednictwem połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="23076-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="23076-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23076-114">PARAMETERS</span></span>

### <span data-ttu-id="23076-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23076-115">-AsJob</span></span>
<span data-ttu-id="23076-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="23076-116">Run the command as a job</span></span>

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

### <span data-ttu-id="23076-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23076-117">-DefaultProfile</span></span>
<span data-ttu-id="23076-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23076-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23076-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23076-119">-InputObject</span></span>
<span data-ttu-id="23076-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="23076-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="23076-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="23076-121">-Location</span></span>
<span data-ttu-id="23076-122">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="23076-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="23076-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23076-123">-Name</span></span>
<span data-ttu-id="23076-124">Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="23076-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="23076-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="23076-125">-NoWait</span></span>
<span data-ttu-id="23076-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="23076-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="23076-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23076-127">-PassThru</span></span>
<span data-ttu-id="23076-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="23076-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="23076-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23076-129">-ResourceGroupName</span></span>
<span data-ttu-id="23076-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23076-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="23076-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="23076-131">-SubscriptionId</span></span>
<span data-ttu-id="23076-132">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="23076-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="23076-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="23076-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="23076-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23076-134">-Confirm</span></span>
<span data-ttu-id="23076-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23076-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23076-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23076-136">-WhatIf</span></span>
<span data-ttu-id="23076-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23076-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23076-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23076-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23076-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23076-139">CommonParameters</span></span>
<span data-ttu-id="23076-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23076-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23076-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23076-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23076-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23076-142">INPUTS</span></span>

### <span data-ttu-id="23076-143">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="23076-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="23076-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23076-144">OUTPUTS</span></span>

### <span data-ttu-id="23076-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23076-145">System.Boolean</span></span>



## <span data-ttu-id="23076-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23076-146">NOTES</span></span>

<span data-ttu-id="23076-147">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="23076-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23076-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23076-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="23076-149">INPUTobject <IInfrastructureInsightsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="23076-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23076-150">`[AlertName <String>]`: Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="23076-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="23076-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="23076-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23076-152">`[Location <String>]`: Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="23076-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="23076-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23076-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="23076-154">`[ResourceRegistrationId <String>]`: Identyfikator rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="23076-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="23076-155">`[ServiceHealth <String>]`: Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="23076-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="23076-156">`[ServiceRegistrationId <String>]`: Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="23076-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="23076-157">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="23076-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="23076-158">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="23076-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="23076-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23076-159">RELATED LINKS</span></span>

