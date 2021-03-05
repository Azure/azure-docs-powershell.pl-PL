---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
ms.openlocfilehash: 31683a7f8d0bea3a2e21588b0451275c74d52e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012705"
---
# <span data-ttu-id="4a159-101">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="4a159-101">Get-AzCloudService</span></span>

## <span data-ttu-id="4a159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a159-102">SYNOPSIS</span></span>
<span data-ttu-id="4a159-103">Wyświetlanie informacji o usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="4a159-103">Display information about a cloud service.</span></span>

## <span data-ttu-id="4a159-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4a159-104">SYNTAX</span></span>

### <span data-ttu-id="4a159-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="4a159-105">List (Default)</span></span>
```
Get-AzCloudService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a159-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="4a159-106">Get</span></span>
```
Get-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a159-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a159-107">GetViaIdentity</span></span>
```
Get-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a159-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="4a159-108">List1</span></span>
```
Get-AzCloudService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a159-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="4a159-109">DESCRIPTION</span></span>
<span data-ttu-id="4a159-110">Wyświetlanie informacji o usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="4a159-110">Display information about a cloud service.</span></span>

## <span data-ttu-id="4a159-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4a159-111">EXAMPLES</span></span>

### <span data-ttu-id="4a159-112">Przykład 1. Uzyskiwanie całej usługi w chmurze w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="4a159-112">Example 1: Get all cloud service under a resource group</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded
ContosOrg         ContosoCSTest     eastus2euap Failed
```

<span data-ttu-id="4a159-113">To polecenie pobiera wszystkie usługi w chmurze w grupie zasobów o nazwie ContosOrg</span><span class="sxs-lookup"><span data-stu-id="4a159-113">This command gets all cloud services in resource group named ContosOrg</span></span>

### <span data-ttu-id="4a159-114">Przykład 2. Uzyskiwanie usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="4a159-114">Example 2: Get cloud service</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded

PS C:\> $cloudService = Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
PS C:\> $cloudService | Format-List
ResourceGroupName : ContosOrg
Configuration     : xxxxxxxx
ConfigurationUrl  :
ExtensionProfile  : xxxxxxxx
Id                : xxxxxxxx
Location          : East US
Name              : ContosoCS
NetworkProfile    : xxxxxxxx
OSProfile         : xxxxxxxx
PackageUrl        : xxxxxxxx
ProvisioningState : Succeeded
RoleProfile       : xxxxxxxx
StartCloudService :
Tag               : {
                      "Owner": "Contos"
                    }
Type              : Microsoft.Compute/cloudServices
UniqueId          : xxxxxxxx
UpgradeMode       : Auto

```

<span data-ttu-id="4a159-115">To polecenie pobiera usługę w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="4a159-115">This command gets cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="4a159-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a159-116">PARAMETERS</span></span>

### <span data-ttu-id="4a159-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a159-117">-DefaultProfile</span></span>
<span data-ttu-id="4a159-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a159-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a159-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a159-119">-InputObject</span></span>
<span data-ttu-id="4a159-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4a159-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a159-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4a159-121">-Name</span></span>
<span data-ttu-id="4a159-122">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="4a159-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a159-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a159-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a159-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a159-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a159-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a159-125">-SubscriptionId</span></span>
<span data-ttu-id="4a159-126">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a159-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4a159-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="4a159-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a159-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a159-128">CommonParameters</span></span>
<span data-ttu-id="4a159-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a159-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a159-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a159-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a159-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a159-131">INPUTS</span></span>

### <span data-ttu-id="4a159-132">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="4a159-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="4a159-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a159-133">OUTPUTS</span></span>

### <span data-ttu-id="4a159-134">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.iCloudService</span><span class="sxs-lookup"><span data-stu-id="4a159-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="4a159-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4a159-135">NOTES</span></span>

<span data-ttu-id="4a159-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4a159-136">ALIASES</span></span>

<span data-ttu-id="4a159-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a159-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a159-138">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4a159-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a159-139">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a159-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a159-140">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="4a159-140">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a159-141">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4a159-141">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="4a159-142">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4a159-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a159-143">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4a159-143">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="4a159-144">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="4a159-144">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="4a159-145">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="4a159-145">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="4a159-146">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a159-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4a159-147">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="4a159-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4a159-148">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="4a159-148">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="4a159-149">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="4a159-149">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="4a159-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a159-150">RELATED LINKS</span></span>

