---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232911"
---
# <span data-ttu-id="f9b3e-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="f9b3e-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="f9b3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b3e-103">Uzyskiwanie klastra według nazwy w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="f9b3e-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="f9b3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9b3e-104">SYNTAX</span></span>

### <span data-ttu-id="f9b3e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f9b3e-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f9b3e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f9b3e-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f9b3e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f9b3e-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f9b3e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f9b3e-108">DESCRIPTION</span></span>
<span data-ttu-id="f9b3e-109">Uzyskiwanie klastra według nazwy w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="f9b3e-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="f9b3e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9b3e-110">EXAMPLES</span></span>

### <span data-ttu-id="f9b3e-111">Przykład 1: Pobierz klaster</span><span class="sxs-lookup"><span data-stu-id="f9b3e-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="f9b3e-112">Pobierz klaster</span><span class="sxs-lookup"><span data-stu-id="f9b3e-112">Get cluster</span></span>

### <span data-ttu-id="f9b3e-113">Przykład 2: Lista klastrów</span><span class="sxs-lookup"><span data-stu-id="f9b3e-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="f9b3e-114">Lista klastrów</span><span class="sxs-lookup"><span data-stu-id="f9b3e-114">List clusters</span></span>

## <span data-ttu-id="f9b3e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9b3e-115">PARAMETERS</span></span>

### <span data-ttu-id="f9b3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b3e-116">-DefaultProfile</span></span>
<span data-ttu-id="f9b3e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b3e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9b3e-118">-InputObject</span></span>
<span data-ttu-id="f9b3e-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f9b3e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9b3e-120">-Name</span></span>
<span data-ttu-id="f9b3e-121">Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="f9b3e-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b3e-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f9b3e-122">-PrivateCloudName</span></span>
<span data-ttu-id="f9b3e-123">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="f9b3e-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="f9b3e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b3e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9b3e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-125">The name of the resource group.</span></span>
<span data-ttu-id="f9b3e-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f9b3e-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f9b3e-127">-SubscriptionId</span></span>
<span data-ttu-id="f9b3e-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f9b3e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b3e-129">CommonParameters</span></span>
<span data-ttu-id="f9b3e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b3e-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9b3e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b3e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9b3e-132">INPUTS</span></span>

### <span data-ttu-id="f9b3e-133">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="f9b3e-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f9b3e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9b3e-134">OUTPUTS</span></span>

### <span data-ttu-id="f9b3e-135">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="f9b3e-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="f9b3e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9b3e-136">NOTES</span></span>

<span data-ttu-id="f9b3e-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f9b3e-137">ALIASES</span></span>

<span data-ttu-id="f9b3e-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9b3e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f9b3e-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f9b3e-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f9b3e-141">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f9b3e-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f9b3e-142">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="f9b3e-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f9b3e-143">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="f9b3e-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f9b3e-144">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="f9b3e-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f9b3e-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f9b3e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f9b3e-146">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f9b3e-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f9b3e-147">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="f9b3e-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f9b3e-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f9b3e-149">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="f9b3e-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f9b3e-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9b3e-151">RELATED LINKS</span></span>

