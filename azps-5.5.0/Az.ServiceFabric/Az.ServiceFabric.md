---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242139"
---
# Moduł Az.ServiceFabric
## Opis
Moduł Azure Service Fabric, za pomocą który można zautomatyzować operacje end-2-end, takie jak tworzenie bezpiecznego klastrów, przewczasowanie certyfikatów klastrów, dodawanie lub usunięcie węzłów z klastrem itp. Poniżej znajduje się pełna lista wszystkich operacji.

## Az.ServiceFabric Cmdlet
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Dodaj nazwę pospolitą lub thumbprint do klastrów na potrzeby uwierzytelniania klienta.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Dodawanie certyfikatu klasteru pomocniczego do klastrów.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Dodaj nazwę pospolitą certyfikatu lub thumbprint do klastra. Spowoduje to zarejestrowanie certyfikatu ponownie dla klastrów na potrzeby uwierzytelniania klienta.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Dodaj rozszerzenie maszyny wirtualnej do typu węzła.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Dodaj klucz tajny certyfikatu do typu węzła.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Dodaj węzły do określonego typu węzła w klastrze.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Dodaj nowy typ węzła do istniejącego klastra.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Uzyskaj szczegóły aplikacji Service Fabric.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Uzyskaj szczegółowe informacje o typie aplikacji Service Fabric.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Uzyskaj szczegółowe informacje o wersji typu materiału usługowego.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Uzyskaj szczegółowe informacje o zasobach klastrów.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Pobierz szczegóły zarządzanego zasobu klastrów.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Pobierz szczegóły zasobu typu węzła zarządzanego.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Uzyskaj szczegółowe informacje o usłudze Service Fabric w określonej aplikacji i klastrze.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Utwórz nową aplikację do tworzenia struktury usług w ramach określonej grupy zasobów i klastrów.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Utwórz nowy typ aplikacji sieci szkieletowej usług w ramach określonej grupy zasobów i klastrów.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Utwórz nową wersję typu aplikacji w określonej grupie zasobów i klastrze.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
To polecenie używa certyfikatów, które ty dostarczasz, lub certyfikatów wygenerowanych przez system z podpisem własnym w celu skonfigurowania nowego klastru materiału usługowego. Może on używać szablonu domyślnego lub niestandardowego, który możesz udostępnić. Możesz określić folder, aby wyeksportować certyfikaty z podpisem własnym lub pobrać je później z magazynu kluczy.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Tworzenie nowego klastru zarządzanego.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Tworzenie nowego zasobu typu węzła.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Utwórz nową usługę szkieletową usług w ramach określonej aplikacji i klastrów.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Usuń aplikację z klastra. Spowoduje to usunięcie wszystkich usług w ramach aplikacji.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Usuń sieć szkieletową usługi z klastrów. Spowoduje to usunięcie wszystkich wersji tego typu w ramach tego zasobu.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Usuń sieć szkieletową usługi z wersji aplikacji o typie aplikacji.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Usuń certyfikaty klientów lub podmioty certyfikatów z uwierzytelniania klienta w klastrze.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Usuwanie certyfikatu klastrów z zabezpieczeń klastrów.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Usuwanie zasobu klastrów.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Remvoe client certificate by thumbprint or common name.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Usuń typ węzła lub określone węzły w obrębie typu węzła.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Usuń rozszerzenie maszyny wirtualnej z typu węzła.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Usuwanie węzłów z określonego typu węzła z klastrów.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Usuwanie pełnego typu węzła z klastra.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Usuń usługę z klastra.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Usuń jedno lub wiele ustawień usługi Fabric z klastrów.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Ponowne uruchamianie określonych węzłów z typu węzła.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Ustawianie właściwości zasobów klastrów.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Ustawia właściwości zasobu typu węzła lub uruchamiaj akcje ponownego projektu dla określonych ndes typu węzła za pomocą parametru -Reimage.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Dodawanie lub aktualizowanie jednego lub wielu ustawień usługi Fabric do klastrowania.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Zmienianie typu uaktualniania sieci szkieletów usług w klastrze.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Aktualizowanie aplikacji do obsługi szkieletów usług. Pozwala to zaktualizować parametry aplikacji i/lub uaktualnić wersję typu aplikacji, co spowoduje uruchomienie uaktualnienia aplikacji.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Aktualizowanie warstwy niezawodności lub maszyny wirtualnej typu węzła w klastrze.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.

