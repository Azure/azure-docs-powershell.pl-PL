---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 43393995fcc370e2b3ff2b20586ab696c39d059b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704622"
---
# <span data-ttu-id="f8b0b-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8b0b-101">New-AzApiManagement</span></span>

## <span data-ttu-id="f8b0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b0b-103">Tworzenie wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="f8b0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8b0b-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b0b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b0b-106">Polecenie cmdlet **New-AzApiManagement** tworzy wdrożenie zarządzania interfejsem API w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="f8b0b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8b0b-107">EXAMPLES</span></span>

### <span data-ttu-id="f8b0b-108">Przykład 1: Tworzenie usługi zarządzania interfejsem API dla warstwy dewelopera</span><span class="sxs-lookup"><span data-stu-id="f8b0b-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="f8b0b-109">To polecenie tworzy usługę zarządzania interfejsem API warstwy dewelopera.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="f8b0b-110">Polecenie określa nazwę organizacji i adres administratora.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="f8b0b-111">Polecenie nie określa parametru *SKU* .</span><span class="sxs-lookup"><span data-stu-id="f8b0b-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="f8b0b-112">Dlatego polecenie cmdlet używa domyślnej wartości dewelopera.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="f8b0b-113">Przykład 2: Tworzenie usługi warstwy standardowej zawierającej trzy jednostki</span><span class="sxs-lookup"><span data-stu-id="f8b0b-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="f8b0b-114">To polecenie tworzy standardową usługę zarządzania interfejsem API o trzech jednostkach.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="f8b0b-115">Przykład 3: Tworzenie usługi zarządzania interfejsem API dla zewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f8b0b-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="f8b0b-116">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z zewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="f8b0b-117">Przykład 4: Tworzenie usługi zarządzania interfejsem API dla wewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f8b0b-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="f8b0b-118">To polecenie tworzy usługę zarządzania interfejsem API w sieci wirtualnej platformy Azure z wewnętrznym punktem końcowym bramy z regionem głównym na zachodnim terenie.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="f8b0b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8b0b-119">PARAMETERS</span></span>

### <span data-ttu-id="f8b0b-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="f8b0b-120">-AdditionalRegions</span></span>
<span data-ttu-id="f8b0b-121">Dodatkowe regiony wdrażania usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="f8b0b-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="f8b0b-122">-AdminEmail</span></span>
<span data-ttu-id="f8b0b-123">Określa źródłowy adres e-mail dla wszystkich powiadomień wysyłanych przez system zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="f8b0b-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f8b0b-124">-AssignIdentity</span></span>
<span data-ttu-id="f8b0b-125">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="f8b0b-126">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="f8b0b-126">-Capacity</span></span>
<span data-ttu-id="f8b0b-127">Określa pojemność jednostki SKU usługi zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="f8b0b-128">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="f8b0b-128">The default is one (1).</span></span>

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

### <span data-ttu-id="f8b0b-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8b0b-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="f8b0b-130">Niestandardowe konfiguracje nazw hostów.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-130">Custom hostname configurations.</span></span> <span data-ttu-id="f8b0b-131">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-131">Default value is $null.</span></span> <span data-ttu-id="f8b0b-132">Przekazanie $null spowoduje ustawienie domyślnej nazwy hosta.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-132">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="f8b0b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b0b-133">-DefaultProfile</span></span>
<span data-ttu-id="f8b0b-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b0b-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f8b0b-135">-Location</span></span>
<span data-ttu-id="f8b0b-136">Określa lokalizację, w której ma zostać utworzona usługa zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="f8b0b-137">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="f8b0b-137">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="f8b0b-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8b0b-138">-Name</span></span>
<span data-ttu-id="f8b0b-139">Określa nazwę wdrożenia funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="f8b0b-140">— Organizacja</span><span class="sxs-lookup"><span data-stu-id="f8b0b-140">-Organization</span></span>
<span data-ttu-id="f8b0b-141">Określa nazwę organizacji.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="f8b0b-142">Funkcja zarządzania interfejsem API używa tego adresu w portalu dewelopera w obszarze powiadomienia e-mail.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="f8b0b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b0b-143">-ResourceGroupName</span></span>
<span data-ttu-id="f8b0b-144">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="f8b0b-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="f8b0b-145">-Sku</span></span>
<span data-ttu-id="f8b0b-146">Określa warstwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="f8b0b-147">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="f8b0b-147">Valid values are:</span></span> 
- <span data-ttu-id="f8b0b-148">Deweloper</span><span class="sxs-lookup"><span data-stu-id="f8b0b-148">Developer</span></span> 
- <span data-ttu-id="f8b0b-149">Standard</span><span class="sxs-lookup"><span data-stu-id="f8b0b-149">Standard</span></span> 
- <span data-ttu-id="f8b0b-150">Premium domyślnym jest deweloper.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-150">Premium The default is Developer.</span></span>

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

