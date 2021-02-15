---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182347"
---
# <span data-ttu-id="8026a-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8026a-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="8026a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8026a-102">SYNOPSIS</span></span>
<span data-ttu-id="8026a-103">Usuwa dostawcę połączenia OpenID.</span><span class="sxs-lookup"><span data-stu-id="8026a-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="8026a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8026a-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8026a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8026a-105">DESCRIPTION</span></span>
<span data-ttu-id="8026a-106">Polecenie **cmdlet Remove-AzApiManagementOpenIdConnectProvider** usuwa dostawcę OpenID Connect dla usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="8026a-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="8026a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8026a-107">EXAMPLES</span></span>

### <span data-ttu-id="8026a-108">Przykład 1. Usuwanie dostawcy</span><span class="sxs-lookup"><span data-stu-id="8026a-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="8026a-109">To polecenie usuwa dostawcę, który ma identyfikator OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="8026a-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="8026a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8026a-110">PARAMETERS</span></span>

### <span data-ttu-id="8026a-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="8026a-111">-Context</span></span>
<span data-ttu-id="8026a-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="8026a-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8026a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8026a-113">-DefaultProfile</span></span>
<span data-ttu-id="8026a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8026a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8026a-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="8026a-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="8026a-116">Określa identyfikator dostawcy, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8026a-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8026a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8026a-117">-PassThru</span></span>
<span data-ttu-id="8026a-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="8026a-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8026a-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8026a-119">-Confirm</span></span>
<span data-ttu-id="8026a-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8026a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8026a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8026a-121">-WhatIf</span></span>
<span data-ttu-id="8026a-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8026a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8026a-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8026a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8026a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8026a-124">CommonParameters</span></span>
<span data-ttu-id="8026a-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8026a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8026a-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8026a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8026a-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8026a-127">INPUTS</span></span>

### <span data-ttu-id="8026a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8026a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8026a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8026a-129">System.String</span></span>

### <span data-ttu-id="8026a-130">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="8026a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8026a-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8026a-131">OUTPUTS</span></span>

### <span data-ttu-id="8026a-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8026a-132">System.Boolean</span></span>

## <span data-ttu-id="8026a-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8026a-133">NOTES</span></span>

## <span data-ttu-id="8026a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8026a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8026a-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8026a-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8026a-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8026a-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8026a-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8026a-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


