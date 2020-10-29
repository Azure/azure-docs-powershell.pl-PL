---
title: Zarządzanie zasobami platformy Azure przy użyciu polecenia Invoke-AzRestMethod
description: Jak zarządzać zasobami za pomocą usługi Azure PowerShell i polecenia cmdlet Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 55d7cc06178257a9288e2d27f810d1180369ddc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753965"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="55328-103">Zarządzanie zasobami platformy Azure przy użyciu polecenia Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="55328-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="55328-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) to polecenie cmdlet usługi Azure PowerShell, które zostało wprowadzone w module Az programu PowerShell w wersji 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="55328-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="55328-105">Umożliwia wykonywanie niestandardowych żądań HTTP do punktu końcowego usługi Azure Resource Management (ARM) przy użyciu kontekstu Az.</span><span class="sxs-lookup"><span data-stu-id="55328-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="55328-106">To polecenie cmdlet jest przydatne, gdy chcesz zarządzać usługami platformy Azure w przypadku funkcji, które nie są jeszcze dostępne w module Az programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="55328-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="55328-107">Jak używać polecenia cmdlet Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="55328-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="55328-108">Na przykład możesz zezwolić na dostęp do usługi Azure Container Registry (ACR) tylko dla określonych sieci lub odmówić dostępu publicznego.</span><span class="sxs-lookup"><span data-stu-id="55328-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="55328-109">W wersji 4.5.0 modułu Az PowerShell ta funkcja nie jest jeszcze dostępna w [module Az.ContainerRegistry programu PowerShell](/powershell/module/Az.ContainerRegistry/).</span><span class="sxs-lookup"><span data-stu-id="55328-109">As of Az PowerShell module version 4.5.0, that feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span> <span data-ttu-id="55328-110">Jednak w międzyczasie można nią zarządzać za pomocą polecenia cmdlet `Invoke-AzRestMethod`.</span><span class="sxs-lookup"><span data-stu-id="55328-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="55328-111">Używanie polecenia cmdlet Invoke-AzRestMethod z operacjami GET</span><span class="sxs-lookup"><span data-stu-id="55328-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="55328-112">W poniższym przykładzie pokazano, jak użyć polecenia cmdlet `Invoke-AzRestMethod` z operacją GET:</span><span class="sxs-lookup"><span data-stu-id="55328-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

<span data-ttu-id="55328-113">Aby zapewnić maksymalną elastyczność, większość parametrów polecenia cmdlet `Invoke-AzRestMethod` jest opcjonalna.</span><span class="sxs-lookup"><span data-stu-id="55328-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="55328-114">Jeśli jednak zarządzasz zasobami w grupie zasobów, najprawdopodobniej musisz podać pełny identyfikator do zasobu lub parametry takie jak grupa zasobów, dostawca zasobów i typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="55328-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="55328-115">Parametry `ResourceType` i `Name` mogą przyjmować wiele wartości w przypadku zasobów, które wymagają więcej niż jednej nazwy.</span><span class="sxs-lookup"><span data-stu-id="55328-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="55328-116">Na przykład w celu manipulowania zapisanym wyszukiwaniem w obszarze roboczym usługi Log Analytics parametry wyglądają podobnie jak w poniższym przykładzie: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span><span class="sxs-lookup"><span data-stu-id="55328-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="55328-117">Korzystając z mapowania opartego na pozycji w tablicy, polecenie cmdlet konstruuje następujący zasób: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span><span class="sxs-lookup"><span data-stu-id="55328-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="55328-118">Parametr `APIVersion` umożliwia korzystanie z określonej wersji interfejsu API, w tym jednej z wersji zapoznawczych.</span><span class="sxs-lookup"><span data-stu-id="55328-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="55328-119">Obsługiwane wersje interfejsu API dla dostawców zasobów platformy Azure można znaleźć w repozytorium GitHub [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).</span><span class="sxs-lookup"><span data-stu-id="55328-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="55328-120">Definicję dla wersji 2019-12-01-preview usługi ACR można znaleźć w następującej lokalizacji: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span><span class="sxs-lookup"><span data-stu-id="55328-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="55328-121">Używanie polecenia cmdlet Invoke-AzRestMethod z operacjami PATCH</span><span class="sxs-lookup"><span data-stu-id="55328-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="55328-122">Dostęp publiczny do istniejącego elementu usługi ACR o nazwie `myacr` w grupie zasobów `myresourcegroup` możesz wyłączyć za pomocą polecenia cmdlet `Invoke-AzRestMethod`.</span><span class="sxs-lookup"><span data-stu-id="55328-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the `Invoke-AzRestMethod` cmdlet.</span></span>

