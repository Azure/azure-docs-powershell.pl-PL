---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239794"
---
# <span data-ttu-id="d6e43-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6e43-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="d6e43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6e43-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e43-103">Pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6e43-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="d6e43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6e43-104">SYNTAX</span></span>

### <span data-ttu-id="d6e43-105">GetAllApiOperations (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d6e43-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6e43-106">GetById</span><span class="sxs-lookup"><span data-stu-id="d6e43-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6e43-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6e43-107">DESCRIPTION</span></span>
<span data-ttu-id="d6e43-108">Operacja **Get-AzApiManagementOperation** pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6e43-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="d6e43-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6e43-109">EXAMPLES</span></span>

### <span data-ttu-id="d6e43-110">Przykład 1. Uzyskiwanie wszystkich operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="d6e43-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="d6e43-111">To polecenie otrzymuje wszystkie operacje zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6e43-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="d6e43-112">Przykład 2. Uzyskiwanie operacji zarządzania interfejsem API za pomocą identyfikatora operacji</span><span class="sxs-lookup"><span data-stu-id="d6e43-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="d6e43-113">To polecenie otrzymuje operację zarządzania interfejsem API za pomocą identyfikatora operacji o nazwie Operation0003.</span><span class="sxs-lookup"><span data-stu-id="d6e43-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="d6e43-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6e43-114">PARAMETERS</span></span>

### <span data-ttu-id="d6e43-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d6e43-115">-ApiId</span></span>
<span data-ttu-id="d6e43-116">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6e43-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="d6e43-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d6e43-117">-ApiRevision</span></span>
<span data-ttu-id="d6e43-118">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6e43-118">Identifier of API Revision.</span></span> <span data-ttu-id="d6e43-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d6e43-119">This parameter is optional.</span></span> <span data-ttu-id="d6e43-120">Jeśli nie zostanie określona, operacja zostanie pobrana z aktualnie aktywnej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6e43-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="d6e43-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d6e43-121">-Context</span></span>
<span data-ttu-id="d6e43-122">Określa wystąpienie obiektu **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="d6e43-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d6e43-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e43-123">-DefaultProfile</span></span>
<span data-ttu-id="d6e43-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6e43-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6e43-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d6e43-125">-OperationId</span></span>
<span data-ttu-id="d6e43-126">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="d6e43-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="d6e43-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e43-127">CommonParameters</span></span>
<span data-ttu-id="d6e43-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6e43-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e43-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6e43-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e43-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6e43-130">INPUTS</span></span>

### <span data-ttu-id="d6e43-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6e43-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6e43-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d6e43-132">System.String</span></span>

## <span data-ttu-id="d6e43-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6e43-133">OUTPUTS</span></span>

### <span data-ttu-id="d6e43-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6e43-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="d6e43-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6e43-135">NOTES</span></span>

## <span data-ttu-id="d6e43-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6e43-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6e43-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6e43-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="d6e43-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6e43-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="d6e43-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6e43-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


