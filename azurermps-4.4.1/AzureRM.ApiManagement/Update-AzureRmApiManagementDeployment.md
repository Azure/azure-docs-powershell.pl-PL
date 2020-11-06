---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525741"
---
# <span data-ttu-id="9e32d-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="9e32d-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="9e32d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e32d-102">SYNOPSIS</span></span>
<span data-ttu-id="9e32d-103">Aktualizuje wdrożenie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9e32d-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e32d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e32d-104">SYNTAX</span></span>

### <span data-ttu-id="9e32d-105">Określona usługa zarządzania interfejsem API (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9e32d-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e32d-106">Aktualizacja z wystąpienia PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e32d-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e32d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9e32d-107">DESCRIPTION</span></span>
<span data-ttu-id="9e32d-108">Polecenie cmdlet **Update-AzureRmApiManagementDeployment** aktualizuje bieżące wdrożenia usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9e32d-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="9e32d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e32d-109">EXAMPLES</span></span>

### <span data-ttu-id="9e32d-110">Przykład 1: aktualizowanie wdrożenia wystąpienia programu ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e32d-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="9e32d-111">To polecenie aktualizuje wdrożenie wystąpienia zarządzania interfejsem API na trzy standardowe pojemności jednostki.</span><span class="sxs-lookup"><span data-stu-id="9e32d-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="9e32d-112">Przykład 2: Pobieranie wystąpienia ApiManagement i skalowanie go</span><span class="sxs-lookup"><span data-stu-id="9e32d-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="9e32d-113">W tym przykładzie otrzymano instancję zarządzania interfejsem API, przeskaluje ją do pięciu jednostek Premium, a następnie dodaje kolejne trzy jednostki do regionu Premium.</span><span class="sxs-lookup"><span data-stu-id="9e32d-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="9e32d-114">Przykład 3: wdrożenie aktualizacji (zewnętrzna Sieć wirtualna)</span><span class="sxs-lookup"><span data-stu-id="9e32d-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="9e32d-115">To polecenie aktualizuje istniejące wdrożenie zarządzania interfejsem API i dołącza do zewnętrznego *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="9e32d-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="9e32d-116">Przykład 4: wdrożenie aktualizacji (wewnętrzna sieć wirtualna)</span><span class="sxs-lookup"><span data-stu-id="9e32d-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="9e32d-117">To polecenie aktualizuje istniejące wdrożenie zarządzania interfejsem API i łączy z *VpnType* wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="9e32d-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="9e32d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e32d-118">PARAMETERS</span></span>

