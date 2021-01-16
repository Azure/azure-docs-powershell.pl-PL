---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322579"
---
# <span data-ttu-id="e5e94-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="e5e94-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="e5e94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5e94-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e94-103">Pobiera klucz tajny klienta z OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="e5e94-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="e5e94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5e94-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5e94-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5e94-105">DESCRIPTION</span></span>
<span data-ttu-id="e5e94-106">Pobiera klucz tajny klienta z OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="e5e94-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="e5e94-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5e94-107">EXAMPLES</span></span>

### <span data-ttu-id="e5e94-108">Przykład 1: Uzyskiwanie klucza tajnego klienta dostawcy przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="e5e94-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="e5e94-109">To polecenie pobiera klucz tajny klienta dla dostawcy o IDENTYFIKATORze OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="e5e94-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="e5e94-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5e94-110">PARAMETERS</span></span>

### <span data-ttu-id="e5e94-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e5e94-111">-Context</span></span>
<span data-ttu-id="e5e94-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e5e94-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e5e94-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e5e94-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e5e94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e94-114">-DefaultProfile</span></span>
<span data-ttu-id="e5e94-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e94-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5e94-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="e5e94-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="e5e94-117">Identyfikator dostawcy usługi OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="e5e94-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="e5e94-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e5e94-118">This parameter is required.</span></span>

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

### <span data-ttu-id="e5e94-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e94-119">CommonParameters</span></span>
<span data-ttu-id="e5e94-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e94-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e94-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5e94-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e94-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5e94-122">INPUTS</span></span>

### <span data-ttu-id="e5e94-123">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e5e94-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e5e94-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e94-124">System.String</span></span>

## <span data-ttu-id="e5e94-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5e94-125">OUTPUTS</span></span>

### <span data-ttu-id="e5e94-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="e5e94-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="e5e94-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5e94-127">NOTES</span></span>

## <span data-ttu-id="e5e94-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5e94-128">RELATED LINKS</span></span>
