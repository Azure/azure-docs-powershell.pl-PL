---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f148f65a6065040a28f936a5dec64f09ff4045eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706947"
---
# <span data-ttu-id="66a18-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="66a18-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="66a18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66a18-102">SYNOPSIS</span></span>
<span data-ttu-id="66a18-103">Usuwa dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="66a18-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="66a18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66a18-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a18-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66a18-105">DESCRIPTION</span></span>
<span data-ttu-id="66a18-106">Polecenie cmdlet **Remove-AzApiManagementOpenIdConnectProvider** Usuwa dostawcę Connect usługi OpenID dla zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="66a18-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="66a18-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66a18-107">EXAMPLES</span></span>

### <span data-ttu-id="66a18-108">Przykład 1. Usuń dostawcę</span><span class="sxs-lookup"><span data-stu-id="66a18-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="66a18-109">To polecenie usuwa dostawcę o IDENTYFIKATORze OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="66a18-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="66a18-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66a18-110">PARAMETERS</span></span>

### <span data-ttu-id="66a18-111">-Context</span><span class="sxs-lookup"><span data-stu-id="66a18-111">-Context</span></span>
<span data-ttu-id="66a18-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="66a18-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="66a18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a18-113">-DefaultProfile</span></span>
<span data-ttu-id="66a18-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66a18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a18-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="66a18-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="66a18-116">Określa identyfikator dostawcy, który usunie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a18-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66a18-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66a18-117">-PassThru</span></span>
<span data-ttu-id="66a18-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="66a18-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="66a18-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66a18-119">-Confirm</span></span>
<span data-ttu-id="66a18-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a18-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a18-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a18-121">-WhatIf</span></span>
<span data-ttu-id="66a18-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a18-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a18-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="66a18-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a18-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a18-124">CommonParameters</span></span>
<span data-ttu-id="66a18-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a18-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a18-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66a18-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a18-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66a18-127">INPUTS</span></span>

### <span data-ttu-id="66a18-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66a18-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66a18-129">System. String</span><span class="sxs-lookup"><span data-stu-id="66a18-129">System.String</span></span>

### <span data-ttu-id="66a18-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66a18-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66a18-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66a18-131">OUTPUTS</span></span>

### <span data-ttu-id="66a18-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66a18-132">System.Boolean</span></span>

## <span data-ttu-id="66a18-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66a18-133">NOTES</span></span>

## <span data-ttu-id="66a18-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66a18-134">RELATED LINKS</span></span>

[<span data-ttu-id="66a18-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="66a18-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="66a18-136">Nowe — AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="66a18-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="66a18-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="66a18-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


