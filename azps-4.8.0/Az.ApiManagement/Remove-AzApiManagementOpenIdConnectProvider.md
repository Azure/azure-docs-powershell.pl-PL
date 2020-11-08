---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063009"
---
# <span data-ttu-id="bbc6c-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bbc6c-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bbc6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbc6c-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc6c-103">Usuwa dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="bbc6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbc6c-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbc6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bbc6c-105">DESCRIPTION</span></span>
<span data-ttu-id="bbc6c-106">Polecenie cmdlet **Remove-AzApiManagementOpenIdConnectProvider** Usuwa dostawcę Connect usługi OpenID dla zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="bbc6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbc6c-107">EXAMPLES</span></span>

### <span data-ttu-id="bbc6c-108">Przykład 1. Usuń dostawcę</span><span class="sxs-lookup"><span data-stu-id="bbc6c-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="bbc6c-109">To polecenie usuwa dostawcę o IDENTYFIKATORze OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="bbc6c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbc6c-110">PARAMETERS</span></span>

### <span data-ttu-id="bbc6c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="bbc6c-111">-Context</span></span>
<span data-ttu-id="bbc6c-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bbc6c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bbc6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc6c-113">-DefaultProfile</span></span>
<span data-ttu-id="bbc6c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbc6c-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bbc6c-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="bbc6c-116">Określa identyfikator dostawcy, który usunie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bbc6c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbc6c-117">-PassThru</span></span>
<span data-ttu-id="bbc6c-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="bbc6c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbc6c-119">-Confirm</span></span>
<span data-ttu-id="bbc6c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc6c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc6c-121">-WhatIf</span></span>
<span data-ttu-id="bbc6c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc6c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbc6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc6c-124">CommonParameters</span></span>
<span data-ttu-id="bbc6c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc6c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbc6c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc6c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbc6c-127">INPUTS</span></span>

### <span data-ttu-id="bbc6c-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bbc6c-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bbc6c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bbc6c-129">System.String</span></span>

### <span data-ttu-id="bbc6c-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bbc6c-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bbc6c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbc6c-131">OUTPUTS</span></span>

### <span data-ttu-id="bbc6c-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbc6c-132">System.Boolean</span></span>

## <span data-ttu-id="bbc6c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbc6c-133">NOTES</span></span>

## <span data-ttu-id="bbc6c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbc6c-134">RELATED LINKS</span></span>

[<span data-ttu-id="bbc6c-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bbc6c-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bbc6c-136">Nowe — AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bbc6c-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bbc6c-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bbc6c-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


