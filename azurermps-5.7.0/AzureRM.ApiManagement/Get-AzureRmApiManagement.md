---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 50a548716019f3b5e80cde4b89ae666f5b6199ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718968"
---
# <span data-ttu-id="49d0f-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="49d0f-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="49d0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="49d0f-103">Pobiera listę lub określony Opis usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="49d0f-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49d0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49d0f-104">SYNTAX</span></span>

### <span data-ttu-id="49d0f-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49d0f-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49d0f-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="49d0f-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49d0f-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="49d0f-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49d0f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="49d0f-108">DESCRIPTION</span></span>
<span data-ttu-id="49d0f-109">Polecenie cmdlet **Get-AzureRmApiManagement** pobiera listę wszystkich usług zarządzania API w obszarze subskrypcja lub określona grupa zasobów lub w ramach określonego zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="49d0f-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="49d0f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49d0f-110">EXAMPLES</span></span>

### <span data-ttu-id="49d0f-111">Przykład 1: uzyskiwanie wszystkich usług zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="49d0f-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="49d0f-112">To polecenie pobiera wszystkie usługi zarządzania API w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="49d0f-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="49d0f-113">Przykład 2: uzyskiwanie wszystkich usług zarządzania interfejsem API według określonej nazwy</span><span class="sxs-lookup"><span data-stu-id="49d0f-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="49d0f-114">To polecenie pobiera całą usługę zarządzania interfejsem API według nazwy.</span><span class="sxs-lookup"><span data-stu-id="49d0f-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="49d0f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49d0f-115">PARAMETERS</span></span>

### <span data-ttu-id="49d0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d0f-116">-DefaultProfile</span></span>
<span data-ttu-id="49d0f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49d0f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="49d0f-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49d0f-118">-Name</span></span>
<span data-ttu-id="49d0f-119">Określa nazwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="49d0f-119">Specifies the name of API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49d0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49d0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="49d0f-121">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="49d0f-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49d0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d0f-122">CommonParameters</span></span>
<span data-ttu-id="49d0f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d0f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49d0f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d0f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49d0f-125">INPUTS</span></span>

### <span data-ttu-id="49d0f-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="49d0f-126">None</span></span>
<span data-ttu-id="49d0f-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="49d0f-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49d0f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49d0f-128">OUTPUTS</span></span>

### <span data-ttu-id="49d0f-129">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. ApiManagement. modele. PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="49d0f-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="49d0f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49d0f-130">NOTES</span></span>

## <span data-ttu-id="49d0f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49d0f-131">RELATED LINKS</span></span>

[<span data-ttu-id="49d0f-132">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="49d0f-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="49d0f-133">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="49d0f-133">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="49d0f-134">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="49d0f-134">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="49d0f-135">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="49d0f-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


