---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345010"
---
# <span data-ttu-id="66a11-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="66a11-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="66a11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66a11-102">SYNOPSIS</span></span>
<span data-ttu-id="66a11-103">Uzyskiwanie autoryzacji obwodu ExpressRoute według nazwy w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="66a11-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="66a11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66a11-104">SYNTAX</span></span>

### <span data-ttu-id="66a11-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="66a11-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="66a11-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="66a11-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="66a11-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="66a11-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="66a11-108">Opis</span><span class="sxs-lookup"><span data-stu-id="66a11-108">DESCRIPTION</span></span>
<span data-ttu-id="66a11-109">Uzyskiwanie autoryzacji obwodu ExpressRoute według nazwy w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="66a11-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="66a11-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66a11-110">EXAMPLES</span></span>

### <span data-ttu-id="66a11-111">Przykład 1: Uzyskaj autoryzację</span><span class="sxs-lookup"><span data-stu-id="66a11-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="66a11-112">To polecenie cmdlet uzyskuje autoryzację `azps-test-auth` w chmurze prywatnej `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="66a11-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="66a11-113">Przykład 2: Autoryzacja listy</span><span class="sxs-lookup"><span data-stu-id="66a11-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="66a11-114">To polecenie cmdlet wyświetla autoryzację `azps-test-auth` w obszarze prywatna chmura `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="66a11-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="66a11-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66a11-115">PARAMETERS</span></span>

### <span data-ttu-id="66a11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a11-116">-DefaultProfile</span></span>
<span data-ttu-id="66a11-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66a11-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a11-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66a11-118">-InputObject</span></span>
<span data-ttu-id="66a11-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="66a11-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="66a11-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66a11-120">-Name</span></span>
<span data-ttu-id="66a11-121">Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="66a11-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="66a11-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="66a11-122">-PrivateCloudName</span></span>
<span data-ttu-id="66a11-123">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="66a11-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="66a11-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a11-124">-ResourceGroupName</span></span>
<span data-ttu-id="66a11-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66a11-125">The name of the resource group.</span></span>
<span data-ttu-id="66a11-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="66a11-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="66a11-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="66a11-127">-SubscriptionId</span></span>
<span data-ttu-id="66a11-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="66a11-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="66a11-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a11-129">CommonParameters</span></span>
<span data-ttu-id="66a11-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a11-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a11-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66a11-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a11-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66a11-132">INPUTS</span></span>

### <span data-ttu-id="66a11-133">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="66a11-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="66a11-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66a11-134">OUTPUTS</span></span>

### <span data-ttu-id="66a11-135">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="66a11-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="66a11-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66a11-136">NOTES</span></span>

<span data-ttu-id="66a11-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="66a11-137">ALIASES</span></span>

<span data-ttu-id="66a11-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66a11-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66a11-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="66a11-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66a11-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66a11-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66a11-141">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="66a11-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66a11-142">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="66a11-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="66a11-143">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="66a11-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="66a11-144">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="66a11-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="66a11-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="66a11-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66a11-146">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="66a11-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="66a11-147">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="66a11-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="66a11-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66a11-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="66a11-149">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="66a11-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="66a11-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="66a11-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="66a11-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66a11-151">RELATED LINKS</span></span>

