---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176498"
---
# <span data-ttu-id="39de4-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="39de4-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="39de4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39de4-102">SYNOPSIS</span></span>
<span data-ttu-id="39de4-103">Generuje adres URL logowania jednokrotnego dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="39de4-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="39de4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="39de4-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39de4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="39de4-105">DESCRIPTION</span></span>
<span data-ttu-id="39de4-106">Polecenie **cmdlet Get-AzApiManagementUserSsoUrl** generuje dla użytkownika adres URL logowania jednokrotnego.</span><span class="sxs-lookup"><span data-stu-id="39de4-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="39de4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="39de4-107">EXAMPLES</span></span>

### <span data-ttu-id="39de4-108">Przykład 1. Uzyskiwanie adresu URL logowania jednokrotnego użytkownika</span><span class="sxs-lookup"><span data-stu-id="39de4-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="39de4-109">To polecenie pobiera adres URL logowania jednokrotnego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="39de4-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="39de4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39de4-110">PARAMETERS</span></span>

### <span data-ttu-id="39de4-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="39de4-111">-Context</span></span>
<span data-ttu-id="39de4-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="39de4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="39de4-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="39de4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="39de4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39de4-114">-DefaultProfile</span></span>
<span data-ttu-id="39de4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="39de4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39de4-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="39de4-116">-UserId</span></span>
<span data-ttu-id="39de4-117">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="39de4-117">Specifies a user ID.</span></span>
<span data-ttu-id="39de4-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="39de4-118">This parameter is required.</span></span>

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

### <span data-ttu-id="39de4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39de4-119">CommonParameters</span></span>
<span data-ttu-id="39de4-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39de4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39de4-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39de4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39de4-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39de4-122">INPUTS</span></span>

### <span data-ttu-id="39de4-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="39de4-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="39de4-124">System.String</span><span class="sxs-lookup"><span data-stu-id="39de4-124">System.String</span></span>

## <span data-ttu-id="39de4-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39de4-125">OUTPUTS</span></span>

### <span data-ttu-id="39de4-126">System.String</span><span class="sxs-lookup"><span data-stu-id="39de4-126">System.String</span></span>

## <span data-ttu-id="39de4-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="39de4-127">NOTES</span></span>

## <span data-ttu-id="39de4-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39de4-128">RELATED LINKS</span></span>

[<span data-ttu-id="39de4-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="39de4-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


