---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: dbc5a10865874830c2f06a59f799722f61a3e9e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706924"
---
# <span data-ttu-id="e0006-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0006-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="e0006-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0006-102">SYNOPSIS</span></span>
<span data-ttu-id="e0006-103">Aktualizuje usługę zarządzania interfejsem API platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e0006-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="e0006-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0006-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0006-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e0006-105">DESCRIPTION</span></span>

<span data-ttu-id="e0006-106">Polecenie cmdlet **Set-AzApiManagement** aktualizuje usługę zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="e0006-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="e0006-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0006-107">EXAMPLES</span></span>

### <span data-ttu-id="e0006-108">Przykład 1 Uzyskiwanie usługi zarządzania interfejsem API i skalowanie jej do Premium i Dodawanie regionu</span><span class="sxs-lookup"><span data-stu-id="e0006-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="e0006-109">W tym przykładzie otrzymano instancję zarządzania interfejsem API, przeskaluje ją do pięciu jednostek Premium, a następnie dodaje kolejne trzy jednostki do regionu Premium.</span><span class="sxs-lookup"><span data-stu-id="e0006-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="e0006-110">Przykład 2: wdrożenie aktualizacji (zewnętrzna Sieć wirtualna)</span><span class="sxs-lookup"><span data-stu-id="e0006-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="e0006-111">To polecenie aktualizuje istniejące wdrożenie zarządzania interfejsem API i dołącza do zewnętrznego *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="e0006-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="e0006-112">Przykład 3: Tworzenie i Inicjowanie wystąpienia PsApiManagementCustomHostNameConfiguration przy użyciu klucza tajnego z zasobu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="e0006-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -AssignIdentity
```

### <span data-ttu-id="e0006-113">Przykład 4: aktualizowanie poczty E-mail w programie Publisher, NotificationSender E-mail i nazwa organizacji</span><span class="sxs-lookup"><span data-stu-id="e0006-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="e0006-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0006-114">PARAMETERS</span></span>

### <span data-ttu-id="e0006-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0006-115">-AsJob</span></span>
<span data-ttu-id="e0006-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e0006-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0006-117">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e0006-117">-AssignIdentity</span></span>
<span data-ttu-id="e0006-118">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0006-118">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e0006-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0006-119">-DefaultProfile</span></span>
<span data-ttu-id="e0006-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0006-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0006-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e0006-121">-InputObject</span></span>
<span data-ttu-id="e0006-122">Wystąpienie ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e0006-122">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="e0006-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0006-123">-PassThru</span></span>
<span data-ttu-id="e0006-124">Wysyła zaktualizowane PsApiManagement do rurociągu, jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="e0006-124">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="e0006-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0006-125">-Confirm</span></span>
<span data-ttu-id="e0006-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0006-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0006-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0006-127">-WhatIf</span></span>
<span data-ttu-id="e0006-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0006-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0006-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e0006-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0006-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0006-130">CommonParameters</span></span>
<span data-ttu-id="e0006-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0006-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0006-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0006-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0006-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0006-133">INPUTS</span></span>

### <span data-ttu-id="e0006-134">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0006-134">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e0006-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0006-135">OUTPUTS</span></span>

### <span data-ttu-id="e0006-136">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0006-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e0006-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0006-137">NOTES</span></span>

## <span data-ttu-id="e0006-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0006-138">RELATED LINKS</span></span>

[<span data-ttu-id="e0006-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0006-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="e0006-140">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0006-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="e0006-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0006-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)