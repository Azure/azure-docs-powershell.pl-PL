---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 5cc7eb81c9ccaf461b1f2ab16e76aa662ea0f57b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544579"
---
# <span data-ttu-id="92377-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="92377-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="92377-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92377-102">SYNOPSIS</span></span>
<span data-ttu-id="92377-103">Generuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92377-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92377-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92377-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92377-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92377-105">DESCRIPTION</span></span>
<span data-ttu-id="92377-106">Polecenie cmdlet **Get-AzureRmApiManagementUserSsoUrl** generuje adres URL logowania jednokrotnego (SSO) użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92377-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="92377-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92377-107">EXAMPLES</span></span>

### <span data-ttu-id="92377-108">Przykład 1. Uzyskaj adres URL rejestracji jednokrotnej użytkownika</span><span class="sxs-lookup"><span data-stu-id="92377-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="92377-109">To polecenie uzyskuje adres URL rejestracji jednokrotnej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92377-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="92377-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92377-110">PARAMETERS</span></span>

### <span data-ttu-id="92377-111">-Context</span><span class="sxs-lookup"><span data-stu-id="92377-111">-Context</span></span>
<span data-ttu-id="92377-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="92377-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="92377-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="92377-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92377-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92377-114">-DefaultProfile</span></span>
<span data-ttu-id="92377-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92377-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92377-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="92377-116">-UserId</span></span>
<span data-ttu-id="92377-117">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92377-117">Specifies a user ID.</span></span>
<span data-ttu-id="92377-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="92377-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92377-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92377-119">CommonParameters</span></span>
<span data-ttu-id="92377-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92377-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92377-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92377-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92377-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92377-122">INPUTS</span></span>

### <span data-ttu-id="92377-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="92377-123">None</span></span>
<span data-ttu-id="92377-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="92377-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92377-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92377-125">OUTPUTS</span></span>

### <span data-ttu-id="92377-126">ciąg</span><span class="sxs-lookup"><span data-stu-id="92377-126">string</span></span>

## <span data-ttu-id="92377-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92377-127">NOTES</span></span>

## <span data-ttu-id="92377-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92377-128">RELATED LINKS</span></span>

[<span data-ttu-id="92377-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="92377-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


