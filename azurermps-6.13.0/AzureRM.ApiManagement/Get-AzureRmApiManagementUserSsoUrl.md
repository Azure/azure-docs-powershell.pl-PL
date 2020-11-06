---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 485150470bce308d3ab6d1a9a70eabd887abab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547696"
---
# <span data-ttu-id="92919-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="92919-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="92919-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92919-102">SYNOPSIS</span></span>
<span data-ttu-id="92919-103">Generuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92919-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92919-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92919-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92919-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92919-105">DESCRIPTION</span></span>
<span data-ttu-id="92919-106">Polecenie cmdlet **Get-AzureRmApiManagementUserSsoUrl** generuje adres URL logowania jednokrotnego (SSO) użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92919-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="92919-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92919-107">EXAMPLES</span></span>

### <span data-ttu-id="92919-108">Przykład 1. Uzyskaj adres URL rejestracji jednokrotnej użytkownika</span><span class="sxs-lookup"><span data-stu-id="92919-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="92919-109">To polecenie uzyskuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92919-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="92919-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92919-110">PARAMETERS</span></span>

### <span data-ttu-id="92919-111">-Context</span><span class="sxs-lookup"><span data-stu-id="92919-111">-Context</span></span>
<span data-ttu-id="92919-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="92919-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="92919-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="92919-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92919-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92919-114">-DefaultProfile</span></span>
<span data-ttu-id="92919-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92919-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92919-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="92919-116">-UserId</span></span>
<span data-ttu-id="92919-117">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92919-117">Specifies a user ID.</span></span>
<span data-ttu-id="92919-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="92919-118">This parameter is required.</span></span>

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

### <span data-ttu-id="92919-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92919-119">CommonParameters</span></span>
<span data-ttu-id="92919-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92919-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92919-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92919-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92919-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92919-122">INPUTS</span></span>

### <span data-ttu-id="92919-123">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="92919-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="92919-124">System. String</span><span class="sxs-lookup"><span data-stu-id="92919-124">System.String</span></span>

## <span data-ttu-id="92919-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92919-125">OUTPUTS</span></span>

### <span data-ttu-id="92919-126">System. String</span><span class="sxs-lookup"><span data-stu-id="92919-126">System.String</span></span>

## <span data-ttu-id="92919-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92919-127">NOTES</span></span>

## <span data-ttu-id="92919-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92919-128">RELATED LINKS</span></span>

[<span data-ttu-id="92919-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="92919-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


