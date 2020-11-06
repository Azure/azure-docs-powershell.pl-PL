---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547240"
---
# <span data-ttu-id="0a80f-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a80f-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="0a80f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a80f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a80f-103">Tworzenie wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0a80f-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a80f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a80f-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a80f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a80f-105">DESCRIPTION</span></span>
<span data-ttu-id="0a80f-106">Polecenie cmdlet **New-AzureRmApiManagement** tworzy wdrożenie zarządzania interfejsem API w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="0a80f-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="0a80f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a80f-107">EXAMPLES</span></span>

### <span data-ttu-id="0a80f-108">Przykład 1: Tworzenie usługi zarządzania interfejsem API dla warstwy dewelopera</span><span class="sxs-lookup"><span data-stu-id="0a80f-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="0a80f-109">To polecenie tworzy usługę zarządzania interfejsem API warstwy dewelopera.</span><span class="sxs-lookup"><span data-stu-id="0a80f-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="0a80f-110">Polecenie określa nazwę organizacji i adres administratora.</span><span class="sxs-lookup"><span data-stu-id="0a80f-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="0a80f-111">Polecenie nie określa parametru *SKU* .</span><span class="sxs-lookup"><span data-stu-id="0a80f-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="0a80f-112">Dlatego polecenie cmdlet używa domyślnej wartości dewelopera.</span><span class="sxs-lookup"><span data-stu-id="0a80f-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="0a80f-113">Przykład 2: Tworzenie usługi warstwy standardowej zawierającej trzy jednostki</span><span class="sxs-lookup"><span data-stu-id="0a80f-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="0a80f-114">To polecenie tworzy standardową usługę zarządzania interfejsem API o trzech jednostkach.</span><span class="sxs-lookup"><span data-stu-id="0a80f-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="0a80f-115">Przykład 3: Tworzenie usługi zarządzania interfejsem API dla zewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0a80f-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="0a80f-116">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z zewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="0a80f-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="0a80f-117">Przykład 4: Tworzenie usługi zarządzania interfejsem API dla wewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0a80f-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="0a80f-118">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z wewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="0a80f-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="0a80f-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a80f-119">PARAMETERS</span></span>

### <span data-ttu-id="0a80f-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="0a80f-120">-AdditionalRegions</span></span>
<span data-ttu-id="0a80f-121">Dodatkowe regiony wdrażania usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="0a80f-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="0a80f-122">-AdminEmail</span></span>
<span data-ttu-id="0a80f-123">Określa źródłowy adres e-mail dla wszystkich powiadomień wysyłanych przez system zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0a80f-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-124">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="0a80f-124">-Capacity</span></span>
<span data-ttu-id="0a80f-125">Określa pojemność jednostki SKU usługi zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="0a80f-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="0a80f-126">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="0a80f-126">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0a80f-127">-Location</span></span>
<span data-ttu-id="0a80f-128">Określa lokalizację, w której to polecenie cmdlet tworzy wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0a80f-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="0a80f-129">Aby uzyskać prawidłowe lokalizacje, Użyj poleceń cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="0a80f-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="0a80f-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="0a80f-130">Valid values are:</span></span> 

