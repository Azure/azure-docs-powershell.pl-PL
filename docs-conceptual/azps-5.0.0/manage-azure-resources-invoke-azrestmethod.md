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
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Zarządzanie zasobami platformy Azure przy użyciu polecenia Invoke-AzRestMethod

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) to polecenie cmdlet usługi Azure PowerShell, które zostało wprowadzone w module Az programu PowerShell w wersji 4.4.0. Umożliwia wykonywanie niestandardowych żądań HTTP do punktu końcowego usługi Azure Resource Management (ARM) przy użyciu kontekstu Az.

To polecenie cmdlet jest przydatne, gdy chcesz zarządzać usługami platformy Azure w przypadku funkcji, które nie są jeszcze dostępne w module Az programu PowerShell.

## <a name="how-to-use-invoke-azrestmethod"></a>Jak używać polecenia cmdlet Invoke-AzRestMethod

Na przykład możesz zezwolić na dostęp do usługi Azure Container Registry (ACR) tylko dla określonych sieci lub odmówić dostępu publicznego. W wersji 4.5.0 modułu Az PowerShell ta funkcja nie jest jeszcze dostępna w [module Az.ContainerRegistry programu PowerShell](/powershell/module/Az.ContainerRegistry/). Jednak w międzyczasie można nią zarządzać za pomocą polecenia cmdlet `Invoke-AzRestMethod`.

## <a name="using-invoke-azrestmethod-with-get-operations"></a>Używanie polecenia cmdlet Invoke-AzRestMethod z operacjami GET

W poniższym przykładzie pokazano, jak użyć polecenia cmdlet `Invoke-AzRestMethod` z operacją GET:

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

Aby zapewnić maksymalną elastyczność, większość parametrów polecenia cmdlet `Invoke-AzRestMethod` jest opcjonalna.
Jeśli jednak zarządzasz zasobami w grupie zasobów, najprawdopodobniej musisz podać pełny identyfikator do zasobu lub parametry takie jak grupa zasobów, dostawca zasobów i typ zasobu.

Parametry `ResourceType` i `Name` mogą przyjmować wiele wartości w przypadku zasobów, które wymagają więcej niż jednej nazwy. Na przykład w celu manipulowania zapisanym wyszukiwaniem w obszarze roboczym usługi Log Analytics parametry wyglądają podobnie jak w poniższym przykładzie: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.

Korzystając z mapowania opartego na pozycji w tablicy, polecenie cmdlet konstruuje następujący zasób: `Id:'/workspaces/my-la/savedsearches/my-search'`.

Parametr `APIVersion` umożliwia korzystanie z określonej wersji interfejsu API, w tym jednej z wersji zapoznawczych. Obsługiwane wersje interfejsu API dla dostawców zasobów platformy Azure można znaleźć w repozytorium GitHub [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).

Definicję dla wersji 2019-12-01-preview usługi ACR można znaleźć w następującej lokalizacji: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>Używanie polecenia cmdlet Invoke-AzRestMethod z operacjami PATCH

Dostęp publiczny do istniejącego elementu usługi ACR o nazwie `myacr` w grupie zasobów `myresourcegroup` możesz wyłączyć za pomocą polecenia cmdlet `Invoke-AzRestMethod`.

Aby wyłączyć dostęp do sieci publicznej, wykonaj wywołanie **PATCH** względem interfejsu API, które zmieni wartość parametru `publicNetwokAccess`, jak pokazano w następującym przykładzie:

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

Właściwość `Payload` jest ciągiem JSON, który pokazuje ścieżkę właściwości do zmodyfikowania.

Wszystkie parametry tego interfejsu API są opisane w skojarzonym z nim pliku **rest-api-spec** .
Konkretną definicję parametru publicNetworkAccess można znaleźć w [pliku JSON rejestru kontenerów](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) dla wersji 2019-12-01-preview interfejsu API.

Aby zezwolić na dostęp do rejestru tylko z określonego adresu IP, należy zmodyfikować ładunek tak, jak pokazano w następującym przykładzie:

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

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>Porównanie z poleceniami cmdlet Get-AzResource, New-AzResource i Remove-AzResource

Polecenia cmdlet `*-AzResource` umożliwiają dostosowanie wywołania interfejsu API REST względem platformy Azure przez określenie typu zasobu, wersji interfejsu API i właściwości do zaktualizowania. Należy jednak najpierw utworzyć właściwości jako `PSObject`. Ten proces wnosi dodatkowy poziom złożoności i może łatwo stać się skomplikowany.

Polecenie cmdlet `Invoke-AzRestMethod` oferuje łatwy sposób zarządzania zasobami platformy Azure. Jak pokazano w poprzednim przykładzie, można utworzyć ciąg JSON i za jego pomocą dostosować wywołanie interfejsu API REST bez konieczności wstępnego tworzenia żadnych obiektów `PSObjects`.

Jeśli masz już doświadczenie z poleceniami cmdlet `*-AzResource`, możesz nadal z nich korzystać. Zakończenie ich obsługi nie jest planowane. Polecenie cmdlet `Invoke-AzRestMethod` to nowy dodatek do zestawu narzędzi.

## <a name="see-also"></a>Zobacz też

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
