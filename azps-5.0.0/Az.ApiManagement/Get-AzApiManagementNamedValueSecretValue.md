---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317401"
---
# <span data-ttu-id="d6f9b-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="d6f9b-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="d6f9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f9b-103">Pobiera tajną wartość określonej nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="d6f9b-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="d6f9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6f9b-104">SYNTAX</span></span>

### <span data-ttu-id="d6f9b-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d6f9b-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6f9b-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="d6f9b-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6f9b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6f9b-107">DESCRIPTION</span></span>
<span data-ttu-id="d6f9b-108">Pobiera tajną wartość określonej nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="d6f9b-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="d6f9b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6f9b-109">EXAMPLES</span></span>

### <span data-ttu-id="d6f9b-110">Przykład 1: pobieranie nazwanej wartości według nazwy</span><span class="sxs-lookup"><span data-stu-id="d6f9b-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="d6f9b-111">To polecenie powoduje wyświetlenie szczegółowych danych o nazwach wartości przy nazwie Nazwa wartości.</span><span class="sxs-lookup"><span data-stu-id="d6f9b-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="d6f9b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6f9b-112">PARAMETERS</span></span>

### <span data-ttu-id="d6f9b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d6f9b-113">-Context</span></span>
<span data-ttu-id="d6f9b-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d6f9b-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d6f9b-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d6f9b-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d6f9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f9b-116">-DefaultProfile</span></span>
<span data-ttu-id="d6f9b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f9b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f9b-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="d6f9b-118">-NamedValueId</span></span>
<span data-ttu-id="d6f9b-119">Identyfikator wartości nazwanej.</span><span class="sxs-lookup"><span data-stu-id="d6f9b-119">Identifier of a the named value.</span></span>
<span data-ttu-id="d6f9b-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d6f9b-120">This parameter is required.</span></span>

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

### <span data-ttu-id="d6f9b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f9b-121">CommonParameters</span></span>
<span data-ttu-id="d6f9b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f9b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f9b-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6f9b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f9b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6f9b-124">INPUTS</span></span>

### <span data-ttu-id="d6f9b-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6f9b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6f9b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d6f9b-126">System.String</span></span>

## <span data-ttu-id="d6f9b-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6f9b-127">OUTPUTS</span></span>

### <span data-ttu-id="d6f9b-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="d6f9b-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="d6f9b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6f9b-129">NOTES</span></span>

## <span data-ttu-id="d6f9b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6f9b-130">RELATED LINKS</span></span>