### <span data-ttu-id="f8b0b-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8b0b-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="f8b0b-152">Certyfikaty wystawione przez wewnętrzny urząd certyfikacji do zainstalowania w usłudze.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="f8b0b-153">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-153">Default value is $null.</span></span>

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

### <span data-ttu-id="f8b0b-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8b0b-154">-Tag</span></span>
<span data-ttu-id="f8b0b-155">Słownik znaczników.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="f8b0b-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f8b0b-156">-VirtualNetwork</span></span>
<span data-ttu-id="f8b0b-157">Konfiguracja sieci wirtualnej w obszarze wdrażania zarządzania interfejsem głównym usługi Azure API.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="f8b0b-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="f8b0b-158">-VpnType</span></span>
<span data-ttu-id="f8b0b-159">Typ sieci wirtualnej wdrożenia ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="f8b0b-160">Prawidłowe wartości to</span><span class="sxs-lookup"><span data-stu-id="f8b0b-160">Valid Values are</span></span> 
- <span data-ttu-id="f8b0b-161">"Brak" (wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-161">"None" (Default Value.</span></span> <span data-ttu-id="f8b0b-162">ApiManagement nie jest częścią żadnej sieci wirtualnej ")</span><span class="sxs-lookup"><span data-stu-id="f8b0b-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="f8b0b-163">"Zewnętrzne" (ApiManagement wdrożenie to konfiguracja w sieci wirtualnej z internetowym punktem końcowym)</span><span class="sxs-lookup"><span data-stu-id="f8b0b-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="f8b0b-164">"Internal" (ApiManagement Deployment to Setup w sieci wirtualnej z punktem końcowym w intranecie)</span><span class="sxs-lookup"><span data-stu-id="f8b0b-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="f8b0b-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b0b-165">CommonParameters</span></span>
<span data-ttu-id="f8b0b-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b0b-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b0b-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b0b-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8b0b-168">INPUTS</span></span>

### <span data-ttu-id="f8b0b-169">System. String</span><span class="sxs-lookup"><span data-stu-id="f8b0b-169">System.String</span></span>

### <span data-ttu-id="f8b0b-170">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. MODELES. PsApiManagementSku, Microsoft. Azure. PowerShell. cmdlet. ApiManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f8b0b-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f8b0b-171">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f8b0b-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f8b0b-172">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f8b0b-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="f8b0b-173">System. Collections. Generic. dictionary ' 2 [[System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = 7cec85d7bea7798e], [System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f8b0b-173">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f8b0b-174">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="f8b0b-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="f8b0b-175">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f8b0b-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="f8b0b-176">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="f8b0b-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="f8b0b-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8b0b-177">OUTPUTS</span></span>

### <span data-ttu-id="f8b0b-178">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8b0b-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f8b0b-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8b0b-179">NOTES</span></span>

## <span data-ttu-id="f8b0b-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8b0b-180">RELATED LINKS</span></span>

[<span data-ttu-id="f8b0b-181">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8b0b-181">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="f8b0b-182">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8b0b-182">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="f8b0b-183">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8b0b-183">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="f8b0b-184">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8b0b-184">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="f8b0b-185">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8b0b-185">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


