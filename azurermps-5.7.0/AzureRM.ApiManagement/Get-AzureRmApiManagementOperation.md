---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1b1547485a4758764cf02eaca4fd7bc26d4ef990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550731"
---
# <span data-ttu-id="5beaf-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5beaf-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="5beaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5beaf-102">SYNOPSIS</span></span>
<span data-ttu-id="5beaf-103">Pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5beaf-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5beaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5beaf-104">SYNTAX</span></span>

### <span data-ttu-id="5beaf-105">GetAllApiOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5beaf-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5beaf-106">GetById</span><span class="sxs-lookup"><span data-stu-id="5beaf-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5beaf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5beaf-107">DESCRIPTION</span></span>
<span data-ttu-id="5beaf-108">**Element get-AzureRmApiManagementOperation** pobiera listę lub określoną operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5beaf-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="5beaf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5beaf-109">EXAMPLES</span></span>

### <span data-ttu-id="5beaf-110">Przykład 1: uzyskiwanie wszystkich operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="5beaf-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="5beaf-111">To polecenie pobiera wszystkie operacje zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="5beaf-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="5beaf-112">Przykład 2: uzyskiwanie operacji zarządzania interfejsem API według identyfikatora operacji</span><span class="sxs-lookup"><span data-stu-id="5beaf-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="5beaf-113">To polecenie pobiera operację zarządzania interfejsem API, podając Identyfikator operacji o nazwie Operation0003.</span><span class="sxs-lookup"><span data-stu-id="5beaf-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="5beaf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5beaf-114">PARAMETERS</span></span>

### <span data-ttu-id="5beaf-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5beaf-115">-ApiId</span></span>
<span data-ttu-id="5beaf-116">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5beaf-116">Specifies the identifier of the API Operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beaf-117">-Context</span><span class="sxs-lookup"><span data-stu-id="5beaf-117">-Context</span></span>
<span data-ttu-id="5beaf-118">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5beaf-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5beaf-119">-DefaultProfile</span></span>
<span data-ttu-id="5beaf-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5beaf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5beaf-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5beaf-121">-OperationId</span></span>
<span data-ttu-id="5beaf-122">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="5beaf-122">Specifies the operation identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beaf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5beaf-123">CommonParameters</span></span>
<span data-ttu-id="5beaf-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5beaf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5beaf-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5beaf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5beaf-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5beaf-126">INPUTS</span></span>

### <span data-ttu-id="5beaf-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5beaf-127">None</span></span>
<span data-ttu-id="5beaf-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5beaf-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5beaf-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5beaf-129">OUTPUTS</span></span>

### <span data-ttu-id="5beaf-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5beaf-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>
<span data-ttu-id="5beaf-131">Szczegóły operacji API w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="5beaf-131">The details of the API Operation in Api Management service.</span></span>

### <span data-ttu-id="5beaf-132">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="5beaf-132">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>
<span data-ttu-id="5beaf-133">Lista operacji interfejsu API w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="5beaf-133">The list of API Operation in Api Management service.</span></span>

## <span data-ttu-id="5beaf-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5beaf-134">NOTES</span></span>

## <span data-ttu-id="5beaf-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5beaf-135">RELATED LINKS</span></span>

[<span data-ttu-id="5beaf-136">Nowe — AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5beaf-136">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5beaf-137">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5beaf-137">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5beaf-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5beaf-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


