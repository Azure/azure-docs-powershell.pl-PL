---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/enable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4a7140d5162f046377e37b92d4e6931abdbb4cf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891789"
---
# <span data-ttu-id="7f6a5-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="7f6a5-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="7f6a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f6a5-102">SYNOPSIS</span></span>


## <span data-ttu-id="7f6a5-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f6a5-103">SYNTAX</span></span>

### <span data-ttu-id="7f6a5-104">Początek (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7f6a5-104">Start (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f6a5-105">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7f6a5-105">StartViaIdentity</span></span>
```
Enable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7f6a5-106">Opis</span><span class="sxs-lookup"><span data-stu-id="7f6a5-106">DESCRIPTION</span></span>


## <span data-ttu-id="7f6a5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f6a5-107">EXAMPLES</span></span>

### <span data-ttu-id="7f6a5-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="7f6a5-108">Example 1:</span></span>
```powershell
PS C:\> Enable-AzsScaleUnitNode -Name "HC1n25r2236"

Stop maintenance mode on a scale unit node.
```

<span data-ttu-id="7f6a5-109">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-109">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="7f6a5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f6a5-110">PARAMETERS</span></span>

### <span data-ttu-id="7f6a5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f6a5-111">-AsJob</span></span>


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

### <span data-ttu-id="7f6a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6a5-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="7f6a5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7f6a5-113">-Force</span></span>


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

### <span data-ttu-id="7f6a5-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f6a5-114">-InputObject</span></span>
<span data-ttu-id="7f6a5-115">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7f6a5-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7f6a5-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f6a5-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f6a5-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f6a5-118">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7f6a5-118">-NoWait</span></span>


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

### <span data-ttu-id="7f6a5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f6a5-119">-PassThru</span></span>


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

### <span data-ttu-id="7f6a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6a5-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f6a5-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7f6a5-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f6a5-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f6a5-122">-Confirm</span></span>
<span data-ttu-id="7f6a5-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f6a5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f6a5-124">-WhatIf</span></span>
<span data-ttu-id="7f6a5-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f6a5-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f6a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6a5-127">CommonParameters</span></span>
<span data-ttu-id="7f6a5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6a5-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f6a5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6a5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f6a5-130">INPUTS</span></span>

### <span data-ttu-id="7f6a5-131">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7f6a5-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="7f6a5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f6a5-132">OUTPUTS</span></span>

### <span data-ttu-id="7f6a5-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f6a5-133">System.Boolean</span></span>



## <span data-ttu-id="7f6a5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f6a5-134">NOTES</span></span>

<span data-ttu-id="7f6a5-135">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f6a5-136">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7f6a5-137">INPUTobject <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="7f6a5-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="7f6a5-138">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="7f6a5-139">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="7f6a5-140">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="7f6a5-141">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="7f6a5-142">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="7f6a5-143">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="7f6a5-144">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7f6a5-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f6a5-145">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="7f6a5-146">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="7f6a5-147">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="7f6a5-148">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="7f6a5-149">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="7f6a5-150">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="7f6a5-151">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="7f6a5-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="7f6a5-153">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="7f6a5-154">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="7f6a5-155">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="7f6a5-156">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="7f6a5-157">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7f6a5-158">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7f6a5-159">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="7f6a5-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="7f6a5-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f6a5-160">RELATED LINKS</span></span>

