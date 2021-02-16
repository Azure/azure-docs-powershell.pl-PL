---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239795"
---
# <span data-ttu-id="9b2cd-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="9b2cd-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="9b2cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2cd-103">Pobiera wartość tajny określonej nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="9b2cd-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="9b2cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b2cd-104">SYNTAX</span></span>

### <span data-ttu-id="9b2cd-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9b2cd-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2cd-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="9b2cd-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b2cd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b2cd-107">DESCRIPTION</span></span>
<span data-ttu-id="9b2cd-108">Pobiera wartość tajny określonej nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="9b2cd-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="9b2cd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b2cd-109">EXAMPLES</span></span>

### <span data-ttu-id="9b2cd-110">Przykład 1. Uzyskiwanie nazwanej wartości według nazwy</span><span class="sxs-lookup"><span data-stu-id="9b2cd-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="9b2cd-111">To polecenie pobiera szczegółowe informacje o nazwanej wartości nadanej nazwie wartości.</span><span class="sxs-lookup"><span data-stu-id="9b2cd-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="9b2cd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b2cd-112">PARAMETERS</span></span>

### <span data-ttu-id="9b2cd-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9b2cd-113">-Context</span></span>
<span data-ttu-id="9b2cd-114">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9b2cd-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9b2cd-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9b2cd-115">This parameter is required.</span></span>

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

### <span data-ttu-id="9b2cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2cd-116">-DefaultProfile</span></span>
<span data-ttu-id="9b2cd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2cd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b2cd-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="9b2cd-118">-NamedValueId</span></span>
<span data-ttu-id="9b2cd-119">Identyfikator nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="9b2cd-119">Identifier of a the named value.</span></span>
<span data-ttu-id="9b2cd-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9b2cd-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2cd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2cd-121">CommonParameters</span></span>
<span data-ttu-id="9b2cd-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2cd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2cd-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b2cd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2cd-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b2cd-124">INPUTS</span></span>

### <span data-ttu-id="9b2cd-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b2cd-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b2cd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9b2cd-126">System.String</span></span>

## <span data-ttu-id="9b2cd-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b2cd-127">OUTPUTS</span></span>

### <span data-ttu-id="9b2cd-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="9b2cd-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="9b2cd-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b2cd-129">NOTES</span></span>

## <span data-ttu-id="9b2cd-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b2cd-130">RELATED LINKS</span></span>
