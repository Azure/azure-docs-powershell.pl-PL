---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: b5eb59c1f2ad631e8cbb9fdffbf65bee00425d43
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054193"
---
# <span data-ttu-id="bc257-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="bc257-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="bc257-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc257-102">SYNOPSIS</span></span>
<span data-ttu-id="bc257-103">Zwracanie żądanej instancji roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="bc257-103">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="bc257-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc257-104">SYNTAX</span></span>

### <span data-ttu-id="bc257-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="bc257-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="bc257-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="bc257-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="bc257-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc257-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="bc257-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bc257-108">DESCRIPTION</span></span>
<span data-ttu-id="bc257-109">Zwracanie żądanej instancji roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="bc257-109">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="bc257-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc257-110">EXAMPLES</span></span>

### <span data-ttu-id="bc257-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="bc257-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance

A list of all infrastructure role instances.
```

<span data-ttu-id="bc257-112">Zwraca listę wszystkich wystąpień ról infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="bc257-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="bc257-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="bc257-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

A single infrastructure role instance based on name.
```

<span data-ttu-id="bc257-114">Zwracanie pojedynczego wystąpienia roli infrastruktury na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="bc257-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="bc257-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc257-115">PARAMETERS</span></span>

### <span data-ttu-id="bc257-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc257-116">-DefaultProfile</span></span>
<span data-ttu-id="bc257-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc257-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc257-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="bc257-118">-Filter</span></span>
<span data-ttu-id="bc257-119">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="bc257-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="bc257-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc257-120">-InputObject</span></span>
<span data-ttu-id="bc257-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="bc257-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc257-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bc257-122">-Location</span></span>
<span data-ttu-id="bc257-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="bc257-123">Location of the resource.</span></span>

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

### <span data-ttu-id="bc257-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc257-124">-Name</span></span>
<span data-ttu-id="bc257-125">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="bc257-125">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="bc257-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc257-126">-PassThru</span></span>
<span data-ttu-id="bc257-127">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="bc257-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bc257-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc257-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc257-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc257-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="bc257-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bc257-130">-SubscriptionId</span></span>
<span data-ttu-id="bc257-131">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc257-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bc257-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="bc257-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bc257-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc257-133">CommonParameters</span></span>
<span data-ttu-id="bc257-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc257-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc257-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc257-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc257-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc257-136">INPUTS</span></span>

### <span data-ttu-id="bc257-137">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="bc257-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="bc257-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc257-138">OUTPUTS</span></span>

### <span data-ttu-id="bc257-139">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IInfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="bc257-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IInfraRoleInstance</span></span>



## <span data-ttu-id="bc257-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc257-140">NOTES</span></span>

<span data-ttu-id="bc257-141">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bc257-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc257-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc257-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bc257-143">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="bc257-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc257-144">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="bc257-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="bc257-145">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="bc257-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="bc257-146">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="bc257-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="bc257-147">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="bc257-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="bc257-148">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="bc257-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="bc257-149">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="bc257-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="bc257-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bc257-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc257-151">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="bc257-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="bc257-152">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="bc257-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="bc257-153">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="bc257-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="bc257-154">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="bc257-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="bc257-155">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="bc257-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="bc257-156">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="bc257-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="bc257-157">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="bc257-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="bc257-158">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc257-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="bc257-159">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="bc257-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="bc257-160">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="bc257-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="bc257-161">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="bc257-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="bc257-162">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="bc257-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="bc257-163">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="bc257-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="bc257-164">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc257-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bc257-165">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="bc257-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="bc257-166">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="bc257-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="bc257-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc257-167">RELATED LINKS</span></span>

