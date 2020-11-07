---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 95784b084f6d106413c65b840dd73f313a47799e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718757"
---
# <span data-ttu-id="5f9d5-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5f9d5-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="5f9d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9d5-103">Pobiera interfejs API.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f9d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f9d5-104">SYNTAX</span></span>

### <span data-ttu-id="5f9d5-105">Wszystkie interfejsy API (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5f9d5-105">All APIs (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f9d5-106">Znajdowanie według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="5f9d5-106">Find by ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f9d5-107">Znajdowanie według nazwy</span><span class="sxs-lookup"><span data-stu-id="5f9d5-107">Find by Name</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f9d5-108">Znajdź według identyfikatora produktu</span><span class="sxs-lookup"><span data-stu-id="5f9d5-108">Find by product ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f9d5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5f9d5-109">DESCRIPTION</span></span>
<span data-ttu-id="5f9d5-110">Polecenie cmdlet **Get-AzureRmApiManagementApi** pobiera co najmniej jeden interfejs API zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="5f9d5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f9d5-111">EXAMPLES</span></span>

### <span data-ttu-id="5f9d5-112">Przykład 1: pobieranie interfejsów API wszystkich zarządzania</span><span class="sxs-lookup"><span data-stu-id="5f9d5-112">Example 1: Get all management APIs</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="5f9d5-113">To polecenie pobiera wszystkie interfejsy API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="5f9d5-114">Przykład 2: uzyskiwanie interfejsu API zarządzania według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="5f9d5-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="5f9d5-115">To polecenie pobiera interfejs API o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="5f9d5-116">Przykład 3: Uzyskaj interfejs API zarządzania według nazwy</span><span class="sxs-lookup"><span data-stu-id="5f9d5-116">Example 3: Get a management API by name</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="5f9d5-117">To polecenie pobiera interfejs API o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="5f9d5-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f9d5-118">PARAMETERS</span></span>

### <span data-ttu-id="5f9d5-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5f9d5-119">-ApiId</span></span>
<span data-ttu-id="5f9d5-120">Określa identyfikator interfejsu API, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="5f9d5-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5f9d5-121">-Context</span></span>
<span data-ttu-id="5f9d5-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5f9d5-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5f9d5-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f9d5-123">-Name</span></span>
<span data-ttu-id="5f9d5-124">Określa nazwę interfejsu API do pobrania.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-124">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d5-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5f9d5-125">-ProductId</span></span>
<span data-ttu-id="5f9d5-126">Określa identyfikator produktu, dla którego ma zostać wyświetlony interfejs API.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-126">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by product ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9d5-127">-DefaultProfile</span></span>
<span data-ttu-id="5f9d5-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f9d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9d5-129">CommonParameters</span></span>
<span data-ttu-id="5f9d5-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f9d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9d5-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f9d5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9d5-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f9d5-132">INPUTS</span></span>

## <span data-ttu-id="5f9d5-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f9d5-133">OUTPUTS</span></span>

### <span data-ttu-id="5f9d5-134">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApi></span><span class="sxs-lookup"><span data-stu-id="5f9d5-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>

## <span data-ttu-id="5f9d5-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f9d5-135">NOTES</span></span>

## <span data-ttu-id="5f9d5-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f9d5-136">RELATED LINKS</span></span>

[<span data-ttu-id="5f9d5-137">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5f9d5-137">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="5f9d5-138">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5f9d5-138">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="5f9d5-139">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5f9d5-139">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="5f9d5-140">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5f9d5-140">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="5f9d5-141">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5f9d5-141">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


