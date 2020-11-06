---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553063"
---
# <span data-ttu-id="455b1-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="455b1-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="455b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="455b1-102">SYNOPSIS</span></span>
<span data-ttu-id="455b1-103">Tworzenie wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="455b1-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="455b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="455b1-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="455b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="455b1-105">DESCRIPTION</span></span>
<span data-ttu-id="455b1-106">Polecenie cmdlet **New-AzureRmApiManagement** tworzy wdrożenie zarządzania interfejsem API w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="455b1-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="455b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="455b1-107">EXAMPLES</span></span>

### <span data-ttu-id="455b1-108">Przykład 1: Tworzenie usługi zarządzania interfejsem API dla warstwy dewelopera</span><span class="sxs-lookup"><span data-stu-id="455b1-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="455b1-109">To polecenie tworzy usługę zarządzania interfejsem API warstwy dewelopera.</span><span class="sxs-lookup"><span data-stu-id="455b1-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="455b1-110">Polecenie określa nazwę organizacji i adres administratora.</span><span class="sxs-lookup"><span data-stu-id="455b1-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="455b1-111">Polecenie nie określa parametru *SKU* .</span><span class="sxs-lookup"><span data-stu-id="455b1-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="455b1-112">Dlatego polecenie cmdlet używa domyślnej wartości dewelopera.</span><span class="sxs-lookup"><span data-stu-id="455b1-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="455b1-113">Przykład 2: Tworzenie usługi warstwy standardowej zawierającej trzy jednostki</span><span class="sxs-lookup"><span data-stu-id="455b1-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="455b1-114">To polecenie tworzy standardową usługę zarządzania interfejsem API o trzech jednostkach.</span><span class="sxs-lookup"><span data-stu-id="455b1-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="455b1-115">Przykład 3: Tworzenie usługi zarządzania interfejsem API dla zewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="455b1-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="455b1-116">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z zewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="455b1-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="455b1-117">Przykład 4: Tworzenie usługi zarządzania interfejsem API dla wewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="455b1-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="455b1-118">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z wewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="455b1-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="455b1-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="455b1-119">PARAMETERS</span></span>

### <span data-ttu-id="455b1-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="455b1-120">-AdditionalRegions</span></span>
<span data-ttu-id="455b1-121">Dodatkowe regiony wdrażania usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="455b1-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="455b1-122">-AdminEmail</span></span>
<span data-ttu-id="455b1-123">Określa źródłowy adres e-mail dla wszystkich powiadomień wysyłanych przez system zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="455b1-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-124">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="455b1-124">-Capacity</span></span>
<span data-ttu-id="455b1-125">Określa pojemność jednostki SKU usługi zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="455b1-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="455b1-126">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="455b1-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="455b1-127">-DefaultProfile</span></span>
<span data-ttu-id="455b1-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="455b1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="455b1-129">-Location</span></span>
<span data-ttu-id="455b1-130">Określa lokalizację, w której ma zostać utworzona usługa zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="455b1-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="455b1-131">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="455b1-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="455b1-132">-Name</span></span>
<span data-ttu-id="455b1-133">Określa nazwę wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="455b1-133">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-134">— Organizacja</span><span class="sxs-lookup"><span data-stu-id="455b1-134">-Organization</span></span>
<span data-ttu-id="455b1-135">Określa nazwę organizacji.</span><span class="sxs-lookup"><span data-stu-id="455b1-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="455b1-136">Funkcja zarządzania interfejsem API używa tego adresu w portalu dewelopera w obszarze powiadomienia e-mail.</span><span class="sxs-lookup"><span data-stu-id="455b1-136">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="455b1-137">-ResourceGroupName</span></span>
<span data-ttu-id="455b1-138">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="455b1-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="455b1-139">-Sku</span></span>
<span data-ttu-id="455b1-140">Określa warstwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="455b1-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="455b1-141">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="455b1-141">Valid values are:</span></span> 

- <span data-ttu-id="455b1-142">Deweloper</span><span class="sxs-lookup"><span data-stu-id="455b1-142">Developer</span></span> 
- <span data-ttu-id="455b1-143">Standard</span><span class="sxs-lookup"><span data-stu-id="455b1-143">Standard</span></span> 
- <span data-ttu-id="455b1-144">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="455b1-144">Premium</span></span> 

<span data-ttu-id="455b1-145">Domyślnym ustawieniem jest deweloper.</span><span class="sxs-lookup"><span data-stu-id="455b1-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="455b1-146">-Tag</span></span>
<span data-ttu-id="455b1-147">Słownik znaczników.</span><span class="sxs-lookup"><span data-stu-id="455b1-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="455b1-148">-VirtualNetwork</span></span>
<span data-ttu-id="455b1-149">Konfiguracja sieci wirtualnej w obszarze wdrażania zarządzania interfejsem głównym usługi Azure API.</span><span class="sxs-lookup"><span data-stu-id="455b1-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="455b1-150">-VpnType</span></span>
<span data-ttu-id="455b1-151">Typ sieci wirtualnej wdrożenia ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="455b1-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="455b1-152">Prawidłowe wartości to</span><span class="sxs-lookup"><span data-stu-id="455b1-152">Valid Values are</span></span> 
- <span data-ttu-id="455b1-153">"Brak" (wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="455b1-153">"None" (Default Value.</span></span> <span data-ttu-id="455b1-154">ApiManagement nie jest częścią żadnej sieci wirtualnej ")</span><span class="sxs-lookup"><span data-stu-id="455b1-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="455b1-155">"Zewnętrzne" (ApiManagement wdrożenie to konfiguracja w sieci wirtualnej z internetowym punktem końcowym)</span><span class="sxs-lookup"><span data-stu-id="455b1-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="455b1-156">"Internal" (ApiManagement Deployment to Setup w sieci wirtualnej z punktem końcowym w intranecie)</span><span class="sxs-lookup"><span data-stu-id="455b1-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455b1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455b1-157">CommonParameters</span></span>
<span data-ttu-id="455b1-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="455b1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455b1-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="455b1-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455b1-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="455b1-160">INPUTS</span></span>

### <span data-ttu-id="455b1-161">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="455b1-161">None</span></span>
<span data-ttu-id="455b1-162">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="455b1-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="455b1-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="455b1-163">OUTPUTS</span></span>

### <span data-ttu-id="455b1-164">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="455b1-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="455b1-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="455b1-165">NOTES</span></span>

## <span data-ttu-id="455b1-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="455b1-166">RELATED LINKS</span></span>

[<span data-ttu-id="455b1-167">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="455b1-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="455b1-168">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="455b1-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="455b1-169">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="455b1-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="455b1-170">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="455b1-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


