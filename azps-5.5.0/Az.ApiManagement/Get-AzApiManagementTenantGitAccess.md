---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187691"
---
# <span data-ttu-id="1cb92-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="1cb92-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="1cb92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb92-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb92-103">Pobiera konfigurację dostępu Git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1cb92-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="1cb92-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1cb92-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cb92-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1cb92-105">DESCRIPTION</span></span>
<span data-ttu-id="1cb92-106">Polecenie **cmdlet Get-AzApiManagementTenantGitAccess** pobiera konfigurację dostępu Git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1cb92-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="1cb92-107">Klucze nie będą uwzględniane w szczegółach wyników.</span><span class="sxs-lookup"><span data-stu-id="1cb92-107">Keys will not be included into result details.</span></span> <span data-ttu-id="1cb92-108">Aby uzyskać klucz tajny klienta, użyj funkcji **Get-AzApiManagementTenantGitAccessSecret.**</span><span class="sxs-lookup"><span data-stu-id="1cb92-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="1cb92-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1cb92-109">EXAMPLES</span></span>

### <span data-ttu-id="1cb92-110">Przykład 1. Uzyskiwanie konfiguracji dostępu do dzierżawy</span><span class="sxs-lookup"><span data-stu-id="1cb92-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="1cb92-111">To polecenie pobiera konfigurację dostępu Do Git w określonym kontekście.</span><span class="sxs-lookup"><span data-stu-id="1cb92-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="1cb92-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cb92-112">PARAMETERS</span></span>

### <span data-ttu-id="1cb92-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="1cb92-113">-Context</span></span>
<span data-ttu-id="1cb92-114">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="1cb92-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1cb92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb92-115">-DefaultProfile</span></span>
<span data-ttu-id="1cb92-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb92-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb92-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb92-117">CommonParameters</span></span>
<span data-ttu-id="1cb92-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb92-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb92-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cb92-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb92-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cb92-120">INPUTS</span></span>

### <span data-ttu-id="1cb92-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1cb92-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="1cb92-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1cb92-122">OUTPUTS</span></span>

### <span data-ttu-id="1cb92-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="1cb92-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="1cb92-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1cb92-124">NOTES</span></span>

## <span data-ttu-id="1cb92-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1cb92-125">RELATED LINKS</span></span>
