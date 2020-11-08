---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsmacaddresspool
schema: 2.0.0
ms.openlocfilehash: f7a2ae035ff0985c84dc78a18131c46239bafd1f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054281"
---
# <span data-ttu-id="2e891-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="2e891-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="2e891-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e891-102">SYNOPSIS</span></span>
<span data-ttu-id="2e891-103">Zwraca żądaną pulę adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="2e891-103">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="2e891-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e891-104">SYNTAX</span></span>

### <span data-ttu-id="2e891-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2e891-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2e891-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2e891-106">Get</span></span>
```
Get-AzsMacAddressPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2e891-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2e891-107">GetViaIdentity</span></span>
```
Get-AzsMacAddressPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="2e891-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2e891-108">DESCRIPTION</span></span>
<span data-ttu-id="2e891-109">Zwraca żądaną pulę adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="2e891-109">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="2e891-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e891-110">EXAMPLES</span></span>

### <span data-ttu-id="2e891-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="2e891-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool

A list of all MAC address pools at a location.
```

<span data-ttu-id="2e891-112">Zwraca listę wszystkich pul adresów MAC w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2e891-112">Returns a list of all MAC address pools at a location.</span></span>

### <span data-ttu-id="2e891-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="2e891-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"

A specific MAC address pool at a location based on name.
```

<span data-ttu-id="2e891-114">Uzyskaj określoną pulę adresów MAC w lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="2e891-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="2e891-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e891-115">PARAMETERS</span></span>

### <span data-ttu-id="2e891-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e891-116">-DefaultProfile</span></span>
<span data-ttu-id="2e891-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e891-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e891-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="2e891-118">-Filter</span></span>
<span data-ttu-id="2e891-119">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="2e891-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="2e891-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e891-120">-InputObject</span></span>
<span data-ttu-id="2e891-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2e891-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2e891-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2e891-122">-Location</span></span>
<span data-ttu-id="2e891-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="2e891-123">Location of the resource.</span></span>

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

### <span data-ttu-id="2e891-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e891-124">-Name</span></span>
<span data-ttu-id="2e891-125">Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="2e891-125">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="2e891-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e891-126">-PassThru</span></span>
<span data-ttu-id="2e891-127">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="2e891-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2e891-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e891-128">-ResourceGroupName</span></span>
<span data-ttu-id="2e891-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e891-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="2e891-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2e891-130">-SubscriptionId</span></span>
<span data-ttu-id="2e891-131">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2e891-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2e891-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2e891-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2e891-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e891-133">CommonParameters</span></span>
<span data-ttu-id="2e891-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e891-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e891-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e891-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e891-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e891-136">INPUTS</span></span>

### <span data-ttu-id="2e891-137">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2e891-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="2e891-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e891-138">OUTPUTS</span></span>

### <span data-ttu-id="2e891-139">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="2e891-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IMacAddressPool</span></span>



## <span data-ttu-id="2e891-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e891-140">NOTES</span></span>

<span data-ttu-id="2e891-141">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2e891-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e891-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e891-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2e891-143">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2e891-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e891-144">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e891-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="2e891-145">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="2e891-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="2e891-146">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="2e891-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="2e891-147">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="2e891-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="2e891-148">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="2e891-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="2e891-149">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="2e891-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="2e891-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2e891-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e891-151">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="2e891-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="2e891-152">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="2e891-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="2e891-153">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="2e891-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2e891-154">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="2e891-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="2e891-155">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="2e891-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="2e891-156">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="2e891-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="2e891-157">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="2e891-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="2e891-158">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e891-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2e891-159">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="2e891-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="2e891-160">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="2e891-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="2e891-161">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2e891-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="2e891-162">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e891-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="2e891-163">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="2e891-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="2e891-164">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2e891-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2e891-165">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2e891-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2e891-166">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e891-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="2e891-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e891-167">RELATED LINKS</span></span>

