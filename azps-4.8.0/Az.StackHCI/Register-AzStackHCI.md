---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222157"
---
# <span data-ttu-id="2e8b4-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="2e8b4-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="2e8b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8b4-103">Register-AzStackHCI tworzy zasób usługi Microsoft. AzureStackHCI w chmurze reprezentujący klaster lokalny i rejestruje klaster lokalny na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="2e8b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e8b4-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="2e8b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e8b4-105">DESCRIPTION</span></span>
<span data-ttu-id="2e8b4-106">Register-AzStackHCI tworzy zasób usługi Microsoft. AzureStackHCI w chmurze reprezentujący klaster lokalny i rejestruje klaster lokalny na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="2e8b4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e8b4-107">EXAMPLES</span></span>

### <span data-ttu-id="2e8b4-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="2e8b4-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="2e8b4-109">C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd": powodzenie ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="2e8b4-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="2e8b4-110">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="2e8b4-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="2e8b4-111">C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd"-ComputerName ClusterNode1 wynik: powodzenie ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="2e8b4-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="2e8b4-112">PRZYKŁAD 3</span><span class="sxs-lookup"><span data-stu-id="2e8b4-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="2e8b4-113">C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -region zachód-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="2e8b4-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="2e8b4-114">PRZYKŁAD 4</span><span class="sxs-lookup"><span data-stu-id="2e8b4-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="2e8b4-115">C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd" — region zachód-resourceName HciCluster1-dzierżawy "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential poświadczenie Get-Credential: powodzenie ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="2e8b4-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="2e8b4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e8b4-116">PARAMETERS</span></span>

### <span data-ttu-id="2e8b4-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2e8b4-117">-SubscriptionId</span></span>
<span data-ttu-id="2e8b4-118">Określa subskrypcję platformy Azure, aby utworzyć zasób.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="2e8b4-119">Jest to jedyny obowiązkowy parametr.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-119">This is the only Mandatory parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-120">-Region</span><span class="sxs-lookup"><span data-stu-id="2e8b4-120">-Region</span></span>
<span data-ttu-id="2e8b4-121">Określa region, w którym ma zostać utworzony zasób.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="2e8b4-122">Domyślnie jest to wschód.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-122">Default is EastUS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2e8b4-123">-ResourceName</span></span>
<span data-ttu-id="2e8b4-124">Określa nazwę zasobu zasobu utworzonego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="2e8b4-125">Jeśli nie określono, używana jest lokalna nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-125">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-126">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="2e8b4-126">-TenantId</span></span>
<span data-ttu-id="2e8b4-127">Określa usługę Azure dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-127">Specifies the Azure TenantId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e8b4-128">-ResourceGroupName</span></span>
<span data-ttu-id="2e8b4-129">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="2e8b4-130">Jeśli nie określono \<LocalClusterName\> — jako nazwy grupy zasobów będzie używana RG.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="2e8b4-131">-ArmAccessToken</span></span>
<span data-ttu-id="2e8b4-132">Określa token dostępu ARM.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="2e8b4-133">Określenie tego wraz z GraphAccessToken i AccountId zapobiega logowaniu się do usługi Azure Interactive.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="2e8b4-134">-GraphAccessToken</span></span>
<span data-ttu-id="2e8b4-135">Określa token dostępu do wykresu.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="2e8b4-136">Określenie tego wraz z ArmAccessToken i AccountId zapobiega logowaniu się do usługi Azure Interactive.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-137">-AccountId</span><span class="sxs-lookup"><span data-stu-id="2e8b4-137">-AccountId</span></span>
<span data-ttu-id="2e8b4-138">Określa token dostępu ARM.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="2e8b4-139">Określenie tego wraz z ArmAccessToken i GraphAccessToken spowoduje uniknięcie logowania do usługi Azure Interactive.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-140">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="2e8b4-140">-EnvironmentName</span></span>
<span data-ttu-id="2e8b4-141">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="2e8b4-142">Domyślna to AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-142">Default is AzureCloud.</span></span>
<span data-ttu-id="2e8b4-143">Prawidłowe wartości to AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="2e8b4-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-144">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="2e8b4-144">-ComputerName</span></span>
<span data-ttu-id="2e8b4-145">Określa nazwę klastra lub jednego z węzłów klastra w klastrze lokalnym, który jest rejestrowany na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-146">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="2e8b4-146">-Credential</span></span>
<span data-ttu-id="2e8b4-147">Określa poświadczenie dla komputera ComputerName.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="2e8b4-148">Domyślnie jest to bieżący użytkownik wykonujący polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-148">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8b4-149">CommonParameters</span></span>
<span data-ttu-id="2e8b4-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8b4-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e8b4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8b4-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e8b4-152">INPUTS</span></span>

## <span data-ttu-id="2e8b4-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e8b4-153">OUTPUTS</span></span>

### <span data-ttu-id="2e8b4-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-154">PSCustomObject.</span></span> <span data-ttu-id="2e8b4-155">Zwraca następujące właściwości w PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="2e8b4-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="2e8b4-156">Wynik: sukces lub niepowodzenie lub PendingForAdminConsent lub anulowane.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="2e8b4-157">ResourceId: Identyfikator zasobu zasobu utworzonego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="2e8b4-158">PortalResourceURL: adres URL zasobu usługi Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="2e8b4-159">PortalAADAppPermissionsURL: adres URL portalu usługi Azure dla uprawnień aplikacji AAD.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="2e8b4-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e8b4-160">NOTES</span></span>

## <span data-ttu-id="2e8b4-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e8b4-161">RELATED LINKS</span></span>
