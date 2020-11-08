---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062489"
---
# <span data-ttu-id="2b13e-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2b13e-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="2b13e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b13e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b13e-103">Pobiera listę lub określoną wartość nazwaną.</span><span class="sxs-lookup"><span data-stu-id="2b13e-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="2b13e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b13e-104">SYNTAX</span></span>

### <span data-ttu-id="2b13e-105">GetAllNamedValues (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2b13e-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b13e-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="2b13e-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b13e-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="2b13e-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b13e-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="2b13e-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b13e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2b13e-109">DESCRIPTION</span></span>
<span data-ttu-id="2b13e-110">Polecenie cmdlet **Get-AzApiManagementNamedValue** pobiera listę lub określoną wartość nazwaną.</span><span class="sxs-lookup"><span data-stu-id="2b13e-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="2b13e-111">Wartość nie zostanie uwzględniona w danych wynikowych, jeśli nazwana wartość jest oznaczona jako tajna.</span><span class="sxs-lookup"><span data-stu-id="2b13e-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="2b13e-112">Aby uzyskać wartość tajną, użyj wartości **Get-AzApiManagementNamedValueSecretValue**.</span><span class="sxs-lookup"><span data-stu-id="2b13e-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="2b13e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b13e-113">EXAMPLES</span></span>

### <span data-ttu-id="2b13e-114">Przykład 1: pobieranie nazwanej wartości według nazwy</span><span class="sxs-lookup"><span data-stu-id="2b13e-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="2b13e-115">To polecenie powoduje wyświetlenie szczegółowych danych o nazwach wartości przy nazwie Nazwa wartości.</span><span class="sxs-lookup"><span data-stu-id="2b13e-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="2b13e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b13e-116">PARAMETERS</span></span>

### <span data-ttu-id="2b13e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="2b13e-117">-Context</span></span>
<span data-ttu-id="2b13e-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2b13e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2b13e-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2b13e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="2b13e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b13e-120">-DefaultProfile</span></span>
<span data-ttu-id="2b13e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b13e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b13e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b13e-122">-Name</span></span>
<span data-ttu-id="2b13e-123">Umożliwia znalezienie nazwanych wartości z nazwami zawierającymi nazwę ciągu.</span><span class="sxs-lookup"><span data-stu-id="2b13e-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="2b13e-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2b13e-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="2b13e-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="2b13e-125">-NamedValueId</span></span>
<span data-ttu-id="2b13e-126">Identyfikator nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="2b13e-126">Identifier of the named value.</span></span>
<span data-ttu-id="2b13e-127">Jeśli ta wartość zostanie określona, spróbuje znaleźć nazwę wartości nazwanej przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="2b13e-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="2b13e-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2b13e-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="2b13e-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b13e-129">-Tag</span></span>
<span data-ttu-id="2b13e-130">Umożliwia znalezienie nazwanych wartości skojarzonych ze znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="2b13e-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="2b13e-131">Jeśli ta wartość zostanie określona, zostaną zwrócone wszystkie właściwości skojarzone ze znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="2b13e-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="2b13e-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2b13e-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="2b13e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b13e-133">CommonParameters</span></span>
<span data-ttu-id="2b13e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b13e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b13e-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b13e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b13e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b13e-136">INPUTS</span></span>

### <span data-ttu-id="2b13e-137">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b13e-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b13e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2b13e-138">System.String</span></span>

## <span data-ttu-id="2b13e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b13e-139">OUTPUTS</span></span>

### <span data-ttu-id="2b13e-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2b13e-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="2b13e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b13e-141">NOTES</span></span>

## <span data-ttu-id="2b13e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b13e-142">RELATED LINKS</span></span>
