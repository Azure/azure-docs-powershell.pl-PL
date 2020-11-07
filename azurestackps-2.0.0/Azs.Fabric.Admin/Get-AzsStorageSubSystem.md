---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891753"
---
# <span data-ttu-id="c486f-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c486f-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="c486f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c486f-102">SYNOPSIS</span></span>
<span data-ttu-id="c486f-103">Zwracanie wymaganego podsystemu magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c486f-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="c486f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c486f-104">SYNTAX</span></span>

### <span data-ttu-id="c486f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c486f-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="c486f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c486f-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="c486f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c486f-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="c486f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c486f-108">DESCRIPTION</span></span>
<span data-ttu-id="c486f-109">Zwracanie wymaganego podsystemu magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c486f-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="c486f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c486f-110">EXAMPLES</span></span>

### <span data-ttu-id="c486f-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="c486f-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="c486f-112">Pobierz wszystkie Podsystemy magazynowania z jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c486f-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="c486f-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="c486f-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="c486f-114">Uzyskaj Podsystem pamięci masowej pod nazwą jednostki skali i nazwy.</span><span class="sxs-lookup"><span data-stu-id="c486f-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="c486f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c486f-115">PARAMETERS</span></span>

### <span data-ttu-id="c486f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c486f-116">-DefaultProfile</span></span>
<span data-ttu-id="c486f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c486f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c486f-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="c486f-118">-Filter</span></span>
<span data-ttu-id="c486f-119">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c486f-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="c486f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c486f-120">-InputObject</span></span>
<span data-ttu-id="c486f-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c486f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c486f-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c486f-122">-Location</span></span>
<span data-ttu-id="c486f-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="c486f-123">Location of the resource.</span></span>

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

### <span data-ttu-id="c486f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c486f-124">-Name</span></span>
<span data-ttu-id="c486f-125">Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="c486f-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="c486f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c486f-126">-PassThru</span></span>
<span data-ttu-id="c486f-127">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="c486f-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c486f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c486f-128">-ResourceGroupName</span></span>
<span data-ttu-id="c486f-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c486f-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="c486f-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c486f-130">-ScaleUnit</span></span>
<span data-ttu-id="c486f-131">Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c486f-131">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c486f-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="c486f-132">-Skip</span></span>
<span data-ttu-id="c486f-133">Parametr pomijania OData.</span><span class="sxs-lookup"><span data-stu-id="c486f-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="c486f-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c486f-134">-SubscriptionId</span></span>
<span data-ttu-id="c486f-135">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c486f-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c486f-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c486f-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c486f-137">-Początek</span><span class="sxs-lookup"><span data-stu-id="c486f-137">-Top</span></span>
<span data-ttu-id="c486f-138">Parametr najwyższy OData.</span><span class="sxs-lookup"><span data-stu-id="c486f-138">OData top parameter.</span></span>

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

### <span data-ttu-id="c486f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c486f-139">CommonParameters</span></span>
<span data-ttu-id="c486f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c486f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c486f-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c486f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c486f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c486f-142">INPUTS</span></span>

### <span data-ttu-id="c486f-143">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c486f-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="c486f-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c486f-144">OUTPUTS</span></span>

### <span data-ttu-id="c486f-145">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20181001. IStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c486f-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="c486f-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c486f-146">NOTES</span></span>

<span data-ttu-id="c486f-147">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c486f-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c486f-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c486f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c486f-149">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="c486f-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c486f-150">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="c486f-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="c486f-151">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="c486f-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="c486f-152">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="c486f-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="c486f-153">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="c486f-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="c486f-154">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="c486f-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="c486f-155">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="c486f-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="c486f-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c486f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c486f-157">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="c486f-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="c486f-158">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="c486f-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="c486f-159">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="c486f-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c486f-160">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="c486f-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="c486f-161">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="c486f-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="c486f-162">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="c486f-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="c486f-163">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="c486f-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="c486f-164">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c486f-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c486f-165">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c486f-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="c486f-166">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c486f-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="c486f-167">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c486f-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="c486f-168">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="c486f-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="c486f-169">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c486f-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c486f-170">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c486f-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c486f-171">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="c486f-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="c486f-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c486f-172">RELATED LINKS</span></span>

