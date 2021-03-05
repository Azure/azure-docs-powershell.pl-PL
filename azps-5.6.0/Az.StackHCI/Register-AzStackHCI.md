---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: 2a6e94512e8bc9bed980c76b5430118d74bd3f6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987519"
---
# <span data-ttu-id="5680e-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="5680e-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="5680e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5680e-102">SYNOPSIS</span></span>
<span data-ttu-id="5680e-103">Register-AzStackHCI utworzy zasób w chmurze Microsoft.AzureStackHCI reprezentujący klaster lokalnym i zarejestruje klastr lokalnego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="5680e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5680e-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="5680e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5680e-105">DESCRIPTION</span></span>
<span data-ttu-id="5680e-106">Register-AzStackHCI utworzy zasób w chmurze Microsoft.AzureStackHCI reprezentujący klaster lokalnym i zarejestruje klastr lokalnego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="5680e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5680e-107">EXAMPLES</span></span>

### <span data-ttu-id="5680e-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="5680e-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/
```

<span data-ttu-id="5680e-109">Wywołuj w jednym z węźle klastrów.</span><span class="sxs-lookup"><span data-stu-id="5680e-109">Invoking on one of the cluster node.</span></span>

### <span data-ttu-id="5680e-110">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="5680e-110">EXAMPLE 2</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="5680e-111">Wywołuj węźle zarządzania.</span><span class="sxs-lookup"><span data-stu-id="5680e-111">Invoking from the management node.</span></span>

### <span data-ttu-id="5680e-112">PRZYKŁAD 3</span><span class="sxs-lookup"><span data-stu-id="5680e-112">EXAMPLE 3</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG 
Result: PendingForAdminConsent
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="5680e-113">Invoking from WAC.</span><span class="sxs-lookup"><span data-stu-id="5680e-113">Invoking from WAC.</span></span>

### <span data-ttu-id="5680e-114">PRZYKŁAD 4</span><span class="sxs-lookup"><span data-stu-id="5680e-114">EXAMPLE 4</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="5680e-115">We wszystkich parametrach.</span><span class="sxs-lookup"><span data-stu-id="5680e-115">Invoking with all the parameters.</span></span>

## <span data-ttu-id="5680e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5680e-116">PARAMETERS</span></span>

### <span data-ttu-id="5680e-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="5680e-117">-AccountId</span></span>
<span data-ttu-id="5680e-118">Określa ARM dostępu.</span><span class="sxs-lookup"><span data-stu-id="5680e-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="5680e-119">Określenie tego wraz z armAccessToken i GraphAccessToken pozwoli uniknąć interakcyjnego logowania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="5680e-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="5680e-120">-ArmAccessToken</span></span>
<span data-ttu-id="5680e-121">Określa ARM dostępu.</span><span class="sxs-lookup"><span data-stu-id="5680e-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="5680e-122">Określenie tego wraz z graphAccessToken i AccountId pozwoli uniknąć interakcyjnego logowania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="5680e-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="5680e-123">-CertificateThumbprint</span></span>
<span data-ttu-id="5680e-124">Określa thumbprint certyfikatu dostępnego we wszystkich węzłach.</span><span class="sxs-lookup"><span data-stu-id="5680e-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="5680e-125">Użytkownik jest odpowiedzialny za zarządzanie certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="5680e-125">User is responsible for managing the certificate.</span></span>

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

### <span data-ttu-id="5680e-126">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="5680e-126">-ComputerName</span></span>
<span data-ttu-id="5680e-127">Określa nazwę klastra lub jeden z węzła klastrów w klastrze lokalnym, który jest zarejestrowany na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="5680e-128">- Credential</span><span class="sxs-lookup"><span data-stu-id="5680e-128">-Credential</span></span>
<span data-ttu-id="5680e-129">Określa poświadczenia dla parametru Nazwa_komputera.</span><span class="sxs-lookup"><span data-stu-id="5680e-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="5680e-130">Wartość domyślna to bieżący użytkownik wykonujący polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5680e-130">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="5680e-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="5680e-131">-EnvironmentName</span></span>
<span data-ttu-id="5680e-132">Określa środowisko platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="5680e-133">Wartością domyślną jest usługa AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="5680e-133">Default is AzureCloud.</span></span>
<span data-ttu-id="5680e-134">Prawidłowe wartości to: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="5680e-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="5680e-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="5680e-135">-GraphAccessToken</span></span>
<span data-ttu-id="5680e-136">Określa token dostępu do wykresu.</span><span class="sxs-lookup"><span data-stu-id="5680e-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="5680e-137">Określenie tego ustawienia wraz z usługami ArmAccessToken i AccountId pozwoli uniknąć interakcyjnego logowania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="5680e-138">— Region</span><span class="sxs-lookup"><span data-stu-id="5680e-138">-Region</span></span>
<span data-ttu-id="5680e-139">Określa region do utworzenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="5680e-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="5680e-140">Wartością domyślną jest region EastUS.</span><span class="sxs-lookup"><span data-stu-id="5680e-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="5680e-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="5680e-141">-RepairRegistration</span></span>
<span data-ttu-id="5680e-142">Naprawianie bieżącej rejestracji HCI usługi Azure Stack w chmurze.</span><span class="sxs-lookup"><span data-stu-id="5680e-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="5680e-143">To polecenie cmdlet usuwa certyfikaty lokalne w węzłach grupowanych i certyfikaty zdalne w aplikacji usługi Azure AD w chmurze i generuje nowe certyfikaty zastępcze dla obu.</span><span class="sxs-lookup"><span data-stu-id="5680e-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="5680e-144">Grupa zasobów, nazwa zasobu i inne opcje rejestracji zostaną zachowane.</span><span class="sxs-lookup"><span data-stu-id="5680e-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="5680e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5680e-145">-ResourceGroupName</span></span>
<span data-ttu-id="5680e-146">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="5680e-147">Jeśli nie określono \<LocalClusterName\> wartości -rg, zostanie użyta jako nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5680e-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="5680e-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5680e-148">-ResourceName</span></span>
<span data-ttu-id="5680e-149">Określa nazwę zasobu utworzonego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="5680e-150">Jeśli nie zostanie określona, zostanie użyta nazwa klastra lokalnego.</span><span class="sxs-lookup"><span data-stu-id="5680e-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="5680e-151">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5680e-151">-SubscriptionId</span></span>
<span data-ttu-id="5680e-152">Określa subskrypcję platformy Azure, aby utworzyć zasób.</span><span class="sxs-lookup"><span data-stu-id="5680e-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="5680e-153">Jest to jedyny parametr obowiązkowy.</span><span class="sxs-lookup"><span data-stu-id="5680e-153">This is the only Mandatory parameter.</span></span>

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

### <span data-ttu-id="5680e-154">- TenantId</span><span class="sxs-lookup"><span data-stu-id="5680e-154">-TenantId</span></span>
<span data-ttu-id="5680e-155">Określa wartość Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="5680e-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="5680e-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="5680e-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="5680e-157">Zamiast interakcyjnego monitu w przeglądarce użyj uwierzytelniania kodu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="5680e-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="5680e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5680e-158">CommonParameters</span></span>
<span data-ttu-id="5680e-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5680e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5680e-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5680e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5680e-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5680e-161">INPUTS</span></span>

## <span data-ttu-id="5680e-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5680e-162">OUTPUTS</span></span>

### <span data-ttu-id="5680e-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="5680e-163">PSCustomObject.</span></span> <span data-ttu-id="5680e-164">Zwraca następujące właściwości w programie PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="5680e-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="5680e-165">Wynik: Powodzenie, Niepowodzenie lub Oczekiwanie NaWSąduAdminconsent lub Anulowane.</span><span class="sxs-lookup"><span data-stu-id="5680e-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="5680e-166">ResourceId: Identyfikator zasobu utworzonego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="5680e-167">PortalResourceURL: adres URL zasobu portalu Azure.</span><span class="sxs-lookup"><span data-stu-id="5680e-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="5680e-168">PortalAADAppPermissionsURL: adres URL portalu Azure dla strony uprawnień aplikacji AAD.</span><span class="sxs-lookup"><span data-stu-id="5680e-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="5680e-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5680e-169">NOTES</span></span>

## <span data-ttu-id="5680e-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5680e-170">RELATED LINKS</span></span>
