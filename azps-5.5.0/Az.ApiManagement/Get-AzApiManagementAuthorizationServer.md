---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192531"
---
# <span data-ttu-id="01c30-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="01c30-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="01c30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c30-102">SYNOPSIS</span></span>
<span data-ttu-id="01c30-103">Otrzymuje serwer autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="01c30-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="01c30-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01c30-104">SYNTAX</span></span>

### <span data-ttu-id="01c30-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="01c30-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01c30-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01c30-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01c30-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="01c30-107">DESCRIPTION</span></span>
<span data-ttu-id="01c30-108">Polecenie **cmdlet Get-AzApiManagementAuthorizationServer** pobiera wszystkie serwery autoryzacji usługi Azure API Management lub określony serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="01c30-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="01c30-109">ClientSecret nie zostanie uwzględniony w szczegółach wyników.</span><span class="sxs-lookup"><span data-stu-id="01c30-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="01c30-110">Aby uzyskać klucz tajny klienta, użyj protokołu **Get-AzApiManagementAuthorizationServerClientSecret.**</span><span class="sxs-lookup"><span data-stu-id="01c30-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="01c30-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01c30-111">EXAMPLES</span></span>

### <span data-ttu-id="01c30-112">Przykład 1. Uzyskiwanie wszystkich serwerów autoryzacji</span><span class="sxs-lookup"><span data-stu-id="01c30-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="01c30-113">To polecenie otrzymuje wszystkie serwery autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="01c30-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="01c30-114">Przykład 2. Uzyskiwanie określonego serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="01c30-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="01c30-115">To polecenie pobiera określony serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="01c30-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="01c30-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01c30-116">PARAMETERS</span></span>

### <span data-ttu-id="01c30-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="01c30-117">-Context</span></span>

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

### <span data-ttu-id="01c30-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c30-118">-DefaultProfile</span></span>
<span data-ttu-id="01c30-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01c30-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01c30-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01c30-120">-ResourceId</span></span>
<span data-ttu-id="01c30-121">Identyfikator zasobu arm serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="01c30-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="01c30-122">Jeśli zostanie określona, spróbuje znaleźć serwer autoryzacji za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="01c30-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="01c30-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="01c30-123">This parameter is required.</span></span>

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

### <span data-ttu-id="01c30-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="01c30-124">-ServerId</span></span>
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

### <span data-ttu-id="01c30-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c30-125">CommonParameters</span></span>
<span data-ttu-id="01c30-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c30-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c30-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01c30-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c30-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01c30-128">INPUTS</span></span>

### <span data-ttu-id="01c30-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01c30-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="01c30-130">System.String</span><span class="sxs-lookup"><span data-stu-id="01c30-130">System.String</span></span>

## <span data-ttu-id="01c30-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01c30-131">OUTPUTS</span></span>

### <span data-ttu-id="01c30-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="01c30-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="01c30-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01c30-133">NOTES</span></span>

## <span data-ttu-id="01c30-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01c30-134">RELATED LINKS</span></span>

[<span data-ttu-id="01c30-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="01c30-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="01c30-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="01c30-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="01c30-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="01c30-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


