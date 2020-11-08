---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: d6bb118a6b7699672209618e1409fe6a9bed466d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055676"
---
# <span data-ttu-id="6360a-101">Disable-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="6360a-101">Disable-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="6360a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6360a-102">SYNOPSIS</span></span>


## <span data-ttu-id="6360a-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6360a-103">SYNTAX</span></span>

### <span data-ttu-id="6360a-104">Zamknięcie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6360a-104">Shutdown (Default)</span></span>
```
Disable-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6360a-105">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6360a-105">ShutdownViaIdentity</span></span>
```
Disable-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6360a-106">Opis</span><span class="sxs-lookup"><span data-stu-id="6360a-106">DESCRIPTION</span></span>
<span data-ttu-id="6360a-107">Zamknij wystąpienie roli infrastruktury w celu obsługi konserwacji.</span><span class="sxs-lookup"><span data-stu-id="6360a-107">Shutdown an infrastructure role instance for maintenance.</span></span>

## <span data-ttu-id="6360a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6360a-108">EXAMPLES</span></span>

### <span data-ttu-id="6360a-109">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="6360a-109">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsInfrastructureRoleInstance -Name "n22r0903-Xrp03"

Shutdown an infrastructure role instance for maintenance.
```

<span data-ttu-id="6360a-110">Zamknij wystąpienie roli infrastruktury w celu obsługi konserwacji.</span><span class="sxs-lookup"><span data-stu-id="6360a-110">Shutdown an infrastructure role instance for maintenance.</span></span>


## <span data-ttu-id="6360a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6360a-111">PARAMETERS</span></span>

### <span data-ttu-id="6360a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6360a-112">-AsJob</span></span>
<span data-ttu-id="6360a-113">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="6360a-113">Run the command as a job</span></span>

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

### <span data-ttu-id="6360a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6360a-114">-DefaultProfile</span></span>
<span data-ttu-id="6360a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6360a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6360a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6360a-116">-Force</span></span>
<span data-ttu-id="6360a-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6360a-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6360a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6360a-118">-InputObject</span></span>
<span data-ttu-id="6360a-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6360a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6360a-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6360a-120">-Location</span></span>
<span data-ttu-id="6360a-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="6360a-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6360a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6360a-122">-Name</span></span>
<span data-ttu-id="6360a-123">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="6360a-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6360a-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6360a-124">-NoWait</span></span>
<span data-ttu-id="6360a-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="6360a-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6360a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6360a-126">-PassThru</span></span>
<span data-ttu-id="6360a-127">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="6360a-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6360a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6360a-128">-ResourceGroupName</span></span>
<span data-ttu-id="6360a-129">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="6360a-129">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6360a-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6360a-130">-SubscriptionId</span></span>
<span data-ttu-id="6360a-131">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6360a-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6360a-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6360a-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6360a-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6360a-133">-Confirm</span></span>
<span data-ttu-id="6360a-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6360a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6360a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6360a-135">-WhatIf</span></span>
<span data-ttu-id="6360a-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6360a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6360a-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6360a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6360a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6360a-138">CommonParameters</span></span>
<span data-ttu-id="6360a-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6360a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6360a-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6360a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6360a-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6360a-141">INPUTS</span></span>

### <span data-ttu-id="6360a-142">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6360a-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="6360a-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6360a-143">OUTPUTS</span></span>

### <span data-ttu-id="6360a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6360a-144">System.Boolean</span></span>



## <span data-ttu-id="6360a-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6360a-145">NOTES</span></span>

<span data-ttu-id="6360a-146">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6360a-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6360a-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6360a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6360a-148">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="6360a-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6360a-149">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="6360a-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="6360a-150">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="6360a-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="6360a-151">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="6360a-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="6360a-152">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="6360a-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="6360a-153">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="6360a-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="6360a-154">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="6360a-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="6360a-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6360a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6360a-156">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="6360a-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="6360a-157">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="6360a-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="6360a-158">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="6360a-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6360a-159">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="6360a-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="6360a-160">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="6360a-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="6360a-161">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="6360a-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="6360a-162">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="6360a-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="6360a-163">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6360a-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="6360a-164">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="6360a-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="6360a-165">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="6360a-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="6360a-166">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="6360a-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="6360a-167">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="6360a-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="6360a-168">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="6360a-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="6360a-169">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6360a-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6360a-170">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6360a-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6360a-171">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="6360a-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="6360a-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6360a-172">RELATED LINKS</span></span>