### <span data-ttu-id="9e32d-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="9e32d-119">-AdditionalRegions</span></span>
<span data-ttu-id="9e32d-120">Określa dodatkowe regiony wdrażania usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9e32d-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e32d-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e32d-121">-ApiManagement</span></span>
<span data-ttu-id="9e32d-122">Określa wystąpienie **PsApiManagement** , z którego ma zostać pozyskana konfiguracja wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="9e32d-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="9e32d-123">Tego parametru należy użyć, jeśli wystąpienie zawiera już wszystkie wymagane zmiany.</span><span class="sxs-lookup"><span data-stu-id="9e32d-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e32d-124">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="9e32d-124">-Capacity</span></span>
<span data-ttu-id="9e32d-125">Określa pojemność jednostki SKU głównego obszaru wdrażania zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9e32d-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e32d-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9e32d-126">-Location</span></span>
<span data-ttu-id="9e32d-127">Określa lokalizację regionu wdrażania zarządzania głównym interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9e32d-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="9e32d-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9e32d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e32d-129">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="9e32d-129">North Central US</span></span>
- <span data-ttu-id="9e32d-130">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="9e32d-130">South Central US</span></span>
- <span data-ttu-id="9e32d-131">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="9e32d-131">Central US</span></span>
- <span data-ttu-id="9e32d-132">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="9e32d-132">West Europe</span></span>
- <span data-ttu-id="9e32d-133">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="9e32d-133">North Europe</span></span>
- <span data-ttu-id="9e32d-134">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="9e32d-134">West US</span></span>
- <span data-ttu-id="9e32d-135">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="9e32d-135">East US</span></span>
- <span data-ttu-id="9e32d-136">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="9e32d-136">East US 2</span></span>
- <span data-ttu-id="9e32d-137">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="9e32d-137">Japan East</span></span>
- <span data-ttu-id="9e32d-138">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="9e32d-138">Japan West</span></span>
- <span data-ttu-id="9e32d-139">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="9e32d-139">Brazil South</span></span>
- <span data-ttu-id="9e32d-140">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="9e32d-140">Southeast Asia</span></span>
- <span data-ttu-id="9e32d-141">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="9e32d-141">East Asia</span></span>
- <span data-ttu-id="9e32d-142">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="9e32d-142">Australia East</span></span>
- <span data-ttu-id="9e32d-143">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="9e32d-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e32d-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e32d-144">-Name</span></span>
<span data-ttu-id="9e32d-145">Określa nazwę zarządzania interfejsem API, które jest aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e32d-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e32d-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e32d-146">-PassThru</span></span>
<span data-ttu-id="9e32d-147">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9e32d-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e32d-148">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9e32d-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e32d-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e32d-149">-ResourceGroupName</span></span>
<span data-ttu-id="9e32d-150">Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9e32d-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e32d-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="9e32d-151">-Sku</span></span>
<span data-ttu-id="9e32d-152">Określa warstwę regionu wdrażania zarządzania INTERFEJSem głównym platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9e32d-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="9e32d-153">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9e32d-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e32d-154">Deweloper</span><span class="sxs-lookup"><span data-stu-id="9e32d-154">Developer</span></span>
- <span data-ttu-id="9e32d-155">Standard</span><span class="sxs-lookup"><span data-stu-id="9e32d-155">Standard</span></span>
- <span data-ttu-id="9e32d-156">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="9e32d-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e32d-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e32d-157">-VirtualNetwork</span></span>
<span data-ttu-id="9e32d-158">Określa konfigurację sieci wirtualnej regionu wdrażania zarządzania INTERFEJSem głównym platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9e32d-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e32d-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="9e32d-159">-VpnType</span></span>
<span data-ttu-id="9e32d-160">Określa typ sieci wirtualnej wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9e32d-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="9e32d-161">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9e32d-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e32d-162">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="9e32d-162">None.</span></span>
<span data-ttu-id="9e32d-163">Wdrożenie zarządzania interfejsem API nie jest częścią żadnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9e32d-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="9e32d-164">Jest to wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="9e32d-164">This is the default value.</span></span> 
- <span data-ttu-id="9e32d-165">Zewnętrz.</span><span class="sxs-lookup"><span data-stu-id="9e32d-165">External.</span></span>
<span data-ttu-id="9e32d-166">Wdrożenie zarządzania interfejsem API ma zewnętrzny, stojący adres wirtualny.</span><span class="sxs-lookup"><span data-stu-id="9e32d-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="9e32d-167">Wspólnego.</span><span class="sxs-lookup"><span data-stu-id="9e32d-167">Internal.</span></span>
<span data-ttu-id="9e32d-168">Wdrożenie zarządzania interfejsem API ma adres wirtualny w intranecie.</span><span class="sxs-lookup"><span data-stu-id="9e32d-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e32d-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e32d-169">-DefaultProfile</span></span>
<span data-ttu-id="9e32d-170">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e32d-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e32d-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e32d-171">CommonParameters</span></span>
<span data-ttu-id="9e32d-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e32d-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e32d-173">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e32d-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e32d-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e32d-174">INPUTS</span></span>

### <span data-ttu-id="9e32d-175">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e32d-175">PsApiManagement</span></span>
<span data-ttu-id="9e32d-176">Parametr "ApiManagement" akceptuje wartość typu "PsApiManagement" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9e32d-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="9e32d-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e32d-177">OUTPUTS</span></span>

### <span data-ttu-id="9e32d-178">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e32d-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9e32d-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e32d-179">NOTES</span></span>

## <span data-ttu-id="9e32d-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e32d-180">RELATED LINKS</span></span>

[<span data-ttu-id="9e32d-181">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e32d-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


