---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 469d10303f286a0feca162e628a1564826b850d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524753"
---
# <span data-ttu-id="8f99e-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f99e-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="8f99e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f99e-102">SYNOPSIS</span></span>
<span data-ttu-id="8f99e-103">Pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f99e-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f99e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f99e-104">SYNTAX</span></span>

### <span data-ttu-id="8f99e-105">GetAllApiOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8f99e-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f99e-106">GetById</span><span class="sxs-lookup"><span data-stu-id="8f99e-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f99e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8f99e-107">DESCRIPTION</span></span>
<span data-ttu-id="8f99e-108">**Element get-AzureRmApiManagementOperation** pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f99e-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="8f99e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f99e-109">EXAMPLES</span></span>

### <span data-ttu-id="8f99e-110">Przykład 1: uzyskiwanie wszystkich operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="8f99e-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="8f99e-111">To polecenie pobiera wszystkie operacje zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="8f99e-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="8f99e-112">Przykład 2: uzyskiwanie operacji zarządzania interfejsem API według identyfikatora operacji</span><span class="sxs-lookup"><span data-stu-id="8f99e-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="8f99e-113">To polecenie pobiera operację zarządzania interfejsem API, podając Identyfikator operacji o nazwie Operation0003.</span><span class="sxs-lookup"><span data-stu-id="8f99e-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="8f99e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f99e-114">PARAMETERS</span></span>

### <span data-ttu-id="8f99e-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8f99e-115">-ApiId</span></span>
<span data-ttu-id="8f99e-116">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f99e-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="8f99e-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="8f99e-117">-ApiRevision</span></span>
<span data-ttu-id="8f99e-118">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f99e-118">Identifier of API Revision.</span></span> <span data-ttu-id="8f99e-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8f99e-119">This parameter is optional.</span></span> <span data-ttu-id="8f99e-120">Jeśli nie określono tej funkcji, operacja zostanie pobrana z obecnej aktywnej wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f99e-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f99e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="8f99e-121">-Context</span></span>
<span data-ttu-id="8f99e-122">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8f99e-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8f99e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f99e-123">-DefaultProfile</span></span>
<span data-ttu-id="8f99e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f99e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f99e-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="8f99e-125">-OperationId</span></span>
<span data-ttu-id="8f99e-126">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="8f99e-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f99e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f99e-127">CommonParameters</span></span>
<span data-ttu-id="8f99e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f99e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f99e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f99e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f99e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f99e-130">INPUTS</span></span>

### <span data-ttu-id="8f99e-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8f99e-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8f99e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8f99e-132">System.String</span></span>

## <span data-ttu-id="8f99e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f99e-133">OUTPUTS</span></span>

### <span data-ttu-id="8f99e-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f99e-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="8f99e-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f99e-135">NOTES</span></span>

## <span data-ttu-id="8f99e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f99e-136">RELATED LINKS</span></span>

[<span data-ttu-id="8f99e-137">Nowe — AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f99e-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="8f99e-138">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f99e-138">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="8f99e-139">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f99e-139">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


