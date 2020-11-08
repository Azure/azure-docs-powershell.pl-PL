---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055664"
---
# <span data-ttu-id="44834-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="44834-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="44834-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44834-102">SYNOPSIS</span></span>
<span data-ttu-id="44834-103">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="44834-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="44834-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44834-104">SYNTAX</span></span>

### <span data-ttu-id="44834-105">PowerOn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="44834-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44834-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44834-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44834-107">Opis</span><span class="sxs-lookup"><span data-stu-id="44834-107">DESCRIPTION</span></span>
<span data-ttu-id="44834-108">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="44834-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="44834-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44834-109">EXAMPLES</span></span>

### <span data-ttu-id="44834-110">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="44834-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="44834-111">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="44834-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="44834-112">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="44834-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="44834-113">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="44834-113">Power on a scale unit node.</span></span> <span data-ttu-id="44834-114">Jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="44834-114">As a job.</span></span>

## <span data-ttu-id="44834-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44834-115">PARAMETERS</span></span>

### <span data-ttu-id="44834-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44834-116">-AsJob</span></span>
<span data-ttu-id="44834-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="44834-117">Run the command as a job</span></span>

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

### <span data-ttu-id="44834-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44834-118">-DefaultProfile</span></span>
<span data-ttu-id="44834-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44834-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44834-120">-Force</span><span class="sxs-lookup"><span data-stu-id="44834-120">-Force</span></span>
<span data-ttu-id="44834-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44834-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="44834-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="44834-122">-InputObject</span></span>
<span data-ttu-id="44834-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="44834-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="44834-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="44834-124">-Location</span></span>
<span data-ttu-id="44834-125">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="44834-125">Location of the resource.</span></span>

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

### <span data-ttu-id="44834-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44834-126">-Name</span></span>
<span data-ttu-id="44834-127">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="44834-127">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="44834-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="44834-128">-NoWait</span></span>
<span data-ttu-id="44834-129">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="44834-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44834-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44834-130">-PassThru</span></span>
<span data-ttu-id="44834-131">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="44834-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44834-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44834-132">-ResourceGroupName</span></span>
<span data-ttu-id="44834-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="44834-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="44834-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="44834-134">-SubscriptionId</span></span>
<span data-ttu-id="44834-135">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44834-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="44834-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="44834-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="44834-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44834-137">-Confirm</span></span>
<span data-ttu-id="44834-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44834-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44834-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44834-139">-WhatIf</span></span>
<span data-ttu-id="44834-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44834-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44834-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44834-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44834-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44834-142">CommonParameters</span></span>
<span data-ttu-id="44834-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44834-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44834-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44834-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44834-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44834-145">INPUTS</span></span>

### <span data-ttu-id="44834-146">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="44834-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="44834-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44834-147">OUTPUTS</span></span>

### <span data-ttu-id="44834-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44834-148">System.Boolean</span></span>

## <span data-ttu-id="44834-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44834-149">NOTES</span></span>

<span data-ttu-id="44834-150">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="44834-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44834-151">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44834-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="44834-152">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="44834-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44834-153">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="44834-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="44834-154">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="44834-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="44834-155">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="44834-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="44834-156">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="44834-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="44834-157">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="44834-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="44834-158">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="44834-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="44834-159">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="44834-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44834-160">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="44834-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="44834-161">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="44834-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="44834-162">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="44834-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="44834-163">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="44834-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="44834-164">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="44834-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="44834-165">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="44834-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="44834-166">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="44834-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="44834-167">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="44834-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="44834-168">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="44834-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="44834-169">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="44834-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="44834-170">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="44834-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="44834-171">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="44834-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="44834-172">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="44834-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="44834-173">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44834-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="44834-174">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="44834-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="44834-175">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="44834-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="44834-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44834-176">RELATED LINKS</span></span>
