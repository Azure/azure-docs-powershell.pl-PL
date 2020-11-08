---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050923"
---
# <span data-ttu-id="45b08-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="45b08-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="45b08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45b08-102">SYNOPSIS</span></span>
<span data-ttu-id="45b08-103">Pobiera listę lub określony Opis usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="45b08-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="45b08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45b08-104">SYNTAX</span></span>

### <span data-ttu-id="45b08-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="45b08-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45b08-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45b08-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45b08-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="45b08-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45b08-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="45b08-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b08-109">Opis</span><span class="sxs-lookup"><span data-stu-id="45b08-109">DESCRIPTION</span></span>
<span data-ttu-id="45b08-110">Polecenie cmdlet **Get-AzApiManagement** pobiera listę wszystkich usług zarządzania API w obszarze subskrypcja lub określona grupa zasobów lub w ramach określonego zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="45b08-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="45b08-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45b08-111">EXAMPLES</span></span>

### <span data-ttu-id="45b08-112">Przykład 1: uzyskiwanie wszystkich usług zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="45b08-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="45b08-113">To polecenie pobiera wszystkie usługi zarządzania API w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="45b08-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="45b08-114">Przykład 2: uzyskiwanie wszystkich usług zarządzania interfejsem API według określonej nazwy</span><span class="sxs-lookup"><span data-stu-id="45b08-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="45b08-115">To polecenie pobiera całą usługę zarządzania interfejsem API według nazwy.</span><span class="sxs-lookup"><span data-stu-id="45b08-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="45b08-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45b08-116">PARAMETERS</span></span>

### <span data-ttu-id="45b08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b08-117">-DefaultProfile</span></span>
<span data-ttu-id="45b08-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45b08-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b08-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45b08-119">-Name</span></span>
<span data-ttu-id="45b08-120">Określa nazwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="45b08-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="45b08-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b08-121">-ResourceGroupName</span></span>
<span data-ttu-id="45b08-122">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="45b08-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="45b08-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45b08-123">-ResourceId</span></span>
<span data-ttu-id="45b08-124">Identyfikator zasobu ARM usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="45b08-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45b08-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b08-125">CommonParameters</span></span>
<span data-ttu-id="45b08-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b08-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b08-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45b08-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b08-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45b08-128">INPUTS</span></span>

### <span data-ttu-id="45b08-129">System. String</span><span class="sxs-lookup"><span data-stu-id="45b08-129">System.String</span></span>

## <span data-ttu-id="45b08-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45b08-130">OUTPUTS</span></span>

### <span data-ttu-id="45b08-131">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="45b08-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="45b08-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45b08-132">NOTES</span></span>

## <span data-ttu-id="45b08-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45b08-133">RELATED LINKS</span></span>

[<span data-ttu-id="45b08-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="45b08-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="45b08-135">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="45b08-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="45b08-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="45b08-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="45b08-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="45b08-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