- <span data-ttu-id="0a80f-131">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="0a80f-131">North Central US</span></span>
- <span data-ttu-id="0a80f-132">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="0a80f-132">South Central US</span></span>
- <span data-ttu-id="0a80f-133">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="0a80f-133">Central US</span></span>
- <span data-ttu-id="0a80f-134">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="0a80f-134">West Europe</span></span>
- <span data-ttu-id="0a80f-135">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="0a80f-135">North Europe</span></span>
- <span data-ttu-id="0a80f-136">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="0a80f-136">West US</span></span>
- <span data-ttu-id="0a80f-137">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="0a80f-137">East US</span></span>
- <span data-ttu-id="0a80f-138">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="0a80f-138">East US 2</span></span>
- <span data-ttu-id="0a80f-139">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="0a80f-139">Japan East</span></span>
- <span data-ttu-id="0a80f-140">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="0a80f-140">Japan West</span></span>
- <span data-ttu-id="0a80f-141">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="0a80f-141">Brazil South</span></span>
- <span data-ttu-id="0a80f-142">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="0a80f-142">Southeast Asia</span></span>
- <span data-ttu-id="0a80f-143">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="0a80f-143">East Asia</span></span>
- <span data-ttu-id="0a80f-144">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="0a80f-144">Australia East</span></span>
- <span data-ttu-id="0a80f-145">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="0a80f-145">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a80f-146">-Name</span></span>
<span data-ttu-id="0a80f-147">Określa nazwę wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0a80f-147">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-148">— Organizacja</span><span class="sxs-lookup"><span data-stu-id="0a80f-148">-Organization</span></span>
<span data-ttu-id="0a80f-149">Określa nazwę organizacji.</span><span class="sxs-lookup"><span data-stu-id="0a80f-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="0a80f-150">Funkcja zarządzania interfejsem API używa tego adresu w portalu dewelopera w obszarze powiadomienia e-mail.</span><span class="sxs-lookup"><span data-stu-id="0a80f-150">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a80f-151">-ResourceGroupName</span></span>
<span data-ttu-id="0a80f-152">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0a80f-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="0a80f-153">-Sku</span></span>
<span data-ttu-id="0a80f-154">Określa warstwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0a80f-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="0a80f-155">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="0a80f-155">Valid values are:</span></span> 

- <span data-ttu-id="0a80f-156">Deweloper</span><span class="sxs-lookup"><span data-stu-id="0a80f-156">Developer</span></span> 
- <span data-ttu-id="0a80f-157">Standard</span><span class="sxs-lookup"><span data-stu-id="0a80f-157">Standard</span></span> 
- <span data-ttu-id="0a80f-158">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="0a80f-158">Premium</span></span> 

<span data-ttu-id="0a80f-159">Domyślnym ustawieniem jest deweloper.</span><span class="sxs-lookup"><span data-stu-id="0a80f-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-160">-Tagi</span><span class="sxs-lookup"><span data-stu-id="0a80f-160">-Tags</span></span>
<span data-ttu-id="0a80f-161">Określa słownik znaczników.</span><span class="sxs-lookup"><span data-stu-id="0a80f-161">Specifies a dictionary of tags.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0a80f-162">-VirtualNetwork</span></span>
<span data-ttu-id="0a80f-163">Konfiguracja sieci wirtualnej w obszarze wdrażania zarządzania interfejsem głównym usługi Azure API.</span><span class="sxs-lookup"><span data-stu-id="0a80f-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="0a80f-164">-VpnType</span></span>
<span data-ttu-id="0a80f-165">Typ sieci wirtualnej wdrożenia ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a80f-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="0a80f-166">Prawidłowe wartości to</span><span class="sxs-lookup"><span data-stu-id="0a80f-166">Valid Values are</span></span> 
- <span data-ttu-id="0a80f-167">"Brak" (wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="0a80f-167">"None" (Default Value.</span></span> <span data-ttu-id="0a80f-168">ApiManagement nie jest częścią żadnej sieci wirtualnej ")</span><span class="sxs-lookup"><span data-stu-id="0a80f-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="0a80f-169">"Zewnętrzne" (ApiManagement wdrożenie to konfiguracja w sieci wirtualnej z internetowym punktem końcowym)</span><span class="sxs-lookup"><span data-stu-id="0a80f-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="0a80f-170">"Internal" (ApiManagement Deployment to Setup w sieci wirtualnej z punktem końcowym w intranecie)</span><span class="sxs-lookup"><span data-stu-id="0a80f-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a80f-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a80f-171">-DefaultProfile</span></span>
<span data-ttu-id="0a80f-172">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a80f-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a80f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a80f-173">CommonParameters</span></span>
<span data-ttu-id="0a80f-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a80f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a80f-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a80f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a80f-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a80f-176">INPUTS</span></span>

## <span data-ttu-id="0a80f-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a80f-177">OUTPUTS</span></span>

### <span data-ttu-id="0a80f-178">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a80f-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0a80f-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a80f-179">NOTES</span></span>

## <span data-ttu-id="0a80f-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a80f-180">RELATED LINKS</span></span>

[<span data-ttu-id="0a80f-181">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a80f-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="0a80f-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a80f-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="0a80f-183">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a80f-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="0a80f-184">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a80f-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


