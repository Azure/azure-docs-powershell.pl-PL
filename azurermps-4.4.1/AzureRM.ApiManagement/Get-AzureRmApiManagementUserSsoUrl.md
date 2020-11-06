---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: a13d37100e553d8d56cf5b040a796adabe08b7d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547247"
---
# <span data-ttu-id="4fd35-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="4fd35-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="4fd35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fd35-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd35-103">Generuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4fd35-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fd35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fd35-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fd35-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4fd35-105">DESCRIPTION</span></span>
<span data-ttu-id="4fd35-106">Polecenie cmdlet **Get-AzureRmApiManagementUserSsoUrl** generuje adres URL logowania jednokrotnego (SSO) użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4fd35-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="4fd35-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fd35-107">EXAMPLES</span></span>

### <span data-ttu-id="4fd35-108">Przykład 1. Uzyskaj adres URL rejestracji jednokrotnej użytkownika</span><span class="sxs-lookup"><span data-stu-id="4fd35-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="4fd35-109">To polecenie uzyskuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4fd35-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="4fd35-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fd35-110">PARAMETERS</span></span>

### <span data-ttu-id="4fd35-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4fd35-111">-Context</span></span>
<span data-ttu-id="4fd35-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4fd35-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="4fd35-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4fd35-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4fd35-114">-UserId</span><span class="sxs-lookup"><span data-stu-id="4fd35-114">-UserId</span></span>
<span data-ttu-id="4fd35-115">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4fd35-115">Specifies a user ID.</span></span>
<span data-ttu-id="4fd35-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4fd35-116">This parameter is required.</span></span>

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

### <span data-ttu-id="4fd35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd35-117">-DefaultProfile</span></span>
<span data-ttu-id="4fd35-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fd35-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fd35-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd35-119">CommonParameters</span></span>
<span data-ttu-id="4fd35-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd35-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd35-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd35-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd35-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fd35-122">INPUTS</span></span>

## <span data-ttu-id="4fd35-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fd35-123">OUTPUTS</span></span>

### <span data-ttu-id="4fd35-124">ciąg</span><span class="sxs-lookup"><span data-stu-id="4fd35-124">string</span></span>

## <span data-ttu-id="4fd35-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fd35-125">NOTES</span></span>

## <span data-ttu-id="4fd35-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fd35-126">RELATED LINKS</span></span>

[<span data-ttu-id="4fd35-127">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="4fd35-127">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


