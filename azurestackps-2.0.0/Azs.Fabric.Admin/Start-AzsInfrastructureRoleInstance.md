---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/start-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 922aea432548557857b627696e156c75a8e46157
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893993"
---
# <span data-ttu-id="ea1f0-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="ea1f0-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="ea1f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1f0-103">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="ea1f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea1f0-104">SYNTAX</span></span>

### <span data-ttu-id="ea1f0-105">PowerOn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea1f0-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea1f0-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ea1f0-106">PowerOnViaIdentity</span></span>
```
Start-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea1f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ea1f0-107">DESCRIPTION</span></span>
<span data-ttu-id="ea1f0-108">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="ea1f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea1f0-109">EXAMPLES</span></span>

### <span data-ttu-id="ea1f0-110">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="ea1f0-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="ea1f0-111">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-111">Power on an infrastructure role instance.</span></span>


## <span data-ttu-id="ea1f0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea1f0-112">PARAMETERS</span></span>

### <span data-ttu-id="ea1f0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea1f0-113">-AsJob</span></span>
<span data-ttu-id="ea1f0-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="ea1f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1f0-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="ea1f0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ea1f0-116">-Force</span></span>
<span data-ttu-id="ea1f0-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ea1f0-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea1f0-118">-InputObject</span></span>
<span data-ttu-id="ea1f0-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ea1f0-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ea1f0-120">-Location</span></span>
<span data-ttu-id="ea1f0-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ea1f0-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea1f0-122">-Name</span></span>
<span data-ttu-id="ea1f0-123">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ea1f0-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ea1f0-124">-NoWait</span></span>
<span data-ttu-id="ea1f0-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ea1f0-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ea1f0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea1f0-126">-PassThru</span></span>
<span data-ttu-id="ea1f0-127">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ea1f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea1f0-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-129">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ea1f0-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ea1f0-130">-SubscriptionId</span></span>
<span data-ttu-id="ea1f0-131">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ea1f0-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ea1f0-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea1f0-133">-Confirm</span></span>
<span data-ttu-id="ea1f0-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea1f0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1f0-135">-WhatIf</span></span>
<span data-ttu-id="ea1f0-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea1f0-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea1f0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1f0-138">CommonParameters</span></span>
<span data-ttu-id="ea1f0-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1f0-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea1f0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1f0-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea1f0-141">INPUTS</span></span>

### <span data-ttu-id="ea1f0-142">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ea1f0-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="ea1f0-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea1f0-143">OUTPUTS</span></span>

### <span data-ttu-id="ea1f0-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea1f0-144">System.Boolean</span></span>



## <span data-ttu-id="ea1f0-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea1f0-145">NOTES</span></span>

<span data-ttu-id="ea1f0-146">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea1f0-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ea1f0-148">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ea1f0-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ea1f0-149">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="ea1f0-150">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="ea1f0-151">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="ea1f0-152">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="ea1f0-153">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="ea1f0-154">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="ea1f0-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ea1f0-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ea1f0-156">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="ea1f0-157">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="ea1f0-158">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ea1f0-159">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="ea1f0-160">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="ea1f0-161">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="ea1f0-162">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="ea1f0-163">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ea1f0-164">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="ea1f0-165">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="ea1f0-166">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="ea1f0-167">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="ea1f0-168">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="ea1f0-169">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ea1f0-170">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ea1f0-171">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea1f0-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="ea1f0-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea1f0-172">RELATED LINKS</span></span>

