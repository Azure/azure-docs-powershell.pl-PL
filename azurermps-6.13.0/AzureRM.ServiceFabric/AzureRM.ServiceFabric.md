---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 6d93775a028e7a590a8da9cc008640fb8484bdf2
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522346"
---
# Moduł AzureRM. servicefabric
## Opis
Moduł sieci szkieletowej usługi Azure, za pomocą którego można zautomatyzować działania końcowe 2-końcowe, takie jak tworzenie bezpiecznego klastra, Przetaczanie certyfikatów klastra, Dodawanie lub usuwanie węzłów z klastra itd. Pełna lista wszystkich operacji jest wymieniona poniżej.

## Polecenia cmdlet AzureRM. servicefabric
### [Dodaj-AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
Dodaj nowy certyfikat do zestawów skali maszyny wirtualnej, które tworzą klaster. Certyfikat jest przeznaczony do użytku jako certyfikat aplikacji.

### [Dodaj-AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.

### [Dodaj-AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
Dodaj pomocniczy certyfikat klastra do klastra.

### [Dodaj-AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
Dodaj węzły do określonego typu węzła w klastrze.

### [Dodaj-AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
Dodawanie nowego typu węzła do istniejącego klastra.

### [Get-AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
Pobieranie szczegółów zasobu klastra.

### [Nowe — AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric. Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany. Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy. 

### [Remove-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.

### [Remove-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.

### [Remove-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
Usuwanie węzłów z określonego typu węzła z poziomu klastra.

### [Remove-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
Usuwanie kompletnego typu węzła z klastra.

### [Remove-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.

### [Update-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.

### [Update-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.

