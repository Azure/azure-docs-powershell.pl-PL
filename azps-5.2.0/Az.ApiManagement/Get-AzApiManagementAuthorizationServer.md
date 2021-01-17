---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338794"
---
# <span data-ttu-id="948ad-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="948ad-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="948ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="948ad-102">SYNOPSIS</span></span>
<span data-ttu-id="948ad-103">Pobiera serwer autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="948ad-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="948ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="948ad-104">SYNTAX</span></span>

### <span data-ttu-id="948ad-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="948ad-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="948ad-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="948ad-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="948ad-107">Opis</span><span class="sxs-lookup"><span data-stu-id="948ad-107">DESCRIPTION</span></span>
<span data-ttu-id="948ad-108">Polecenie cmdlet **Get-AzApiManagementAuthorizationServer** pobiera wszystkie serwery autoryzacji zarządzania API platformy Azure lub określony serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="948ad-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="948ad-109">ClientSecret nie zostaną uwzględnione w szczegółach wyników.</span><span class="sxs-lookup"><span data-stu-id="948ad-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="948ad-110">Aby uzyskać klucz tajny klienta, użyj polecenie **Get-AzApiManagementAuthorizationServerClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="948ad-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="948ad-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="948ad-111">EXAMPLES</span></span>

### <span data-ttu-id="948ad-112">Przykład 1: pobieranie wszystkich serwerów autoryzacji</span><span class="sxs-lookup"><span data-stu-id="948ad-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="948ad-113">To polecenie pobiera wszystkie serwery autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="948ad-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="948ad-114">Przykład 2: uzyskiwanie określonego serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="948ad-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="948ad-115">To polecenie pobiera określony serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="948ad-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="948ad-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="948ad-116">PARAMETERS</span></span>

### <span data-ttu-id="948ad-117">-Context</span><span class="sxs-lookup"><span data-stu-id="948ad-117">-Context</span></span>

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

### <span data-ttu-id="948ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948ad-118">-DefaultProfile</span></span>
<span data-ttu-id="948ad-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="948ad-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="948ad-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="948ad-120">-ResourceId</span></span>
<span data-ttu-id="948ad-121">Identyfikator zasobu ARM serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="948ad-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="948ad-122">Jeśli zostanie określona, spróbuje znaleźć serwer autoryzacji według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="948ad-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="948ad-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="948ad-123">This parameter is required.</span></span>

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

### <span data-ttu-id="948ad-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="948ad-124">-ServerId</span></span>
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

### <span data-ttu-id="948ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948ad-125">CommonParameters</span></span>
<span data-ttu-id="948ad-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948ad-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="948ad-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948ad-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="948ad-128">INPUTS</span></span>

### <span data-ttu-id="948ad-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="948ad-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="948ad-130">System. String</span><span class="sxs-lookup"><span data-stu-id="948ad-130">System.String</span></span>

## <span data-ttu-id="948ad-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="948ad-131">OUTPUTS</span></span>

### <span data-ttu-id="948ad-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="948ad-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="948ad-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="948ad-133">NOTES</span></span>

## <span data-ttu-id="948ad-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="948ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="948ad-135">Nowe — AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="948ad-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="948ad-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="948ad-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="948ad-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="948ad-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


