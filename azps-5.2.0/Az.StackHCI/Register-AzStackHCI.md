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
# <span data-ttu-id="63742-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="63742-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="63742-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63742-102">SYNOPSIS</span></span>
<span data-ttu-id="63742-103">Register-AzStackHCI tworzy zasób usługi Microsoft. AzureStackHCI w chmurze reprezentujący klaster lokalny i rejestruje klaster lokalny na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="63742-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="63742-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63742-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="63742-105">Opis</span><span class="sxs-lookup"><span data-stu-id="63742-105">DESCRIPTION</span></span>
<span data-ttu-id="63742-106">Register-AzStackHCI tworzy zasób usługi Microsoft. AzureStackHCI w chmurze reprezentujący klaster lokalny i rejestruje klaster lokalny na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="63742-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="63742-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63742-107">EXAMPLES</span></span>

### <span data-ttu-id="63742-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="63742-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="63742-109">C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd": powodzenie ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="63742-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="63742-110">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="63742-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="63742-111">C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd"-ComputerName ClusterNode1 wynik: powodzenie ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="63742-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="63742-112">PRZYKŁAD 3</span><span class="sxs-lookup"><span data-stu-id="63742-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="63742-113">C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -region zachód-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="63742-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="63742-114">PRZYKŁAD 4</span><span class="sxs-lookup"><span data-stu-id="63742-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="63742-115">C:\PS \> register-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd" — region zachód-resourceName HciCluster1-dzierżawy "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential poświadczenie Get-Credential: powodzenie ResourceID:/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="63742-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="63742-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63742-116">PARAMETERS</span></span>

### <span data-ttu-id="63742-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="63742-117">-AccountId</span></span>
<span data-ttu-id="63742-118">Określa token dostępu ARM.</span><span class="sxs-lookup"><span data-stu-id="63742-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="63742-119">Określenie tego wraz z ArmAccessToken i GraphAccessToken spowoduje uniknięcie logowania do usługi Azure Interactive.</span><span class="sxs-lookup"><span data-stu-id="63742-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="63742-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="63742-120">-ArmAccessToken</span></span>
<span data-ttu-id="63742-121">Określa token dostępu ARM.</span><span class="sxs-lookup"><span data-stu-id="63742-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="63742-122">Określenie tego wraz z GraphAccessToken i AccountId zapobiega logowaniu się do usługi Azure Interactive.</span><span class="sxs-lookup"><span data-stu-id="63742-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="63742-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="63742-123">-CertificateThumbprint</span></span>
<span data-ttu-id="63742-124">Określa odcisk palca certyfikatu dostępny we wszystkich węzłach.</span><span class="sxs-lookup"><span data-stu-id="63742-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="63742-125">Użytkownik jest odpowiedzialny za zarządzanie certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="63742-125">User is responsible for managing the certificate.</span></span>

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

### <span data-ttu-id="63742-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="63742-126">-ComputerName</span></span>
<span data-ttu-id="63742-127">Określa nazwę klastra lub jednego z węzłów klastra w klastrze lokalnym, który jest rejestrowany na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="63742-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="63742-128">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="63742-128">-Credential</span></span>
<span data-ttu-id="63742-129">Określa poświadczenie dla komputera ComputerName.</span><span class="sxs-lookup"><span data-stu-id="63742-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="63742-130">Domyślnie jest to bieżący użytkownik wykonujący polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63742-130">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="63742-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="63742-131">-EnvironmentName</span></span>
<span data-ttu-id="63742-132">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="63742-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="63742-133">Domyślna to AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="63742-133">Default is AzureCloud.</span></span>
<span data-ttu-id="63742-134">Prawidłowe wartości to AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="63742-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="63742-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="63742-135">-GraphAccessToken</span></span>
<span data-ttu-id="63742-136">Określa token dostępu do wykresu.</span><span class="sxs-lookup"><span data-stu-id="63742-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="63742-137">Określenie tego wraz z ArmAccessToken i AccountId zapobiega logowaniu się do usługi Azure Interactive.</span><span class="sxs-lookup"><span data-stu-id="63742-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="63742-138">-Region</span><span class="sxs-lookup"><span data-stu-id="63742-138">-Region</span></span>
<span data-ttu-id="63742-139">Określa region, w którym ma zostać utworzony zasób.</span><span class="sxs-lookup"><span data-stu-id="63742-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="63742-140">Domyślnie jest to wschód.</span><span class="sxs-lookup"><span data-stu-id="63742-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="63742-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="63742-141">-RepairRegistration</span></span>
<span data-ttu-id="63742-142">Naprawianie bieżącej rejestracji HCL stosu platformy Azure w chmurze.</span><span class="sxs-lookup"><span data-stu-id="63742-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="63742-143">To polecenie cmdlet usuwa certyfikaty lokalne z węzłów klastrowanych oraz certyfikaty zdalne w aplikacji usługi Azure AD w chmurze i generuje nowe certyfikaty zastępcze dla obu.</span><span class="sxs-lookup"><span data-stu-id="63742-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="63742-144">Grupa zasobów, nazwa zasobu i inne opcje rejestracji są zachowywane.</span><span class="sxs-lookup"><span data-stu-id="63742-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="63742-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63742-145">-ResourceGroupName</span></span>
<span data-ttu-id="63742-146">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="63742-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="63742-147">Jeśli nie określono \<LocalClusterName\> — jako nazwy grupy zasobów będzie używana RG.</span><span class="sxs-lookup"><span data-stu-id="63742-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="63742-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="63742-148">-ResourceName</span></span>
<span data-ttu-id="63742-149">Określa nazwę zasobu zasobu utworzonego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="63742-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="63742-150">Jeśli nie określono, używana jest lokalna nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="63742-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="63742-151">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="63742-151">-SubscriptionId</span></span>
<span data-ttu-id="63742-152">Określa subskrypcję platformy Azure, aby utworzyć zasób.</span><span class="sxs-lookup"><span data-stu-id="63742-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="63742-153">Jest to jedyny obowiązkowy parametr.</span><span class="sxs-lookup"><span data-stu-id="63742-153">This is the only Mandatory parameter.</span></span>

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

### <span data-ttu-id="63742-154">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="63742-154">-TenantId</span></span>
<span data-ttu-id="63742-155">Określa usługę Azure dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="63742-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="63742-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="63742-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="63742-157">Użyj uwierzytelniania kodu urządzenia zamiast interakcyjnego monitu przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="63742-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="63742-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63742-158">CommonParameters</span></span>
<span data-ttu-id="63742-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63742-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63742-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63742-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63742-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63742-161">INPUTS</span></span>

## <span data-ttu-id="63742-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63742-162">OUTPUTS</span></span>

### <span data-ttu-id="63742-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="63742-163">PSCustomObject.</span></span> <span data-ttu-id="63742-164">Zwraca następujące właściwości w PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="63742-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="63742-165">Wynik: sukces lub niepowodzenie lub PendingForAdminConsent lub anulowane.</span><span class="sxs-lookup"><span data-stu-id="63742-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="63742-166">ResourceId: Identyfikator zasobu zasobu utworzonego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="63742-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="63742-167">PortalResourceURL: adres URL zasobu usługi Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="63742-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="63742-168">PortalAADAppPermissionsURL: adres URL portalu usługi Azure dla uprawnień aplikacji AAD.</span><span class="sxs-lookup"><span data-stu-id="63742-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="63742-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63742-169">NOTES</span></span>

## <span data-ttu-id="63742-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63742-170">RELATED LINKS</span></span>
