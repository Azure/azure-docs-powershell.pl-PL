---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93704379"
---
# AZ. moduł servicefabric
## Opis
Moduł sieci szkieletowej usługi Azure, za pomocą którego można zautomatyzować działania końcowe 2-końcowe, takie jak tworzenie bezpiecznego klastra, Przetaczanie certyfikatów klastra, Dodawanie lub usuwanie węzłów z klastra itd. Pełna lista wszystkich operacji jest wymieniona poniżej.

## AZ. polecenia cmdlet w usłudze servicefabric
### [Dodaj-AzServiceFabricApplicationCertificate](Add-AzServiceFabricApplicationCertificate.md)
Dodaj nowy certyfikat do zestawów skali maszyny wirtualnej, które tworzą klaster. Certyfikat jest przeznaczony do użytku jako certyfikat aplikacji.

### [Dodaj-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.

### [Dodaj-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Dodaj pomocniczy certyfikat klastra do klastra.

### [Dodaj-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Dodaj węzły do określonego typu węzła w klastrze.

### [Dodaj-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Dodawanie nowego typu węzła do istniejącego klastra.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Pobieranie szczegółów zasobu klastra.

### [Nowe — AzServiceFabricCluster](New-AzServiceFabricCluster.md)
To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric. Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany. Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy. 

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Usuwanie węzłów z określonego typu węzła z poziomu klastra.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Usuwanie kompletnego typu węzła z klastra.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.

