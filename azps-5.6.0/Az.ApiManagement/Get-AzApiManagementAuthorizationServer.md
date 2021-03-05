---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 098fb692e1710b9463650f0e398d999f0a2b1062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983770"
---
# <span data-ttu-id="aa60d-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aa60d-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="aa60d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa60d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa60d-103">Otrzymuje serwer autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aa60d-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="aa60d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa60d-104">SYNTAX</span></span>

### <span data-ttu-id="aa60d-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="aa60d-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa60d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa60d-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa60d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa60d-107">DESCRIPTION</span></span>
<span data-ttu-id="aa60d-108">Polecenie **cmdlet Get-AzApiManagementAuthorizationServer** pobiera wszystkie serwery autoryzacji usługi Azure API Management lub określony serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="aa60d-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="aa60d-109">ClientSecret nie zostanie uwzględniony w szczegółach wyników.</span><span class="sxs-lookup"><span data-stu-id="aa60d-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="aa60d-110">Aby uzyskać klucz tajny klienta, użyj protokołu **Get-AzApiManagementAuthorizationServerClientSecret.**</span><span class="sxs-lookup"><span data-stu-id="aa60d-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="aa60d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa60d-111">EXAMPLES</span></span>

### <span data-ttu-id="aa60d-112">Przykład 1. Uzyskiwanie wszystkich serwerów autoryzacji</span><span class="sxs-lookup"><span data-stu-id="aa60d-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="aa60d-113">To polecenie otrzymuje wszystkie serwery autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aa60d-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="aa60d-114">Przykład 2. Uzyskiwanie określonego serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="aa60d-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="aa60d-115">To polecenie pobiera określony serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="aa60d-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="aa60d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa60d-116">PARAMETERS</span></span>

### <span data-ttu-id="aa60d-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="aa60d-117">-Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa60d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa60d-118">-DefaultProfile</span></span>
<span data-ttu-id="aa60d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa60d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa60d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa60d-120">-ResourceId</span></span>
<span data-ttu-id="aa60d-121">Identyfikator zasobu arm serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="aa60d-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="aa60d-122">Jeśli zostanie określona, spróbuje znaleźć serwer autoryzacji za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="aa60d-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="aa60d-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="aa60d-123">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa60d-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="aa60d-124">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa60d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa60d-125">CommonParameters</span></span>
<span data-ttu-id="aa60d-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa60d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa60d-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa60d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa60d-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa60d-128">INPUTS</span></span>

### <span data-ttu-id="aa60d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa60d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa60d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="aa60d-130">System.String</span></span>

## <span data-ttu-id="aa60d-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa60d-131">OUTPUTS</span></span>

### <span data-ttu-id="aa60d-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aa60d-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="aa60d-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa60d-133">NOTES</span></span>

## <span data-ttu-id="aa60d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa60d-134">RELATED LINKS</span></span>

[<span data-ttu-id="aa60d-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aa60d-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="aa60d-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aa60d-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="aa60d-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aa60d-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


