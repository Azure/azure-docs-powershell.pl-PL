---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 99b98bd402d6ac22da4f05ce07a08a2c5980359b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707099"
---
# <span data-ttu-id="3f9cc-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f9cc-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="3f9cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f9cc-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9cc-103">Pobiera listę lub określony Opis usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3f9cc-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="3f9cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f9cc-104">SYNTAX</span></span>

### <span data-ttu-id="3f9cc-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3f9cc-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f9cc-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3f9cc-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f9cc-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="3f9cc-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f9cc-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f9cc-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f9cc-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3f9cc-109">DESCRIPTION</span></span>
<span data-ttu-id="3f9cc-110">Polecenie cmdlet **Get-AzApiManagement** pobiera listę wszystkich usług zarządzania API w obszarze subskrypcja lub określona grupa zasobów lub w ramach określonego zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3f9cc-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="3f9cc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f9cc-111">EXAMPLES</span></span>

### <span data-ttu-id="3f9cc-112">Przykład 1: uzyskiwanie wszystkich usług zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="3f9cc-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="3f9cc-113">To polecenie pobiera wszystkie usługi zarządzania API w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3f9cc-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="3f9cc-114">Przykład 2: uzyskiwanie wszystkich usług zarządzania interfejsem API według określonej nazwy</span><span class="sxs-lookup"><span data-stu-id="3f9cc-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="3f9cc-115">To polecenie pobiera całą usługę zarządzania interfejsem API według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3f9cc-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="3f9cc-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f9cc-116">PARAMETERS</span></span>

### <span data-ttu-id="3f9cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9cc-117">-DefaultProfile</span></span>
<span data-ttu-id="3f9cc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f9cc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f9cc-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f9cc-119">-Name</span></span>
<span data-ttu-id="3f9cc-120">Określa nazwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3f9cc-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="3f9cc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f9cc-121">-ResourceGroupName</span></span>
<span data-ttu-id="3f9cc-122">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3f9cc-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="3f9cc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f9cc-123">-ResourceId</span></span>
<span data-ttu-id="3f9cc-124">Identyfikator zasobu ARM usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3f9cc-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="3f9cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9cc-125">CommonParameters</span></span>
<span data-ttu-id="3f9cc-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f9cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9cc-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f9cc-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9cc-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f9cc-128">INPUTS</span></span>

### <span data-ttu-id="3f9cc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3f9cc-129">System.String</span></span>

## <span data-ttu-id="3f9cc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f9cc-130">OUTPUTS</span></span>

### <span data-ttu-id="3f9cc-131">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f9cc-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3f9cc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f9cc-132">NOTES</span></span>

## <span data-ttu-id="3f9cc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f9cc-133">RELATED LINKS</span></span>

[<span data-ttu-id="3f9cc-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f9cc-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="3f9cc-135">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f9cc-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="3f9cc-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f9cc-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="3f9cc-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f9cc-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