<span data-ttu-id="55328-123">Aby wyłączyć dostęp do sieci publicznej, wykonaj wywołanie **PATCH** względem interfejsu API, które zmieni wartość parametru `publicNetwokAccess`, jak pokazano w następującym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="55328-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

<span data-ttu-id="55328-124">Właściwość `Payload` jest ciągiem JSON, który pokazuje ścieżkę właściwości do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="55328-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="55328-125">Wszystkie parametry tego interfejsu API są opisane w skojarzonym z nim pliku **rest-api-spec** .</span><span class="sxs-lookup"><span data-stu-id="55328-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="55328-126">Konkretną definicję parametru publicNetworkAccess można znaleźć w [pliku JSON rejestru kontenerów](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) dla wersji 2019-12-01-preview interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="55328-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="55328-127">Aby zezwolić na dostęp do rejestru tylko z określonego adresu IP, należy zmodyfikować ładunek tak, jak pokazano w następującym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="55328-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="55328-128">Porównanie z poleceniami cmdlet Get-AzResource, New-AzResource i Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="55328-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="55328-129">Polecenia cmdlet `*-AzResource` umożliwiają dostosowanie wywołania interfejsu API REST względem platformy Azure przez określenie typu zasobu, wersji interfejsu API i właściwości do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="55328-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="55328-130">Należy jednak najpierw utworzyć właściwości jako `PSObject`.</span><span class="sxs-lookup"><span data-stu-id="55328-130">However, the properties need to be created first as a `PSObject`.</span></span> <span data-ttu-id="55328-131">Ten proces wnosi dodatkowy poziom złożoności i może łatwo stać się skomplikowany.</span><span class="sxs-lookup"><span data-stu-id="55328-131">This process adds an additional level of complexity and can easily become complicated.</span></span>

<span data-ttu-id="55328-132">Polecenie cmdlet `Invoke-AzRestMethod` oferuje łatwy sposób zarządzania zasobami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="55328-132">`Invoke-AzRestMethod` offers a simple way to manage Azure resources.</span></span> <span data-ttu-id="55328-133">Jak pokazano w poprzednim przykładzie, można utworzyć ciąg JSON i za jego pomocą dostosować wywołanie interfejsu API REST bez konieczności wstępnego tworzenia żadnych obiektów `PSObjects`.</span><span class="sxs-lookup"><span data-stu-id="55328-133">As shown in the previous example, you can build a JSON string and use it to customize the REST API call without having to precreate any `PSObjects`.</span></span>

<span data-ttu-id="55328-134">Jeśli masz już doświadczenie z poleceniami cmdlet `*-AzResource`, możesz nadal z nich korzystać.</span><span class="sxs-lookup"><span data-stu-id="55328-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="55328-135">Zakończenie ich obsługi nie jest planowane.</span><span class="sxs-lookup"><span data-stu-id="55328-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="55328-136">Polecenie cmdlet `Invoke-AzRestMethod` to nowy dodatek do zestawu narzędzi.</span><span class="sxs-lookup"><span data-stu-id="55328-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to your toolkit.</span></span>

## <a name="see-also"></a><span data-ttu-id="55328-137">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="55328-137">See Also</span></span>

* [<span data-ttu-id="55328-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="55328-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="55328-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="55328-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="55328-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="55328-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
