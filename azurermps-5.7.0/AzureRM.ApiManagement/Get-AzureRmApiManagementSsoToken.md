---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 927343f6a80edb82b933bfa382bbf6b690b90f07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544596"
---
# <span data-ttu-id="9de67-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="9de67-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="9de67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9de67-102">SYNOPSIS</span></span>
<span data-ttu-id="9de67-103">Pobiera link z tokenem SSO do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9de67-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9de67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9de67-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9de67-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9de67-105">DESCRIPTION</span></span>
<span data-ttu-id="9de67-106">Polecenie cmdlet **Get-AzureRmApiManagementSsoToken** zwraca link (adres URL), który zawiera token logowania jednokrotnego (SSO) do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9de67-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="9de67-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9de67-107">EXAMPLES</span></span>

### <span data-ttu-id="9de67-108">Przykład 1: uzyskiwanie tokenu SSO usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="9de67-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="9de67-109">To polecenie pobiera token SSO usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9de67-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="9de67-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9de67-110">PARAMETERS</span></span>

### <span data-ttu-id="9de67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de67-111">-DefaultProfile</span></span>
<span data-ttu-id="9de67-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9de67-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9de67-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9de67-113">-Name</span></span>
<span data-ttu-id="9de67-114">Określa nazwę wystąpienia zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9de67-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="9de67-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de67-115">-ResourceGroupName</span></span>
<span data-ttu-id="9de67-116">Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9de67-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="9de67-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de67-117">CommonParameters</span></span>
<span data-ttu-id="9de67-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de67-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de67-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de67-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de67-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9de67-120">INPUTS</span></span>

### <span data-ttu-id="9de67-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9de67-121">None</span></span>
<span data-ttu-id="9de67-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9de67-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9de67-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9de67-123">OUTPUTS</span></span>

### <span data-ttu-id="9de67-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9de67-124">System.String</span></span>

## <span data-ttu-id="9de67-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9de67-125">NOTES</span></span>

## <span data-ttu-id="9de67-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9de67-126">RELATED LINKS</span></span>

[<span data-ttu-id="9de67-127">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9de67-127">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


