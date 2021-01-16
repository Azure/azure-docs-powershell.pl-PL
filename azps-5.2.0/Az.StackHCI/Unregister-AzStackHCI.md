---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349918"
---
# <span data-ttu-id="003c4-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="003c4-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="003c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="003c4-102">SYNOPSIS</span></span>
<span data-ttu-id="003c4-103">Unregister-AzStackHCI usuwa zasób usługi Microsoft. AzureStackHCI w chmurze reprezentujący klaster lokalny i wyrejestrowuje klaster lokalny na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="003c4-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="003c4-104">Zarejestrowane informacje dostępne w klastrze są używane do wyrejestrowywania klastra, jeśli nie są przekazywane żadne parametry.</span><span class="sxs-lookup"><span data-stu-id="003c4-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="003c4-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="003c4-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="003c4-106">Opis</span><span class="sxs-lookup"><span data-stu-id="003c4-106">DESCRIPTION</span></span>
<span data-ttu-id="003c4-107">Unregister-AzStackHCI usuwa zasób usługi Microsoft. AzureStackHCI w chmurze reprezentujący klaster lokalny i wyrejestrowuje klaster lokalny na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="003c4-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="003c4-108">Zarejestrowane informacje dostępne w klastrze są używane do wyrejestrowywania klastra, jeśli nie są przekazywane żadne parametry.</span><span class="sxs-lookup"><span data-stu-id="003c4-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="003c4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="003c4-109">EXAMPLES</span></span>

### <span data-ttu-id="003c4-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="003c4-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="003c4-111">C:\PS \> Wyrejestrowanie — wynik AzStackHCI: sukces</span><span class="sxs-lookup"><span data-stu-id="003c4-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="003c4-112">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="003c4-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="003c4-113">C:\PS \> Wyrejestrowanie — AzStackHCI-ComputerName ClusterNode1 wynik: sukces</span><span class="sxs-lookup"><span data-stu-id="003c4-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="003c4-114">PRZYKŁAD 3</span><span class="sxs-lookup"><span data-stu-id="003c4-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="003c4-115">C:\PS \> Wyrejestrowanie-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-confirm: $false wynik: sukces</span><span class="sxs-lookup"><span data-stu-id="003c4-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="003c4-116">PRZYKŁAD 4</span><span class="sxs-lookup"><span data-stu-id="003c4-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="003c4-117">C:\PS \> Wyrejestrowanie-AzStackHCI-Identyfikator subskrypcji "12a0f531-56cb-4340-9501-257726d741fd"-resourceName HciCluster1-dzierżawy "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential Get-Credential wynik: sukces</span><span class="sxs-lookup"><span data-stu-id="003c4-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="003c4-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="003c4-118">PARAMETERS</span></span>

### <span data-ttu-id="003c4-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="003c4-119">-AccountId</span></span>
<span data-ttu-id="003c4-120">Określa token dostępu ARM.</span><span class="sxs-lookup"><span data-stu-id="003c4-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="003c4-121">Określenie tego wraz z ArmAccessToken i GraphAccessToken spowoduje uniknięcie logowania do usługi Azure Interactive.</span><span class="sxs-lookup"><span data-stu-id="003c4-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="003c4-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="003c4-122">-ArmAccessToken</span></span>
<span data-ttu-id="003c4-123">Określa token dostępu ARM.</span><span class="sxs-lookup"><span data-stu-id="003c4-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="003c4-124">Określenie tego wraz z GraphAccessToken i AccountId zapobiega logowaniu się do usługi Azure Interactive.</span><span class="sxs-lookup"><span data-stu-id="003c4-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="003c4-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="003c4-125">-ComputerName</span></span>
<span data-ttu-id="003c4-126">Umożliwia określenie jednego węzła klastra w klastrze lokalnym, który jest rejestrowany na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="003c4-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003c4-127">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="003c4-127">-Credential</span></span>
<span data-ttu-id="003c4-128">Określa poświadczenie dla komputera ComputerName.</span><span class="sxs-lookup"><span data-stu-id="003c4-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="003c4-129">Domyślnie jest to bieżący użytkownik wykonujący polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="003c4-129">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003c4-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="003c4-130">-EnvironmentName</span></span>
<span data-ttu-id="003c4-131">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="003c4-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="003c4-132">Domyślna to AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="003c4-132">Default is AzureCloud.</span></span>
<span data-ttu-id="003c4-133">Prawidłowe wartości to AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="003c4-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003c4-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="003c4-134">-GraphAccessToken</span></span>
<span data-ttu-id="003c4-135">Określa token dostępu do wykresu.</span><span class="sxs-lookup"><span data-stu-id="003c4-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="003c4-136">Określenie tego wraz z ArmAccessToken i AccountId zapobiega logowaniu się do usługi Azure Interactive.</span><span class="sxs-lookup"><span data-stu-id="003c4-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="003c4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003c4-137">-ResourceGroupName</span></span>
<span data-ttu-id="003c4-138">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="003c4-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="003c4-139">Jeśli nie określono \<LocalClusterName\> — jako nazwy grupy zasobów będzie używana RG.</span><span class="sxs-lookup"><span data-stu-id="003c4-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="003c4-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="003c4-140">-ResourceName</span></span>
<span data-ttu-id="003c4-141">Określa nazwę zasobu zasobu utworzonego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="003c4-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="003c4-142">Jeśli nie określono, używana jest lokalna nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="003c4-142">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="003c4-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="003c4-143">-SubscriptionId</span></span>
<span data-ttu-id="003c4-144">Określa subskrypcję platformy Azure do utworzenia zasobu</span><span class="sxs-lookup"><span data-stu-id="003c4-144">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003c4-145">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="003c4-145">-TenantId</span></span>
<span data-ttu-id="003c4-146">Określa usługę Azure dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="003c4-146">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="003c4-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="003c4-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="003c4-148">Użyj uwierzytelniania kodu urządzenia zamiast interakcyjnego monitu przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="003c4-148">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="003c4-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="003c4-149">-Confirm</span></span>
<span data-ttu-id="003c4-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="003c4-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003c4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003c4-151">-WhatIf</span></span>
<span data-ttu-id="003c4-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="003c4-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="003c4-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="003c4-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003c4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003c4-154">CommonParameters</span></span>
<span data-ttu-id="003c4-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="003c4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003c4-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="003c4-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003c4-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="003c4-157">INPUTS</span></span>

## <span data-ttu-id="003c4-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="003c4-158">OUTPUTS</span></span>

### <span data-ttu-id="003c4-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="003c4-159">PSCustomObject.</span></span> <span data-ttu-id="003c4-160">Zwraca następujące właściwości w PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="003c4-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="003c4-161">Wynik: powodzenie lub nieudane lub anulowane.</span><span class="sxs-lookup"><span data-stu-id="003c4-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="003c4-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="003c4-162">NOTES</span></span>

## <span data-ttu-id="003c4-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="003c4-163">RELATED LINKS</span></span>
