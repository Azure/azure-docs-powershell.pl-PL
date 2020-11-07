---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891782"
---
# <span data-ttu-id="6e327-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="6e327-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="6e327-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e327-102">SYNOPSIS</span></span>


## <span data-ttu-id="6e327-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e327-103">SYNTAX</span></span>

### <span data-ttu-id="6e327-104">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6e327-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="6e327-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="6e327-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="6e327-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6e327-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="6e327-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6e327-107">DESCRIPTION</span></span>


## <span data-ttu-id="6e327-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e327-108">EXAMPLES</span></span>

### <span data-ttu-id="6e327-109">Przykład 1. Aby uzyskać listę wszystkich pul granicznych bram.</span><span class="sxs-lookup"><span data-stu-id="6e327-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="6e327-110">Wyświetlanie listy wszystkich pul z systemem Edge.</span><span class="sxs-lookup"><span data-stu-id="6e327-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="6e327-111">Przykład 2: uzyskiwanie określonej puli bram brzegowych.</span><span class="sxs-lookup"><span data-stu-id="6e327-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="6e327-112">Pobierz określoną pulę bram brzegowych.</span><span class="sxs-lookup"><span data-stu-id="6e327-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="6e327-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e327-113">PARAMETERS</span></span>

### <span data-ttu-id="6e327-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e327-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="6e327-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="6e327-115">-Filter</span></span>


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

### <span data-ttu-id="6e327-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e327-116">-InputObject</span></span>
<span data-ttu-id="6e327-117">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="6e327-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6e327-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6e327-118">-Location</span></span>


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

### <span data-ttu-id="6e327-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e327-119">-Name</span></span>


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

### <span data-ttu-id="6e327-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e327-120">-PassThru</span></span>


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

### <span data-ttu-id="6e327-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e327-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="6e327-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6e327-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="6e327-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e327-123">CommonParameters</span></span>
<span data-ttu-id="6e327-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e327-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e327-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e327-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e327-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e327-126">INPUTS</span></span>

### <span data-ttu-id="6e327-127">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6e327-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="6e327-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e327-128">OUTPUTS</span></span>

### <span data-ttu-id="6e327-129">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="6e327-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="6e327-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e327-130">NOTES</span></span>

<span data-ttu-id="6e327-131">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6e327-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e327-132">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6e327-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6e327-133">INPUTobject <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="6e327-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="6e327-134">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="6e327-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="6e327-135">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="6e327-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="6e327-136">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="6e327-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="6e327-137">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="6e327-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="6e327-138">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="6e327-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="6e327-139">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="6e327-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="6e327-140">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6e327-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e327-141">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="6e327-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="6e327-142">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="6e327-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="6e327-143">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="6e327-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6e327-144">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="6e327-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="6e327-145">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="6e327-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="6e327-146">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="6e327-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="6e327-147">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="6e327-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="6e327-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e327-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="6e327-149">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="6e327-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="6e327-150">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="6e327-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="6e327-151">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="6e327-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="6e327-152">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="6e327-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="6e327-153">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6e327-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6e327-154">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6e327-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6e327-155">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="6e327-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="6e327-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e327-156">RELATED LINKS</span></span>

