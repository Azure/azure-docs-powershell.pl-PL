---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/15/2019
ms.locfileid: "93704570"
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

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Pobierz szczegóły aplikacji sieci szkieletowej usług.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Pobieranie szczegółów typu aplikacji sieci szkieletowej usług.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Uzyskiwanie szczegółowych informacji o wersji typu aplikacji sieci szkieletowej usług.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Pobieranie szczegółów zasobu klastra.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Pobierz szczegóły usługi programu Service Fabric w określonej aplikacji i klastrze.

### [Nowe — AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Utwórz nową aplikację sieci szkieletowej usługi w ramach określonej grupy zasobów i klastra.

### [Nowe — AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Utwórz nowy typ aplikacji sieci szkieletowej usług pod określoną grupą zasobów i klastrem.

### [Nowe — AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Tworzenie nowej wersji typu aplikacji w ramach określonej grupy zasobów i klastra.

### [Nowe — AzServiceFabricCluster](New-AzServiceFabricCluster.md)
To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric. Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany. Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy. 

### [Nowe — AzServiceFabricService](New-AzServiceFabricService.md)
Tworzenie nowej usługi programu Fabric Service w ramach określonej aplikacji i klastra.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Usuwanie aplikacji z klastra. Spowoduje to usunięcie wszystkich usług objętych aplikacją.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Usuwanie usługi Fabric typ aplikacji z klastra. Spowoduje to usunięcie wszystkich wersji typów w obszarze ten zasób.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Usuwanie usługi sieci szkieletowej w wersji typu aplikacji z klastra.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Usuwanie węzłów z określonego typu węzła z poziomu klastra.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Usuwanie kompletnego typu węzła z klastra.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Usuwanie usługi z klastra.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Aktualizowanie aplikacji sieci szkieletowej usługi. Umożliwia to zaktualizowanie parametrów aplikacji i/lub uaktualnienie wersji typu aplikacji, która wyzwoli uaktualnienie aplikacji.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.

