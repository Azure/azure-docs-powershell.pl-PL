---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: e0bce4f579b2000bc970e35ceb03da03fdffb211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524742"
---
# <span data-ttu-id="ef894-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="ef894-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="ef894-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef894-102">SYNOPSIS</span></span>
<span data-ttu-id="ef894-103">Pobiera link z tokenem SSO do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ef894-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef894-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef894-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef894-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef894-105">DESCRIPTION</span></span>
<span data-ttu-id="ef894-106">Polecenie cmdlet **Get-AzureRmApiManagementSsoToken** zwraca link (adres URL), który zawiera token logowania jednokrotnego (SSO) do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ef894-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="ef894-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef894-107">EXAMPLES</span></span>

### <span data-ttu-id="ef894-108">Przykład 1: uzyskiwanie tokenu SSO usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="ef894-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="ef894-109">To polecenie pobiera token SSO usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ef894-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="ef894-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef894-110">PARAMETERS</span></span>

### <span data-ttu-id="ef894-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef894-111">-DefaultProfile</span></span>
<span data-ttu-id="ef894-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef894-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef894-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef894-113">-Name</span></span>
<span data-ttu-id="ef894-114">Określa nazwę wystąpienia zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ef894-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="ef894-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef894-115">-ResourceGroupName</span></span>
<span data-ttu-id="ef894-116">Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ef894-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="ef894-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef894-117">CommonParameters</span></span>
<span data-ttu-id="ef894-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef894-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef894-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef894-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef894-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef894-120">INPUTS</span></span>

### <span data-ttu-id="ef894-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ef894-121">System.String</span></span>

## <span data-ttu-id="ef894-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef894-122">OUTPUTS</span></span>

### <span data-ttu-id="ef894-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ef894-123">System.String</span></span>

## <span data-ttu-id="ef894-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef894-124">NOTES</span></span>

## <span data-ttu-id="ef894-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef894-125">RELATED LINKS</span></span>

[<span data-ttu-id="ef894-126">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef894-126">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


