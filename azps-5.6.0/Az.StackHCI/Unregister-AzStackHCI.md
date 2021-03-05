---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: 3f38a11cd5d4a124e7db7a99422239f73cbe96dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976202"
---
# <span data-ttu-id="822d0-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="822d0-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="822d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="822d0-102">SYNOPSIS</span></span>
<span data-ttu-id="822d0-103">Unregister-AzStackHCI usunąć zasób chmury Microsoft.AzureStackHCI reprezentujący klaster lokalnego i wyrejestruje klaster lokalnego z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="822d0-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="822d0-104">Zarejestrowane informacje dostępne w klastrze są używane do wyrejestrowania klastrów, jeśli nie zostaną przekazane żadne parametry.</span><span class="sxs-lookup"><span data-stu-id="822d0-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="822d0-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="822d0-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="822d0-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="822d0-106">DESCRIPTION</span></span>
<span data-ttu-id="822d0-107">Unregister-AzStackHCI usunąć zasób chmury Microsoft.AzureStackHCI reprezentujący klaster lokalnego i wyrejestruje klaster lokalnego z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="822d0-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="822d0-108">Zarejestrowane informacje dostępne w klastrze są używane do wyrejestrowania klastrów, jeśli nie zostaną przekazane żadne parametry.</span><span class="sxs-lookup"><span data-stu-id="822d0-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="822d0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="822d0-109">EXAMPLES</span></span>

### <span data-ttu-id="822d0-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="822d0-110">EXAMPLE 1</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
<span data-ttu-id="822d0-111">Invoking on one of the cluster node</span><span class="sxs-lookup"><span data-stu-id="822d0-111">Invoking on one of the cluster node</span></span>

### <span data-ttu-id="822d0-112">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="822d0-112">EXAMPLE 2</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
<span data-ttu-id="822d0-113">Invoking from the management node</span><span class="sxs-lookup"><span data-stu-id="822d0-113">Invoking from the management node</span></span>

### <span data-ttu-id="822d0-114">PRZYKŁAD 3</span><span class="sxs-lookup"><span data-stu-id="822d0-114">EXAMPLE 3</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
<span data-ttu-id="822d0-115">Invoking from WAC</span><span class="sxs-lookup"><span data-stu-id="822d0-115">Invoking from WAC</span></span>

### <span data-ttu-id="822d0-116">PRZYKŁAD 4</span><span class="sxs-lookup"><span data-stu-id="822d0-116">EXAMPLE 4</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
<span data-ttu-id="822d0-117">Nawołuj do wszystkich parametrów</span><span class="sxs-lookup"><span data-stu-id="822d0-117">Invoking with all the parameters</span></span>

## <span data-ttu-id="822d0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="822d0-118">PARAMETERS</span></span>

### <span data-ttu-id="822d0-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="822d0-119">-AccountId</span></span>
<span data-ttu-id="822d0-120">Określa ARM dostępu.</span><span class="sxs-lookup"><span data-stu-id="822d0-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="822d0-121">Określenie tego wraz z armAccessToken i GraphAccessToken pozwoli uniknąć interakcyjnego logowania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="822d0-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="822d0-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="822d0-122">-ArmAccessToken</span></span>
<span data-ttu-id="822d0-123">Określa ARM dostępu.</span><span class="sxs-lookup"><span data-stu-id="822d0-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="822d0-124">Określenie tego wraz z graphAccessToken i AccountId pozwoli uniknąć interakcyjnego logowania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="822d0-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="822d0-125">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="822d0-125">-ComputerName</span></span>
<span data-ttu-id="822d0-126">Określa jeden z węzła klastrów w klastrze lokalnym, który jest zarejestrowany na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="822d0-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="822d0-127">- Credential</span><span class="sxs-lookup"><span data-stu-id="822d0-127">-Credential</span></span>
<span data-ttu-id="822d0-128">Określa poświadczenia dla parametru Nazwa_komputera.</span><span class="sxs-lookup"><span data-stu-id="822d0-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="822d0-129">Wartość domyślna to bieżący użytkownik wykonujący polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="822d0-129">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="822d0-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="822d0-130">-EnvironmentName</span></span>
<span data-ttu-id="822d0-131">Określa środowisko platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="822d0-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="822d0-132">Wartością domyślną jest usługa AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="822d0-132">Default is AzureCloud.</span></span>
<span data-ttu-id="822d0-133">Prawidłowe wartości to: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="822d0-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="822d0-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="822d0-134">-GraphAccessToken</span></span>
<span data-ttu-id="822d0-135">Określa token dostępu do wykresu.</span><span class="sxs-lookup"><span data-stu-id="822d0-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="822d0-136">Określenie tego ustawienia wraz z usługami ArmAccessToken i AccountId pozwoli uniknąć interakcyjnego logowania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="822d0-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="822d0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="822d0-137">-ResourceGroupName</span></span>
<span data-ttu-id="822d0-138">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="822d0-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="822d0-139">Jeśli nie określono \<LocalClusterName\> wartości -rg, zostanie użyta jako nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="822d0-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="822d0-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="822d0-140">-ResourceName</span></span>
<span data-ttu-id="822d0-141">Określa nazwę zasobu utworzonego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="822d0-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="822d0-142">Jeśli nie zostanie określona, zostanie użyta nazwa klastra lokalnego.</span><span class="sxs-lookup"><span data-stu-id="822d0-142">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="822d0-143">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="822d0-143">-SubscriptionId</span></span>
<span data-ttu-id="822d0-144">Określa subskrypcję platformy Azure w celu utworzenia zasobu</span><span class="sxs-lookup"><span data-stu-id="822d0-144">Specifies the Azure Subscription to create the resource</span></span>

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

### <span data-ttu-id="822d0-145">- TenantId</span><span class="sxs-lookup"><span data-stu-id="822d0-145">-TenantId</span></span>
<span data-ttu-id="822d0-146">Określa wartość Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="822d0-146">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="822d0-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="822d0-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="822d0-148">Zamiast interakcyjnego monitu w przeglądarce użyj uwierzytelniania kodu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="822d0-148">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="822d0-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="822d0-149">-Confirm</span></span>
<span data-ttu-id="822d0-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="822d0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="822d0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="822d0-151">-WhatIf</span></span>
<span data-ttu-id="822d0-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="822d0-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="822d0-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="822d0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="822d0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822d0-154">CommonParameters</span></span>
<span data-ttu-id="822d0-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="822d0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822d0-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="822d0-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822d0-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="822d0-157">INPUTS</span></span>

## <span data-ttu-id="822d0-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="822d0-158">OUTPUTS</span></span>

### <span data-ttu-id="822d0-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="822d0-159">PSCustomObject.</span></span> <span data-ttu-id="822d0-160">Zwraca następujące właściwości w programie PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="822d0-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="822d0-161">Wynik: Sukces, niepowodzenie lub anulowanie.</span><span class="sxs-lookup"><span data-stu-id="822d0-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="822d0-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="822d0-162">NOTES</span></span>

## <span data-ttu-id="822d0-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="822d0-163">RELATED LINKS</span></span>
