---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053621"
---
# <span data-ttu-id="1d0a0-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="1d0a0-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="1d0a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="1d0a0-103">Pobiera link z tokenem SSO do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1d0a0-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="1d0a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d0a0-104">SYNTAX</span></span>

### <span data-ttu-id="1d0a0-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1d0a0-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d0a0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d0a0-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d0a0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1d0a0-107">DESCRIPTION</span></span>
<span data-ttu-id="1d0a0-108">Polecenie cmdlet **Get-AzApiManagementSsoToken** zwraca link (adres URL), który zawiera token logowania jednokrotnego (SSO) do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1d0a0-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="1d0a0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d0a0-109">EXAMPLES</span></span>

### <span data-ttu-id="1d0a0-110">Przykład 1: uzyskiwanie tokenu SSO usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="1d0a0-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="1d0a0-111">To polecenie pobiera token SSO usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1d0a0-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="1d0a0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d0a0-112">PARAMETERS</span></span>

### <span data-ttu-id="1d0a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d0a0-113">-DefaultProfile</span></span>
<span data-ttu-id="1d0a0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d0a0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d0a0-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1d0a0-115">-InputObject</span></span>
<span data-ttu-id="1d0a0-116">Wystąpienie PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1d0a0-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="1d0a0-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1d0a0-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d0a0-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d0a0-118">-Name</span></span>
<span data-ttu-id="1d0a0-119">Określa nazwę wystąpienia zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1d0a0-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d0a0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d0a0-120">-ResourceGroupName</span></span>
<span data-ttu-id="1d0a0-121">Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1d0a0-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d0a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d0a0-122">CommonParameters</span></span>
<span data-ttu-id="1d0a0-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d0a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d0a0-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d0a0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d0a0-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d0a0-125">INPUTS</span></span>

### <span data-ttu-id="1d0a0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1d0a0-126">System.String</span></span>

## <span data-ttu-id="1d0a0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d0a0-127">OUTPUTS</span></span>

### <span data-ttu-id="1d0a0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1d0a0-128">System.String</span></span>

## <span data-ttu-id="1d0a0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d0a0-129">NOTES</span></span>

## <span data-ttu-id="1d0a0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d0a0-130">RELATED LINKS</span></span>

[<span data-ttu-id="1d0a0-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d0a0-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


