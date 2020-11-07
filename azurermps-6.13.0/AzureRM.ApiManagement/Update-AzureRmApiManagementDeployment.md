---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: f8f0273ab624cd81488734f9b84debc045f6fed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526361"
---
# <span data-ttu-id="d6f94-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="d6f94-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="d6f94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6f94-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f94-103">Aktualizuje wdrożenie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6f94-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6f94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6f94-104">SYNTAX</span></span>

### <span data-ttu-id="d6f94-105">UpdateSpecificService (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6f94-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6f94-106">UpdateFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="d6f94-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6f94-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6f94-107">DESCRIPTION</span></span>
<span data-ttu-id="d6f94-108">Polecenie cmdlet **Update-AzureRmApiManagementDeployment** aktualizuje bieżące wdrożenia usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6f94-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="d6f94-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6f94-109">EXAMPLES</span></span>

### <span data-ttu-id="d6f94-110">Przykład 1: aktualizowanie wdrożenia wystąpienia programu ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f94-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```powershell
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="d6f94-111">To polecenie aktualizuje wdrożenie wystąpienia zarządzania interfejsem API na trzy standardowe pojemności jednostki.</span><span class="sxs-lookup"><span data-stu-id="d6f94-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="d6f94-112">Przykład 2: Pobieranie wystąpienia ApiManagement i skalowanie go</span><span class="sxs-lookup"><span data-stu-id="d6f94-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```powershell
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="d6f94-113">W tym przykładzie otrzymano instancję zarządzania interfejsem API, przeskaluje ją do pięciu jednostek Premium, a następnie dodaje kolejne trzy jednostki do regionu Premium.</span><span class="sxs-lookup"><span data-stu-id="d6f94-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="d6f94-114">Przykład 3: wdrożenie aktualizacji (zewnętrzna Sieć wirtualna)</span><span class="sxs-lookup"><span data-stu-id="d6f94-114">Example 3: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="d6f94-115">To polecenie aktualizuje istniejące wdrożenie zarządzania interfejsem API i dołącza do zewnętrznego *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="d6f94-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="d6f94-116">Przykład 4: wdrożenie aktualizacji (wewnętrzna sieć wirtualna)</span><span class="sxs-lookup"><span data-stu-id="d6f94-116">Example 4: Update deployment (internal VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="d6f94-117">To polecenie aktualizuje istniejące wdrożenie zarządzania interfejsem API i łączy z *VpnType* wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="d6f94-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="d6f94-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6f94-118">PARAMETERS</span></span>

### <span data-ttu-id="d6f94-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="d6f94-119">-AdditionalRegions</span></span>
<span data-ttu-id="d6f94-120">Określa dodatkowe regiony wdrażania usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="d6f94-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f94-121">-ApiManagement</span></span>
<span data-ttu-id="d6f94-122">Określa wystąpienie **PsApiManagement** , z którego ma zostać pozyskana konfiguracja wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d6f94-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="d6f94-123">Tego parametru należy użyć, jeśli wystąpienie zawiera już wszystkie wymagane zmiany.</span><span class="sxs-lookup"><span data-stu-id="d6f94-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-124">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="d6f94-124">-Capacity</span></span>
<span data-ttu-id="d6f94-125">Określa pojemność jednostki SKU głównego obszaru wdrażania zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f94-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f94-126">-DefaultProfile</span></span>
<span data-ttu-id="d6f94-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f94-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d6f94-128">-Location</span></span>
<span data-ttu-id="d6f94-129">Określa lokalizację regionu wdrażania zarządzania głównym interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6f94-129">Specifies the location of the master API Management deployment region.</span></span>
<span data-ttu-id="d6f94-130">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="d6f94-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6f94-131">-Name</span></span>
<span data-ttu-id="d6f94-132">Określa nazwę zarządzania interfejsem API, które jest aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6f94-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6f94-133">-PassThru</span></span>
<span data-ttu-id="d6f94-134">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d6f94-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6f94-135">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d6f94-135">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f94-136">-ResourceGroupName</span></span>
<span data-ttu-id="d6f94-137">Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6f94-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="d6f94-138">-Sku</span></span>
<span data-ttu-id="d6f94-139">Określa warstwę regionu wdrażania zarządzania INTERFEJSem głównym platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f94-139">Specifies the tier of the master Azure API Management deployment region.</span></span>
<span data-ttu-id="d6f94-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d6f94-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6f94-141">Deweloper</span><span class="sxs-lookup"><span data-stu-id="d6f94-141">Developer</span></span>
- <span data-ttu-id="d6f94-142">Standard</span><span class="sxs-lookup"><span data-stu-id="d6f94-142">Standard</span></span>
- <span data-ttu-id="d6f94-143">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="d6f94-143">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d6f94-144">-VirtualNetwork</span></span>
<span data-ttu-id="d6f94-145">Określa konfigurację sieci wirtualnej regionu wdrażania zarządzania INTERFEJSem głównym platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f94-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="d6f94-146">-VpnType</span></span>
<span data-ttu-id="d6f94-147">Określa typ sieci wirtualnej wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6f94-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="d6f94-148">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d6f94-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6f94-149">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="d6f94-149">None.</span></span>
<span data-ttu-id="d6f94-150">Wdrożenie zarządzania interfejsem API nie jest częścią żadnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d6f94-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="d6f94-151">Jest to wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="d6f94-151">This is the default value.</span></span> 
- <span data-ttu-id="d6f94-152">Zewnętrz.</span><span class="sxs-lookup"><span data-stu-id="d6f94-152">External.</span></span>
<span data-ttu-id="d6f94-153">Wdrożenie zarządzania interfejsem API ma zewnętrzny, stojący adres wirtualny.</span><span class="sxs-lookup"><span data-stu-id="d6f94-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="d6f94-154">Wspólnego.</span><span class="sxs-lookup"><span data-stu-id="d6f94-154">Internal.</span></span>
<span data-ttu-id="d6f94-155">Wdrożenie zarządzania interfejsem API ma adres wirtualny w intranecie.</span><span class="sxs-lookup"><span data-stu-id="d6f94-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f94-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f94-156">CommonParameters</span></span>
<span data-ttu-id="d6f94-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f94-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f94-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f94-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f94-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6f94-159">INPUTS</span></span>

### <span data-ttu-id="d6f94-160">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f94-160">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="d6f94-161">Parametry: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d6f94-161">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="d6f94-162">System. String</span><span class="sxs-lookup"><span data-stu-id="d6f94-162">System.String</span></span>

### <span data-ttu-id="d6f94-163">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="d6f94-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="d6f94-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d6f94-164">System.Int32</span></span>

### <span data-ttu-id="d6f94-165">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d6f94-165">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="d6f94-166">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVpnType</span><span class="sxs-lookup"><span data-stu-id="d6f94-166">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType</span></span>

### <span data-ttu-id="d6f94-167">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ApiManagement. MODELES. PsApiManagementRegion, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="d6f94-167">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d6f94-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6f94-168">OUTPUTS</span></span>

### <span data-ttu-id="d6f94-169">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f94-169">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="d6f94-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6f94-170">NOTES</span></span>

## <span data-ttu-id="d6f94-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6f94-171">RELATED LINKS</span></span>

[<span data-ttu-id="d6f94-172">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f94-172">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

