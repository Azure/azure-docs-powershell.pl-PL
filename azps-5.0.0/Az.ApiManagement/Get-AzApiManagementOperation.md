---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317365"
---
# <span data-ttu-id="fd62b-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fd62b-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="fd62b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd62b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd62b-103">Pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="fd62b-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="fd62b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd62b-104">SYNTAX</span></span>

### <span data-ttu-id="fd62b-105">GetAllApiOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fd62b-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd62b-106">GetById</span><span class="sxs-lookup"><span data-stu-id="fd62b-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd62b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fd62b-107">DESCRIPTION</span></span>
<span data-ttu-id="fd62b-108">**Element get-AzApiManagementOperation** pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="fd62b-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="fd62b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd62b-109">EXAMPLES</span></span>

### <span data-ttu-id="fd62b-110">Przykład 1: uzyskiwanie wszystkich operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="fd62b-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="fd62b-111">To polecenie pobiera wszystkie operacje zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="fd62b-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="fd62b-112">Przykład 2: uzyskiwanie operacji zarządzania interfejsem API według identyfikatora operacji</span><span class="sxs-lookup"><span data-stu-id="fd62b-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="fd62b-113">To polecenie pobiera operację zarządzania interfejsem API, podając Identyfikator operacji o nazwie Operation0003.</span><span class="sxs-lookup"><span data-stu-id="fd62b-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="fd62b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd62b-114">PARAMETERS</span></span>

### <span data-ttu-id="fd62b-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fd62b-115">-ApiId</span></span>
<span data-ttu-id="fd62b-116">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="fd62b-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="fd62b-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="fd62b-117">-ApiRevision</span></span>
<span data-ttu-id="fd62b-118">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="fd62b-118">Identifier of API Revision.</span></span> <span data-ttu-id="fd62b-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="fd62b-119">This parameter is optional.</span></span> <span data-ttu-id="fd62b-120">Jeśli nie określono tej funkcji, operacja zostanie pobrana z obecnej aktywnej wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="fd62b-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="fd62b-121">-Context</span><span class="sxs-lookup"><span data-stu-id="fd62b-121">-Context</span></span>
<span data-ttu-id="fd62b-122">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fd62b-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fd62b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd62b-123">-DefaultProfile</span></span>
<span data-ttu-id="fd62b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd62b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd62b-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="fd62b-125">-OperationId</span></span>
<span data-ttu-id="fd62b-126">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="fd62b-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="fd62b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd62b-127">CommonParameters</span></span>
<span data-ttu-id="fd62b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd62b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd62b-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd62b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd62b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd62b-130">INPUTS</span></span>

### <span data-ttu-id="fd62b-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fd62b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fd62b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fd62b-132">System.String</span></span>

## <span data-ttu-id="fd62b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd62b-133">OUTPUTS</span></span>

### <span data-ttu-id="fd62b-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fd62b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="fd62b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd62b-135">NOTES</span></span>

## <span data-ttu-id="fd62b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd62b-136">RELATED LINKS</span></span>

[<span data-ttu-id="fd62b-137">Nowe — AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fd62b-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="fd62b-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fd62b-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="fd62b-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fd62b-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


