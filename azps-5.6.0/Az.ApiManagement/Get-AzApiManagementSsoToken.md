---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: eae199f28314db5aa50fa3247b46f02a407802fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004954"
---
# <span data-ttu-id="b82d7-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="b82d7-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="b82d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b82d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b82d7-103">Pobiera link z tokenem logowania jednokrotnego do wdrożonego portalu zarządzania usługą zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="b82d7-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="b82d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b82d7-104">SYNTAX</span></span>

### <span data-ttu-id="b82d7-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b82d7-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b82d7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b82d7-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b82d7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b82d7-107">DESCRIPTION</span></span>
<span data-ttu-id="b82d7-108">Polecenie **cmdlet Get-AzApiManagementSsoToken** zwraca link (URL) zawierający token logowania jednokrotnego (SSO) do wdrożonego portalu zarządzania usługą zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="b82d7-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="b82d7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b82d7-109">EXAMPLES</span></span>

### <span data-ttu-id="b82d7-110">Przykład 1. Uzyskiwanie tokenu logowania jednokrotnego usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="b82d7-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="b82d7-111">To polecenie pobiera token logowania jednokrotnego usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="b82d7-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="b82d7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b82d7-112">PARAMETERS</span></span>

### <span data-ttu-id="b82d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b82d7-113">-DefaultProfile</span></span>
<span data-ttu-id="b82d7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b82d7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b82d7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b82d7-115">-InputObject</span></span>
<span data-ttu-id="b82d7-116">Wystąpienie programu PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b82d7-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="b82d7-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b82d7-117">This parameter is required.</span></span>

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

### <span data-ttu-id="b82d7-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b82d7-118">-Name</span></span>
<span data-ttu-id="b82d7-119">Określa nazwę wystąpienia zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b82d7-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="b82d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b82d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="b82d7-121">Określa nazwę grupy zasobów, w której istnieje zarządzanie interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="b82d7-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="b82d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82d7-122">CommonParameters</span></span>
<span data-ttu-id="b82d7-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b82d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82d7-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b82d7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82d7-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b82d7-125">INPUTS</span></span>

### <span data-ttu-id="b82d7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b82d7-126">System.String</span></span>

## <span data-ttu-id="b82d7-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b82d7-127">OUTPUTS</span></span>

### <span data-ttu-id="b82d7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b82d7-128">System.String</span></span>

## <span data-ttu-id="b82d7-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b82d7-129">NOTES</span></span>

## <span data-ttu-id="b82d7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b82d7-130">RELATED LINKS</span></span>

[<span data-ttu-id="b82d7-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b82d7-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


