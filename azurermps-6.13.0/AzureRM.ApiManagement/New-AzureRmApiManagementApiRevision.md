---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: 2ee3954569067000d445ecd7dab034db41734829
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542055"
---
# <span data-ttu-id="7d9e2-101">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7d9e2-101">New-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="7d9e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9e2-103">Tworzy nową poprawkę istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-103">Creates a new Revision of an Existing API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d9e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d9e2-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d9e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d9e2-105">DESCRIPTION</span></span>

<span data-ttu-id="7d9e2-106">Polecenie cmdlet **New-AzureRmApiManagementApiRevision** tworzy poprawkę API dla istniejącego interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-106">The **New-AzureRmApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="7d9e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="7d9e2-108">Przykład 1: Tworzenie poprawki interfejsu API dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="7d9e2-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="7d9e2-109">To polecenie tworzy wersję API `2` `echo-api` interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="7d9e2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d9e2-110">PARAMETERS</span></span>

### <span data-ttu-id="7d9e2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7d9e2-111">-ApiId</span></span>
<span data-ttu-id="7d9e2-112">Identyfikator interfejsu API, dla którego ma zostać utworzona poprawka.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="7d9e2-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7d9e2-113">-ApiRevision</span></span>
<span data-ttu-id="7d9e2-114">Identyfikator poprawki API.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="7d9e2-115">-Context</span><span class="sxs-lookup"><span data-stu-id="7d9e2-115">-Context</span></span>
<span data-ttu-id="7d9e2-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7d9e2-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9e2-118">-DefaultProfile</span></span>
<span data-ttu-id="7d9e2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d9e2-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d9e2-120">-Confirm</span></span>
<span data-ttu-id="7d9e2-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d9e2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d9e2-122">-WhatIf</span></span>
<span data-ttu-id="7d9e2-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d9e2-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d9e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9e2-125">CommonParameters</span></span>
<span data-ttu-id="7d9e2-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d9e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9e2-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d9e2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9e2-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d9e2-128">INPUTS</span></span>

### <span data-ttu-id="7d9e2-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7d9e2-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="7d9e2-130">Parametry: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d9e2-130">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="7d9e2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7d9e2-131">System.String</span></span>

## <span data-ttu-id="7d9e2-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d9e2-132">OUTPUTS</span></span>

### <span data-ttu-id="7d9e2-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7d9e2-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7d9e2-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d9e2-134">NOTES</span></span>

## <span data-ttu-id="7d9e2-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d9e2-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d9e2-136">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7d9e2-136">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="7d9e2-137">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7d9e2-137">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="7d9e2-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7d9e2-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)
