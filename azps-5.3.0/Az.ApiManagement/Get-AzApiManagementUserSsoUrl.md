---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502453"
---
# <span data-ttu-id="89440-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="89440-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="89440-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89440-102">SYNOPSIS</span></span>
<span data-ttu-id="89440-103">Generuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89440-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="89440-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89440-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89440-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89440-105">DESCRIPTION</span></span>
<span data-ttu-id="89440-106">Polecenie cmdlet **Get-AzApiManagementUserSsoUrl** generuje adres URL logowania jednokrotnego (SSO) użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89440-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="89440-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89440-107">EXAMPLES</span></span>

### <span data-ttu-id="89440-108">Przykład 1. Uzyskaj adres URL rejestracji jednokrotnej użytkownika</span><span class="sxs-lookup"><span data-stu-id="89440-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="89440-109">To polecenie uzyskuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89440-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="89440-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89440-110">PARAMETERS</span></span>

### <span data-ttu-id="89440-111">-Context</span><span class="sxs-lookup"><span data-stu-id="89440-111">-Context</span></span>
<span data-ttu-id="89440-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="89440-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="89440-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="89440-113">This parameter is required.</span></span>

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

### <span data-ttu-id="89440-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89440-114">-DefaultProfile</span></span>
<span data-ttu-id="89440-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89440-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89440-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="89440-116">-UserId</span></span>
<span data-ttu-id="89440-117">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89440-117">Specifies a user ID.</span></span>
<span data-ttu-id="89440-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="89440-118">This parameter is required.</span></span>

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

### <span data-ttu-id="89440-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89440-119">CommonParameters</span></span>
<span data-ttu-id="89440-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89440-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89440-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89440-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89440-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89440-122">INPUTS</span></span>

### <span data-ttu-id="89440-123">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="89440-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="89440-124">System. String</span><span class="sxs-lookup"><span data-stu-id="89440-124">System.String</span></span>

## <span data-ttu-id="89440-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89440-125">OUTPUTS</span></span>

### <span data-ttu-id="89440-126">System. String</span><span class="sxs-lookup"><span data-stu-id="89440-126">System.String</span></span>

## <span data-ttu-id="89440-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89440-127">NOTES</span></span>

## <span data-ttu-id="89440-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89440-128">RELATED LINKS</span></span>

[<span data-ttu-id="89440-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="89440-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


