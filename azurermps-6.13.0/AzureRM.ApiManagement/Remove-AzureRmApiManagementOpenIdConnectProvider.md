---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6b4ccac87f963f9948c67d3162f1677b9860583b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524681"
---
# <span data-ttu-id="b9409-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b9409-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b9409-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9409-102">SYNOPSIS</span></span>
<span data-ttu-id="b9409-103">Usuwa dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="b9409-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9409-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9409-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9409-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9409-105">DESCRIPTION</span></span>
<span data-ttu-id="b9409-106">Polecenie cmdlet **Remove-AzureRmApiManagementOpenIdConnectProvider** Usuwa dostawcę Connect usługi OpenID dla zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="b9409-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="b9409-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9409-107">EXAMPLES</span></span>

### <span data-ttu-id="b9409-108">Przykład 1. Usuń dostawcę</span><span class="sxs-lookup"><span data-stu-id="b9409-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="b9409-109">To polecenie usuwa dostawcę o IDENTYFIKATORze OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="b9409-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="b9409-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9409-110">PARAMETERS</span></span>

### <span data-ttu-id="b9409-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b9409-111">-Context</span></span>
<span data-ttu-id="b9409-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b9409-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9409-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9409-113">-DefaultProfile</span></span>
<span data-ttu-id="b9409-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9409-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9409-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b9409-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b9409-116">Określa identyfikator dostawcy, który usunie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9409-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b9409-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9409-117">-PassThru</span></span>
<span data-ttu-id="b9409-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="b9409-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="b9409-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9409-119">-Confirm</span></span>
<span data-ttu-id="b9409-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9409-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9409-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9409-121">-WhatIf</span></span>
<span data-ttu-id="b9409-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9409-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9409-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9409-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9409-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9409-124">CommonParameters</span></span>
<span data-ttu-id="b9409-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9409-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9409-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9409-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9409-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9409-127">INPUTS</span></span>

### <span data-ttu-id="b9409-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b9409-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b9409-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b9409-129">System.String</span></span>

### <span data-ttu-id="b9409-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b9409-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b9409-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9409-131">OUTPUTS</span></span>

### <span data-ttu-id="b9409-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9409-132">System.Boolean</span></span>

## <span data-ttu-id="b9409-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9409-133">NOTES</span></span>

## <span data-ttu-id="b9409-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9409-134">RELATED LINKS</span></span>

[<span data-ttu-id="b9409-135">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b9409-135">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b9409-136">Nowe — AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b9409-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b9409-137">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b9409-137">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


