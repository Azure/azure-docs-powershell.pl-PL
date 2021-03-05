---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: b4c89a1f0da5e4ce07d9d2174fce031365e09cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979073"
---
# <span data-ttu-id="0f1ca-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="0f1ca-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="0f1ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="0f1ca-103">Generuje adres URL logowania jednokrotnego dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0f1ca-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="0f1ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f1ca-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f1ca-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="0f1ca-106">Polecenie **cmdlet Get-AzApiManagementUserSsoUrl** generuje dla użytkownika adres URL logowania jednokrotnego.</span><span class="sxs-lookup"><span data-stu-id="0f1ca-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="0f1ca-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="0f1ca-108">Przykład 1. Uzyskiwanie adresu URL logowania jednokrotnego użytkownika</span><span class="sxs-lookup"><span data-stu-id="0f1ca-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="0f1ca-109">To polecenie pobiera adres URL logowania jednokrotnego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0f1ca-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="0f1ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f1ca-110">PARAMETERS</span></span>

### <span data-ttu-id="0f1ca-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="0f1ca-111">-Context</span></span>
<span data-ttu-id="0f1ca-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="0f1ca-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0f1ca-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0f1ca-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0f1ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f1ca-114">-DefaultProfile</span></span>
<span data-ttu-id="0f1ca-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f1ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f1ca-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="0f1ca-116">-UserId</span></span>
<span data-ttu-id="0f1ca-117">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0f1ca-117">Specifies a user ID.</span></span>
<span data-ttu-id="0f1ca-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0f1ca-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0f1ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f1ca-119">CommonParameters</span></span>
<span data-ttu-id="0f1ca-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f1ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f1ca-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f1ca-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f1ca-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f1ca-122">INPUTS</span></span>

### <span data-ttu-id="0f1ca-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0f1ca-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0f1ca-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0f1ca-124">System.String</span></span>

## <span data-ttu-id="0f1ca-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f1ca-125">OUTPUTS</span></span>

### <span data-ttu-id="0f1ca-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0f1ca-126">System.String</span></span>

## <span data-ttu-id="0f1ca-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f1ca-127">NOTES</span></span>

## <span data-ttu-id="0f1ca-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f1ca-128">RELATED LINKS</span></span>

[<span data-ttu-id="0f1ca-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0f1ca-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


