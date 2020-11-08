---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055737"
---
# <span data-ttu-id="8d42a-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="8d42a-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="8d42a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d42a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d42a-103">Zwraca żądaną lokalizację sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="8d42a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d42a-104">SYNTAX</span></span>

### <span data-ttu-id="8d42a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8d42a-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d42a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8d42a-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8d42a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d42a-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="8d42a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8d42a-108">DESCRIPTION</span></span>
<span data-ttu-id="8d42a-109">Zwraca żądaną lokalizację sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="8d42a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d42a-110">EXAMPLES</span></span>

### <span data-ttu-id="8d42a-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="8d42a-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="8d42a-112">Wyświetlanie listy wszystkich lokalizacji sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="8d42a-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="8d42a-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="8d42a-114">Uzyskaj lokalizację na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="8d42a-114">Get a location based on the name.</span></span>

## <span data-ttu-id="8d42a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d42a-115">PARAMETERS</span></span>

### <span data-ttu-id="8d42a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d42a-116">-DefaultProfile</span></span>
<span data-ttu-id="8d42a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d42a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d42a-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="8d42a-118">-FabricLocation</span></span>
<span data-ttu-id="8d42a-119">Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-119">Fabric location.</span></span>

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

### <span data-ttu-id="8d42a-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="8d42a-120">-Filter</span></span>
<span data-ttu-id="8d42a-121">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="8d42a-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="8d42a-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d42a-122">-InputObject</span></span>
<span data-ttu-id="8d42a-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8d42a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d42a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d42a-124">-PassThru</span></span>
<span data-ttu-id="8d42a-125">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="8d42a-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d42a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d42a-126">-ResourceGroupName</span></span>
<span data-ttu-id="8d42a-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d42a-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="8d42a-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8d42a-128">-SubscriptionId</span></span>
<span data-ttu-id="8d42a-129">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d42a-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d42a-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8d42a-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8d42a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d42a-131">CommonParameters</span></span>
<span data-ttu-id="8d42a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d42a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d42a-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d42a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d42a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d42a-134">INPUTS</span></span>

### <span data-ttu-id="8d42a-135">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8d42a-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="8d42a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d42a-136">OUTPUTS</span></span>

### <span data-ttu-id="8d42a-137">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IFabricLocation</span><span class="sxs-lookup"><span data-stu-id="8d42a-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="8d42a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d42a-138">NOTES</span></span>

<span data-ttu-id="8d42a-139">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8d42a-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d42a-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d42a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8d42a-141">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8d42a-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d42a-142">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="8d42a-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="8d42a-143">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="8d42a-144">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="8d42a-145">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="8d42a-146">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="8d42a-147">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8d42a-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="8d42a-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8d42a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d42a-149">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="8d42a-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="8d42a-150">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="8d42a-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="8d42a-151">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="8d42a-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8d42a-152">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="8d42a-153">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="8d42a-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="8d42a-154">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="8d42a-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="8d42a-155">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="8d42a-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="8d42a-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d42a-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8d42a-157">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="8d42a-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="8d42a-158">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="8d42a-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="8d42a-159">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8d42a-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="8d42a-160">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="8d42a-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="8d42a-161">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d42a-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8d42a-162">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8d42a-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8d42a-163">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="8d42a-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="8d42a-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d42a-164">RELATED LINKS</span></span>

