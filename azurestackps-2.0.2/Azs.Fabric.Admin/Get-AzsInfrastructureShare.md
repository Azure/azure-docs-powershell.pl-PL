---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055639"
---
# <span data-ttu-id="ac44e-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="ac44e-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="ac44e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac44e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac44e-103">Zwraca żądany udział pliku sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="ac44e-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="ac44e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac44e-104">SYNTAX</span></span>

### <span data-ttu-id="ac44e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ac44e-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="ac44e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ac44e-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ac44e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ac44e-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="ac44e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ac44e-108">DESCRIPTION</span></span>
<span data-ttu-id="ac44e-109">Zwraca żądany udział pliku sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="ac44e-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="ac44e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac44e-110">EXAMPLES</span></span>

### <span data-ttu-id="ac44e-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="ac44e-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="ac44e-112">Zwraca listę wszystkich udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="ac44e-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="ac44e-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="ac44e-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="ac44e-114">Zwraca udział pliku na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="ac44e-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="ac44e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac44e-115">PARAMETERS</span></span>

### <span data-ttu-id="ac44e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac44e-116">-DefaultProfile</span></span>
<span data-ttu-id="ac44e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac44e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac44e-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="ac44e-118">-Filter</span></span>
<span data-ttu-id="ac44e-119">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="ac44e-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="ac44e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ac44e-120">-InputObject</span></span>
<span data-ttu-id="ac44e-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ac44e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac44e-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ac44e-122">-Location</span></span>
<span data-ttu-id="ac44e-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ac44e-123">Location of the resource.</span></span>

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

### <span data-ttu-id="ac44e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ac44e-124">-Name</span></span>
<span data-ttu-id="ac44e-125">Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="ac44e-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="ac44e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac44e-126">-PassThru</span></span>
<span data-ttu-id="ac44e-127">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ac44e-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ac44e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac44e-128">-ResourceGroupName</span></span>
<span data-ttu-id="ac44e-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ac44e-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="ac44e-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="ac44e-130">-Skip</span></span>
<span data-ttu-id="ac44e-131">Parametr pomijania OData.</span><span class="sxs-lookup"><span data-stu-id="ac44e-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="ac44e-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ac44e-132">-SubscriptionId</span></span>
<span data-ttu-id="ac44e-133">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ac44e-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ac44e-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ac44e-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ac44e-135">-Początek</span><span class="sxs-lookup"><span data-stu-id="ac44e-135">-Top</span></span>
<span data-ttu-id="ac44e-136">Parametr najwyższy OData.</span><span class="sxs-lookup"><span data-stu-id="ac44e-136">OData top parameter.</span></span>

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

### <span data-ttu-id="ac44e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac44e-137">CommonParameters</span></span>
<span data-ttu-id="ac44e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac44e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac44e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac44e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac44e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac44e-140">INPUTS</span></span>

### <span data-ttu-id="ac44e-141">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ac44e-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="ac44e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac44e-142">OUTPUTS</span></span>

### <span data-ttu-id="ac44e-143">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IFileShare</span><span class="sxs-lookup"><span data-stu-id="ac44e-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="ac44e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac44e-144">NOTES</span></span>

<span data-ttu-id="ac44e-145">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ac44e-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac44e-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac44e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ac44e-147">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ac44e-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac44e-148">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="ac44e-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="ac44e-149">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="ac44e-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="ac44e-150">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="ac44e-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="ac44e-151">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="ac44e-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="ac44e-152">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="ac44e-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="ac44e-153">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ac44e-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="ac44e-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ac44e-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac44e-155">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ac44e-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="ac44e-156">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ac44e-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="ac44e-157">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ac44e-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ac44e-158">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="ac44e-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="ac44e-159">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="ac44e-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="ac44e-160">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="ac44e-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="ac44e-161">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="ac44e-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="ac44e-162">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ac44e-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ac44e-163">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="ac44e-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="ac44e-164">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="ac44e-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="ac44e-165">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ac44e-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="ac44e-166">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="ac44e-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="ac44e-167">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ac44e-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ac44e-168">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ac44e-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ac44e-169">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="ac44e-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="ac44e-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac44e-170">RELATED LINKS</span></span>

