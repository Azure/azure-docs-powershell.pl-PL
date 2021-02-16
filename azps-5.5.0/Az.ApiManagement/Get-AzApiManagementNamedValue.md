---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239803"
---
# <span data-ttu-id="79291-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="79291-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="79291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79291-102">SYNOPSIS</span></span>
<span data-ttu-id="79291-103">Pobiera listę lub określonej nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="79291-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="79291-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79291-104">SYNTAX</span></span>

### <span data-ttu-id="79291-105">GetAllNamedValues (Default)</span><span class="sxs-lookup"><span data-stu-id="79291-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79291-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="79291-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79291-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="79291-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79291-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="79291-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79291-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="79291-109">DESCRIPTION</span></span>
<span data-ttu-id="79291-110">Polecenie **cmdlet Get-AzApiManagementNamedValue** pobiera listę lub określoną nazwaną wartość.</span><span class="sxs-lookup"><span data-stu-id="79291-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="79291-111">Wartość nie będzie uwzględniana w szczegółach wyników, jeśli nazwana wartość została oznaczona jako tajny.</span><span class="sxs-lookup"><span data-stu-id="79291-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="79291-112">Aby uzyskać wartość tajny, użyj właściwości **Get-AzApiManagementNamedValueSecretValue.**</span><span class="sxs-lookup"><span data-stu-id="79291-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="79291-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79291-113">EXAMPLES</span></span>

### <span data-ttu-id="79291-114">Przykład 1. Uzyskiwanie nazwanej wartości według nazwy</span><span class="sxs-lookup"><span data-stu-id="79291-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="79291-115">To polecenie pobiera szczegółowe informacje o nazwanej wartości nadanej nazwie wartości.</span><span class="sxs-lookup"><span data-stu-id="79291-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="79291-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79291-116">PARAMETERS</span></span>

### <span data-ttu-id="79291-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="79291-117">-Context</span></span>
<span data-ttu-id="79291-118">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="79291-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="79291-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="79291-119">This parameter is required.</span></span>

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

### <span data-ttu-id="79291-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79291-120">-DefaultProfile</span></span>
<span data-ttu-id="79291-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79291-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79291-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="79291-122">-Name</span></span>
<span data-ttu-id="79291-123">Znajduje nazwane wartości z nazwami zawierającymi ciąg Name.</span><span class="sxs-lookup"><span data-stu-id="79291-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="79291-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="79291-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79291-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="79291-125">-NamedValueId</span></span>
<span data-ttu-id="79291-126">Identyfikator nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="79291-126">Identifier of the named value.</span></span>
<span data-ttu-id="79291-127">Jeśli zostanie określona, identyfikator spróbuje znaleźć nazwaną wartość.</span><span class="sxs-lookup"><span data-stu-id="79291-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="79291-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="79291-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79291-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="79291-129">-Tag</span></span>
<span data-ttu-id="79291-130">Znajduje nazwane wartości skojarzone ze znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="79291-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="79291-131">Jeśli zostanie określona, zostaną zwrócone wszystkie właściwości skojarzone ze znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="79291-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="79291-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="79291-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79291-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79291-133">CommonParameters</span></span>
<span data-ttu-id="79291-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79291-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79291-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79291-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79291-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79291-136">INPUTS</span></span>

### <span data-ttu-id="79291-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="79291-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="79291-138">System.String</span><span class="sxs-lookup"><span data-stu-id="79291-138">System.String</span></span>

## <span data-ttu-id="79291-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79291-139">OUTPUTS</span></span>

### <span data-ttu-id="79291-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="79291-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="79291-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79291-141">NOTES</span></span>

## <span data-ttu-id="79291-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79291-142">RELATED LINKS</span></span>
