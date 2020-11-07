---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 40c9166ab650f7cb31ac53c55397bb7bc635f6e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704632"
---
# <span data-ttu-id="660a8-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="660a8-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="660a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="660a8-102">SYNOPSIS</span></span>
<span data-ttu-id="660a8-103">Pobiera link z tokenem SSO do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="660a8-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="660a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="660a8-104">SYNTAX</span></span>

```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="660a8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="660a8-105">DESCRIPTION</span></span>
<span data-ttu-id="660a8-106">Polecenie cmdlet **Get-AzApiManagementSsoToken** zwraca link (adres URL), który zawiera token logowania jednokrotnego (SSO) do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="660a8-106">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="660a8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="660a8-107">EXAMPLES</span></span>

### <span data-ttu-id="660a8-108">Przykład 1: uzyskiwanie tokenu SSO usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="660a8-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="660a8-109">To polecenie pobiera token SSO usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="660a8-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="660a8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="660a8-110">PARAMETERS</span></span>

### <span data-ttu-id="660a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660a8-111">-DefaultProfile</span></span>
<span data-ttu-id="660a8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="660a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="660a8-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="660a8-113">-Name</span></span>
<span data-ttu-id="660a8-114">Określa nazwę wystąpienia zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="660a8-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="660a8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="660a8-115">-ResourceGroupName</span></span>
<span data-ttu-id="660a8-116">Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="660a8-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="660a8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660a8-117">CommonParameters</span></span>
<span data-ttu-id="660a8-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660a8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660a8-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660a8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660a8-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="660a8-120">INPUTS</span></span>

### <span data-ttu-id="660a8-121">System. String</span><span class="sxs-lookup"><span data-stu-id="660a8-121">System.String</span></span>

## <span data-ttu-id="660a8-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="660a8-122">OUTPUTS</span></span>

### <span data-ttu-id="660a8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="660a8-123">System.String</span></span>

## <span data-ttu-id="660a8-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="660a8-124">NOTES</span></span>

## <span data-ttu-id="660a8-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="660a8-125">RELATED LINKS</span></span>

[<span data-ttu-id="660a8-126">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="660a8-126">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


