---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: d84efcf68885e6d2e39ae15944c5f60298044ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526410"
---
# <span data-ttu-id="826bf-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="826bf-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="826bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="826bf-102">SYNOPSIS</span></span>
<span data-ttu-id="826bf-103">Pobiera interfejs API.</span><span class="sxs-lookup"><span data-stu-id="826bf-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="826bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="826bf-104">SYNTAX</span></span>

### <span data-ttu-id="826bf-105">GetAllApis (domyślny)</span><span class="sxs-lookup"><span data-stu-id="826bf-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="826bf-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="826bf-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="826bf-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="826bf-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="826bf-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="826bf-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="826bf-109">Opis</span><span class="sxs-lookup"><span data-stu-id="826bf-109">DESCRIPTION</span></span>
<span data-ttu-id="826bf-110">Polecenie cmdlet **Get-AzureRmApiManagementApi** pobiera co najmniej jeden interfejs API zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="826bf-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="826bf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="826bf-111">EXAMPLES</span></span>

### <span data-ttu-id="826bf-112">Przykład 1: pobieranie interfejsów API wszystkich zarządzania</span><span class="sxs-lookup"><span data-stu-id="826bf-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="826bf-113">To polecenie pobiera wszystkie interfejsy API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="826bf-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="826bf-114">Przykład 2: uzyskiwanie interfejsu API zarządzania według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="826bf-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="826bf-115">To polecenie pobiera interfejs API o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="826bf-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="826bf-116">Przykład 3: Uzyskaj interfejs API zarządzania według nazwy</span><span class="sxs-lookup"><span data-stu-id="826bf-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="826bf-117">To polecenie pobiera interfejs API o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="826bf-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="826bf-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="826bf-118">PARAMETERS</span></span>

### <span data-ttu-id="826bf-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="826bf-119">-ApiId</span></span>
<span data-ttu-id="826bf-120">Określa identyfikator interfejsu API, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="826bf-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="826bf-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="826bf-121">-ApiRevision</span></span>
<span data-ttu-id="826bf-122">Identyfikator poprawki konkretnej wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="826bf-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="826bf-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="826bf-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="826bf-124">-Context</span><span class="sxs-lookup"><span data-stu-id="826bf-124">-Context</span></span>
<span data-ttu-id="826bf-125">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="826bf-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="826bf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="826bf-126">-DefaultProfile</span></span>
<span data-ttu-id="826bf-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="826bf-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="826bf-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="826bf-128">-Name</span></span>
<span data-ttu-id="826bf-129">Określa nazwę interfejsu API do pobrania.</span><span class="sxs-lookup"><span data-stu-id="826bf-129">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="826bf-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="826bf-130">-ProductId</span></span>
<span data-ttu-id="826bf-131">Określa identyfikator produktu, dla którego ma zostać wyświetlony interfejs API.</span><span class="sxs-lookup"><span data-stu-id="826bf-131">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="826bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="826bf-132">CommonParameters</span></span>
<span data-ttu-id="826bf-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="826bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="826bf-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="826bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="826bf-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="826bf-135">INPUTS</span></span>

### <span data-ttu-id="826bf-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="826bf-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="826bf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="826bf-137">System.String</span></span>

## <span data-ttu-id="826bf-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="826bf-138">OUTPUTS</span></span>

### <span data-ttu-id="826bf-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="826bf-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="826bf-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="826bf-140">NOTES</span></span>

## <span data-ttu-id="826bf-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="826bf-141">RELATED LINKS</span></span>

[<span data-ttu-id="826bf-142">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="826bf-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="826bf-143">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="826bf-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="826bf-144">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="826bf-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="826bf-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="826bf-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="826bf-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="826bf-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


