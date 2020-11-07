---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717969"
---
# <span data-ttu-id="1f8f2-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1f8f2-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="1f8f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8f2-103">Aktualizuje usługę zarządzania interfejsem API platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1f8f2-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f8f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f8f2-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f8f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f8f2-105">DESCRIPTION</span></span>

<span data-ttu-id="1f8f2-106">Polecenie cmdlet **Set-AzureRmApiManagement** aktualizuje usługę zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="1f8f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f8f2-107">EXAMPLES</span></span>

### <span data-ttu-id="1f8f2-108">Przykład 1 Uzyskiwanie usługi zarządzania interfejsem API i skalowanie jej do Premium i Dodawanie regionu</span><span class="sxs-lookup"><span data-stu-id="1f8f2-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="1f8f2-109">W tym przykładzie otrzymano instancję zarządzania interfejsem API, przeskaluje ją do pięciu jednostek Premium, a następnie dodaje kolejne trzy jednostki do regionu Premium.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="1f8f2-110">Przykład 2: wdrożenie aktualizacji (zewnętrzna Sieć wirtualna)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="1f8f2-111">To polecenie aktualizuje istniejące wdrożenie zarządzania interfejsem API i dołącza do zewnętrznego *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="1f8f2-112">Przykład 3: Tworzenie i Inicjowanie wystąpienia PsApiManagementCustomHostNameConfiguration przy użyciu klucza tajnego z zasobu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="1f8f2-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="1f8f2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f8f2-113">PARAMETERS</span></span>

### <span data-ttu-id="1f8f2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f8f2-114">-AsJob</span></span>
<span data-ttu-id="1f8f2-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1f8f2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f8f2-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1f8f2-116">-AssignIdentity</span></span>
<span data-ttu-id="1f8f2-117">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1f8f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8f2-118">-DefaultProfile</span></span>
<span data-ttu-id="1f8f2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f8f2-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1f8f2-120">-InputObject</span></span>
<span data-ttu-id="1f8f2-121">Wystąpienie ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-121">The ApiManagement instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8f2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f8f2-122">-PassThru</span></span>
<span data-ttu-id="1f8f2-123">Wysyła zaktualizowane PsApiManagement do rurociągu, jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="1f8f2-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f8f2-124">-Confirm</span></span>
<span data-ttu-id="1f8f2-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f8f2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f8f2-126">-WhatIf</span></span>
<span data-ttu-id="1f8f2-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f8f2-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f8f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8f2-129">CommonParameters</span></span>
<span data-ttu-id="1f8f2-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8f2-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f8f2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8f2-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f8f2-132">INPUTS</span></span>

### <span data-ttu-id="1f8f2-133">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1f8f2-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="1f8f2-134">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1f8f2-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f8f2-135">OUTPUTS</span></span>

### <span data-ttu-id="1f8f2-136">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1f8f2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1f8f2-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f8f2-137">NOTES</span></span>

## <span data-ttu-id="1f8f2-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f8f2-138">RELATED LINKS</span></span>

[<span data-ttu-id="1f8f2-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1f8f2-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="1f8f2-140">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1f8f2-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="1f8f2-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1f8f2-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)
