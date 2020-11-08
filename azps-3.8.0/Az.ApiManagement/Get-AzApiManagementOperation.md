---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050895"
---
# <span data-ttu-id="30adc-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="30adc-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="30adc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30adc-102">SYNOPSIS</span></span>
<span data-ttu-id="30adc-103">Pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="30adc-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="30adc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30adc-104">SYNTAX</span></span>

### <span data-ttu-id="30adc-105">GetAllApiOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="30adc-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30adc-106">GetById</span><span class="sxs-lookup"><span data-stu-id="30adc-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30adc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="30adc-107">DESCRIPTION</span></span>
<span data-ttu-id="30adc-108">**Element get-AzApiManagementOperation** pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="30adc-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="30adc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30adc-109">EXAMPLES</span></span>

### <span data-ttu-id="30adc-110">Przykład 1: uzyskiwanie wszystkich operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="30adc-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="30adc-111">To polecenie pobiera wszystkie operacje zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="30adc-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="30adc-112">Przykład 2: uzyskiwanie operacji zarządzania interfejsem API według identyfikatora operacji</span><span class="sxs-lookup"><span data-stu-id="30adc-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="30adc-113">To polecenie pobiera operację zarządzania interfejsem API, podając Identyfikator operacji o nazwie Operation0003.</span><span class="sxs-lookup"><span data-stu-id="30adc-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="30adc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30adc-114">PARAMETERS</span></span>

### <span data-ttu-id="30adc-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="30adc-115">-ApiId</span></span>
<span data-ttu-id="30adc-116">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="30adc-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="30adc-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="30adc-117">-ApiRevision</span></span>
<span data-ttu-id="30adc-118">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="30adc-118">Identifier of API Revision.</span></span> <span data-ttu-id="30adc-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="30adc-119">This parameter is optional.</span></span> <span data-ttu-id="30adc-120">Jeśli nie określono tej funkcji, operacja zostanie pobrana z obecnej aktywnej wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="30adc-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="30adc-121">-Context</span><span class="sxs-lookup"><span data-stu-id="30adc-121">-Context</span></span>
<span data-ttu-id="30adc-122">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="30adc-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="30adc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30adc-123">-DefaultProfile</span></span>
<span data-ttu-id="30adc-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30adc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30adc-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="30adc-125">-OperationId</span></span>
<span data-ttu-id="30adc-126">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="30adc-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="30adc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30adc-127">CommonParameters</span></span>
<span data-ttu-id="30adc-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30adc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30adc-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30adc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30adc-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30adc-130">INPUTS</span></span>

### <span data-ttu-id="30adc-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="30adc-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="30adc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="30adc-132">System.String</span></span>

## <span data-ttu-id="30adc-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30adc-133">OUTPUTS</span></span>

### <span data-ttu-id="30adc-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="30adc-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="30adc-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30adc-135">NOTES</span></span>

## <span data-ttu-id="30adc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30adc-136">RELATED LINKS</span></span>

[<span data-ttu-id="30adc-137">Nowe — AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="30adc-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="30adc-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="30adc-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="30adc-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="30adc-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


