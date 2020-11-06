---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: bff36b7bcb37dd099f9aa50a99bed9538111e8d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551440"
---
# <span data-ttu-id="c914c-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c914c-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="c914c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c914c-102">SYNOPSIS</span></span>
<span data-ttu-id="c914c-103">Pobiera listę lub określony Opis usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="c914c-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c914c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c914c-104">SYNTAX</span></span>

### <span data-ttu-id="c914c-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c914c-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c914c-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c914c-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c914c-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="c914c-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c914c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c914c-108">DESCRIPTION</span></span>
<span data-ttu-id="c914c-109">Polecenie cmdlet **Get-AzureRmApiManagement** pobiera listę wszystkich usług zarządzania API w obszarze subskrypcja lub określona grupa zasobów lub w ramach określonego zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="c914c-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="c914c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c914c-110">EXAMPLES</span></span>

### <span data-ttu-id="c914c-111">Przykład 1: uzyskiwanie wszystkich usług zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="c914c-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="c914c-112">To polecenie pobiera wszystkie usługi zarządzania API w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c914c-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="c914c-113">Przykład 2: uzyskiwanie wszystkich usług zarządzania interfejsem API według określonej nazwy</span><span class="sxs-lookup"><span data-stu-id="c914c-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="c914c-114">To polecenie pobiera całą usługę zarządzania interfejsem API według nazwy.</span><span class="sxs-lookup"><span data-stu-id="c914c-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="c914c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c914c-115">PARAMETERS</span></span>

### <span data-ttu-id="c914c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c914c-116">-DefaultProfile</span></span>
<span data-ttu-id="c914c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c914c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c914c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c914c-118">-Name</span></span>
<span data-ttu-id="c914c-119">Określa nazwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="c914c-119">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c914c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c914c-120">-ResourceGroupName</span></span>
<span data-ttu-id="c914c-121">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="c914c-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c914c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c914c-122">CommonParameters</span></span>
<span data-ttu-id="c914c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c914c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c914c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c914c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c914c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c914c-125">INPUTS</span></span>

### <span data-ttu-id="c914c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c914c-126">System.String</span></span>

## <span data-ttu-id="c914c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c914c-127">OUTPUTS</span></span>

### <span data-ttu-id="c914c-128">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c914c-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c914c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c914c-129">NOTES</span></span>

## <span data-ttu-id="c914c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c914c-130">RELATED LINKS</span></span>

[<span data-ttu-id="c914c-131">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c914c-131">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="c914c-132">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c914c-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="c914c-133">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c914c-133">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="c914c-134">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c914c-134">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


