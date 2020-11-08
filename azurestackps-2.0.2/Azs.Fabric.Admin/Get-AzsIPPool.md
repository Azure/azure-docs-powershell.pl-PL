---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055935"
---
# <span data-ttu-id="b3f98-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="b3f98-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="b3f98-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3f98-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f98-103">Zwraca żądaną pulę adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b3f98-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="b3f98-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3f98-104">SYNTAX</span></span>

### <span data-ttu-id="b3f98-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b3f98-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b3f98-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b3f98-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b3f98-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3f98-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="b3f98-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b3f98-108">DESCRIPTION</span></span>
<span data-ttu-id="b3f98-109">Zwraca żądaną pulę adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b3f98-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="b3f98-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3f98-110">EXAMPLES</span></span>

### <span data-ttu-id="b3f98-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="b3f98-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="b3f98-112">Pobierz wszystkie pule adresów IP infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="b3f98-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="b3f98-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="b3f98-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="b3f98-114">Uzyskiwanie puli adresów IP infrastruktury na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="b3f98-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="b3f98-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3f98-115">PARAMETERS</span></span>

### <span data-ttu-id="b3f98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f98-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="b3f98-117">-Filter</span><span class="sxs-lookup"><span data-stu-id="b3f98-117">-Filter</span></span>
<span data-ttu-id="b3f98-118">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="b3f98-118">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3f98-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3f98-119">-InputObject</span></span>
<span data-ttu-id="b3f98-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b3f98-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b3f98-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b3f98-121">-Location</span></span>
<span data-ttu-id="b3f98-122">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b3f98-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3f98-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3f98-123">-Name</span></span>
<span data-ttu-id="b3f98-124">Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b3f98-124">IP pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3f98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3f98-125">-PassThru</span></span>
<span data-ttu-id="b3f98-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="b3f98-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3f98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f98-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3f98-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3f98-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3f98-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b3f98-129">-SubscriptionId</span></span>
<span data-ttu-id="b3f98-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f98-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b3f98-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b3f98-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3f98-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f98-132">CommonParameters</span></span>
<span data-ttu-id="b3f98-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3f98-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f98-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3f98-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f98-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3f98-135">INPUTS</span></span>

### <span data-ttu-id="b3f98-136">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b3f98-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="b3f98-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3f98-137">OUTPUTS</span></span>

### <span data-ttu-id="b3f98-138">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="b3f98-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="b3f98-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3f98-139">NOTES</span></span>

<span data-ttu-id="b3f98-140">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b3f98-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3f98-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3f98-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b3f98-142">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b3f98-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3f98-143">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3f98-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="b3f98-144">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="b3f98-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="b3f98-145">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="b3f98-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="b3f98-146">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="b3f98-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="b3f98-147">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="b3f98-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="b3f98-148">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b3f98-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="b3f98-149">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b3f98-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3f98-150">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="b3f98-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="b3f98-151">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="b3f98-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="b3f98-152">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b3f98-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b3f98-153">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="b3f98-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="b3f98-154">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="b3f98-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="b3f98-155">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="b3f98-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="b3f98-156">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="b3f98-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="b3f98-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3f98-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b3f98-158">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="b3f98-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="b3f98-159">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="b3f98-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="b3f98-160">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b3f98-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="b3f98-161">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3f98-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="b3f98-162">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="b3f98-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="b3f98-163">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f98-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b3f98-164">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b3f98-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b3f98-165">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3f98-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="b3f98-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3f98-166">RELATED LINKS</span></span>

