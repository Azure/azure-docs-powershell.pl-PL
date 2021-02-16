---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201315"
---
# <span data-ttu-id="b3e16-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="b3e16-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="b3e16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e16-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e16-103">Uzyskuje klucz tajny klienta dostawcy OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="b3e16-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="b3e16-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b3e16-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3e16-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b3e16-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e16-106">Uzyskuje klucz tajny klienta dostawcy OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="b3e16-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="b3e16-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b3e16-107">EXAMPLES</span></span>

### <span data-ttu-id="b3e16-108">Przykład 1. Klucz tajny klienta dostawcy przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="b3e16-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="b3e16-109">To polecenie uzyskuje klucz tajny klienta dostawcy, który ma identyfikator OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="b3e16-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="b3e16-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3e16-110">PARAMETERS</span></span>

### <span data-ttu-id="b3e16-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b3e16-111">-Context</span></span>
<span data-ttu-id="b3e16-112">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b3e16-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b3e16-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b3e16-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b3e16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e16-114">-DefaultProfile</span></span>
<span data-ttu-id="b3e16-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e16-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e16-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b3e16-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b3e16-117">Identyfikator dostawcy OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="b3e16-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="b3e16-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b3e16-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b3e16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e16-119">CommonParameters</span></span>
<span data-ttu-id="b3e16-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e16-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3e16-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e16-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3e16-122">INPUTS</span></span>

### <span data-ttu-id="b3e16-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b3e16-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b3e16-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b3e16-124">System.String</span></span>

## <span data-ttu-id="b3e16-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3e16-125">OUTPUTS</span></span>

### <span data-ttu-id="b3e16-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="b3e16-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="b3e16-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b3e16-127">NOTES</span></span>

## <span data-ttu-id="b3e16-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3e16-128">RELATED LINKS</span></span>
