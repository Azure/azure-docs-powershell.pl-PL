---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 98e90b4c8275028ab3e62e7383505775271e8d09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717280"
---
# <span data-ttu-id="50467-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="50467-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="50467-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50467-102">SYNOPSIS</span></span>
<span data-ttu-id="50467-103">Tworzenie wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="50467-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50467-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50467-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50467-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50467-105">DESCRIPTION</span></span>
<span data-ttu-id="50467-106">Polecenie cmdlet **New-AzureRmApiManagement** tworzy wdrożenie zarządzania interfejsem API w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="50467-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="50467-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50467-107">EXAMPLES</span></span>

### <span data-ttu-id="50467-108">Przykład 1: Tworzenie usługi zarządzania interfejsem API dla warstwy dewelopera</span><span class="sxs-lookup"><span data-stu-id="50467-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="50467-109">To polecenie tworzy usługę zarządzania interfejsem API warstwy dewelopera.</span><span class="sxs-lookup"><span data-stu-id="50467-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="50467-110">Polecenie określa nazwę organizacji i adres administratora.</span><span class="sxs-lookup"><span data-stu-id="50467-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="50467-111">Polecenie nie określa parametru *SKU* .</span><span class="sxs-lookup"><span data-stu-id="50467-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="50467-112">Dlatego polecenie cmdlet używa domyślnej wartości dewelopera.</span><span class="sxs-lookup"><span data-stu-id="50467-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="50467-113">Przykład 2: Tworzenie usługi warstwy standardowej zawierającej trzy jednostki</span><span class="sxs-lookup"><span data-stu-id="50467-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="50467-114">To polecenie tworzy standardową usługę zarządzania interfejsem API o trzech jednostkach.</span><span class="sxs-lookup"><span data-stu-id="50467-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="50467-115">Przykład 3: Tworzenie usługi zarządzania interfejsem API dla zewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="50467-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="50467-116">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z zewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="50467-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="50467-117">Przykład 4: Tworzenie usługi zarządzania interfejsem API dla wewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="50467-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="50467-118">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z wewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="50467-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="50467-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50467-119">PARAMETERS</span></span>

### <span data-ttu-id="50467-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="50467-120">-AdditionalRegions</span></span>
<span data-ttu-id="50467-121">Dodatkowe regiony wdrażania usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="50467-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="50467-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="50467-122">-AdminEmail</span></span>
<span data-ttu-id="50467-123">Określa źródłowy adres e-mail dla wszystkich powiadomień wysyłanych przez system zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="50467-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="50467-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="50467-124">-AssignIdentity</span></span>
<span data-ttu-id="50467-125">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="50467-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="50467-126">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="50467-126">-Capacity</span></span>
<span data-ttu-id="50467-127">Określa pojemność jednostki SKU usługi zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="50467-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="50467-128">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="50467-128">The default is one (1).</span></span>

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

