---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 5762cbd1c972f5500a15be8fea8595165add3afc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054133"
---
# <span data-ttu-id="29f4d-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="29f4d-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="29f4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="29f4d-103">Uruchom ponownie wystąpienie roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="29f4d-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="29f4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29f4d-104">SYNTAX</span></span>

### <span data-ttu-id="29f4d-105">Ponowna rozruch (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="29f4d-105">Reboot (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="29f4d-106">RebootViaIdentity</span><span class="sxs-lookup"><span data-stu-id="29f4d-106">RebootViaIdentity</span></span>
```
Restart-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29f4d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="29f4d-107">DESCRIPTION</span></span>
<span data-ttu-id="29f4d-108">Uruchom ponownie wystąpienie roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="29f4d-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="29f4d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29f4d-109">EXAMPLES</span></span>

### <span data-ttu-id="29f4d-110">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="29f4d-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="29f4d-111">Uruchom ponownie wystąpienie roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="29f4d-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="29f4d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29f4d-112">PARAMETERS</span></span>

### <span data-ttu-id="29f4d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29f4d-113">-AsJob</span></span>
<span data-ttu-id="29f4d-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="29f4d-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="29f4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f4d-115">-DefaultProfile</span></span>
<span data-ttu-id="29f4d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29f4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="29f4d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="29f4d-117">-Force</span></span>
<span data-ttu-id="29f4d-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="29f4d-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="29f4d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29f4d-119">-InputObject</span></span>
<span data-ttu-id="29f4d-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="29f4d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RebootViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="29f4d-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="29f4d-121">-Location</span></span>
<span data-ttu-id="29f4d-122">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="29f4d-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="29f4d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29f4d-123">-Name</span></span>
<span data-ttu-id="29f4d-124">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="29f4d-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="29f4d-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="29f4d-125">-NoWait</span></span>
<span data-ttu-id="29f4d-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="29f4d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="29f4d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29f4d-127">-PassThru</span></span>
<span data-ttu-id="29f4d-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="29f4d-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="29f4d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f4d-129">-ResourceGroupName</span></span>
<span data-ttu-id="29f4d-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29f4d-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```
### <span data-ttu-id="29f4d-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="29f4d-131">-SubscriptionId</span></span>
<span data-ttu-id="29f4d-132">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="29f4d-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="29f4d-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="29f4d-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="29f4d-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29f4d-134">-Confirm</span></span>
<span data-ttu-id="29f4d-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29f4d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29f4d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29f4d-136">-WhatIf</span></span>
<span data-ttu-id="29f4d-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29f4d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29f4d-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29f4d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29f4d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f4d-139">CommonParameters</span></span>
<span data-ttu-id="29f4d-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f4d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f4d-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29f4d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f4d-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29f4d-142">INPUTS</span></span>

### <span data-ttu-id="29f4d-143">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="29f4d-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="29f4d-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29f4d-144">OUTPUTS</span></span>

### <span data-ttu-id="29f4d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29f4d-145">System.Boolean</span></span>



## <span data-ttu-id="29f4d-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29f4d-146">NOTES</span></span>

<span data-ttu-id="29f4d-147">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="29f4d-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29f4d-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="29f4d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="29f4d-149">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="29f4d-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29f4d-150">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="29f4d-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="29f4d-151">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="29f4d-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="29f4d-152">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="29f4d-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="29f4d-153">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="29f4d-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="29f4d-154">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="29f4d-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="29f4d-155">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="29f4d-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="29f4d-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="29f4d-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29f4d-157">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="29f4d-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="29f4d-158">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="29f4d-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="29f4d-159">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="29f4d-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="29f4d-160">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="29f4d-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="29f4d-161">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="29f4d-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="29f4d-162">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="29f4d-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="29f4d-163">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="29f4d-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="29f4d-164">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29f4d-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="29f4d-165">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="29f4d-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="29f4d-166">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="29f4d-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="29f4d-167">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="29f4d-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="29f4d-168">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="29f4d-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="29f4d-169">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="29f4d-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="29f4d-170">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="29f4d-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="29f4d-171">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="29f4d-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="29f4d-172">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="29f4d-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="29f4d-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29f4d-173">RELATED LINKS</span></span>

