---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893934"
---
# <span data-ttu-id="39f94-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="39f94-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="39f94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39f94-102">SYNOPSIS</span></span>
<span data-ttu-id="39f94-103">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="39f94-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="39f94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39f94-104">SYNTAX</span></span>

### <span data-ttu-id="39f94-105">PowerOff (domyślny)</span><span class="sxs-lookup"><span data-stu-id="39f94-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39f94-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39f94-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39f94-107">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="39f94-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39f94-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39f94-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39f94-109">Opis</span><span class="sxs-lookup"><span data-stu-id="39f94-109">DESCRIPTION</span></span>
<span data-ttu-id="39f94-110">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="39f94-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="39f94-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39f94-111">EXAMPLES</span></span>

### <span data-ttu-id="39f94-112">Przykład 1: {{dodanie tytułu}}</span><span class="sxs-lookup"><span data-stu-id="39f94-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="39f94-113">Wyłącz funkcję wyłączania roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="39f94-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="39f94-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39f94-114">PARAMETERS</span></span>

### <span data-ttu-id="39f94-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39f94-115">-AsJob</span></span>
<span data-ttu-id="39f94-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="39f94-116">Run the command as a job</span></span>

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

### <span data-ttu-id="39f94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f94-117">-DefaultProfile</span></span>
<span data-ttu-id="39f94-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39f94-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39f94-119">-Force</span><span class="sxs-lookup"><span data-stu-id="39f94-119">-Force</span></span>
<span data-ttu-id="39f94-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="39f94-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="39f94-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39f94-121">-InputObject</span></span>
<span data-ttu-id="39f94-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="39f94-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="39f94-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="39f94-123">-Location</span></span>
<span data-ttu-id="39f94-124">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="39f94-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39f94-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39f94-125">-Name</span></span>
<span data-ttu-id="39f94-126">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="39f94-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39f94-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="39f94-127">-NoWait</span></span>
<span data-ttu-id="39f94-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="39f94-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="39f94-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39f94-129">-PassThru</span></span>
<span data-ttu-id="39f94-130">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="39f94-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="39f94-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f94-131">-ResourceGroupName</span></span>
<span data-ttu-id="39f94-132">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="39f94-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39f94-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="39f94-133">-SubscriptionId</span></span>
<span data-ttu-id="39f94-134">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="39f94-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="39f94-135">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="39f94-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39f94-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39f94-136">-Confirm</span></span>
<span data-ttu-id="39f94-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f94-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39f94-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39f94-138">-WhatIf</span></span>
<span data-ttu-id="39f94-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f94-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39f94-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39f94-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39f94-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f94-141">CommonParameters</span></span>
<span data-ttu-id="39f94-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f94-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f94-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39f94-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f94-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39f94-144">INPUTS</span></span>

### <span data-ttu-id="39f94-145">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="39f94-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="39f94-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39f94-146">OUTPUTS</span></span>

### <span data-ttu-id="39f94-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39f94-147">System.Boolean</span></span>



## <span data-ttu-id="39f94-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39f94-148">NOTES</span></span>

<span data-ttu-id="39f94-149">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="39f94-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39f94-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39f94-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="39f94-151">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="39f94-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39f94-152">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="39f94-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="39f94-153">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="39f94-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="39f94-154">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="39f94-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="39f94-155">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="39f94-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="39f94-156">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="39f94-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="39f94-157">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="39f94-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="39f94-158">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="39f94-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39f94-159">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="39f94-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="39f94-160">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="39f94-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="39f94-161">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="39f94-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="39f94-162">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="39f94-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="39f94-163">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="39f94-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="39f94-164">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="39f94-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="39f94-165">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="39f94-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="39f94-166">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="39f94-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="39f94-167">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="39f94-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="39f94-168">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="39f94-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="39f94-169">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="39f94-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="39f94-170">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="39f94-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="39f94-171">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="39f94-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="39f94-172">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="39f94-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="39f94-173">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="39f94-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="39f94-174">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="39f94-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="39f94-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39f94-175">RELATED LINKS</span></span>

