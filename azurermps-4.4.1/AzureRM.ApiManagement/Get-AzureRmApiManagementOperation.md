---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547264"
---
# <span data-ttu-id="68fd7-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="68fd7-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="68fd7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="68fd7-103">Pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="68fd7-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68fd7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68fd7-104">SYNTAX</span></span>

### <span data-ttu-id="68fd7-105">Wszystkie operacje API (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="68fd7-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68fd7-106">Znajdowanie według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="68fd7-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68fd7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="68fd7-107">DESCRIPTION</span></span>
<span data-ttu-id="68fd7-108">**Element get-AzureRmApiManagementOperation** pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="68fd7-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="68fd7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68fd7-109">EXAMPLES</span></span>

### <span data-ttu-id="68fd7-110">Przykład 1: uzyskiwanie wszystkich operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="68fd7-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="68fd7-111">To polecenie pobiera wszystkie operacje zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="68fd7-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="68fd7-112">Przykład 2: uzyskiwanie operacji zarządzania interfejsem API według identyfikatora operacji</span><span class="sxs-lookup"><span data-stu-id="68fd7-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="68fd7-113">To polecenie pobiera operację zarządzania interfejsem API, podając Identyfikator operacji o nazwie Operation0003.</span><span class="sxs-lookup"><span data-stu-id="68fd7-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="68fd7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68fd7-114">PARAMETERS</span></span>

### <span data-ttu-id="68fd7-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="68fd7-115">-ApiId</span></span>
<span data-ttu-id="68fd7-116">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="68fd7-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="68fd7-117">-Context</span><span class="sxs-lookup"><span data-stu-id="68fd7-117">-Context</span></span>
<span data-ttu-id="68fd7-118">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="68fd7-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fd7-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="68fd7-119">-OperationId</span></span>
<span data-ttu-id="68fd7-120">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="68fd7-120">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fd7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fd7-121">-DefaultProfile</span></span>
<span data-ttu-id="68fd7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68fd7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68fd7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fd7-123">CommonParameters</span></span>
<span data-ttu-id="68fd7-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68fd7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fd7-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fd7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fd7-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68fd7-126">INPUTS</span></span>

## <span data-ttu-id="68fd7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68fd7-127">OUTPUTS</span></span>

### <span data-ttu-id="68fd7-128">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="68fd7-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="68fd7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68fd7-129">NOTES</span></span>

## <span data-ttu-id="68fd7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68fd7-130">RELATED LINKS</span></span>

[<span data-ttu-id="68fd7-131">Nowe — AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="68fd7-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="68fd7-132">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="68fd7-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="68fd7-133">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="68fd7-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