### <span data-ttu-id="50467-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="50467-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="50467-130">Niestandardowe konfiguracje nazw hostów.</span><span class="sxs-lookup"><span data-stu-id="50467-130">Custom hostname configurations.</span></span> <span data-ttu-id="50467-131">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="50467-131">Default value is $null.</span></span> <span data-ttu-id="50467-132">Przekazanie $null spowoduje ustawienie domyślnej nazwy hosta.</span><span class="sxs-lookup"><span data-stu-id="50467-132">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50467-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50467-133">-DefaultProfile</span></span>
<span data-ttu-id="50467-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50467-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50467-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="50467-135">-Location</span></span>
<span data-ttu-id="50467-136">Określa lokalizację, w której ma zostać utworzona usługa zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="50467-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="50467-137">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="50467-137">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="50467-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50467-138">-Name</span></span>
<span data-ttu-id="50467-139">Określa nazwę wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="50467-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="50467-140">— Organizacja</span><span class="sxs-lookup"><span data-stu-id="50467-140">-Organization</span></span>
<span data-ttu-id="50467-141">Określa nazwę organizacji.</span><span class="sxs-lookup"><span data-stu-id="50467-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="50467-142">Funkcja zarządzania interfejsem API używa tego adresu w portalu dewelopera w obszarze powiadomienia e-mail.</span><span class="sxs-lookup"><span data-stu-id="50467-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="50467-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50467-143">-ResourceGroupName</span></span>
<span data-ttu-id="50467-144">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="50467-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="50467-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="50467-145">-Sku</span></span>
<span data-ttu-id="50467-146">Określa warstwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="50467-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="50467-147">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="50467-147">Valid values are:</span></span> 
- <span data-ttu-id="50467-148">Deweloper</span><span class="sxs-lookup"><span data-stu-id="50467-148">Developer</span></span> 
- <span data-ttu-id="50467-149">Standard</span><span class="sxs-lookup"><span data-stu-id="50467-149">Standard</span></span> 
- <span data-ttu-id="50467-150">Premium domyślnym jest deweloper.</span><span class="sxs-lookup"><span data-stu-id="50467-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50467-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="50467-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="50467-152">Certyfikaty wystawione przez wewnętrzny urząd certyfikacji do zainstalowania w usłudze.</span><span class="sxs-lookup"><span data-stu-id="50467-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="50467-153">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="50467-153">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50467-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="50467-154">-Tag</span></span>
<span data-ttu-id="50467-155">Słownik znaczników.</span><span class="sxs-lookup"><span data-stu-id="50467-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="50467-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="50467-156">-VirtualNetwork</span></span>
<span data-ttu-id="50467-157">Konfiguracja sieci wirtualnej w obszarze wdrażania zarządzania interfejsem głównym usługi Azure API.</span><span class="sxs-lookup"><span data-stu-id="50467-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="50467-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="50467-158">-VpnType</span></span>
<span data-ttu-id="50467-159">Typ sieci wirtualnej wdrożenia ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="50467-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="50467-160">Prawidłowe wartości to</span><span class="sxs-lookup"><span data-stu-id="50467-160">Valid Values are</span></span> 
- <span data-ttu-id="50467-161">"Brak" (wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="50467-161">"None" (Default Value.</span></span> <span data-ttu-id="50467-162">ApiManagement nie jest częścią żadnej sieci wirtualnej ")</span><span class="sxs-lookup"><span data-stu-id="50467-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="50467-163">"Zewnętrzne" (ApiManagement wdrożenie to konfiguracja w sieci wirtualnej z internetowym punktem końcowym)</span><span class="sxs-lookup"><span data-stu-id="50467-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="50467-164">"Internal" (ApiManagement Deployment to Setup w sieci wirtualnej z punktem końcowym w intranecie)</span><span class="sxs-lookup"><span data-stu-id="50467-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="50467-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50467-165">CommonParameters</span></span>
<span data-ttu-id="50467-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50467-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50467-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50467-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50467-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50467-168">INPUTS</span></span>

### <span data-ttu-id="50467-169">System. String</span><span class="sxs-lookup"><span data-stu-id="50467-169">System.String</span></span>

### <span data-ttu-id="50467-170">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. MODELES. PsApiManagementSku, Microsoft. Azure. Commands. ApiManagement, Version = 6.1.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="50467-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="50467-171">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="50467-171">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="50467-172">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="50467-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="50467-173">System. Collections. Generic. dictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="50467-173">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="50467-174">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="50467-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="50467-175">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="50467-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="50467-176">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="50467-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="50467-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50467-177">OUTPUTS</span></span>

### <span data-ttu-id="50467-178">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="50467-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="50467-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50467-179">NOTES</span></span>

## <span data-ttu-id="50467-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50467-180">RELATED LINKS</span></span>

[<span data-ttu-id="50467-181">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="50467-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="50467-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="50467-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="50467-183">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="50467-183">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)

[<span data-ttu-id="50467-184">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="50467-184">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="50467-185">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="50467-185">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


