---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: a87c75058e3ebfb1ae7d14e729fdc9280cdccb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704667"
---
# <span data-ttu-id="5cf05-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cf05-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="5cf05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cf05-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf05-103">Pobiera interfejs API.</span><span class="sxs-lookup"><span data-stu-id="5cf05-103">Gets an API.</span></span>

## <span data-ttu-id="5cf05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cf05-104">SYNTAX</span></span>

### <span data-ttu-id="5cf05-105">GetAllApis (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5cf05-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5cf05-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="5cf05-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cf05-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="5cf05-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cf05-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="5cf05-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cf05-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5cf05-109">DESCRIPTION</span></span>
<span data-ttu-id="5cf05-110">Polecenie cmdlet **Get-AzApiManagementApi** pobiera co najmniej jeden interfejs API zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf05-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="5cf05-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cf05-111">EXAMPLES</span></span>

### <span data-ttu-id="5cf05-112">Przykład 1: pobieranie interfejsów API wszystkich zarządzania</span><span class="sxs-lookup"><span data-stu-id="5cf05-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="5cf05-113">To polecenie pobiera wszystkie interfejsy API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="5cf05-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="5cf05-114">Przykład 2: uzyskiwanie interfejsu API zarządzania według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="5cf05-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="5cf05-115">To polecenie pobiera interfejs API o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="5cf05-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="5cf05-116">Przykład 3: Uzyskaj interfejs API zarządzania według nazwy</span><span class="sxs-lookup"><span data-stu-id="5cf05-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="5cf05-117">To polecenie pobiera interfejs API o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="5cf05-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="5cf05-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cf05-118">PARAMETERS</span></span>

### <span data-ttu-id="5cf05-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5cf05-119">-ApiId</span></span>
<span data-ttu-id="5cf05-120">Określa identyfikator interfejsu API, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="5cf05-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="5cf05-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="5cf05-121">-ApiRevision</span></span>
<span data-ttu-id="5cf05-122">Identyfikator poprawki konkretnej wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5cf05-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="5cf05-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="5cf05-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="5cf05-124">-Context</span><span class="sxs-lookup"><span data-stu-id="5cf05-124">-Context</span></span>
<span data-ttu-id="5cf05-125">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5cf05-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5cf05-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf05-126">-DefaultProfile</span></span>
<span data-ttu-id="5cf05-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf05-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cf05-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5cf05-128">-Name</span></span>
<span data-ttu-id="5cf05-129">Określa nazwę interfejsu API do pobrania.</span><span class="sxs-lookup"><span data-stu-id="5cf05-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="5cf05-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5cf05-130">-ProductId</span></span>
<span data-ttu-id="5cf05-131">Określa identyfikator produktu, dla którego ma zostać wyświetlony interfejs API.</span><span class="sxs-lookup"><span data-stu-id="5cf05-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="5cf05-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf05-132">CommonParameters</span></span>
<span data-ttu-id="5cf05-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf05-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf05-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf05-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf05-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cf05-135">INPUTS</span></span>

### <span data-ttu-id="5cf05-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5cf05-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5cf05-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf05-137">System.String</span></span>

## <span data-ttu-id="5cf05-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cf05-138">OUTPUTS</span></span>

### <span data-ttu-id="5cf05-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cf05-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="5cf05-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cf05-140">NOTES</span></span>

## <span data-ttu-id="5cf05-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cf05-141">RELATED LINKS</span></span>

[<span data-ttu-id="5cf05-142">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cf05-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="5cf05-143">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cf05-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="5cf05-144">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cf05-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="5cf05-145">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cf05-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="5cf05-146">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cf05-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)

