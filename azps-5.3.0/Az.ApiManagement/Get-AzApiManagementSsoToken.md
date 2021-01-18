---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502469"
---
# <span data-ttu-id="aa8d6-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="aa8d6-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="aa8d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="aa8d6-103">Pobiera link z tokenem SSO do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aa8d6-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="aa8d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa8d6-104">SYNTAX</span></span>

### <span data-ttu-id="aa8d6-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa8d6-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa8d6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa8d6-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa8d6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aa8d6-107">DESCRIPTION</span></span>
<span data-ttu-id="aa8d6-108">Polecenie cmdlet **Get-AzApiManagementSsoToken** zwraca link (adres URL), który zawiera token logowania jednokrotnego (SSO) do wdrożonego portalu zarządzania usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aa8d6-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="aa8d6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa8d6-109">EXAMPLES</span></span>

### <span data-ttu-id="aa8d6-110">Przykład 1: uzyskiwanie tokenu SSO usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="aa8d6-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="aa8d6-111">To polecenie pobiera token SSO usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aa8d6-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="aa8d6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa8d6-112">PARAMETERS</span></span>

### <span data-ttu-id="aa8d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa8d6-113">-DefaultProfile</span></span>
<span data-ttu-id="aa8d6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa8d6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa8d6-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa8d6-115">-InputObject</span></span>
<span data-ttu-id="aa8d6-116">Wystąpienie PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="aa8d6-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="aa8d6-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="aa8d6-117">This parameter is required.</span></span>

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

### <span data-ttu-id="aa8d6-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa8d6-118">-Name</span></span>
<span data-ttu-id="aa8d6-119">Określa nazwę wystąpienia zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aa8d6-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="aa8d6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa8d6-120">-ResourceGroupName</span></span>
<span data-ttu-id="aa8d6-121">Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aa8d6-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="aa8d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa8d6-122">CommonParameters</span></span>
<span data-ttu-id="aa8d6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa8d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa8d6-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa8d6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa8d6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa8d6-125">INPUTS</span></span>

### <span data-ttu-id="aa8d6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="aa8d6-126">System.String</span></span>

## <span data-ttu-id="aa8d6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa8d6-127">OUTPUTS</span></span>

### <span data-ttu-id="aa8d6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa8d6-128">System.String</span></span>

## <span data-ttu-id="aa8d6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa8d6-129">NOTES</span></span>

## <span data-ttu-id="aa8d6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa8d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="aa8d6-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="aa8d6-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


