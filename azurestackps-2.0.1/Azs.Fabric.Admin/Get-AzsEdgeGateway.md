---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054322"
---
# <span data-ttu-id="34c06-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="34c06-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="34c06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34c06-102">SYNOPSIS</span></span>
<span data-ttu-id="34c06-103">Zwraca żądaną bramę graniczną.</span><span class="sxs-lookup"><span data-stu-id="34c06-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="34c06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34c06-104">SYNTAX</span></span>

### <span data-ttu-id="34c06-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="34c06-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="34c06-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="34c06-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="34c06-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="34c06-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="34c06-108">Opis</span><span class="sxs-lookup"><span data-stu-id="34c06-108">DESCRIPTION</span></span>
<span data-ttu-id="34c06-109">Zwraca żądaną bramę graniczną.</span><span class="sxs-lookup"><span data-stu-id="34c06-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="34c06-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34c06-110">EXAMPLES</span></span>

### <span data-ttu-id="34c06-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="34c06-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="34c06-112">Zwraca listę wszystkich bram do brzegu w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="34c06-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="34c06-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34c06-113">PARAMETERS</span></span>

### <span data-ttu-id="34c06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c06-114">-DefaultProfile</span></span>
<span data-ttu-id="34c06-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34c06-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34c06-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="34c06-116">-Filter</span></span>
<span data-ttu-id="34c06-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="34c06-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="34c06-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34c06-118">-InputObject</span></span>
<span data-ttu-id="34c06-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="34c06-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="34c06-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="34c06-120">-Location</span></span>
<span data-ttu-id="34c06-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="34c06-121">Location of the resource.</span></span>

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

### <span data-ttu-id="34c06-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34c06-122">-Name</span></span>
<span data-ttu-id="34c06-123">Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="34c06-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="34c06-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34c06-124">-PassThru</span></span>
<span data-ttu-id="34c06-125">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="34c06-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="34c06-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c06-126">-ResourceGroupName</span></span>
<span data-ttu-id="34c06-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34c06-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="34c06-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="34c06-128">-SubscriptionId</span></span>
<span data-ttu-id="34c06-129">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="34c06-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="34c06-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="34c06-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="34c06-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c06-131">CommonParameters</span></span>
<span data-ttu-id="34c06-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c06-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c06-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34c06-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c06-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34c06-134">INPUTS</span></span>

### <span data-ttu-id="34c06-135">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="34c06-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="34c06-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34c06-136">OUTPUTS</span></span>

### <span data-ttu-id="34c06-137">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="34c06-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="34c06-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34c06-138">NOTES</span></span>

<span data-ttu-id="34c06-139">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="34c06-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34c06-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34c06-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="34c06-141">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="34c06-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34c06-142">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="34c06-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="34c06-143">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="34c06-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="34c06-144">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="34c06-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="34c06-145">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="34c06-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="34c06-146">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="34c06-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="34c06-147">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="34c06-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="34c06-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="34c06-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34c06-149">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="34c06-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="34c06-150">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="34c06-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="34c06-151">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="34c06-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="34c06-152">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="34c06-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="34c06-153">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="34c06-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="34c06-154">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="34c06-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="34c06-155">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="34c06-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="34c06-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34c06-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="34c06-157">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="34c06-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="34c06-158">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="34c06-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="34c06-159">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="34c06-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="34c06-160">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="34c06-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="34c06-161">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="34c06-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="34c06-162">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="34c06-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="34c06-163">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="34c06-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="34c06-164">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="34c06-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="34c06-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34c06-165">RELATED LINKS</span></span>

