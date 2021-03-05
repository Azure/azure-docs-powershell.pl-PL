---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 516bc63d7866ffd8a3c16fd224a49697c0cc972f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001802"
---
# <span data-ttu-id="7e0f6-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="7e0f6-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="7e0f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0f6-103">Pobiera wystąpienie roli z usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="7e0f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7e0f6-104">SYNTAX</span></span>

### <span data-ttu-id="7e0f6-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7e0f6-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7e0f6-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7e0f6-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7e0f6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7e0f6-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7e0f6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7e0f6-108">DESCRIPTION</span></span>
<span data-ttu-id="7e0f6-109">Pobiera wystąpienie roli z usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="7e0f6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7e0f6-110">EXAMPLES</span></span>

### <span data-ttu-id="7e0f6-111">Przykład 1. Uzyskiwanie wszystkich wystąpień ról</span><span class="sxs-lookup"><span data-stu-id="7e0f6-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="7e0f6-112">To polecenie pobiera właściwości wszystkich wystąpień ról usługi w chmurze o nazwie ContosoCS, które należą do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="7e0f6-113">Przykład 2. Uzyskiwanie właściwości pojedynczego wystąpienia roli</span><span class="sxs-lookup"><span data-stu-id="7e0f6-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="7e0f6-114">To polecenie pobiera właściwości wystąpienia roli o nazwie ContosoFrontEnd_IN_0 o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="7e0f6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e0f6-115">PARAMETERS</span></span>

### <span data-ttu-id="7e0f6-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="7e0f6-116">-CloudServiceName</span></span>
<span data-ttu-id="7e0f6-117">.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-117">.</span></span>

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

### <span data-ttu-id="7e0f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0f6-118">-DefaultProfile</span></span>
<span data-ttu-id="7e0f6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e0f6-120">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="7e0f6-120">-Expand</span></span>
<span data-ttu-id="7e0f6-121">Wyrażenie rozwijania, które ma być stosowane do operacji.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-121">The expand expression to apply to the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e0f6-122">-InputObject</span></span>
<span data-ttu-id="7e0f6-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e0f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e0f6-125">.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-125">.</span></span>

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

### <span data-ttu-id="7e0f6-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="7e0f6-126">-RoleInstanceName</span></span>
<span data-ttu-id="7e0f6-127">Nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-127">Name of the role instance.</span></span>

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

### <span data-ttu-id="7e0f6-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e0f6-128">-SubscriptionId</span></span>
<span data-ttu-id="7e0f6-129">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7e0f6-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7e0f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0f6-131">CommonParameters</span></span>
<span data-ttu-id="7e0f6-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0f6-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e0f6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0f6-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e0f6-134">INPUTS</span></span>

### <span data-ttu-id="7e0f6-135">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="7e0f6-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="7e0f6-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e0f6-136">OUTPUTS</span></span>

### <span data-ttu-id="7e0f6-137">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.IRoleInstance</span><span class="sxs-lookup"><span data-stu-id="7e0f6-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="7e0f6-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7e0f6-138">NOTES</span></span>

<span data-ttu-id="7e0f6-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7e0f6-139">ALIASES</span></span>

<span data-ttu-id="7e0f6-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e0f6-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7e0f6-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7e0f6-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7e0f6-143">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="7e0f6-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7e0f6-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="7e0f6-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="7e0f6-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7e0f6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7e0f6-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="7e0f6-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="7e0f6-147">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="7e0f6-148">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="7e0f6-149">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7e0f6-150">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7e0f6-151">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="7e0f6-152">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="7e0f6-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e0f6-153">RELATED LINKS</span></span>

