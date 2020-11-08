---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064754"
---
# AZ. moduł servicefabric
## Opis
Moduł sieci szkieletowej usługi Azure, za pomocą którego można zautomatyzować działania końcowe 2-końcowe, takie jak tworzenie bezpiecznego klastra, Przetaczanie certyfikatów klastra, Dodawanie lub usuwanie węzłów z klastra itd. Pełna lista wszystkich operacji jest wymieniona poniżej.

## AZ. polecenia cmdlet w usłudze servicefabric
### [Dodaj-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.

### [Dodaj-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Dodaj pomocniczy certyfikat klastra do klastra.

### [Dodaj-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Dodawanie nazwy pospolitej certyfikatu lub odcisku palca do klastra. Spowoduje to ponowne zarejestrowanie certyfikatu w celu uwierzytelnienia klienta.

### [Dodaj-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Dodaj rozszerzenie maszyny wirtualnej do typu węzła.

### [Dodaj-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Dodaj klucz tajny certyfikatu do typu węzła.

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

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Uzyskiwanie szczegółów zarządzanego zasobu klastra.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Pobierz szczegóły zasobu typu zarządzanego węzła.

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

### [Nowe — AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Tworzenie nowego zarządzanego klastra.

### [Nowe — AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Tworzenie nowego zasobu typu węzeł.

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

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Usuń zasób klastra.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Remvoe certyfikat klienta według odcisku palca lub nazwy pospolitej.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Usuwanie typu węzła lub określonych węzłów w obrębie typu węzła.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Usuń rozszerzenie maszyny wirtualnej z typu węzła.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Usuwanie węzłów z określonego typu węzła z poziomu klastra.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Usuwanie kompletnego typu węzła z klastra.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Usuwanie usługi z klastra.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Ponownie uruchom określone węzły z typu węzła.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Ustawianie właściwości zasobu klastra.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Ustawia właściwości zasobu typu węzła lub uruchamia akcje ponownego tworzenia obrazów dla konkretnej usługi NDES typu węzła z parametrem-Reimage.

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

