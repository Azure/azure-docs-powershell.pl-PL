---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: ad9c09118252499f99708ae99d36ee9ba2418ff2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349942"
---
# Register-AzStackHCI

## STRESZCZENIe
Register-AzStackHCI tworzy zasób usługi Microsoft. AzureStackHCI w chmurze reprezentujący klaster lokalny i rejestruje klaster lokalny na platformie Azure.

## POLECENIA

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## Opis
Register-AzStackHCI tworzy zasób usługi Microsoft. AzureStackHCI w chmurze reprezentujący klaster lokalny i rejestruje klaster lokalny na platformie Azure.

## Przykłady

### PRZYKŁAD 1
```
Invoking on one of the cluster node.
```

C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd": powodzenie ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/

### PRZYKŁAD 2
```
Invoking from the management node
```

C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd"-ComputerName ClusterNode1 wynik: powodzenie ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

### PRZYKŁAD 3
```
Invoking from WAC
```

C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -region zachód-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

### PRZYKŁAD 4
```
Invoking with all the parameters
```

C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd" — region zachód-resourceName HciCluster1-dzierżawy "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential poświadczenie Get-Credential: powodzenie ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

## PARAMETRÓW

### -AccountId
Określa token dostępu ARM.
Określenie tego wraz z ArmAccessToken i GraphAccessToken spowoduje uniknięcie logowania do usługi Azure Interactive.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
Określa token dostępu ARM.
Określenie tego wraz z GraphAccessToken i AccountId zapobiega logowaniu się do usługi Azure Interactive.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint
Określa odcisk palca certyfikatu dostępny we wszystkich węzłach. Użytkownik jest odpowiedzialny za zarządzanie certyfikatem.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Określa nazwę klastra lub jednego z węzłów klastra w klastrze lokalnym, który jest rejestrowany na platformie Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Poświadczenie
Określa poświadczenie dla komputera ComputerName.
Domyślnie jest to bieżący użytkownik wykonujący polecenie cmdlet.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Określa środowisko Azure.
Domyślna to AzureCloud.
Prawidłowe wartości to AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Określa token dostępu do wykresu.
Określenie tego wraz z ArmAccessToken i AccountId zapobiega logowaniu się do usługi Azure Interactive.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
Określa region, w którym ma zostać utworzony zasób.
Domyślnie jest to wschód.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RepairRegistration
Naprawianie bieżącej rejestracji HCL stosu platformy Azure w chmurze. To polecenie cmdlet usuwa certyfikaty lokalne z węzłów klastrowanych oraz certyfikaty zdalne w aplikacji usługi Azure AD w chmurze i generuje nowe certyfikaty zastępcze dla obu. Grupa zasobów, nazwa zasobu i inne opcje rejestracji są zachowywane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
Jeśli nie określono \<LocalClusterName\> — jako nazwy grupy zasobów będzie używana RG.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Określa nazwę zasobu zasobu utworzonego na platformie Azure.
Jeśli nie określono, używana jest lokalna nazwa klastra.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subskrypcji
Określa subskrypcję platformy Azure, aby utworzyć zasób.
Jest to jedyny obowiązkowy parametr.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dzierżawy
Określa usługę Azure dzierżawy.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDeviceAuthentication
Użyj uwierzytelniania kodu urządzenia zamiast interakcyjnego monitu przeglądarki.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

## WYSYŁA

### PSCustomObject. Zwraca następujące właściwości w PSCustomObject
### Wynik: sukces lub niepowodzenie lub PendingForAdminConsent lub anulowane.
### ResourceId: Identyfikator zasobu zasobu utworzonego na platformie Azure.
### PortalResourceURL: adres URL zasobu usługi Azure Portal.
### PortalAADAppPermissionsURL: adres URL portalu usługi Azure dla uprawnień aplikacji AAD.
## INFORMACYJN

## LINKI POKREWNE
