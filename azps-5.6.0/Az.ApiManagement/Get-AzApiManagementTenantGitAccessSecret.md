---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 471c861e8601317daf1e12de3a292d84bfce416e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004874"
---
# <span data-ttu-id="b7cf7-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="b7cf7-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="b7cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cf7-103">Pobiera klucze konfiguracji git dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b7cf7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7cf7-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7cf7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7cf7-105">DESCRIPTION</span></span>
<span data-ttu-id="b7cf7-106">Pobiera klucze konfiguracji git dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b7cf7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7cf7-107">EXAMPLES</span></span>

### <span data-ttu-id="b7cf7-108">Przykład 1. Uzyskiwanie konfiguracji dostępu do dzierżawy</span><span class="sxs-lookup"><span data-stu-id="b7cf7-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="b7cf7-109">To polecenie pobiera klucze konfiguracji git dostępu w określonym kontekście.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="b7cf7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7cf7-110">PARAMETERS</span></span>

### <span data-ttu-id="b7cf7-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b7cf7-111">-Context</span></span>
<span data-ttu-id="b7cf7-112">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b7cf7-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b7cf7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cf7-114">-DefaultProfile</span></span>
<span data-ttu-id="b7cf7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7cf7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cf7-116">CommonParameters</span></span>
<span data-ttu-id="b7cf7-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cf7-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7cf7-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cf7-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7cf7-119">INPUTS</span></span>

### <span data-ttu-id="b7cf7-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b7cf7-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b7cf7-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7cf7-121">OUTPUTS</span></span>

### <span data-ttu-id="b7cf7-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b7cf7-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b7cf7-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7cf7-123">NOTES</span></span>

## <span data-ttu-id="b7cf7-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7cf7-124">RELATED LINKS</span></span>
