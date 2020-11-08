---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062474"
---
# <span data-ttu-id="34890-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="34890-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="34890-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34890-102">SYNOPSIS</span></span>
<span data-ttu-id="34890-103">Generuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="34890-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="34890-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34890-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34890-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34890-105">DESCRIPTION</span></span>
<span data-ttu-id="34890-106">Polecenie cmdlet **Get-AzApiManagementUserSsoUrl** generuje adres URL logowania jednokrotnego (SSO) użytkownika.</span><span class="sxs-lookup"><span data-stu-id="34890-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="34890-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34890-107">EXAMPLES</span></span>

### <span data-ttu-id="34890-108">Przykład 1. Uzyskaj adres URL rejestracji jednokrotnej użytkownika</span><span class="sxs-lookup"><span data-stu-id="34890-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="34890-109">To polecenie uzyskuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="34890-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="34890-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34890-110">PARAMETERS</span></span>

### <span data-ttu-id="34890-111">-Context</span><span class="sxs-lookup"><span data-stu-id="34890-111">-Context</span></span>
<span data-ttu-id="34890-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="34890-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="34890-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="34890-113">This parameter is required.</span></span>

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

### <span data-ttu-id="34890-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34890-114">-DefaultProfile</span></span>
<span data-ttu-id="34890-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34890-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34890-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="34890-116">-UserId</span></span>
<span data-ttu-id="34890-117">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="34890-117">Specifies a user ID.</span></span>
<span data-ttu-id="34890-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="34890-118">This parameter is required.</span></span>

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

### <span data-ttu-id="34890-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34890-119">CommonParameters</span></span>
<span data-ttu-id="34890-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34890-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34890-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34890-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34890-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34890-122">INPUTS</span></span>

### <span data-ttu-id="34890-123">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="34890-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="34890-124">System. String</span><span class="sxs-lookup"><span data-stu-id="34890-124">System.String</span></span>

## <span data-ttu-id="34890-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34890-125">OUTPUTS</span></span>

### <span data-ttu-id="34890-126">System. String</span><span class="sxs-lookup"><span data-stu-id="34890-126">System.String</span></span>

## <span data-ttu-id="34890-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34890-127">NOTES</span></span>

## <span data-ttu-id="34890-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34890-128">RELATED LINKS</span></span>

[<span data-ttu-id="34890-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="34890-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


