---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: 56246de86606aeb07dd8ccdbcfbf2dc35b32a5a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004897"
---
# <span data-ttu-id="1740f-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="1740f-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="1740f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1740f-102">SYNOPSIS</span></span>
<span data-ttu-id="1740f-103">Pobiera klucze konfiguracji dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1740f-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="1740f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1740f-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1740f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1740f-105">DESCRIPTION</span></span>
<span data-ttu-id="1740f-106">Pobiera klucze konfiguracji dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1740f-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="1740f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1740f-107">EXAMPLES</span></span>

### <span data-ttu-id="1740f-108">Przykład 1. Uzyskiwanie kluczy konfiguracji dostępu do dzierżawy</span><span class="sxs-lookup"><span data-stu-id="1740f-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="1740f-109">To polecenie pobiera klucze konfiguracji dostępu dzierżawy w określonym kontekście.</span><span class="sxs-lookup"><span data-stu-id="1740f-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="1740f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1740f-110">PARAMETERS</span></span>

### <span data-ttu-id="1740f-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="1740f-111">-Context</span></span>
<span data-ttu-id="1740f-112">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1740f-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1740f-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1740f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1740f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1740f-114">-DefaultProfile</span></span>
<span data-ttu-id="1740f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1740f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1740f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1740f-116">CommonParameters</span></span>
<span data-ttu-id="1740f-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1740f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1740f-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1740f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1740f-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1740f-119">INPUTS</span></span>

### <span data-ttu-id="1740f-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1740f-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="1740f-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1740f-121">OUTPUTS</span></span>

### <span data-ttu-id="1740f-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="1740f-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="1740f-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1740f-123">NOTES</span></span>

## <span data-ttu-id="1740f-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1740f-124">RELATED LINKS</span></span>
