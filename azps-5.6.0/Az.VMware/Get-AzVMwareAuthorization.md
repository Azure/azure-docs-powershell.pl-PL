---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
ms.openlocfilehash: dad73292e6875e2cf38244ed74e0519490860c4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991824"
---
# <span data-ttu-id="03336-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="03336-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="03336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03336-102">SYNOPSIS</span></span>
<span data-ttu-id="03336-103">Uzyskiwanie autoryzacji obwodu usługi ExpressRoute według nazwy w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="03336-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="03336-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03336-104">SYNTAX</span></span>

### <span data-ttu-id="03336-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="03336-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="03336-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="03336-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="03336-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="03336-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="03336-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="03336-108">DESCRIPTION</span></span>
<span data-ttu-id="03336-109">Uzyskiwanie autoryzacji obwodu usługi ExpressRoute według nazwy w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="03336-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="03336-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03336-110">EXAMPLES</span></span>

### <span data-ttu-id="03336-111">Przykład 1. Uzyskiwanie autoryzacji</span><span class="sxs-lookup"><span data-stu-id="03336-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="03336-112">To polecenie cmdlet uzyskuje autoryzację `azps-test-auth` w chmurze prywatnej `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="03336-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="03336-113">Przykład 2. Autoryzacja listy</span><span class="sxs-lookup"><span data-stu-id="03336-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="03336-114">To polecenie cmdlet wyświetla autoryzację `azps-test-auth` w chmurze prywatnej `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="03336-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="03336-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03336-115">PARAMETERS</span></span>

### <span data-ttu-id="03336-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03336-116">-DefaultProfile</span></span>
<span data-ttu-id="03336-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03336-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03336-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03336-118">-InputObject</span></span>
<span data-ttu-id="03336-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="03336-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="03336-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="03336-120">-Name</span></span>
<span data-ttu-id="03336-121">Nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="03336-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03336-122">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="03336-122">-PrivateCloudName</span></span>
<span data-ttu-id="03336-123">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="03336-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="03336-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03336-124">-ResourceGroupName</span></span>
<span data-ttu-id="03336-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03336-125">The name of the resource group.</span></span>
<span data-ttu-id="03336-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="03336-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="03336-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03336-127">-SubscriptionId</span></span>
<span data-ttu-id="03336-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="03336-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="03336-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03336-129">CommonParameters</span></span>
<span data-ttu-id="03336-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03336-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03336-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03336-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03336-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03336-132">INPUTS</span></span>

### <span data-ttu-id="03336-133">Microsoft.Azure.PowerShell.Cmdlet.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="03336-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="03336-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03336-134">OUTPUTS</span></span>

### <span data-ttu-id="03336-135">Microsoft.Azure.PowerShell.cmdlet.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="03336-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="03336-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03336-136">NOTES</span></span>

<span data-ttu-id="03336-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="03336-137">ALIASES</span></span>

<span data-ttu-id="03336-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03336-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03336-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="03336-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03336-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03336-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03336-141">INPUTOBJECT: <IVMWareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="03336-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03336-142">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="03336-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="03336-143">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="03336-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="03336-144">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="03336-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="03336-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="03336-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03336-146">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="03336-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="03336-147">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="03336-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="03336-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03336-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="03336-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="03336-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="03336-150">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="03336-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="03336-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03336-151">RELATED LINKS</span></span>

