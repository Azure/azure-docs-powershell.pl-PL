---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178027"
---
# <span data-ttu-id="06d59-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="06d59-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="06d59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d59-102">SYNOPSIS</span></span>
<span data-ttu-id="06d59-103">Aktualizacje usługi Azure Api Management</span><span class="sxs-lookup"><span data-stu-id="06d59-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="06d59-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06d59-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06d59-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="06d59-105">DESCRIPTION</span></span>

<span data-ttu-id="06d59-106">Polecenie **cmdlet Set-AzApiManagement** aktualizuje usługę Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="06d59-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="06d59-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06d59-107">EXAMPLES</span></span>

### <span data-ttu-id="06d59-108">Przykład 1. Uzyskaj usługę zarządzania interfejsem API i przeskaluj ją do wersji Premium i dodaj region</span><span class="sxs-lookup"><span data-stu-id="06d59-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="06d59-109">Ten przykład uzyskuje wystąpienie zarządzania interfejsem API, skaluje je do pięciu jednostek premium, a następnie dodaje dodatkowe trzy jednostki do regionu premium.</span><span class="sxs-lookup"><span data-stu-id="06d59-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="06d59-110">Przykład 2. Aktualizowanie wdrożenia (zewnętrzna sieć VNET)</span><span class="sxs-lookup"><span data-stu-id="06d59-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="06d59-111">To polecenie aktualizuje istniejące wdrożenie zarządzania interfejsem API i dołącza do zewnętrznego typu *VpnType.*</span><span class="sxs-lookup"><span data-stu-id="06d59-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="06d59-112">Przykład 3. Tworzenie i inicjowanie wystąpienia parametru PsApiManagementCustomHostNameConfiguration przy użyciu klucza tajnego z zasobu KeyVault</span><span class="sxs-lookup"><span data-stu-id="06d59-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="06d59-113">Przykład 4. Aktualizowanie adresu e-mail programu Publisher, adresu e-mail programu NotificationSender i nazwy organizacji</span><span class="sxs-lookup"><span data-stu-id="06d59-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="06d59-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06d59-114">PARAMETERS</span></span>

### <span data-ttu-id="06d59-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="06d59-115">-AsJob</span></span>
<span data-ttu-id="06d59-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="06d59-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06d59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d59-117">-DefaultProfile</span></span>
<span data-ttu-id="06d59-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06d59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d59-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06d59-119">-InputObject</span></span>
<span data-ttu-id="06d59-120">Wystąpienie ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="06d59-120">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="06d59-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06d59-121">-PassThru</span></span>
<span data-ttu-id="06d59-122">Wysyła zaktualizowaną wiadomość PsApiManagement do potoku, jeśli operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="06d59-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="06d59-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="06d59-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="06d59-124">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do używania z usługami zarządzania kluczami, np. Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="06d59-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="06d59-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="06d59-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="06d59-126">Przypisz tożsamości użytkowników do tego serwera do używania z usługami zarządzania kluczami, np. Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="06d59-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d59-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06d59-127">-Confirm</span></span>
<span data-ttu-id="06d59-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06d59-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06d59-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d59-129">-WhatIf</span></span>
<span data-ttu-id="06d59-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06d59-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06d59-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06d59-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06d59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d59-132">CommonParameters</span></span>
<span data-ttu-id="06d59-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d59-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06d59-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d59-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06d59-135">INPUTS</span></span>

### <span data-ttu-id="06d59-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="06d59-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="06d59-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06d59-137">OUTPUTS</span></span>

### <span data-ttu-id="06d59-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="06d59-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="06d59-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06d59-139">NOTES</span></span>

## <span data-ttu-id="06d59-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06d59-140">RELATED LINKS</span></span>

[<span data-ttu-id="06d59-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="06d59-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="06d59-142">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="06d59-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="06d59-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="06d59-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
