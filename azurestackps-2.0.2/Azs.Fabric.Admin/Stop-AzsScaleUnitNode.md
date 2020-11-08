---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055775"
---
# <span data-ttu-id="46438-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="46438-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="46438-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46438-102">SYNOPSIS</span></span>
<span data-ttu-id="46438-103">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="46438-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="46438-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46438-104">SYNTAX</span></span>

### <span data-ttu-id="46438-105">PowerOff (domyślny)</span><span class="sxs-lookup"><span data-stu-id="46438-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="46438-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="46438-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="46438-107">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="46438-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="46438-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="46438-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46438-109">Opis</span><span class="sxs-lookup"><span data-stu-id="46438-109">DESCRIPTION</span></span>
<span data-ttu-id="46438-110">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="46438-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="46438-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46438-111">EXAMPLES</span></span>

### <span data-ttu-id="46438-112">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="46438-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="46438-113">Wyłączanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="46438-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="46438-114">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="46438-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="46438-115">Wyłączanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="46438-115">Power down a scale unit node.</span></span> <span data-ttu-id="46438-116">Jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="46438-116">As a job.</span></span>

## <span data-ttu-id="46438-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46438-117">PARAMETERS</span></span>

### <span data-ttu-id="46438-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46438-118">-AsJob</span></span>
<span data-ttu-id="46438-119">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="46438-119">Run the command as a job</span></span>

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

### <span data-ttu-id="46438-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46438-120">-DefaultProfile</span></span>
<span data-ttu-id="46438-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46438-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46438-122">-Force</span><span class="sxs-lookup"><span data-stu-id="46438-122">-Force</span></span>
<span data-ttu-id="46438-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="46438-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="46438-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="46438-124">-InputObject</span></span>
<span data-ttu-id="46438-125">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="46438-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="46438-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="46438-126">-Location</span></span>
<span data-ttu-id="46438-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="46438-127">Location of the resource.</span></span>

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

### <span data-ttu-id="46438-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46438-128">-Name</span></span>
<span data-ttu-id="46438-129">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="46438-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="46438-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="46438-130">-NoWait</span></span>
<span data-ttu-id="46438-131">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="46438-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="46438-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46438-132">-PassThru</span></span>
<span data-ttu-id="46438-133">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="46438-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="46438-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46438-134">-ResourceGroupName</span></span>
<span data-ttu-id="46438-135">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="46438-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="46438-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="46438-136">-SubscriptionId</span></span>
<span data-ttu-id="46438-137">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46438-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="46438-138">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="46438-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="46438-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46438-139">-Confirm</span></span>
<span data-ttu-id="46438-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46438-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46438-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46438-141">-WhatIf</span></span>
<span data-ttu-id="46438-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46438-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46438-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46438-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46438-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46438-144">CommonParameters</span></span>
<span data-ttu-id="46438-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46438-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46438-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46438-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46438-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46438-147">INPUTS</span></span>

### <span data-ttu-id="46438-148">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="46438-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="46438-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46438-149">OUTPUTS</span></span>

### <span data-ttu-id="46438-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46438-150">System.Boolean</span></span>

## <span data-ttu-id="46438-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46438-151">NOTES</span></span>

<span data-ttu-id="46438-152">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="46438-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46438-153">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46438-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="46438-154">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="46438-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46438-155">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="46438-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="46438-156">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="46438-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="46438-157">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="46438-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="46438-158">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="46438-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="46438-159">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="46438-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="46438-160">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="46438-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="46438-161">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="46438-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46438-162">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="46438-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="46438-163">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="46438-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="46438-164">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="46438-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="46438-165">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="46438-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="46438-166">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="46438-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="46438-167">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="46438-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="46438-168">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="46438-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="46438-169">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46438-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="46438-170">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="46438-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="46438-171">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="46438-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="46438-172">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="46438-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="46438-173">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="46438-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="46438-174">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="46438-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="46438-175">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46438-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="46438-176">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="46438-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="46438-177">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="46438-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="46438-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46438-178">RELATED LINKS</span></span>
