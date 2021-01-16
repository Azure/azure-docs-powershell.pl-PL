---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382706"
---
# <span data-ttu-id="74bb4-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="74bb4-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="74bb4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="74bb4-103">Uzyskaj prywatną chmurę</span><span class="sxs-lookup"><span data-stu-id="74bb4-103">Get a private cloud</span></span>

## <span data-ttu-id="74bb4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74bb4-104">SYNTAX</span></span>

### <span data-ttu-id="74bb4-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="74bb4-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="74bb4-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="74bb4-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="74bb4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74bb4-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="74bb4-108">Lista</span><span class="sxs-lookup"><span data-stu-id="74bb4-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="74bb4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="74bb4-109">DESCRIPTION</span></span>
<span data-ttu-id="74bb4-110">Uzyskaj prywatną chmurę</span><span class="sxs-lookup"><span data-stu-id="74bb4-110">Get a private cloud</span></span>

## <span data-ttu-id="74bb4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74bb4-111">EXAMPLES</span></span>

### <span data-ttu-id="74bb4-112">Przykład 1: Lista prywatna chmura w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="74bb4-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="74bb4-113">Lista prywatnej chmury w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="74bb4-113">List private cloud under subscription</span></span>

### <span data-ttu-id="74bb4-114">Przykład 2: Lista prywatna chmura w obszarze Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="74bb4-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="74bb4-115">Lista prywatna chmura w obszarze Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="74bb4-115">List private cloud under resource group</span></span>

### <span data-ttu-id="74bb4-116">Przykład 3: Uzyskaj prywatną chmurę</span><span class="sxs-lookup"><span data-stu-id="74bb4-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="74bb4-117">Pobierz prywatną chmurę</span><span class="sxs-lookup"><span data-stu-id="74bb4-117">Get private cloud</span></span>

## <span data-ttu-id="74bb4-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74bb4-118">PARAMETERS</span></span>

### <span data-ttu-id="74bb4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74bb4-119">-DefaultProfile</span></span>
<span data-ttu-id="74bb4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74bb4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74bb4-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74bb4-121">-InputObject</span></span>
<span data-ttu-id="74bb4-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="74bb4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74bb4-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74bb4-123">-Name</span></span>
<span data-ttu-id="74bb4-124">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="74bb4-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74bb4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74bb4-125">-ResourceGroupName</span></span>
<span data-ttu-id="74bb4-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74bb4-126">The name of the resource group.</span></span>
<span data-ttu-id="74bb4-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="74bb4-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="74bb4-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="74bb4-128">-SubscriptionId</span></span>
<span data-ttu-id="74bb4-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="74bb4-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="74bb4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74bb4-130">CommonParameters</span></span>
<span data-ttu-id="74bb4-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74bb4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74bb4-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74bb4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74bb4-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74bb4-133">INPUTS</span></span>

### <span data-ttu-id="74bb4-134">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="74bb4-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="74bb4-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74bb4-135">OUTPUTS</span></span>

### <span data-ttu-id="74bb4-136">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="74bb4-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="74bb4-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74bb4-137">NOTES</span></span>

<span data-ttu-id="74bb4-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="74bb4-138">ALIASES</span></span>

<span data-ttu-id="74bb4-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74bb4-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74bb4-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="74bb4-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74bb4-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74bb4-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74bb4-142">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="74bb4-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74bb4-143">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="74bb4-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="74bb4-144">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="74bb4-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="74bb4-145">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="74bb4-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="74bb4-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="74bb4-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74bb4-147">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="74bb4-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="74bb4-148">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="74bb4-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="74bb4-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74bb4-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="74bb4-150">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="74bb4-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="74bb4-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="74bb4-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="74bb4-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74bb4-152">RELATED LINKS</span></span>

