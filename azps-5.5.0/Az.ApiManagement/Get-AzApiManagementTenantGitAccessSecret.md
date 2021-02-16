---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178107"
---
# <span data-ttu-id="ced1d-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="ced1d-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="ced1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ced1d-102">SYNOPSIS</span></span>
<span data-ttu-id="ced1d-103">Pobiera klucze konfiguracji git dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ced1d-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="ced1d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ced1d-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ced1d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ced1d-105">DESCRIPTION</span></span>
<span data-ttu-id="ced1d-106">Pobiera klucze konfiguracji git dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ced1d-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="ced1d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ced1d-107">EXAMPLES</span></span>

### <span data-ttu-id="ced1d-108">Przykład 1. Uzyskiwanie konfiguracji dostępu do dzierżawy</span><span class="sxs-lookup"><span data-stu-id="ced1d-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="ced1d-109">To polecenie pobiera klucze konfiguracji git dostępu w określonym kontekście.</span><span class="sxs-lookup"><span data-stu-id="ced1d-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="ced1d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ced1d-110">PARAMETERS</span></span>

### <span data-ttu-id="ced1d-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="ced1d-111">-Context</span></span>
<span data-ttu-id="ced1d-112">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ced1d-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ced1d-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ced1d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ced1d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced1d-114">-DefaultProfile</span></span>
<span data-ttu-id="ced1d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ced1d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced1d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced1d-116">CommonParameters</span></span>
<span data-ttu-id="ced1d-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced1d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced1d-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ced1d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced1d-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ced1d-119">INPUTS</span></span>

### <span data-ttu-id="ced1d-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ced1d-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="ced1d-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ced1d-121">OUTPUTS</span></span>

### <span data-ttu-id="ced1d-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="ced1d-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="ced1d-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ced1d-123">NOTES</span></span>

## <span data-ttu-id="ced1d-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ced1d-124">RELATED LINKS</span></span>
