---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsvolume
schema: 2.0.0
ms.openlocfilehash: a423470454e77c58a8b611a47c737e5d86bfd1cf
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061619"
---
# <span data-ttu-id="84800-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="84800-101">Get-AzsVolume</span></span>

## <span data-ttu-id="84800-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84800-102">SYNOPSIS</span></span>
<span data-ttu-id="84800-103">Zwraca żądaną ilość miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="84800-103">Return the requested a storage volume.</span></span>

## <span data-ttu-id="84800-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84800-104">SYNTAX</span></span>

### <span data-ttu-id="84800-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="84800-105">List (Default)</span></span>
```
Get-AzsVolume -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="84800-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="84800-106">Get</span></span>
```
Get-AzsVolume -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="84800-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="84800-107">GetViaIdentity</span></span>
```
Get-AzsVolume -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="84800-108">Opis</span><span class="sxs-lookup"><span data-stu-id="84800-108">DESCRIPTION</span></span>
<span data-ttu-id="84800-109">Zwraca żądaną ilość miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="84800-109">Return the requested a storage volume.</span></span>

## <span data-ttu-id="84800-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84800-110">EXAMPLES</span></span>

### <span data-ttu-id="84800-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="84800-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="84800-112">Zapoznaj się z listą wszystkich woluminów magazynu w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="84800-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="84800-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="84800-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name ee594cf5-cf54-46b4-a641-139553307195
```

<span data-ttu-id="84800-114">Pobierz wolumin magazynu według nazwy w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="84800-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="84800-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84800-115">PARAMETERS</span></span>

### <span data-ttu-id="84800-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84800-116">-DefaultProfile</span></span>
<span data-ttu-id="84800-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84800-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84800-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="84800-118">-Filter</span></span>
<span data-ttu-id="84800-119">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="84800-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="84800-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84800-120">-InputObject</span></span>
<span data-ttu-id="84800-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="84800-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="84800-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="84800-122">-Location</span></span>
<span data-ttu-id="84800-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="84800-123">Location of the resource.</span></span>

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

### <span data-ttu-id="84800-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84800-124">-Name</span></span>
<span data-ttu-id="84800-125">Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="84800-125">Name of the storage volume.</span></span>

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

### <span data-ttu-id="84800-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84800-126">-PassThru</span></span>
<span data-ttu-id="84800-127">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="84800-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="84800-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84800-128">-ResourceGroupName</span></span>
<span data-ttu-id="84800-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84800-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="84800-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="84800-130">-ScaleUnit</span></span>
<span data-ttu-id="84800-131">Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="84800-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="84800-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="84800-132">-Skip</span></span>
<span data-ttu-id="84800-133">Parametr pomijania OData.</span><span class="sxs-lookup"><span data-stu-id="84800-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="84800-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="84800-134">-StorageSubSystem</span></span>
<span data-ttu-id="84800-135">Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="84800-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="84800-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="84800-136">-SubscriptionId</span></span>
<span data-ttu-id="84800-137">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84800-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="84800-138">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="84800-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="84800-139">-Początek</span><span class="sxs-lookup"><span data-stu-id="84800-139">-Top</span></span>
<span data-ttu-id="84800-140">Parametr najwyższy OData.</span><span class="sxs-lookup"><span data-stu-id="84800-140">OData top parameter.</span></span>

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

### <span data-ttu-id="84800-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84800-141">CommonParameters</span></span>
<span data-ttu-id="84800-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84800-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84800-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84800-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84800-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84800-144">INPUTS</span></span>

### <span data-ttu-id="84800-145">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="84800-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="84800-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84800-146">OUTPUTS</span></span>

### <span data-ttu-id="84800-147">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20190501. IVolume</span><span class="sxs-lookup"><span data-stu-id="84800-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IVolume</span></span>



## <span data-ttu-id="84800-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84800-148">NOTES</span></span>

<span data-ttu-id="84800-149">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="84800-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84800-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="84800-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="84800-151">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="84800-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="84800-152">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="84800-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="84800-153">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="84800-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="84800-154">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="84800-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="84800-155">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="84800-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="84800-156">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="84800-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="84800-157">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="84800-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="84800-158">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="84800-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="84800-159">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="84800-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="84800-160">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="84800-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="84800-161">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="84800-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="84800-162">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="84800-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="84800-163">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="84800-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="84800-164">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="84800-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="84800-165">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="84800-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="84800-166">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84800-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="84800-167">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="84800-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="84800-168">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="84800-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="84800-169">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="84800-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="84800-170">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="84800-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="84800-171">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84800-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="84800-172">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="84800-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="84800-173">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="84800-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="84800-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84800-174">RELATED LINKS</span></span>

